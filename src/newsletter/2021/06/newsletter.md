---
title: June 2021 Newsletter
date: 2021-06-03 06:00:00
type: post
blog: true
tags:
    - Newsletter
extras: true
---

If you currently roster less than 10 IL-eligible players, are you even trying?

![albies punched](https://thumbs.gfycat.com/NextDearestBushsqueaker-size_restricted.gif)

## Matchups To Watch

<div class="weekContainer" v-for="week in weeks">
<h1>Week {{week.week}}</h1>

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

## Power Rankings
<ol>
<li v-for="team in power">{{team}}</li>
</ol>

<h2 class="titleHug">Category Leaders</h2>
*as of June 3rd
<LeagueLeaders :categories="categories"/>

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
</style>

<script>
export default {
  data() {
    return {
        weeks: [
            {
                week: 10,
                matchups: [
                    {
                        team1: "Big League Chu",
                        team1Img: "https://cdn.theathletic.com/app/uploads/2021/04/03221300/USATSI_15841662-scaled-e1617503906972-1024x683.jpg",
                        team2: "The Gamblers",
                        team2Img: "https://www.mercurynews.com/wp-content/uploads/2019/03/1136357164.jpg",
                        story: "First matchup was a 5-5 tie. Two top teams in Aaron West. Two teams atop the power rankings. Loser has to tell Nick Pollack the winner knows more about baseball than them."
                    },
                    {
                        team1: "Beanetown Cruz Line",
                        team1Img: "https://s.hdnux.com/photos/01/05/05/53/18111186/5/rawImage.jpg",
                        team2: "Back2Back Jax",
                        team2Img: "https://blogredmachine.com/wp-content/uploads/getty-images/2017/07/1270466631.jpeg",
                        story: "Two top teams in the Aaron East duke it out. Back2Back Jax took their first matchup 5-3-2 in week 5."
                    }
                ]
            },
            {
                week: 11,
                matchups: [
                    {
                        team1: "Back2Back Jax",
                        team1Img: "https://media-cldnry.s-nbcnews.com/image/upload/newscms/2020_18/3327906/200428-trey-mancini-cs-208p-3327906.jpg",
                        team2: "The Gamblers",
                        team2Img: "https://images2.minutemediacdn.com/image/fetch/w_2000,h_2000,c_fit/https%3A%2F%2Fdairylandexpress.com%2Fwp-content%2Fuploads%2Fgetty-images%2F2018%2F08%2F1272516491.jpeg",
                        story: "Two of the top teams in the league in a duel."
                    }
                ]
            },
            {
                week: 12,
                matchups: [
                    {
                        team1: "Big League Chu",
                        team1Img: "https://cdn.theathletic.com/app/uploads/2021/04/08131501/040421-AMF-3718-Tarik-Skubal-1024x683.jpg",
                        team2: "Back2Back Jax",
                        team2Img: "https://www.ocregister.com/wp-content/uploads/2021/05/GettyImages-1313034545-1.jpg",
                        story: "All the top teams seem to be playing each other this month."
                    }
                ]
            },
            {
                week: 13,
                matchups: [
                    {
                        team1: "Wayne's Hardware",
                        team1Img: "https://fansided.com/wp-content/uploads/imagn-images/2020/10/15062590.jpeg",
                        team2: "Maine Cobra Kai",
                        team2Img: "https://specials-images.forbesimg.com/imageserve/5f274f3a60d6621f98938f64/960x0.jpg?fit=scale",
                        story: "Two teams sitting atop each Koufax division at the time of this writing."
                    },
                    {
                        team1: "Beanetown Cruz Line",
                        team1Img: "https://cdn.vox-cdn.com/thumbor/2AA20soNGZ_aLgv6sDdAHNbyTZw=/0x0:3022x2156/1200x800/filters:focal(1456x79:1938x561)/cdn.vox-cdn.com/uploads/chorus_image/image/68967453/1304898076.0.jpg",
                        team2: "The Gamblers",
                        team2Img: "https://cdn.vox-cdn.com/thumbor/hHmC4dtoILxZX4-YKzZVAUIpyOM=/0x0:3016x3584/1200x800/filters:focal(321x563:803x1045)/cdn.vox-cdn.com/uploads/chorus_image/image/68949833/1306209281.0.jpg",
                        story: "Solid teams each sitting in second place in their respective Aaron division at the time of this writing."
                    }
                ]
            }
        ],
        power: [
            "Big League Chu",
            "The Gamblers",
            "Back2Back Jax",
            "Maine Cobra Kai",
            "Wayne's Hardware",
            "CT Clippers",
            "Beanetown Cruz Line",	
            "Torrano Beisbol Birds",
            "Forgot About Trea",
            "Preston Perennials",
            "Springfield Isotopes",
            "Mookie and The Betts",
            "Bringers of W.A.R.",
            "Fried Chicken Sandwich",
            "The Emporium",
            "Team Riptide",
            "Vlad and The Inhalers",
            "Hone Ron Runners",
            "The Royal Rooters",
            "Cat Scratch Fever",
        ],
        categories: [
            {
                category: 'Runs',
                value: 304,
                udlTeam: 'Back2Back Jax',
                udlTeamLogo: 'https://larrybrownsports.com/wp-content/uploads/2016/07/max-scherzer-eyes.jpg',
                playerName: 'Jesse Winker',
                playerImage: 'https://cdn.vox-cdn.com/thumbor/m2-TS-jO_6FQfMaCIzHffDNVZfc=/1400x1400/filters:format(jpeg)/cdn.vox-cdn.com/uploads/chorus_asset/file/22532201/usa_today_16106416.jpg'
            },
            {
                category: 'Home Runs',
                value: 96,
                udlTeam: 'The Gamblers',
                udlTeamLogo: 'https://i.imgur.com/y1qKgk1.jpg',
                playerName: 'Matt Olson',
                playerImage: 'https://www.nbcsports.com/sites/rsnunited/files/styles/article_hero_image/public/archive/assets_article/bayarea/2020/03/02/mattolsonusa.jpg'
            },
            {
                category: 'RBI',
                value: 299,
                udlTeam: 'Back2Back Jax',
                udlTeamLogo: 'https://larrybrownsports.com/wp-content/uploads/2016/07/max-scherzer-eyes.jpg',
                playerName: 'Trey Mancini',
                playerImage: 'https://d29m18w01sxjzp.cloudfront.net/th_q_750_390_99934_mancinitrey.jpg'
            },
            {
                category: 'Stolen Bases',
                value: 53,
                udlTeam: 'Back2Back Jax',
                udlTeamLogo: 'https://larrybrownsports.com/wp-content/uploads/2016/07/max-scherzer-eyes.jpg',
                playerName: 'Whit Merrifield',
                playerImage: 'https://images2.minutemediacdn.com/image/fetch/c_fill,g_auto,f_auto,h_2417,w_3200/https%3A%2F%2Fkckingdom.com%2Fwp-content%2Fuploads%2Fimagn-images%2F2018%2F08%2F14982704.jpeg'
            },
            {
                category: 'OBP',
                value: .3445,
                udlTeam: 'Team Riptide',
                udlTeamLogo: 'https://img.fantrax.com/logos/tmLogo_q9qkntnviwcl7gnr_512.jpg',
                playerName: 'Rhys Hoskins',
                playerImage: 'https://cdn.vox-cdn.com/thumbor/DSABymUuKfK_lZ0FsMaJZmuuTaA=/0x0:1323x1978/1400x1050/filters:focal(558x324:768x534):format(jpeg)/cdn.vox-cdn.com/uploads/chorus_image/image/56165441/usa_today_10210707.0.jpg'
            },
            {
                category: 'Strikeouts',
                value: 475,
                udlTeam: 'Springfield Isotopes',
                udlTeamLogo: 'https://capaddicts.com/wp-content/uploads/2015/08/simpsons-springfield-isotopes.png',
                playerName: 'Chris Bassitt',
                playerImage: 'https://www.toledoblade.com/image/2007/02/01/1140x_a10-7_cTC/Sidelines-Spotlight-athlete-Chris-Bassitt.jpg'
            },
            {
                category: 'Quality Starts',
                value: 35,
                udlTeam: 'The Royal Rooters',
                udlTeamLogo: 'https://g.espncdn.com/lm-static/logo-packs/core/Incredibles/incredibles_8.svg',
                playerName: 'Yusei Kikuchi',
                playerImage: 'https://www.thedailyworld.com/wp-content/uploads/2020/02/20590801_web1_TSR-SPORTS-BBA-BOSOX-MARINERS-2-SE--1-.jpg'
            },
            {
                category: 'ERA',
                value: 3.219,
                udlTeam: 'Mookie and The Betts',
                udlTeamLogo: 'https://www.thewrap.com/wp-content/uploads/2019/02/rocket-1.jpg',
                playerName: 'Brandon Woodruff',
                playerImage: 'https://images2.minutemediacdn.com/image/fetch/w_2000,h_2000,c_fit/https%3A%2F%2Freviewingthebrew.com%2Fwp-content%2Fuploads%2Fgetty-images%2F2020%2F07%2F1227833183.jpeg'
            },
            {
                category: 'WHIP',
                value: 1.090,
                udlTeam: 'Back2Back Jax',
                udlTeamLogo: 'https://larrybrownsports.com/wp-content/uploads/2016/07/max-scherzer-eyes.jpg',
                playerName: 'Max Scherzer',
                playerImage: 'https://i1.wp.com/russianmachineneverbreaks.com/wp-content/uploads/2019/11/nationals-parade31-max-scherzer.jpg?fit=1500%2C1000&ssl=1'
            },
            {
                category: 'Saves + Holds',
                value: 49,
                udlTeam: 'Big League Chu',
                udlTeamLogo: 'https://img.fantrax.com/logos/tmLogo_x1joq2kojf9xmujh_512.jpg',
                playerName: 'Adam Ottavino',
                playerImage: 'https://bosoxinjection.com/wp-content/uploads/getty-images/2017/07/1306383275.jpeg'
            }
        ]
    };
  },
}
</script>