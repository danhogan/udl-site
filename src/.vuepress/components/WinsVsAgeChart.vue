<template>
    <div>
<!-- This can serve as a tutorial in how to not do things -->
    <div id="chartHere"></div>
    <!-- <script src="https://cdnjs.cloudflare.com/ajax/libs/d3/3.5.17/d3.min.js"></script> -->
    <script>
var d3Script = document.createElement('script');  
d3Script.setAttribute('src','https://cdnjs.cloudflare.com/ajax/libs/d3/3.5.17/d3.min.js');
document.head.appendChild(d3Script);

        const finalObject = [
        {
            "team": "Torrano Beisbol Birds",
            "averageAge": 27.83,
            "wins": 108
        },
        {
            "team": "Cat Scratch Fever",
            "averageAge": 27.39,
            "wins": 89
        },
        {
            "team": "Team Riptide",
            "averageAge": 27.33,
            "wins": 112
        },
        {
            "team": "Boston Narb Sluggers",
            "averageAge": 25.33,
            "wins": 33
        },
        {
            "team": "Back2Back Jax",
            "averageAge": 29.19,
            "wins": 114
        },
        {
            "team": "Vengeful Tuna",
            "averageAge": 31.11,
            "wins": 119
        },
        {
            "team": "Discount Bob's Couch Emporium",
            "averageAge": 29.68,
            "wins": 119
        },
        {
            "team": "The Gamblers",
            "averageAge": 27.73,
            "wins": 121
        },
        {
            "team": "Big League Chu",
            "averageAge": 28.26,
            "wins": 88
        },
        {
            "team": "The Royal Rooters",
            "averageAge": 24.81,
            "wins": 54
        },
        {
            "team": "Wayne's Hardware",
            "averageAge": 26.95,
            "wins": 87
        },
        {
            "team": "Havana Pigs",
            "averageAge": 29.27,
            "wins": 68
        },
        {
            "team": "Team !Ponche!",
            "averageAge": 28.96,
            "wins": 125
        },
        {
            "team": "Acuna Matata",
            "averageAge": 25.73,
            "wins": 57
        },
        {
            "team": "Bringers of W.A.R.",
            "averageAge": 27.88,
            "wins": 108
        },
        {
            "team": "Preston Perennials",
            "averageAge": 29.12,
            "wins": 90
        },
        {
            "team": "Maine Cobra Kai ",
            "averageAge": 27.93,
            "wins": 128
        },
        {
            "team": "Forgot  About Trea",
            "averageAge": 27.83,
            "wins": 104
        },
        {
            "team": "Springfield Isotopes",
            "averageAge": 27.24,
            "wins": 104
        },
        {
            "team": "Hone Ron Runners",
            "averageAge": 30.41,
            "wins": 132
        }
        ]

        var margin = {
            top: 20,
            right: 20,
            bottom: 30,
            left: 40
        },
            width = 800 - margin.left - margin.right,
            height = 500 - margin.top - margin.bottom;

        var x = d3.scale.linear()
            .range([0, width]);

        var y = d3.scale.linear()
            .range([height, 0]);

        var xAxis = d3.svg.axis()
            .scale(x)
            .orient("bottom");

        var yAxis = d3.svg.axis()
            .scale(y)
            .orient("left");

        var div = d3.select("#chartHere").append("div")	
            .attr("class", "tooltip")				
            .style("opacity", 0);

        var svg = d3.select("#chartHere").append("svg")
            .attr("width", width + margin.left + margin.right)
            .attr("height", height + margin.top + margin.bottom)
            .append("g")
            .attr("transform", "translate(" + margin.left + "," + margin.top + ")");

        var data = create_data();

        data.forEach(function (d) {
            d.x = +d.x;
            d.y = +d.y;
            d.yhat = +d.yhat;
        });

        var line = d3.svg.line()
            .x(function (d) {
                return x(d.x);
            })
            .y(function (d) {
                return y(d.yhat);
            });

        x.domain(d3.extent(data, function (d) {
            return d.x;
        }));
        y.domain(d3.extent(data, function (d) {
            return d.y;
        }));

        svg.append("g")
            .attr("class", "x axis")
            .attr("transform", "translate(0," + height + ")")
            .call(xAxis)
            .append("text")
            .attr("class", "label")
            .attr("x", width)
            .attr("y", -6)
            .style("text-anchor", "end")
            .text("Average Age of Current Roster");

        svg.append("g")
            .attr("class", "y axis")
            .call(yAxis)
            .append("text")
            .attr("class", "label")
            .attr("transform", "rotate(-90)")
            .attr("y", 6)
            .attr("dy", ".71em")
            .style("text-anchor", "end")
            .text("2018 Wins")

        svg.append("g")
            .attr("class", "grid")
            .attr("transform", "translate(0," + height + ")")
            .call(make_x_axis()
                .tickSize(-height, 0, 0)
                .tickFormat("")
            )

        svg.append("g")
            .attr("class", "grid")
            .call(make_y_axis()
                .tickSize(-width, 0, 0)
                .tickFormat("")
            )

        svg.selectAll(".dot")
            .data(data)
            .enter().append("circle")
            .attr("class", "dot")
            .attr("r", 4.5)
            .attr("cx", function (d) {
                return x(d.x);
            })
            .attr("cy", function (d) {
                return y(d.y);
            })
            .on("mouseover", function(d) {
                div.transition()		
                    .duration(200)		
                    .style("opacity", .9);		
                div	.html(d.name + "<br/>" + d.x + "<span> yrs</span><br/>" + d.y + "<span> wins</span>")	
                    .style("left", (d3.event.pageX) + "px")		
                    .style("top", (d3.event.pageY - 28) + "px");	
                })					
            .on("mouseout", function(d) {		
                div.transition()		
                    .duration(200)		
                    .style("opacity", 0);	
            })

        svg.append("path")
            .datum(data)
            .attr("class", "line")
            .attr("d", line);

        function make_x_axis() {        
            return d3.svg.axis()
                .scale(x)
                .orient("bottom")
                .ticks(5)
        }

        function make_y_axis() {        
            return d3.svg.axis()
                .scale(y)
                .orient("left")
                .ticks(5)
        }

        function create_data() {
            var x = [];
            var y = [];
            var teamNames = [];
            var n = 20;
            var x_mean = 0;
            var y_mean = 0;
            var term1 = 0;
            var term2 = 0;
            // create x and y values
            for (var i = 0; i < n; i++) {
                y.push(finalObject[i].wins);
                x.push(finalObject[i].averageAge);
                teamNames.push(finalObject[i].team)
                x_mean += x[i]
                y_mean += y[i]
            }
            // calculate mean x and y
            x_mean /= n;
            y_mean /= n;

            // calculate coefficients
            var xr = 0;
            var yr = 0;
            for (i = 0; i < x.length; i++) {
                xr = x[i] - x_mean;
                yr = y[i] - y_mean;
                term1 += xr * yr;
                term2 += xr * xr;

            }
            var b1 = term1 / term2;
            var b0 = y_mean - (b1 * x_mean);
            // perform regression 

            yhat = [];
            // fit line using coeffs
            for (i = 0; i < x.length; i++) {
                yhat.push(b0 + (x[i] * b1));
            }

            var data = [];
            for (i = 0; i < y.length; i++) {
                data.push({
                    "yhat": yhat[i],
                    "y": y[i],
                    "x": x[i],
                    "name": teamNames[i]
                })
            }
            return (data);
        }
    </script>
    </div>
</template>

<style>
    .line {
        stroke: rgba(233, 24, 62, 0.308);
        fill: none;
        stroke-width: 2;
    }

    .axis path,
    .axis line {
        fill: none;
        stroke: black;
        shape-rendering: crispEdges;
    }

    .axis text {
        font-size: 10px;
        font-family: sans-serif;
    }

    .text-label {
        font-size: 10px;
        font-family: sans-serif;
    }

    .dot {
        stroke: #000000;
        fill: rgb(0, 12, 116)
    }

    div.tooltip {	
        position: absolute;			
        text-align: center;			
        width: 120px;					
        height: 45px;					
        padding: 2px;				
        font: 12px sans-serif;		
        background: rgb(202, 202, 202);	
        border: 0px;		
        border-radius: 8px;			
        pointer-events: none;			
    }

    .grid .tick {
        stroke: lightgrey;
        opacity: 0.7;
    }
    .grid path {
        stroke-width: 0;
    }
</style>