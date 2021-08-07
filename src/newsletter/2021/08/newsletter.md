---
title: August 2021 Newsletter
date: 2021-08-06 06:00:00
type: post
blog: true
tags:
    - Newsletter
extras: true
---

What a trade deadline!

<iframe src="https://giphy.com/embed/9FewsNojQFQJO" width="480" height="270" frameBorder="0" class="giphy-embed" allowFullScreen></iframe>

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
*as of morning of August 6th
<LeagueLeaders :categories="categories"/>

<h2 class="titleHug">Playoff Picture 👀👀👀</h2>
If the playoffs started today, here's what the playoff bracket would look like (sorry if it doesn't look so great on mobile):
<PlayoffPicture :playoffs="playoffs"/>

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
                week: 18,
                matchups: [
                    {
                        team1: "The Gamblers",
                        team1Img: "https://chicago.cbslocal.com/wp-content/uploads/sites/15116062/2021/08/GettyImages-1331837143.jpg?w=1500",
                        team2: "Hone Ron Runners",
                        team2Img: "https://cdn.vox-cdn.com/thumbor/xiDRMAFbkaUr3gD40hJaj85Pp6s=/0x0:2295x1530/1200x800/filters:focal(965x582:1331x948)/cdn.vox-cdn.com/uploads/chorus_image/image/69677540/usa_today_16490193.0.jpg",
                        story: "Largely putting this here to provoke some smack-talk in Slack. 😄"
                    }
                ]
            },
            {
                week: 19,
                matchups: [
                    {
                        team1: "Forgot About Trea",
                        team1Img: "https://www.nbcsports.com/sites/nbcsports.com/files/styles/article_hero_image/public/2021/08/04/riley.jpg?itok=VP-oNCED",
                        team2: "Torrano Beisbol Birds",
                        team2Img: "https://a.espncdn.com/media/motion/2021/0805/dm_210805_MLB_One-Play_Blue_Jays_Bichette_homer/dm_210805_MLB_One-Play_Blue_Jays_Bichette_homer.jpg",
                        story: "Two hot squads with eyes on the playoffs."
                    },
                    {
                        team1: "Maine Cobra Kai",
                        team1Img: "https://blogredmachine.com/wp-content/uploads/getty-images/2017/07/1156831885.jpeg",
                        team2: "Back2Back Jax",
                        team2Img: "https://climbingtalshill.com/wp-content/uploads/imagn-images/2017/07/16488644.jpeg",
                        story: "Two division leaders trying to hold on to their spots."
                    }
                ]
            },
            {
                week: 20,
                matchups: [
                    {
                        team1: "Torrano Beisbol Birds",
                        team1Img: "https://a2.espncdn.com/combiner/i?img=%2Fmedia%2Fmotion%2F2021%2F0803%2Fdm_210803_mlb_hilliard_hr_rev1%2Fdm_210803_mlb_hilliard_hr_rev1.jpg",
                        team2: "Maine Cobra Kai",
                        team2Img: "https://cdn.theathletic.com/app/uploads/2021/08/05001818/GettyImages-1234466275-1024x683.jpg",
                        story: "Get the feeling this one could decide some playoff seeding."
                    }
                ]
            },
            {
                week: 21,
                matchups: [
                    {
                        team1: "Wayne's Hardware",
                        team1Img: "https://www.redlegnation.com/wp-content/uploads/2019/11/joeyvotto12.jpg",
                        team2: "Big League Chu",
                        team2Img: "https://www.ocregister.com/wp-content/uploads/2021/05/LDN-L-FREEWAY-0329-08-LO-1.jpg",
                        story: "Playoff implications?"
                    },
                    {
                        team1: "Forgot About Trea",
                        team1Img: "https://images.actionnetwork.com/blog/2021/08/Wheeler-1.jpg",
                        team2: "Beanetown Cruz Line",
                        team2Img: "https://imengine.prod.srp.navigacloud.com/?uuid=0f4549f4-42d4-5e09-8cfe-701e7c3168d2&type=primary&q=72&width=1024",
                        story: "Big matchup right before the playoffs."
                    }
                ]
            }
        ],
        power: [
            "Back2Back Jax",
            "The Gamblers",
            "Torrano Beisbol Birds",
            "Big League Chu",
            "Beanetown Cruz Line",	
            "Forgot About Trea",
            "Maine Cobra Kai",
            "Wayne's Hardware",
            "CT Clippers",
            "Bringers of W.A.R.",
            "Team Riptide",
            "Springfield Isotopes",
            "Preston Perennials",
            "Hone Ron Runners",
            "Mookie and The Betts",
            "Fried Chicken Sandwich",
            "The Emporium",
            "Vlad and The Inhalers",
            "Cat Scratch Fever",
            "The Royal Rooters",
        ],
        categories: [
            {
                category: 'Runs',
                value: 581,
                udlTeam: 'Back2Back Jax',
                udlTeamLogo: 'https://larrybrownsports.com/wp-content/uploads/2016/07/max-scherzer-eyes.jpg',
                playerName: 'Jesse Winker',
                playerImage: 'https://i.ytimg.com/vi/itameNpL7ec/maxresdefault.jpg'
            },
            {
                category: 'Home Runs',
                value: 182,
                udlTeam: 'The Gamblers',
                udlTeamLogo: 'https://i.imgur.com/y1qKgk1.jpg',
                playerName: 'Jorge Soler',
                playerImage: 'https://cdn.vox-cdn.com/thumbor/Adu4qhYgHGiLqlKAu4ADrJRe7YI=/0x0:3000x2099/1200x800/filters:focal(1726x600:2206x1080)/cdn.vox-cdn.com/uploads/chorus_image/image/69673956/1234437757.10.jpg'
            },
            {
                category: 'RBI',
                value: 548,
                udlTeam: 'Tie - Torrano Beisbol Birds and CT Clippers',
                udlTeamLogo: 'https://i.imgur.com/H2vkfYW.jpg',
                playerName: 'Bo Bichette',
                playerImage: 'https://s.yimg.com/ny/api/res/1.2/gF_zKTBw6OMruLeNE7ayqA--/YXBwaWQ9aGlnaGxhbmRlcjt3PTY0MDtoPTM2MC4wNDA0NzIxNzUzNzk0/https://s.yimg.com/os/creatr-uploaded-images/2021-04/0b185340-9337-11eb-96f9-58f52fc121d2'
            },
            {
                category: 'Stolen Bases',
                value: 108,
                udlTeam: 'Back2Back Jax',
                udlTeamLogo: 'https://larrybrownsports.com/wp-content/uploads/2016/07/max-scherzer-eyes.jpg',
                playerName: 'Starling Marte',
                playerImage: 'https://cdn.vox-cdn.com/thumbor/UZsZx87AqY5pBmdywWxET_rBtJU=/0x0:5208x3472/1200x800/filters:focal(2188x1320:3020x2152)/cdn.vox-cdn.com/uploads/chorus_image/image/69675424/1234386604.0.jpg'
            },
            {
                category: 'OBP',
                value: .3492,
                udlTeam: 'Riptide',
                udlTeamLogo: 'https://img.fantrax.com/logos/tmLogo_q9qkntnviwcl7gnr_512.jpg',
                playerName: 'Bryce Harper',
                playerImage: 'https://washington.cbslocal.com/wp-content/uploads/sites/15909891/2017/02/bryce-harper.jpg?w=870'
            },
            {
                category: 'Strikeouts',
                value: 910,
                udlTeam: 'Springfield Isotopes',
                udlTeamLogo: 'https://capaddicts.com/wp-content/uploads/2015/08/simpsons-springfield-isotopes.png',
                playerName: 'Dylan Cease',
                playerImage: 'https://img.mlbstatic.com/mlb-images/image/private/ar_16:9,g_auto,q_auto:good,w_1024,c_fill,f_jpg,dpr_3.0/mlb/rsp0kqmopfpub214f18n'
            },
            {
                category: 'Quality Starts',
                value: 65,
                udlTeam: 'CT Clippers',
                udlTeamLogo: 'https://g.espncdn.com/lm-static/logo-packs/core/StarWarsTheRiseOfSkywalker/rise-skywalker-bb-8.svg',
                playerName: 'Walker Buehler',
                playerImage: 'https://www.lexingtonfamily.com/wp-content/uploads/2012/06/Scholar-Athlete-Walker-buehler-720x959.jpg'
            },
            {
                category: 'ERA',
                value: 3.403,
                udlTeam: 'Hone Ron Runners',
                udlTeamLogo: 'https://g.espncdn.com/lm-static/logo-packs/core/Solo/ESPN_Star_Wars_Lando-01.svg',
                playerName: 'Tylor Megill',
                playerImage: 'https://09d1d85a2275582e9dad-7b3e649a230e2ba2cff912d8af17e0b5.ssl.cf1.rackcdn.com/1343-10-Purple-20.jpg'
            },
            {
                category: 'WHIP',
                value: 1.115,
                udlTeam: 'Back2Back Jax',
                udlTeamLogo: 'https://larrybrownsports.com/wp-content/uploads/2016/07/max-scherzer-eyes.jpg',
                playerName: 'Kris Bubic',
                playerImage: 'https://gostanford.com/images/2018/2/12/Kris_Bubic_020918_BD_248.JPG'
            },
            {
                category: 'Saves + Holds',
                value: 89,
                udlTeam: 'Beanetown Cruz Line',
                udlTeamLogo: 'https://i.ibb.co/LYNJdbP/40823296-s.jpg',
                playerName: 'Lou Trivino',
                playerImage: 'https://rockathletics.com/images/2012/2/7//37%20Lou%20Trivino.jpg?width=300'
            }
        ],
        playoffs: {
            teams: {
                "3": {
                    udlTeam: 'Maine Cobra Kai',
                    udlTeamLogo: 'https://g.espncdn.com/s/flblm/logos/At%20the%20Ballpark-Robb%20Harskamp/Ballpark-11.svg',
                    title: "Koufax West Champ"
                },
                "4": {
                    udlTeam: 'Wayne\'s Hardware',
                    udlTeamLogo: 'https://res.cloudinary.com/teepublic/image/private/s--LYtlPysQ--/t_Preview/b_rgb:eae0c7,c_limit,f_jpg,h_630,q_90,w_630/v1482729132/production/designs/990736_1.jpg',
                    title: "Koufax East Champ"
                },
                "8": {
                    udlTeam: 'CT Clippers',
                    udlTeamLogo: 'https://g.espncdn.com/lm-static/logo-packs/core/StarWarsTheRiseOfSkywalker/rise-skywalker-bb-8.svg',
                    title: "Koufax Wild Card #2"
                },
                "7": {
                    udlTeam: 'Forgot About Trea',
                    udlTeamLogo: 'https://g.espncdn.com/s/flblm/logos/At%20the%20Ballpark-Robb%20Harskamp/Ballpark-01.svg',
                    title: "Koufax Wild Card #1"
                },
                "1": {
                    udlTeam: 'Back2Back Jax',
                    udlTeamLogo: 'https://larrybrownsports.com/wp-content/uploads/2016/07/max-scherzer-eyes.jpg',
                    title: "Aaron East Champ"
                },
                "6": {
                    udlTeam: 'Beanetown Cruz Line',
                    udlTeamLogo: 'https://i.ibb.co/LYNJdbP/40823296-s.jpg',
                    title: "Aaron Wild Card #2"
                },
                "5": {
                    udlTeam: 'Torrano Beisbol Birds',
                    udlTeamLogo: 'https://i.imgur.com/H2vkfYW.jpg',
                    title: "Aaron Wild Card #1"
                },
                "2": {
                    udlTeam: 'The Gamblers',
                    udlTeamLogo: 'https://i.imgur.com/y1qKgk1.jpg',
                    title: "Aaron West Champ"
                },
            }
        }
    };
  },
}
</script>