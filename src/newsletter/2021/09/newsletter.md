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
*as of September 3rd
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
                value: 863,
                udlTeam: 'Back2Back Jax',
                udlTeamLogo: 'https://larrybrownsports.com/wp-content/uploads/2016/07/max-scherzer-eyes.jpg',
                playerName: 'Anthony Rendon',
                playerImage: 'https://upload.wikimedia.org/wikipedia/commons/0/0a/Anthony_Rendon_%2814430676940%29.jpg'
            },
            {
                category: 'Home Runs',
                value: 271,
                udlTeam: 'Back2Back Jax',
                udlTeamLogo: 'https://larrybrownsports.com/wp-content/uploads/2016/07/max-scherzer-eyes.jpg',
                playerName: 'Eugenio Suarez',
                playerImage: 'https://imagesvc.timeincapp.com/v3/fan/image?url=https://blogredmachine.com/wp-content/uploads/getty-images/2017/07/966940688.jpeg&c=sc&w=850&h=560'
            },
            {
                category: 'RBI',
                value: 825,
                udlTeam: 'Back2Back Jax',
                udlTeamLogo: 'https://larrybrownsports.com/wp-content/uploads/2016/07/max-scherzer-eyes.jpg',
                playerName: 'Corey Dickerson',
                playerImage: 'https://www.inquirer.com/resizer/xanp9SfpZzXlw50mI2DkOEQhkh4=/1400x932/smart/arc-anglerfish-arc2-prod-pmn.s3.amazonaws.com/public/SG5UUAJUSBBZZPP5M67QJFIIOI.jpg'
            },
            {
                category: 'Stolen Bases',
                value: 123,
                udlTeam: 'Bringers of W.A.R.',
                udlTeamLogo: 'https://i.imgur.com/94GmH6O_d.jpg?maxwidth=640&shape=thumb&fidelity=medium',
                playerName: 'Mallex Smith',
                playerImage: 'https://cdn-images-1.medium.com/max/2400/1*lGUmOBOiujim1QeCDxT0Tg.jpeg'
            },
            {
                category: 'OBP',
                value: .3551,
                udlTeam: 'Team !Ponche!',
                udlTeamLogo: 'https://g.espncdn.com/lm-static/flb/images/default_logos/5.svg',
                playerName: 'Kolten Wong',
                playerImage: 'https://cdn.vox-cdn.com/thumbor/6bTT9QL9SZALn4T6i88tvLgHeqg=/0x0:3478x2625/1200x800/filters:focal(1297x210:1853x766)/cdn.vox-cdn.com/uploads/chorus_image/image/60004911/usa_today_10869569.0.jpg'
            },
            {
                category: 'Strikeouts',
                value: 1175,
                udlTeam: 'The Gamblers',
                udlTeamLogo: 'https://i.imgur.com/y1qKgk1.jpg',
                playerName: 'Luis Castillo',
                playerImage: 'https://imagesvc.timeincapp.com/v3/fan/image?url=https://aroundthefoghorn.com/wp-content/uploads/getty-images/2016/04/976408576.jpeg&c=sc&w=1600&h=1067'
            },
            {
                category: 'Quality Starts',
                value: 87,
                udlTeam: 'Team Riptide',
                udlTeamLogo: 'https://img.fantrax.com/logos/tmLogo_q9qkntnviwcl7gnr_512.jpg',
                playerName: 'Jack Flaherty',
                playerImage: 'https://cdn.vox-cdn.com/thumbor/LtAzYfUjQEagd3FaS3KO-pZE5x8=/0x0:4183x3433/1200x800/filters:focal(1444x88:2112x756)/cdn.vox-cdn.com/uploads/chorus_image/image/56525221/usa_today_10253154.0.jpg'
            },
            {
                category: 'ERA',
                value: 3.712,
                udlTeam: 'Hone Ron Runners',
                udlTeamLogo: 'https://g.espncdn.com/lm-static/logo-packs/core/Solo/ESPN_Star_Wars_Lando-01.svg',
                playerName: 'Jacob DeGrom',
                playerImage: 'https://res-2.cloudinary.com/ybmedia/image/upload/c_crop,h_1123,w_2000,x_0,y_28/c_fill,f_auto,h_495,q_auto,w_880/v1/m/2/3/2323efe5c4e7689fa1bda72af9e0feb85312935a/12534647.jpg'
            },
            {
                category: 'WHIP',
                value: 1.193,
                udlTeam: 'Preston Perennials',
                udlTeamLogo: 'http://vandenberg.id.au/uploads/images/PP-small.jpg',
                playerName: 'Shane Bieber',
                playerImage: 'https://cdn.vox-cdn.com/thumbor/gWhl63ydAlxHlAiIyAvpq5wGuac=/0x0:3014x2009/1200x800/filters:focal(1408x277:1890x759)/cdn.vox-cdn.com/uploads/chorus_image/image/60592087/1004910524.jpg.0.jpg'
            },
            {
                category: 'Saves + Holds',
                value: 102,
                udlTeam: 'Big League Chu',
                udlTeamLogo: 'https://img.fantrax.com/logos/tmLogo_x1joq2kojf9xmujh_512.jpg',
                playerName: 'Kirby Yates',
                playerImage: 'https://thenypost.files.wordpress.com/2019/05/kirby-yates.jpg?quality=90&strip=all'
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
                    udlTeam: 'Bringers of W.A.R.',
                    udlTeamLogo: 'https://i.imgur.com/94GmH6O_d.jpg?maxwidth=640&shape=thumb&fidelity=medium',
                    title: "Koufax East Champ"
                },
                "6": {
                    udlTeam: 'Team !Ponche!',
                    udlTeamLogo: 'https://g.espncdn.com/lm-static/flb/images/default_logos/5.svg',
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
                "7": {
                    udlTeam: 'Big League Chu',
                    udlTeamLogo: 'https://img.fantrax.com/logos/tmLogo_x1joq2kojf9xmujh_512.jpg',
                    title: "Aaron Wild Card #2"
                },
                "4": {
                    udlTeam: 'Discount Bob\'s Couch Emporium',
                    udlTeamLogo: 'http://g.espncdn.com/lm-app/lm/img/shell/shield-FLB.svg',
                    title: "Aaron West Champ"
                },
                "5": {
                    udlTeam: 'The Gamblers',
                    udlTeamLogo: 'https://i.imgur.com/y1qKgk1.jpg',
                    title: "Aaron Wild Card #1"
                },
            }
        },
        weeks: [
            {
                matchups: [
                    {
                        team1: "Back2Back Jax",
                        team1Img: "https://cdn.mlbtraderumors.com/files/2018/05/anthony-rendon-nationals-1024x749.jpg",
                        team2: "Forgot About Trea",
                        team2Img: "https://s.yimg.com/ny/api/res/1.2/7YQ2AWMAfoCthuLSLLOc_g--~A/YXBwaWQ9aGlnaGxhbmRlcjtzbT0xO3c9ODAw/http://media.zenfs.com/en-US/homerun/nbcsports.com/7010d418f5f13129b8f3533226cc7f55",
                        story: "Back2Back Jax may have the most lethal offense in the league and they just got Willson Contreras and Edwin Encarnacion back. Oh boy. Anthony Rendon continues to mess around trying to steal the MVP. Kerhsaw plus a two-start Scherzer could make the difference for the Jax if they can keep the likes of Andrew Cashner and Robbie Ray afloat. \n Forgot About Trea needs some Washington bats to remain hot as they ride Trea Turner and Juan Soto into the playoffs. Whit Merrifield and Kris Bryant also wait in the wings to make a big impact. Trea's pitching might be a little riskier, but there's plenty of upside. Lucas Gioloto, Mike Fiers, Zack Wheeler, and Miles Mikolas all can put in big starts. Wheeler's performance in Washington on Wednesday could prove to be a large factor in this UDL first-round matchup."
                    },
                    {
                        team1: "Discount Bob\'s Couch Emporium",
                        team1Img: "https://b.fssta.com/uploads/2019/07/pi-fsw-brewers-christian-yelich-reds-070119.jpg",
                        team2: "The Gamblers",
                        team2Img: "https://image.masslive.com/home/mass-media/width600/img/redsox_impact/photo/jd-martinez-885bd725b66f95f0.jpg",
                        story: "Discount Bob\'s Couch Emporium is lollygagging into the playoffs hoping Christian Yelich can go nuclear in September once again. Either that or Jake Cave will have to save the day. The Emporium has an interesting array of pitching that could easily go either way. \n The Gamblers are roaring into the playoffs behind studs like Aaron Judge and J.D. Martinez. Solid pitching with decent matchups puts the Gamblers in a good position to go for the underdog win here."
                    },
                    {
                        team1: "Bringers of W.A.R.",
                        team1Img: "https://fivethirtyeight.com/wp-content/uploads/2019/08/GettyImages-1161893364-1-e1565305146478.jpg?w=575",
                        team2: "Team !Ponche!",
                        team2Img: "https://thecomeback.com/wp-content/uploads/2016/08/578055522.jpg",
                        story: "The Bringers of W.A.R. have the bats and speed to compete with anyone. Mike Trout is Mike Trout and Mallex Smith has a 'chief thief' title to uphold. Can old-man Pujols make a difference in the fantasy playoffs of 2019? Bringers of W.A.R. pitching has lucked into some nice matchups during this first-round matchup as well. \n Team !Ponche\'s! offense is firing on all cylinders with Yadier Molina, Freddie Freeman, Kolten Wong, Nolan Arenado, Ketel Marte, and wow - the whole lineup is swinging a hot bat. However, leaving David Peralta in the lineup while he's recovering from surgery likely won't be helpful. Team !Ponche! has Greinke in Milwaukee and Corbin at Atlanta that could prove to be important starts. Jake Arrieta, who is also recovering from surgery, is cheering on Team !Ponche! in the lineup."
                    },
                    {
                        team1: "Hone Ron Runners",
                        team1Img: "https://i.kinja-img.com/gawker-media/image/upload/s--ZP6_XTmq--/c_scale,f_auto,fl_progressive,q_80,w_800/futehocw713yof5l0ezy.jpg",
                        team2: "Big League Chu",
                        team2Img: "https://www.washingtonpost.com/resizer/Kh1Ki1j9tHCgIvGkcwTa5jEwutc=/1484x0/arc-anglerfish-washpost-prod-washpost.s3.amazonaws.com/public/KP5E2IECCMI6TEZ5OUAQODXGNE.jpg",
                        story: "Hone Ron Runners are storming into the playoffs as the top seed of the Koufax League. Aristedes Aquino continues to be ridiculous and Adalberto Mondesi came flying back from injury. A hot Tommy Pham and Kevin Newman combined with the solid Justin Turner will make for an offense difficult to compete with. The Runners also roster top-flight pitching in the likes of Jacob DeGrom and Justin Verlander. Maybe Madison Bumgarner can give the Runners a little playoff magic too. Solid relievers make Hone Ron Runners an all-around juggernaut. \n Big League Chu needs Jorge Polanco and Mark Canha to stay hot in order to compete in the offensive categories in this matchup. Solid starts from Jon Lester, Chris Paddack, Stephen Strasburg, and Charlie Morton might help be able to compete with the Runners' top arms."
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