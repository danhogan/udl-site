---
title: July 2019 Newsletter
date: 2019-07-29 06:00:00
type: post
blog: true
tags:
    - Newsletter
extras: true
---

Getting close to the playoffs! Make your final trades before the deadline!

## UDL Player of the Month - Yuli Gurriel - Bringers of W.A.R.
![yuli](/yuli-edited.jpg)
Yuli Gurriel is hitting .411/.442/.878 with 12 home runs in July so far. That's a .467 ISO and 246 wRC+. Perhaps these powers come from being coupled with his brother on Bringers of W.A.R. This extreme hot streak from the 35-year-old has helped propel Bringers of W.A.R. to the top of the entire Koufax conference.

## Articles
<div class="articleContainer">
<a href="/newsletter/2019/07/matchups.html" class="article">
    <img src="https://i.ytimg.com/vi/g4diNGvUEzM/maxresdefault.jpg">
    <div>
        <h3>Matchups To Watch</h3>
    </div>
</a>

<a href="https://ultimatedynastyleague.slack.com/files/UCZSGGMK7/FLGP4KWAF/brandon_kalashian_udl_league_owner_boston_narb_sluggers_28th_july_2019.mp4" target="_blank" class="article">
    <img src="https://ca.slack-edge.com/TCWBT3X7C-UCZSGGMK7-74f0d99497a8-512">
    <div>
        <h3>Vegemite With Vandenberg</h3>
        <span>ft. Brandon K - Boston Narb Sluggers</span>
    </div>
</a>

<a href="/newsletter/2019/07/first-rounders.html" class="article">
    <img src="http://mlb.mlb.com/assets/images/0/7/0/197029070/cuts/hamcatch_0kmpj4mg_7t3rvln8.jpg">
    <div>
        <h3>UDL First Rounders</h3>
    </div>
</a>
</div>

<h2 class="titleHug">Category Leaders - End of July</h2>
*as of the morning of July 29th
<LeagueLeaders :categories="categories"/>

<h2 class="titleHug">End of July Playoff Picture</h2>
Just 5 matchups left before the playoffs. Crunch time! If the playoffs started today, here's what the playoff bracket would look like (sorry if it doesn't look so great on mobile):
<PlayoffPicture :playoffs="playoffs"/>

#### Rest In Peace, Tyler Skaggs

![skaggs](https://usatftw.files.wordpress.com/2019/07/skaggs.jpg?w=1000&h=600&crop=1)

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
        categories: [
            {
                category: 'Runs',
                value: 653,
                udlTeam: 'Back2Back Jax',
                udlTeamLogo: 'https://larrybrownsports.com/wp-content/uploads/2016/07/max-scherzer-eyes.jpg',
                playerName: 'Xander Bogaerts',
                playerImage: 'https://imagesvc.timeincapp.com/v3/fan/image?url=https://bosoxinjection.com/wp-content/uploads/getty-images/2017/07/1000294898.jpeg&c=sc&w=850&h=560'
            },
            {
                category: 'Home Runs',
                value: 209,
                udlTeam: 'Back2Back Jax',
                udlTeamLogo: 'https://larrybrownsports.com/wp-content/uploads/2016/07/max-scherzer-eyes.jpg',
                playerName: 'Eugenio Suarez',
                playerImage: 'https://imagesvc.timeincapp.com/v3/fan/image?url=https://blogredmachine.com/wp-content/uploads/getty-images/2017/07/966940688.jpeg&c=sc&w=850&h=560'
            },
            {
                category: 'RBI',
                value: 624,
                udlTeam: 'Back2Back Jax',
                udlTeamLogo: 'https://larrybrownsports.com/wp-content/uploads/2016/07/max-scherzer-eyes.jpg',
                playerName: 'Anthony Rendon',
                playerImage: 'https://imagesvc.timeincapp.com/v3/fan/image?url=https%3A%2F%2Fcalltothepen.com%2Fwp-content%2Fuploads%2Fgetty-images%2F2016%2F04%2F1141052158.jpeg&c=sc&w=850&h=560'
            },
            {
                category: 'Stolen Bases',
                value: 99,
                udlTeam: 'Bringers of W.A.R.',
                udlTeamLogo: 'https://i.imgur.com/94GmH6O_d.jpg?maxwidth=640&shape=thumb&fidelity=medium',
                playerName: 'Mallex Smith',
                playerImage: 'https://cdn-images-1.medium.com/max/2400/1*lGUmOBOiujim1QeCDxT0Tg.jpeg'
            },
            {
                category: 'OBP',
                value: .3525,
                udlTeam: 'Team !Ponche!',
                udlTeamLogo: 'https://g.espncdn.com/lm-static/flb/images/default_logos/5.svg',
                playerName: 'Ketel Marte',
                playerImage: 'https://arizonasports.com/wp-content/uploads/2019/04/GettyImages-1140688071-620x370.jpg'
            },
            {
                category: 'Strikeouts',
                value: 893,
                udlTeam: 'Bringers of W.A.R.',
                udlTeamLogo: 'https://i.imgur.com/94GmH6O_d.jpg?maxwidth=640&shape=thumb&fidelity=medium',
                playerName: 'Lance Lynn',
                playerImage: 'https://imagesvc.timeincapp.com/v3/fan/image?url=https%3A%2F%2Fnolanwritin.com%2Fwp-content%2Fuploads%2Fgetty-images%2F2017%2F07%2F1141809155.jpeg&c=sc&w=850&h=560'
            },
            {
                category: 'Quality Starts',
                value: 69,
                udlTeam: 'Bringers of W.A.R.',
                udlTeamLogo: 'https://i.imgur.com/94GmH6O_d.jpg?maxwidth=640&shape=thumb&fidelity=medium',
                playerName: 'Hyun-Jin Ryu',
                playerImage: 'https://static01.nyt.com/images/2019/05/31/sports/31metsweb1/31metsweb1-articleLarge.jpg?quality=75&auto=webp&disable=upscale'
            },
            {
                category: 'ERA',
                value: 3.556,
                udlTeam: 'Bringers of W.A.R.',
                udlTeamLogo: 'https://i.imgur.com/94GmH6O_d.jpg?maxwidth=640&shape=thumb&fidelity=medium',
                playerName: 'Brad Keller',
                playerImage: 'https://cdn.vox-cdn.com/thumbor/LA50LvheoSlbB3F3QT4jRjzV4lg=/0x0:5067x3347/1200x800/filters:focal(1845x176:2655x986)/cdn.vox-cdn.com/uploads/chorus_image/image/59765607/952558268.jpg.0.jpg'
            },
            {
                category: 'WHIP',
                value: 1.188,
                udlTeam: 'Preston Perennials',
                udlTeamLogo: 'http://vandenberg.id.au/uploads/images/PP-small.jpg',
                playerName: 'Shane Bieber',
                playerImage: 'https://cdn.vox-cdn.com/thumbor/gWhl63ydAlxHlAiIyAvpq5wGuac=/0x0:3014x2009/1200x800/filters:focal(1408x277:1890x759)/cdn.vox-cdn.com/uploads/chorus_image/image/60592087/1004910524.jpg.0.jpg'
            },
            {
                category: 'Saves + Holds',
                value: 83,
                udlTeam: 'Cat Scratch Fever',
                udlTeamLogo: 'https://upload.wikimedia.org/wikipedia/en/8/87/Keyboard_cat.jpg',
                playerName: 'Seth Lugo',
                playerImage: 'https://cdn.vox-cdn.com/thumbor/e09g_O6UfnOfT5gefm7IlhksreA=/0x0:3662x2559/1200x800/filters:focal(1544x170:2128x754)/cdn.vox-cdn.com/uploads/chorus_image/image/63867940/1140570748.jpg.0.jpg'
            }
        ],
        playoffs: {
            koufax: {
                "2": {
                    udlTeam: 'Hone Ron Runners',
                    udlTeamLogo: 'https://g.espncdn.com/lm-static/logo-packs/core/Solo/ESPN_Star_Wars_Lando-01.svg',
                    title: "Koufax West Champ"
                },
                "1": {
                    udlTeam: 'Bringers of W.A.R.',
                    udlTeamLogo: 'https://i.imgur.com/94GmH6O_d.jpg?maxwidth=640&shape=thumb&fidelity=medium',
                    title: "Koufax East Champ"
                },
                "3": {
                    udlTeam: 'Team !Ponche!',
                    udlTeamLogo: 'https://g.espncdn.com/lm-static/flb/images/default_logos/5.svg',
                    title: "Wild Card #1"
                },
                "4": {
                    udlTeam: 'Preston Perennials',
                    udlTeamLogo: 'http://vandenberg.id.au/uploads/images/PP-small.jpg',
                    title: "Wild Card #2"
                },
            },
            aaron: {
                "1": {
                    udlTeam: 'Back2Back Jax',
                    udlTeamLogo: 'https://larrybrownsports.com/wp-content/uploads/2016/07/max-scherzer-eyes.jpg',
                    title: "Aaron East Champ"
                },
                "3": {
                    udlTeam: 'Big League Chu',
                    udlTeamLogo: 'https://img.fantrax.com/logos/tmLogo_x1joq2kojf9xmujh_512.jpg',
                    title: "Wild Card #1"
                },
                "2": {
                    udlTeam: 'Discount Bob\'s Couch Emporium',
                    udlTeamLogo: 'http://g.espncdn.com/lm-app/lm/img/shell/shield-FLB.svg',
                    title: "Aaron West Champ"
                },
                "4": {
                    udlTeam: 'The Gamblers',
                    udlTeamLogo: 'https://i.imgur.com/y1qKgk1.jpg',
                    title: "Wild Card #2"
                },
            }
        }
    };
  },
}
</script>