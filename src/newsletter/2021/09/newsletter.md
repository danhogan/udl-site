---
title: Playoffs 2021 Newsletter
date: 2021-09-06 06:00:00
type: post
blog: true
tags:
    - Newsletter
extras: true
---

The playoffs are here! Congrats to those that made it! Here is the bracket we have:
<PlayoffPicture :playoffs="playoffs"/>

## Playoff Matchups - A Closer Look
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

<h2 class="titleHug">Category Leaders - End of UDL Regular Season</h2>
*as of morning of September 6th
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
</style>

<script>
export default {
  data() {
    return {
        categories: [
            {
                category: 'Runs',
                value: 745,
                udlTeam: 'Forgot About Trea',
                udlTeamLogo: 'https://g.espncdn.com/s/flblm/logos/At%20the%20Ballpark-Robb%20Harskamp/Ballpark-01.svg',
                playerName: 'Mitch Haniger',
                playerImage: 'https://miro.medium.com/max/5184/1*MziMKwSwItArbVawLuLmUg.jpeg'
            },
            {
                category: 'Home Runs',
                value: 234,
                udlTeam: 'Forgot About Trea',
                udlTeamLogo: 'https://g.espncdn.com/s/flblm/logos/At%20the%20Ballpark-Robb%20Harskamp/Ballpark-01.svg',
                playerName: 'Salvador Perez',
                playerImage: 'https://kckingdom.com/wp-content/uploads/imagn-images/2017/07/14963304.jpeg'
            },
            {
                category: 'RBI',
                value: 715,
                udlTeam: 'Forgot About Trea',
                udlTeamLogo: 'https://g.espncdn.com/s/flblm/logos/At%20the%20Ballpark-Robb%20Harskamp/Ballpark-01.svg',
                playerName: 'Austin Riley',
                playerImage: 'https://i0.wp.com/www.sportstalkatl.com/wp-content/uploads/2021/06/dlv210608022-atl-v-phi.jpg?fit=1000%2C667&ssl=1'
            },
            {
                category: 'Stolen Bases',
                value: 142,
                udlTeam: 'Back2Back Jax',
                udlTeamLogo: 'https://larrybrownsports.com/wp-content/uploads/2016/07/max-scherzer-eyes.jpg',
                playerName: 'Starling Marte',
                playerImage: 'https://sportshub.cbsistatic.com/i/r/2021/08/10/935477e2-b5ab-4e2b-b501-5b73bc535b39/thumbnail/1200x675/6da17c9307b3341f5fdd5f9d35b8687e/gettyimages-13329739391.jpg'
            },
            {
                category: 'OBP',
                value: .3471,
                udlTeam: 'Riptide',
                udlTeamLogo: 'https://img.fantrax.com/logos/tmLogo_q9qkntnviwcl7gnr_512.jpg',
                playerName: 'Bryce Harper',
                playerImage: 'https://thatballsouttahere.com/wp-content/uploads/getty-images/2021/08/1336711074.jpeg'
            },
            {
                category: 'Strikeouts',
                value: 1157,
                udlTeam: 'The Gamblers',
                udlTeamLogo: 'https://i.imgur.com/y1qKgk1.jpg',
                playerName: 'Corbin Burnes',
                playerImage: 'https://www.yourbasin.com/wp-content/uploads/sites/78/2021/08/1de9c462a3754fe2976dd3d987c43b1c-1.jpg?w=2560&h=1440&crop=1'
            },
            {
                category: 'Quality Starts',
                value: 82,
                udlTeam: 'CT Clippers',
                udlTeamLogo: 'https://g.espncdn.com/lm-static/logo-packs/core/StarWarsTheRiseOfSkywalker/rise-skywalker-bb-8.svg',
                playerName: 'Walker Buehler',
                playerImage: 'https://www.ocregister.com/wp-content/uploads/2021/08/AP21233092281388.jpg?w=525'
            },
            {
                category: 'ERA',
                value: 3.374,
                udlTeam: 'The Gamblers',
                udlTeamLogo: 'https://i.imgur.com/y1qKgk1.jpg',
                playerName: 'Lance Lynn',
                playerImage: 'https://www.golfdigest.com/content/dam/images/golfdigest/fullset/2021/lancelynn_chicagowhitesox.jpg'
            },
            {
                category: 'WHIP',
                value: 1.126,
                udlTeam: 'Big League Chu',
                udlTeamLogo: 'https://img.fantrax.com/logos/tmLogo_x1joq2kojf9xmujh_512.jpg',
                playerName: 'Charlie Morton',
                playerImage: 'https://www.ajc.com/resizer/6BhTm_r69a3TgFhphkAKGmOzw2w=/814x458/cloudfront-us-east-1.images.arcpublishing.com/ajc/2XQXUSUNESPCODNZ44YZBAX5L4.jpg'
            },
            {
                category: 'Saves + Holds',
                value: 112,
                udlTeam: 'Beanetown Cruz Line',
                udlTeamLogo: 'https://i.ibb.co/LYNJdbP/40823296-s.jpg',
                playerName: 'Liam Hendriks',
                playerImage: 'https://www.imago-images.com/bild/sp/1005886794/s.jpg'
            }
        ],
        playoffs: {
            teams: {
                "2": {
                    udlTeam: 'The Gamblers',
                    udlTeamLogo: 'https://i.imgur.com/y1qKgk1.jpg',
                    title: "Aaron West Champ"
                },
                "3": {
                    udlTeam: 'Springfield Isotopes',
                    udlTeamLogo: 'https://capaddicts.com/wp-content/uploads/2015/08/simpsons-springfield-isotopes.png',
                    title: "Koufax West Champ"
                },
                "4": {
                    udlTeam: 'Wayne\'s Hardware',
                    udlTeamLogo: 'https://res.cloudinary.com/teepublic/image/private/s--LYtlPysQ--/t_Preview/b_rgb:eae0c7,c_limit,f_jpg,h_630,q_90,w_630/v1482729132/production/designs/990736_1.jpg',
                    title: "Koufax East Champion"
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
                "6": {
                    udlTeam: 'Big League Chu',
                    udlTeamLogo: 'https://img.fantrax.com/logos/tmLogo_x1joq2kojf9xmujh_512.jpg',
                    title: "Aaron Wild Card #2"
                },
                "7": {
                    udlTeam: 'Main Cobra Kai',
                    udlTeamLogo: 'https://g.espncdn.com/s/flblm/logos/At%20the%20Ballpark-Robb%20Harskamp/Ballpark-11.svg',
                    title: "Koufax Wild Card #1"
                },
                "5": {
                    udlTeam: 'Torrano Beisbol Birds',
                    udlTeamLogo: 'https://i.imgur.com/H2vkfYW.jpg',
                    title: "Aaron Wild Card #1"
                },
            }
        },
        weeks: [
            {
                matchups: [
                    {
                        team1: "Back2Back Jax",
                        team1Img: "https://thumbor.forbes.com/thumbor/960x0/https%3A%2F%2Fspecials-images.forbesimg.com%2Fimageserve%2F61194eaf6d0325c1992edc62%2FMLB--AUG-04-Astros-at-Dodgers%2F960x0.jpg%3Ffit%3Dscale",
                        team2: "Forgot About Trea",
                        team2Img: "https://www.kansascity.com/latest-news/p7u4nw/picture253840568/alternates/FREE_768/AP21241801948416.jpg",
                        story: "Back2Back Jax comes in as the #1 overall seed and does so for a reason. There is plenty of prowess in the lineup and an awful lot of speed, including the far-and-away two best theifs of the year in Starling Marte and Whit Merrifield. The rotation is hanging on the back of Max Scherzer and a solid bullpen could play a big factor as well. A possible two-start week from Scherzer could be huge and Chris Flexen, who has been racking up quality starts the last month, gets a nice matchup at home against Arizona.\nForgot About Trea comes in with the other major Nat-turned-Dodger and a load of hot offense including Salvador Perez and the always-incredible Juan Soto. Lucas Giolito has landed on the IL at a rather inopportune time and the uncertainty of Alex Wood's availability isn't encouraging either. Zack Wheeler will have to come up big in his Rocky Road matchup."
                    },
                    {
                        team1: "Wayne's Hardware",
                        team1Img: "https://jaysjournal.com/wp-content/uploads/getty-images/2017/07/1270154028.jpeg",
                        team2: "Torrano Beisbol Birds",
                        team2Img: "https://cdn.vox-cdn.com/thumbor/5DHzqwj6dsBBCZLia9esjDa2aNA=/0x0:3000x2000/1200x800/filters:focal(1260x760:1740x1240)/cdn.vox-cdn.com/uploads/chorus_image/image/69790289/1234927573.0.jpg",
                        story: "Wayne's Hardware features a solid lineup including the hot bat of Randy Arozarena. Joey Votto doing his thing again would be huge. The pitching staff features the red-hot Logan Webb, but gets him on a week he pitches in Coors. Luckily, the rotation also features Cy Young-hopeful Robbie Ray and some other arms that have potential to make a solid impact.\nBo Bichette leads the Torrano Beisbol Birds into battle alongside Manny Machado and the hot bat of Alex Verdugo. A potential two-start Aaron Nola could be a big factor if the ace can return to form. Adam Wainwright has been anchoring the staff recently, but gets a tough matchup against the Dodgers. This matchup could easily go either way."
                    },
                    {
                        team1: "Springfield Isotopes",
                        team1Img: "https://cdn.vox-cdn.com/thumbor/c3wBpH6DBqZpRXow_in0Jlq2zg8=/0x0:4335x2890/1200x800/filters:focal(1677x562:2369x1254)/cdn.vox-cdn.com/uploads/chorus_image/image/69725519/usa_today_16536703.0.jpg",
                        team2: "Big League Chu",
                        team2Img: "https://sportshub.cbsistatic.com/i/r/2021/08/11/32019cd7-38f2-4461-9274-32bf6900473c/thumbnail/1200x675/7c85ccff5ebfd14d51b4058573f1569b/cedricmullins.jpg",
                        story: "The Springfield Isotopes tried to tell me they wouldn't be here, but are one of the hottest teams in the UDL. Ty France and Javy Baez lead the charge with the offense while Dylan Cease and Jose Berrios try to hold the pitching together. The formidable bullpen led by Emmanuel Clase could also be a key factor.\nBig League Chu fought tooth and nail in the final week of the regular season to edge their way into the playoffs. Cedric Mullins, Ian Happ, and Lorenzo Cain are swinging hot bats that will carry the offensive production. A solid rotation featuring Tarik Skubal, Charlie Morton, and Blake Snell offers plenty of potential. Big League Chu also features one of the strongest bullpens in the league led by Josh Hader. This could be a fun one in the saves+holds category."
                    },
                    {
                        team1: "The Gamblers",
                        team1Img: "https://cdn.theathletic.com/app/uploads/2020/09/17010604/USATSI_14939556-1024x772.jpg",
                        team2: "Maine Cobra Kai",
                        team2Img: "https://cdn.vox-cdn.com/thumbor/qcedGMkAKwJahhAclxRlLNiIQQ4=/1400x1400/filters:format(jpeg)/cdn.vox-cdn.com/uploads/chorus_asset/file/22825988/usa_today_16677944.jpg",
                        story: "The Gamblers feature a thumping lineup including Matt Olson, Jorge Soler, J.D. Martinez, and Aaron Judge. Can Eugenio Suarez make a difference? The Gamblers pitching is stacked, but will Lance Lynn return to make a start this week? Either way, Luis Castillo and Corbin Burnes know how to hurl a few baseballs. Joe Musgrove is certainly great too, but has a tough matchup at Dodger Stadium. All those aces, but will it be a two-start Bailey Ober that tips the scales?\nYou can't spell Schwindel without \"win\". We shall see if Frank Schwindel can continue to carry the offense along with Nick Castellanos, Josh Bell, and Trevor Story. The Maine Cobra Kai rotation offers plenty of potential and includes two-start weeks from Lance McCullers and Jameson Taillon. It could be a tough go against The Gamblers rotation, but there is still hope!"
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