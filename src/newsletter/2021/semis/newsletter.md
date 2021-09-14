---
title: Semifinals 2021
date: 2021-09-14 16:00:00
type: post
blog: true
tags:
    - Newsletter
extras: true
---

## Quarterfinal Recap

### Back2Back Jax defeats Forgot About Trea
![Juan Soto](https://sportsnaut.com/wp-content/uploads/2021/09/MLB-Washington-Nationals-at-Atlanta-Braves-16710654-scaled.jpg)

The #1 overall seed took care of business and won a pretty close matchup. Sneaking by with one more run and one more home run was clutch as even 16 scoreless innings from Max Shcherzer was not enough to take the win in ERA. Getting one more save+hold was clutch as well.

### Torrano Beisbol Birds defeats Wayne's Hardware
![Alex Colome](https://img.mlbstatic.com/mlb-images/image/private/t_2x1/t_w1536/mlb/fi1c2s0uv5zxt3lvddje.jpg)

The Beisbol Birds offense was just a touch better and the pitching was able to hold it together enough to grab the ratio wins.

### Big League Chu defeats Springfield Isotopes
![Ian Happ](https://assets.cubsinsider.com/wp-content/uploads/2021/09/10073019/AP21249687697032-scaled.jpg)

Big League Chu came up big against perhaps the hottest team in the UDL. It was a very close matchup across the board with two well-matched teams, but Big League Chu had the edge everywhere except stolen bases.

### Maine Cobra Kai defeats The Gamblers
![Lance McCullers](https://cdn.theathletic.com/app/uploads/2021/09/12175750/GettyImages-1339874691-1024x683.jpg)

Maine Cobra Kai came up huge on the pitching side to take down one of the strongest rotations in the league. Two quality starts and 14 strikeouts from Lance McCullers Jr. proved too much for Corbin Burnes' 8 no-hit innings. Josh Bell and Ryan McMahon played their part as well keeping the edge on the offensive side.

## Onto The Semis

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
                        story: "Torrano Beisbol Birds get a potential two-starts from both Adam Wainwright and Rich Hill - so yay for old-dude pitching. The Birds had a touch more fire in their bats last week, but anything could happen and Back2Back Jax has stolen bases pretty well on lock. Back2Back Jax also gets Kershaw back for a potential 2 starts to go along with teammate Max Scherzer who is on quite a tear."
                    },
                    {
                        team1: "Big League Chu",
                        team1Img: "https://www.ajc.com/resizer/SWLPqPI02xELS3VGS9AVKeSbw68=/814x458/cloudfront-us-east-1.images.arcpublishing.com/ajc/S5WUKDZVIREQJHP3JDWHKYPAWQ.jpg",
                        team2: "Maine Cobra Kai",
                        team2Img: "https://9b16f79ca967fd0708d1-2713572fef44aa49ec323e813b06d2d9.ssl.cf2.rackcdn.com/1140x_a10-7_cTC/Miami-Marlins-v-Washington-Nationals-2-1631314656.jpg",
                        story: "Big League Chu had the better offense last week while Maine Cobra Kai had standout pitching. I could see a lot of categories \"meet in the middle\" and be very close. Two starts from E-Rod and Eovaldi give Cobra Kai the volume potential to be strong in strikeouts and quality starts again while Big League Chu almost certainly will run away with saves+holds. The ratios could be key."
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