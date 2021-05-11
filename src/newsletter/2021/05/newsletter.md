---
title: May 2021 Newsletter
date: 2021-05-11 06:00:00
type: post
blog: true
tags:
    - Newsletter
extras: true
---

Well it's been quite the start!

![mercedes](https://chumley.barstoolsports.com/union/giphy/2021/04/19/85fcdf81.gif?crop=4%3A3)

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
*as of May 11th
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
                week: 6,
                matchups: [
                    {
                        team1: "Maine Cobra Kai",
                        team1Img: "https://www.gannett-cdn.com/presto/2020/08/18/USAT/c8dde623-1d11-4476-9845-cd85be7e1714-McCullers_on_Kelly_.jpg",
                        team2: "Hone Ron Runners",
                        team2Img: "https://images2.minutemediacdn.com/image/fetch/w_736,h_485,c_fill,g_auto,f_auto/https%3A%2F%2Ftomahawktake.com%2Fwp-content%2Fuploads%2Fgetty-images%2F2017%2F07%2F1228645822-850x560.jpeg",
                        story: "Two top teams in Koufax West. Two top teams to throw jabs on Slack. Let's do it."
                    },
                    {
                        team1: "Torrano Beisbol Birds",
                        team1Img: "https://cdn.theathletic.com/app/uploads/2020/08/18010637/GettyImages-1227944578-scaled-e1597727218605-1024x683.jpg",
                        team2: "Back2Back Jax",
                        team2Img: "https://www.star-telegram.com/latest-news/n8zfgn/picture241010196/alternates/FREE_768/AP20060247327125.jpg",
                        story: "Two top teams in the Aaron East duke it out. Back2Back Jax took their first matchup 7-3."
                    }
                ]
            },
            {
                week: 7,
                matchups: [
                    {
                        team1: "Wayne's Hardware",
                        team1Img: "https://cdn-media.theathletic.com/cdn-cgi/image/fit=cover,width=700,height=466/6GzOnU3pIcCx_pjcqj3WXKaPm_1440x.960.jpg",
                        team2: "CT Clippers",
                        team2Img: "https://img.mlbstatic.com/mlb-images/image/private/t_16x9/t_w1024/mlb/xkktrffpnp0ofjhmjanx",
                        story: "Two top teams in Koufax East in a battle."
                    },
                    {
                        team1: "Torrano Beisbol Birds",
                        team1Img: "https://images2.minutemediacdn.com/image/fetch/w_736,h_485,c_fill,g_auto,f_auto/https%3A%2F%2Fmotorcitybengals.com%2Fwp-content%2Fuploads%2Fimagn-images%2F2017%2F07%2F15652616-850x560.jpeg",
                        team2: "Beanetown Cruz Line",
                        team2Img: "https://ca-times.brightspotcdn.com/dims4/default/7ba7576/2147483647/strip/true/crop/3834x2160+0+0/resize/1486x837!/quality/90/?url=https%3A%2F%2Fcalifornia-times-brightspot.s3.amazonaws.com%2F15%2Fbc%2F24b15625419ba9426c69649483dc%2Fpadres-pirates-baseball-91915.jpg",
                        story: "The defending champ faces a division rival that's currently ahead in the standings."
                    }
                ]
            },
            {
                week: 8,
                matchups: [
                    {
                        team1: "Maine Kobra Kai",
                        team1Img: "https://images2.minutemediacdn.com/image/fetch/c_fill,g_auto,f_auto,h_2134,w_3200/https%3A%2F%2Fsouthsideshowdown.com%2Fwp-content%2Fuploads%2Fgetty-images%2F2017%2F07%2F1311824976.jpeg",
                        team2: "Preston Perennials",
                        team2Img: "https://awaybackgone.com/wp-content/uploads/getty-images/2017/07/1166518231-1.jpeg",
                        story: "Strong contenders in Koufax West face off."
                    },
                    {
                        team1: "Torrano Beisbol Birds",
                        team1Img: "https://cdn.vox-cdn.com/thumbor/HrGZ4ZCyKNb5yp4P0JdWYUSPFYE=/0x0:3000x2000/1200x800/filters:focal(1189x86:1669x566)/cdn.vox-cdn.com/uploads/chorus_image/image/61623767/1037822020.jpg.0.jpg",
                        team2: "The Gamblers",
                        team2Img: "https://bosoxinjection.com/wp-content/uploads/getty-images/2020/03/1209878262.jpeg",
                        story: "The Torrano Beisbol birds continue their gauntlet of a May against the mighty Gamblers."
                    }
                ]
            },
            {
                week: 9,
                matchups: [
                    {
                        team1: "Hone Ron Runners",
                        team1Img: "https://ca-times.brightspotcdn.com/dims4/default/58a82aa/2147483647/strip/true/crop/4211x2808+0+0/resize/1486x991!/quality/90/?url=https%3A%2F%2Fcalifornia-times-brightspot.s3.amazonaws.com%2Fde%2Fb9%2F4f461cf24127a5e18133134db654%2Fangels-rangers-baseball-63647.jpg",
                        team2: "Preston Perennials",
                        team2Img: "https://patch.com/img/cdn20/getty/22848544/20210126/015211/styles/patch_image/public/gettyimages-1172348002___26134307227.jpg",
                        story: "Another strong Koufax West battle."
                    }
                ]
            }
        ],
        power: [
            "Back2Back Jax",
            "The Gamblers",
            "Maine Cobra Kai",
            "Big League Chu",
            "Wayne's Hardware",
            "Preston Perennials",
            "CT Clippers",
            "Hone Ron Runners",
            "Torrano Beisbol Birds",
            "Beanetown Cruz Line",	
            "Bringers of W.A.R.",
            "Mookie and The Betts",
            "Springfield Isotopes",
            "The Emporium",
            "Team Riptide",
            "Forgot About Trea",
            "Fried Chicken Sandwich",
            "Vlad and The Inhalers",
            "The Royal Rooters",
            "Cat Scratch Fever",
        ],
        categories: [
            {
                category: 'Runs',
                value: 197,
                udlTeam: 'Back2Back Jax',
                udlTeamLogo: 'https://larrybrownsports.com/wp-content/uploads/2016/07/max-scherzer-eyes.jpg',
                playerName: 'Isiah Kiner-Falefa',
                playerImage: 'https://www.staradvertiser.com/wp-content/uploads/2019/08/web1_AP19244132668428.jpg'
            },
            {
                category: 'Home Runs',
                value: 59,
                udlTeam: 'The Gamblers',
                udlTeamLogo: 'https://i.imgur.com/y1qKgk1.jpg',
                playerName: 'J.D. Martinez',
                playerImage: 'https://bosoxinjection.com/wp-content/uploads/imagn-images/2017/07/14505162.jpeg'
            },
            {
                category: 'RBI',
                value: 198,
                udlTeam: 'Back2Back Jax',
                udlTeamLogo: 'https://larrybrownsports.com/wp-content/uploads/2016/07/max-scherzer-eyes.jpg',
                playerName: 'Trey Mancini',
                playerImage: 'https://cdn.theathletic.com/app/uploads/2019/07/03014435/USATSI_12978999-1024x745.jpg'
            },
            {
                category: 'Stolen Bases',
                value: 35,
                udlTeam: 'Back2Back Jax',
                udlTeamLogo: 'https://larrybrownsports.com/wp-content/uploads/2016/07/max-scherzer-eyes.jpg',
                playerName: 'Whit Merrfield',
                playerImage: 'https://primetimesportstalk.com/wp-content/uploads/2020/01/USATSI_13371086-0x0_c.jpg'
            },
            {
                category: 'OBP',
                value: .3481,
                udlTeam: 'Preston Perennials',
                udlTeamLogo: 'http://vandenberg.id.au/uploads/images/PP-small.jpg',
                playerName: 'Max Muncy',
                playerImage: 'https://www.gannett-cdn.com/presto/2018/10/27/USAT/a77fa33c-5fe3-4dc7-b268-f4b1eba43e79-USATSI_11529191.jpg'
            },
            {
                category: 'Strikeouts',
                value: 301,
                udlTeam: 'Big League Chu',
                udlTeamLogo: 'https://img.fantrax.com/logos/tmLogo_x1joq2kojf9xmujh_512.jpg',
                playerName: 'Tyler Glasnow',
                playerImage: 'https://cloudfront-us-east-1.images.arcpublishing.com/tbt/BAH2AEZJBJDTLOVG57OFMDBSUA.JPG'
            },
            {
                category: 'Quality Starts',
                value: 22,
                udlTeam: 'Tie - The Royal Rooters and CT Clippers',
                udlTeamLogo: 'https://g.espncdn.com/lm-static/logo-packs/core/Incredibles/incredibles_8.svg',
                playerName: 'Kyle Gibson',
                playerImage: 'https://www.star-telegram.com/latest-news/istua3/picture245795435/alternates/FREE_1140/Kyle%20Gibson%20art%200916.jpg'
            },
            {
                category: 'ERA',
                value: 3.061,
                udlTeam: 'Hone Ron Runners',
                udlTeamLogo: 'https://g.espncdn.com/lm-static/logo-packs/core/Solo/ESPN_Star_Wars_Lando-01.svg',
                playerName: 'Jacob DeGrom',
                playerImage: 'https://res-2.cloudinary.com/ybmedia/image/upload/c_crop,h_1123,w_2000,x_0,y_28/c_fill,f_auto,h_495,q_auto,w_880/v1/m/2/3/2323efe5c4e7689fa1bda72af9e0feb85312935a/12534647.jpg'
            },
            {
                category: 'WHIP',
                value: 1.045,
                udlTeam: 'Back2Back Jax',
                udlTeamLogo: 'https://larrybrownsports.com/wp-content/uploads/2016/07/max-scherzer-eyes.jpg',
                playerName: 'Max Scherzer',
                playerImage: 'https://storage.googleapis.com/afs-prod/media/3e5246784bcb4707bcb33a032917e63a/3000.jpeg'
            },
            {
                category: 'Saves + Holds',
                value: 31,
                udlTeam: 'Big League Chu',
                udlTeamLogo: 'https://img.fantrax.com/logos/tmLogo_x1joq2kojf9xmujh_512.jpg',
                playerName: 'Ian Kennedy',
                playerImage: 'https://www.star-telegram.com/latest-news/nkmhvy/picture251246969/alternates/LANDSCAPE_1140/AP21124587190671.jpg'
            }
        ]
    };
  },
}
</script>