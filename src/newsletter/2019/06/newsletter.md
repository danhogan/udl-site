---
title: June 2019 Newsletter
date: 2019-07-04 06:00:00
type: post
blog: true
tags:
    - Newsletter
extras: true
---

It's nearly the All-Star break!

## UDL Player of the Month - DJ LeMahieu - The Gamblers
![lemahieu](/lemahieu-edited.jpg)
DJ Lemahieu has been proving to everyone that he's not just a product of Coors. In the month of June, LeMahieu slashed .395/.434/.658 and collected a staggering run plus RBI total of 55. He's been extra hot over the last 2 weeks hitting for a wRC+ of 313. That's stupid. May DJ and The Gamblers have mercy on us all.

Again, if you want help with a logo, I'm willing to try to help.

I've been messing around with the layout of things here. Hopefully you can still find things alright.

<div class="articleContainer">
<a href="/newsletter/2019/06/powerrankings.html" class="article">
    <img src="https://2.bp.blogspot.com/-MwFgEUyE5qo/WkMcQv1zJ1I/AAAAAAAAJG4/mLoYsjuTQ9gjb9h8eJZ0gTABinanih2-gCLcBGAs/s1600/Baseball-Bat.jpg">
    <div>
        <h3>Power Rankings</h3>
        <span>by Austin B (The Gamblers)</span>
    </div>
</a>

<a href="/newsletter/2019/06/matchups.html" class="article">
    <img src="https://i.ytimg.com/vi/g4diNGvUEzM/maxresdefault.jpg">
    <div>
        <h3>Matchups To Watch</h3>
    </div>
</a>

<a href="https://ultimatedynastyleague.slack.com/files/UCZSGGMK7/FKE79KYL9/joe_feery_udl_league_owner_bringers_of_war.mp4" target="_blank" class="article">
    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/10/Vegemiteontoast_large.jpg/235px-Vegemiteontoast_large.jpg">
    <div>
        <h3>Vegemite With Vandenberg</h3>
        <span>ft. Joe - Bringers of W.A.R.</span>
    </div>
</a>
</div>

<h2 class="titleHug">Category Leaders - End of June</h2>
*as of the morning of July 1st
<LeagueLeaders :categories="categories"/>

<h2 class="titleHug">End of June Playoff Picture</h2>
Already just 8 matchups left before the playofs. If the playoffs started today, here's what the playoff bracket would look like (sorry if it doesn't look so great on mobile):
<PlayoffPicture :playoffs="playoffs"/>

#### Let's keep this party rollin'!

![muncy-shirt](https://i.redd.it/nyxgpl85if431.jpg)

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
                value: 546,
                udlTeam: 'Maine Cobra Kai',
                udlTeamLogo: 'https://g.espncdn.com/s/flblm/logos/At%20the%20Ballpark-Robb%20Harskamp/Ballpark-11.svg',
                playerName: 'Dansby Swanson',
                playerImage: 'https://cdnph.upi.com/svc/sv/upi/3851498960269/2017/1/84da580f11893f43ae64f1cfc90152b8/Dansby-Swanson-delivers-in-clutch-as-Atlanta-Braves-edge-Oakland-As.jpg'
            },
            {
                category: 'Home Runs',
                value: 169,
                udlTeam: 'Maine Cobra Kai',
                udlTeamLogo: 'https://g.espncdn.com/s/flblm/logos/At%20the%20Ballpark-Robb%20Harskamp/Ballpark-11.svg',
                playerName: 'Gary Sanchez',
                playerImage: 'https://cdn.vox-cdn.com/thumbor/4P6tTiRoeUWN56YsPrjxPemxqkY=/0x0:4908x3378/1200x800/filters:focal(2062x1297:2846x2081)/cdn.vox-cdn.com/uploads/chorus_image/image/61415611/1031073442.jpg.0.jpg'
            },
            {
                category: 'RBI',
                value: 527,
                udlTeam: 'Maine Cobra Kai',
                udlTeamLogo: 'https://g.espncdn.com/s/flblm/logos/At%20the%20Ballpark-Robb%20Harskamp/Ballpark-11.svg',
                playerName: 'Josh Bell',
                playerImage: 'https://media.golfdigest.com/photos/578f9c5acf244f0c2ee9e17a/master/pass/Josh-Bell-Pirates.jpg'
            },
            {
                category: 'Stolen Bases',
                value: 86,
                udlTeam: 'Bringers of W.A.R.',
                udlTeamLogo: 'https://i.imgur.com/94GmH6O_d.jpg?maxwidth=640&shape=thumb&fidelity=medium',
                playerName: 'Mallex Smith',
                playerImage: 'https://cdn-images-1.medium.com/max/2400/1*lGUmOBOiujim1QeCDxT0Tg.jpeg'
            },
            {
                category: 'OBP',
                value: .3552,
                udlTeam: 'Forgot About Trea',
                udlTeamLogo: 'https://g.espncdn.com/s/flblm/logos/At%20the%20Ballpark-Robb%20Harskamp/Ballpark-01.svg',
                playerName: 'Juan Soto',
                playerImage: 'https://cdnph.upi.com/svc/sv/upi/4341529362612/2018/1/f9de5257cbaea16a77e5d8078af94857/Nats-rookie-Juan-Soto-smashes-homer-before-MLB-debut.jpg'
            },
            {
                category: 'Strikeouts',
                value: 710,
                udlTeam: 'Bringers of W.A.R.',
                udlTeamLogo: 'https://i.imgur.com/94GmH6O_d.jpg?maxwidth=640&shape=thumb&fidelity=medium',
                playerName: 'Lance Lynn',
                playerImage: 'https://imagesvc.timeincapp.com/v3/fan/image?url=https%3A%2F%2Fnolanwritin.com%2Fwp-content%2Fuploads%2Fgetty-images%2F2017%2F07%2F1141809155.jpeg&c=sc&w=850&h=560'
            },
            {
                category: 'Quality Starts',
                value: 55,
                udlTeam: 'Bringers of W.A.R.',
                udlTeamLogo: 'https://i.imgur.com/94GmH6O_d.jpg?maxwidth=640&shape=thumb&fidelity=medium',
                playerName: 'Hyun-Jin Ryu',
                playerImage: 'https://static01.nyt.com/images/2019/05/31/sports/31metsweb1/31metsweb1-articleLarge.jpg?quality=75&auto=webp&disable=upscale'
            },
            {
                category: 'ERA',
                value: 3.392,
                udlTeam: 'Bringers of W.A.R.',
                udlTeamLogo: 'https://i.imgur.com/94GmH6O_d.jpg?maxwidth=640&shape=thumb&fidelity=medium',
                playerName: 'Mike Minor',
                playerImage: 'https://imagesvc.timeincapp.com/v3/fan/image?url=https://nolanwritin.com/wp-content/uploads/getty-images/2018/04/943164002-toronto-blue-jays-v-texas-rangers.jpg.jpg&'
            },
            {
                category: 'WHIP',
                value: 1.169,
                udlTeam: 'Big League Chu',
                udlTeamLogo: 'https://img.fantrax.com/logos/tmLogo_x1joq2kojf9xmujh_512.jpg',
                playerName: 'Josh Hader',
                playerImage: 'https://www.gannett-cdn.com/media/2018/07/17/USATODAY/USATODAY/636674651639573051-USATSI-10970060.jpg'
            },
            {
                category: 'Saves + Holds',
                value: 67,
                udlTeam: 'Big League Chu',
                udlTeamLogo: 'https://img.fantrax.com/logos/tmLogo_x1joq2kojf9xmujh_512.jpg',
                playerName: 'Tony Watson',
                playerImage: 'https://www.ocregister.com/wp-content/uploads/2018/03/gettyimages-939899792.jpg?w=441'
            }
        ],
        playoffs: {
            koufax: {
                "1": {
                    udlTeam: 'Hone Ron Runners',
                    udlTeamLogo: 'https://g.espncdn.com/lm-static/logo-packs/core/Solo/ESPN_Star_Wars_Lando-01.svg',
                    title: "Koufax West Champ"
                },
                "2": {
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
                    udlTeam: 'Forgot About Trea',
                    udlTeamLogo: 'https://g.espncdn.com/s/flblm/logos/At%20the%20Ballpark-Robb%20Harskamp/Ballpark-01.svg',
                    title: "Wild Card #2"
                },
            },
            aaron: {
                "1": {
                    udlTeam: 'Back2Back Jax',
                    udlTeamLogo: 'https://larrybrownsports.com/wp-content/uploads/2016/07/max-scherzer-eyes.jpg',
                    title: "Aaron East Champ"
                },
                "2": {
                    udlTeam: 'Big League Chu',
                    udlTeamLogo: 'https://img.fantrax.com/logos/tmLogo_x1joq2kojf9xmujh_512.jpg',
                    title: "Aaron West Champ"
                },
                "3": {
                    udlTeam: 'Discount Bob\'s Couch Emporium',
                    udlTeamLogo: 'http://g.espncdn.com/lm-app/lm/img/shell/shield-FLB.svg',
                    title: "Wild Card #1"
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