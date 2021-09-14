---
title: Semifinals 2021
date: 2021-09-14 00:00:00
type: post
blog: true
tags:
    - Newsletter
extras: true
---

The Aaron League couldn't quite pull off the sweep and three wild cards move into the semis. Congrats to those who are moving on and congrats to the rest on a great season. Here are the teams that remain:
<div class="wrapper">
    <div class="item">
        <div class="item-parent">
            <p>UDL Championship</p>
        </div>
        <div class="item-childrens">
            <div class="item-child">
                <div class="item">
                    <div class="item-parent">
                        <p>Semifinals</p>
                    </div>
                    <div class="item-childrens">
                        <div class="item-child">
                            <div class="block">
                                <img :src="playoffs.teams[1].udlTeamLogo">
                                <div>
                                    <h2>{{playoffs.teams[1].title}}</h2>
                                    <p>1. {{playoffs.teams[1].udlTeam}}</p>
                                </div>
                            </div>
                        </div>
                        <div class="item-child">
                            <div class="block">
                                <img :src="playoffs.teams[5].udlTeamLogo">
                                <div>
                                    <h2>{{playoffs.teams[5].title}}</h2>
                                    <p>5. {{playoffs.teams[5].udlTeam}}</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="item-child">
                <div class="item">
                    <div class="item-parent">
                        <p>Semifinals</p>
                    </div>
                    <div class="item-childrens">
                        <div class="item-child">
                            <div class="block">
                                <img :src="playoffs.teams[6].udlTeamLogo">
                                <div>
                                    <h2>{{playoffs.teams[6].title}}</h2>
                                    <p>6. {{playoffs.teams[6].udlTeam}}</p>
                                </div>
                            </div>
                        </div>
                        <div class="item-child">
                            <div class="block">
                                <img :src="playoffs.teams[7].udlTeamLogo">
                                <div>
                                    <h2>{{playoffs.teams[7].title}}</h2>
                                    <p>7. {{playoffs.teams[7].udlTeam}}</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>

## Semifinal Matchups - A Closer Look
<div class="weekContainer" v-for="week in weeks">

<div class="matchupContainer" v-for="matchup in week.matchups">

<!-- add records and place in division -->
<h2>{{matchup.team1}} vs {{matchup.team2}}</h2>
<div class="matchupImages">
<img class="team1Img" :src="matchup.team1Img">
<img class="vsLogo" src="http://static1.comicvine.com/uploads/original/11112/111129141/5440487-1122329314-52705.png">
<img class="team2Img" :src="matchup.team2Img">
</div>
<p :inner-html.prop="matchup.story | newLines"></p>

</div>

</div>


<style>
.authorName {
    font-size: 1rem;
}

.titleHug {
    margin-bottom: .3em;
}

.articleContainer {
    display: grid;
    grid-template-columns: auto auto;
    grid-row-gap: 1em;
    grid-column-gap: 1em;
}

@media only screen and (max-width: 1024px) {
    .articleContainer {
        grid-template-columns: auto;
    }
}

.article {
    box-shadow: 0 4px 6px 0 hsla(0, 0%, 0%, 0.2);
    cursor: pointer;
}

.article:hover {
    box-shadow: 0 8px 12px 0 hsla(0, 0%, 0%, 0.4);
}

.article > img {
    display: block;
    width: 100%;
    height: 20em;
    object-fit: cover;
}

.article > div {
    padding: 1em;
    height: 3em;
}

.article h3 {
    margin: 0;
}

.article h3, .article span {
    color: #2c3e50;
}


.matchupImages {
    margin-top: 20px;
    display: grid;
    grid-template-columns: repeat(6, 1fr);
    grid-column-gap: 1em;
    grid-auto-rows: 20em;
}

/* @media (max-width: 1024px) {
    .matchupImages {
        grid-template-columns: auto;
        grid-row-gap: 1em;
    }
} */

.matchupImages > img {
    height: 20em;
    object-fit: cover;
}

.matchupImages > .team1Img { grid-column: 1 / 4; grid-row: 1; width: 100%; }
.matchupImages > .vsLogo { grid-column: 3 / 5; grid-row: 1; z-index: 1; height: 5em; width: 6em; margin: auto; }
.matchupImages > .team2Img { grid-column: 4 / 7; grid-row: 1; width: 100%; }

@media (max-width: 900px) {
   .matchupImages {
       grid-template-columns: auto;
       grid-template-rows: repeat(6, 1fr);
       grid-row-gap: 1em;
    }
   .matchupImages > .team1Img { grid-row: 1 / 4; grid-column: 1; }
   .matchupImages > .vsLogo { grid-row: 2 / 6; grid-column: 1; }
   .matchupImages > .team2Img { grid-row: 4 / 7; grid-column: 1; }
}

.wrapper {
    background-color: DarkSalmon;
    display: flex;
    height: 600px;
    justify-content: center;
}

.item {
    display: flex;
    flex-direction: row-reverse;
}
.item .block, .item p {
    margin: 0;
    background-color: Beige;
}
.item .block {
    padding: 10px;
    min-width: 15em;
}
.item-parent > p {
    padding: 10px;
}
.item-parent {
    position: relative;
    margin-left: 50px;
    display: flex;
    align-items: center;
}
.item-parent:after {
    position: absolute;
    content: '';
    width: 25px;
    height: 2px;
    left: 0;
    top: 50%;
    background-color: #fff;
    transform: translateX(-100%);
}
.item-childrens {
    display: flex;
    flex-direction: column;
    justify-content: center;
}
.item-child {
    display: flex;
    align-items: flex-start;
    justify-content: flex-end;
    margin-top: 10px;
    margin-bottom: 10px;
    position: relative;
}
.item-child:before {
    content: '';
    position: absolute;
    background-color: #fff;
    right: 0;
    top: 50%;
    transform: translateX(100%);
    width: 25px;
    height: 2px;
}
.item-child:after {
    content: '';
    position: absolute;
    background-color: #fff;
    right: -25px;
    height: calc(50% + 22px);
    width: 2px;
    top: 50%;
}
.item-child:last-child:after {
    transform: translateY(-100%);
}
.item-child:only-child:after {
    display: none;
}

.block {
    display: flex;
    align-items: flex-start;
    /* Beige */
    background: #333;
    padding: 1rem;
    max-width: 15rem;
    margin: 0 0 1rem 0;
}
.block > img {
    width: 75px;
    margin: 0 1rem 0 0;
}
.block > div {
    flex: 1;
}
.block h2 {
    font-weight: 500;
    margin: 0 0 0.5rem 0;
    font-size: 1rem;
}
</style>

<script>
export default {
  data() {
    return {
        playoffs: {
            teams: {
                "1": {
                    udlTeam: 'Back2Back Jax',
                    udlTeamLogo: 'https://larrybrownsports.com/wp-content/uploads/2016/07/max-scherzer-eyes.jpg',
                    title: "Aaron East Champ"
                },
                "6": {
                    udlTeam: 'Big League Chu',
                    udlTeamLogo: 'https://img.fantrax.com/logos/tmLogo_x1joq2kojf9xmujh_512.jpg',
                    title: "Aaron Wild Card #2"
                },
                "7": {
                    udlTeam: 'Maine Cobra Kai',
                    udlTeamLogo: 'https://g.espncdn.com/s/flblm/logos/At%20the%20Ballpark-Robb%20Harskamp/Ballpark-11.svg',
                    title: "Koufax Wild Card #1"
                },
                "5": {
                    udlTeam: 'Torrano Beisbol Birds',
                    udlTeamLogo: 'https://i.imgur.com/H2vkfYW.jpg',
                    title: "Aaron Wild Card #1"
                }
            }
        },
        weeks: [
            {
                matchups: [
                    {
                        team1: "Back2Back Jax",
                        team1Img: "https://www.mcclatchy-wires.com/incoming/avyj21/picture253936798/alternates/FREE_1140/Braves_Dodgers_Baseball_82350.jpg",
                        team2: "Torrano Beisbol Birds",
                        team2Img: "https://detroit.cbslocal.com/wp-content/uploads/sites/15909782/2021/09/GettyImages-1339074447-e1631196447188.jpg",
                        story: "Discount Bob's Couch Emporium stopped the hot Gamblers in their tracks behind big performances from the bats of Christian Yelich, Kyle Schwarber, AJ Pollock, and Matt Joyce. Archie Bradley and Emilio Pagan helped seal down the pitching end with 3 saves apiece. \n Forgot About Trea demolished the Back2Back Jax juggernaut - quite an upset for the 8 seed. Juan Soto, Carlos Martinez, Lucas Gioloto, and a two-start Tony Disco all helped to make a big difference. \n Both squads in this semifinal matchup got through the first round with solid bullpen performances. Now we get to see how they matchup against each other. Many other categorical stats were similar for both teams in their quarterfinal matchup. Forgot About Trea could have an advantage with several two-start pitchers - though the matchups could be tough. The Emporium has Bauer and Fried lined up for two-starts as well. Many things seem even and balanced between these two squads. This could be a close one."
                    },
                    {
                        team1: "Big League Chu",
                        team1Img: "https://www.ajc.com/resizer/SWLPqPI02xELS3VGS9AVKeSbw68=/814x458/cloudfront-us-east-1.images.arcpublishing.com/ajc/S5WUKDZVIREQJHP3JDWHKYPAWQ.jpg",
                        team2: "Maine Cobra Kai",
                        team2Img: "https://9b16f79ca967fd0708d1-2713572fef44aa49ec323e813b06d2d9.ssl.cf2.rackcdn.com/1140x_a10-7_cTC/Miami-Marlins-v-Washington-Nationals-2-1631314656.jpg",
                        story: "Big League Chu's Matt Chapman had just two hits in his quarterfinal matchup - both home runs. Two bombs along with eight walks accounts for not a bad week in an OBP league. Mark Canha and Asdrubal Cabrera also came up big on the offensive side of the ball. In spite of a Jon Lester implosion, he still had two starts and racked up sixteen big Ks for BLC. Chaz Roe with three holds may be the unsung hero allowing Big League Chu to just beat out the Runners in the saves+holds category.  \n Team !Ponche\'s! offense is still cookin'. Ketel Marte and Joc Pederson had monster weeks in the quarterfinal matchup. The two-start Sandy Alcantara came up with fifteen big Ks for Team !Ponche! on the pitching side - perhaps it was Jake Arrieta's injured, intimidating stare that pushed Sandy onward. \n The semifinal story here seems like it could be a case of Big League Chu's pitching vs Team !Ponche's! bats. Can either team find a way to put a dent in each other? Big League Chu could be fighting a tough battle going up against a two-start Greinke. However, as we saw in the first round of our playoffs this year, anything can happen."
                    }
                ]
            }
        ]
    };
  },
  filters: {
      newLines: function(str){
          return str.replace(/(\r\n|\n|\r)/gm, "<br><br>")
      }
  }
}
</script>