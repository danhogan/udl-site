---
title: July 2021 Newsletter
date: 2021-07-01 06:00:00
type: post
blog: true
tags:
    - Newsletter
extras: true
---

Happy Summer

![ohtani](https://thumbs.gfycat.com/CautiousSlowFlies-size_restricted.gif)

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
*as of July 1st
<LeagueLeaders :categories="categories"/>

<h2 class="titleHug">Way-Too-Early Playoff Picture 👀👀👀</h2>
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
                week: 14,
                matchups: [
                    {
                        team1: "CT Clippers",
                        team1Img: "https://ca-times.brightspotcdn.com/dims4/default/d2717eb/2147483647/strip/true/crop/4452x3112+0+0/resize/1486x1039!/quality/90/?url=https%3A%2F%2Fcalifornia-times-brightspot.s3.amazonaws.com%2F5b%2F16%2F46576c64405ab0b1f3f845495d9e%2Fhttps-delivery.gettyimages.com%2Fdownloads%2F1180111636.jpg",
                        team2: "Beanetown Cruz Line",
                        team2Img: "https://www.skornorth.com/wp-content/uploads/2019/09/USATSI_13233057-scaled.jpg",
                        story: "A battle of two strong teams each sitting in second place in their divisions."
                    },
                    {
                        team1: "Wayne's Hardware",
                        team1Img: "https://images2.minutemediacdn.com/image/fetch/w_2000,h_2000,c_fit/https%3A%2F%2Freviewingthebrew.com%2Fwp-content%2Fuploads%2Fgetty-images%2F2017%2F07%2F1272132786.jpeg",
                        team2: "Torrano Beisbol Birds",
                        team2Img: "https://secureservercdn.net/45.40.146.28/m2i.7b3.myftpupload.com/wp-content/uploads/2020/09/USATSI_14776027-1024x683.jpg",
                        story: "A division leader takes on a strong squad fighting to stay in the hunt."
                    },
                    {
                        team1: "Springfield Isotopes",
                        team1Img: "https://images2.minutemediacdn.com/image/fetch/w_736,h_485,c_fill,g_auto,f_auto/https%3A%2F%2Freviewingthebrew.com%2Fwp-content%2Fuploads%2Fimagn-images%2F2017%2F07%2F16171792-850x560.jpeg",
                        team2: "The Gamblers",
                        team2Img: "https://www.sfexaminer.com/wp-content/uploads/2021/04/24810926_web1_210411-SFE-giants_1.jpg",
                        story: "Loads of pitching. These two teams are atop the league in strikeouts."
                    }
                ]
            },
            {
                week: 15,
                matchups: [
                    {
                        team1: "The Gamblers",
                        team1Img: "https://ca-times.brightspotcdn.com/dims4/default/4a2efcf/2147483647/strip/true/crop/4155x2770+0+0/resize/1486x991!/quality/90/?url=https%3A%2F%2Fcalifornia-times-brightspot.s3.amazonaws.com%2Fab%2F3d%2F6f1e57d04a9da2e689cc63996451%2Fastros-padres-baseball-24871.jpg",
                        team2: "Forgot About Trea",
                        team2Img: "https://arc-anglerfish-washpost-prod-washpost.s3.amazonaws.com/public/2J6RQTXEYMI6VAWYLZK5I7UQZI.jpg",
                        story: "Another battle of two strong teams each sitting in second place in their divisions."
                    }
                ]
            },
            {
                week: 16,
                matchups: [
                    {
                        team1: "Wayne's Hardware",
                        team1Img: "https://jaysjournal.com/wp-content/uploads/getty-images/2017/07/1270154028.jpeg",
                        team2: "Beanetown Cruz Line",
                        team2Img: "https://ca-times.brightspotcdn.com/dims4/default/558e3b0/2147483647/strip/true/crop/3240x2160+297+0/resize/2400x1600!/quality/90/?url=https%3A%2F%2Fcalifornia-times-brightspot.s3.amazonaws.com%2Fcb%2F00%2F0a14dd204a27b5a6dabdd1521402%2Fpadres-pirates-baseball-23349.jpg",
                        story: "That same division leader as before takes on another strong Aaron East squad."
                    },
                    {
                        team1: "Maine Cobra Kai",
                        team1Img: "https://images2.minutemediacdn.com/image/fetch/c_fill,g_auto,f_auto,h_2133,w_3200/https%3A%2F%2Fblogredmachine.com%2Fwp-content%2Fuploads%2Fgetty-images%2F2017%2F07%2F1163260630.jpeg",
                        team2: "The Gamblers",
                        team2Img: "https://sportshub.cbsistatic.com/i/r/2018/08/11/902e6b9a-ef5a-421c-b175-66f1923a74e7/thumbnail/1200x675/bad82fd0489393ee09a4dc9344e79d3b/j-d-martinez.jpg",
                        story: "Two strong teams with a lot of UDL experience trying to make their mark."
                    }
                ]
            }
        ],
        power: [
            "Back2Back Jax",
            "Big League Chu",
            "The Gamblers",
            "Wayne's Hardware",
            "Beanetown Cruz Line",	
            "Maine Cobra Kai",
            "Torrano Beisbol Birds",
            "CT Clippers",
            "Forgot About Trea",
            "Preston Perennials",
            "Springfield Isotopes",
            "Mookie and The Betts",
            "Bringers of W.A.R.",
            "Team Riptide",
            "Fried Chicken Sandwich",
            "The Emporium",
            "Hone Ron Runners",
            "Vlad and The Inhalers",
            "Cat Scratch Fever",
            "The Royal Rooters",
        ],
        categories: [
            {
                category: 'Runs',
                value: 446,
                udlTeam: 'Back2Back Jax',
                udlTeamLogo: 'https://larrybrownsports.com/wp-content/uploads/2016/07/max-scherzer-eyes.jpg',
                playerName: 'Xander Bogaerts',
                playerImage: 'https://bosoxinjection.com/wp-content/uploads/getty-images/2017/07/1232366054.jpeg'
            },
            {
                category: 'Home Runs',
                value: 133,
                udlTeam: 'The Gamblers',
                udlTeamLogo: 'https://i.imgur.com/y1qKgk1.jpg',
                playerName: 'Matt Olson',
                playerImage: 'https://whitecleatbeat.com/wp-content/uploads/getty-images/2017/07/1266998536.jpeg'
            },
            {
                category: 'RBI',
                value: 423,
                udlTeam: 'Back2Back Jax',
                udlTeamLogo: 'https://larrybrownsports.com/wp-content/uploads/2016/07/max-scherzer-eyes.jpg',
                playerName: 'Anthony Rendon',
                playerImage: 'https://sportsspectrum.s3.amazonaws.com/live/wp-content/uploads/2021/03/20104937/AP21075857219680-1.jpg'
            },
            {
                category: 'Stolen Bases',
                value: 77,
                udlTeam: 'Back2Back Jax',
                udlTeamLogo: 'https://larrybrownsports.com/wp-content/uploads/2016/07/max-scherzer-eyes.jpg',
                playerName: 'Starling Marte',
                playerImage: 'https://www.yardbarker.com/media/a/9/a9c1e73228d1736e2f7cfddd023ad754981807e0/thumb_16x9/starling-marte-leaves-game-due-possible-oblique.jpg?v=1'
            },
            {
                category: 'OBP',
                value: .3439,
                udlTeam: 'Preston Perennials',
                udlTeamLogo: 'https://vandenberg.id.au/uploads/images/PP-small.jpg',
                playerName: 'Justin Turner',
                playerImage: 'https://cdnph.upi.com/pv/upi/d06d0fbe1ed9e85985b4dc0153a124a4/NLDS-DIAMONDBACKS-DODGERS.jpg'
            },
            {
                category: 'Strikeouts',
                value: 685,
                udlTeam: 'Springfield Isotopes',
                udlTeamLogo: 'https://capaddicts.com/wp-content/uploads/2015/08/simpsons-springfield-isotopes.png',
                playerName: 'Dylan Cease',
                playerImage: 'https://cdn.vox-cdn.com/thumbor/5tJHZubKhe0zN-U2NDPIvD3hBmI=/0x0:1200x630/1200x800/filters:focal(504x219:696x411)/cdn.vox-cdn.com/uploads/chorus_image/image/63556939/st19_cease_01_8x10_1_e1555276484892.0.jpg'
            },
            {
                category: 'Quality Starts',
                value: 50,
                udlTeam: 'CT Clippers',
                udlTeamLogo: 'https://g.espncdn.com/lm-static/logo-packs/core/StarWarsTheRiseOfSkywalker/rise-skywalker-bb-8.svg',
                playerName: 'Walker Buehler',
                playerImage: 'https://cdn.vox-cdn.com/thumbor/RaU7XcgnJj0CfXwOwCI8Zz2GAVU=/1400x1050/filters:format(jpeg)/cdn.vox-cdn.com/uploads/chorus_asset/file/13658484/usa_today_11524294.jpg'
            },
            {
                category: 'ERA',
                value: 3.238,
                udlTeam: 'Springfield Isotopes',
                udlTeamLogo: 'https://capaddicts.com/wp-content/uploads/2015/08/simpsons-springfield-isotopes.png',
                playerName: 'Freddy Peralta',
                playerImage: 'https://x-default-stgec.uplynk.com/ausw/slices/574/44c3f81cadf84cf5a6f4e6d100388208/574eac682a8b4cb6987875c29231a0be/poster_225d013e36c14686a6e4d1495183ae17.jpg'
            },
            {
                category: 'WHIP',
                value: 1.102,
                udlTeam: 'Mookie and The Betts',
                udlTeamLogo: 'https://www.thewrap.com/wp-content/uploads/2019/02/rocket-1.jpg',
                playerName: 'Pablo Lopez',
                playerImage: 'https://vibesofsilence.com/wp-content/uploads/2017/11/PabloLopez_ElPatio_Cover.jpg'
            },
            {
                category: 'Saves + Holds',
                value: 71,
                udlTeam: 'Big League Chu',
                udlTeamLogo: 'https://img.fantrax.com/logos/tmLogo_x1joq2kojf9xmujh_512.jpg',
                playerName: 'Josh Hader',
                playerImage: 'https://fanatics.frgimages.com/FFImage/thumb.aspx?i=/productimages/_3698000/altimages/ff_3698508-3b2160430749e0fd8012alt1_full.jpg&w=900'
            }
        ],
        playoffs: {
            teams: {
                "6": {
                    udlTeam: 'Maine Cobra Kai',
                    udlTeamLogo: 'https://g.espncdn.com/s/flblm/logos/At%20the%20Ballpark-Robb%20Harskamp/Ballpark-11.svg',
                    title: "Koufax West Champ"
                },
                "4": {
                    udlTeam: 'Wayne\'s Hardware',
                    udlTeamLogo: 'https://res.cloudinary.com/teepublic/image/private/s--LYtlPysQ--/t_Preview/b_rgb:eae0c7,c_limit,f_jpg,h_630,q_90,w_630/v1482729132/production/designs/990736_1.jpg',
                    title: "Koufax East Champ"
                },
                "7": {
                    udlTeam: 'CT Clippers',
                    udlTeamLogo: 'https://g.espncdn.com/lm-static/logo-packs/core/StarWarsTheRiseOfSkywalker/rise-skywalker-bb-8.svg',
                    title: "Koufax Wild Card #1"
                },
                "8": {
                    udlTeam: 'Forgot About Trea',
                    udlTeamLogo: 'https://g.espncdn.com/s/flblm/logos/At%20the%20Ballpark-Robb%20Harskamp/Ballpark-01.svg',
                    title: "Koufax Wild Card #2"
                },
                "1": {
                    udlTeam: 'Back2Back Jax',
                    udlTeamLogo: 'https://larrybrownsports.com/wp-content/uploads/2016/07/max-scherzer-eyes.jpg',
                    title: "Aaron East Champ"
                },
                "5": {
                    udlTeam: 'Beanetown Cruz Line',
                    udlTeamLogo: 'https://i.ibb.co/LYNJdbP/40823296-s.jpg',
                    title: "Aaron Wild Card #2"
                },
                "2": {
                    udlTeam: 'Big League Chu',
                    udlTeamLogo: 'https://img.fantrax.com/logos/tmLogo_x1joq2kojf9xmujh_512.jpg',
                    title: "Aaron West Champ"
                },
                "3": {
                    udlTeam: 'The Gamblers',
                    udlTeamLogo: 'https://i.imgur.com/y1qKgk1.jpg',
                    title: "Aaron Wild Card #1"
                },
            }
        }
    };
  },
}
</script>