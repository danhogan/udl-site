---
title: Championship Final 2021
date: 2021-09-20 06:00:00
type: post
blog: true
tags:
    - Newsletter
extras: true
---

## Semifinal Recap

### Torrano Beisbol Birds defeats Back2Back Jax
![Adam Wainwright](https://nypost.com/wp-content/uploads/sites/2/2021/09/Adam-Wainwright-Mets.jpg?quality=90&strip=all)

The Torrano Beisbol Birds keep rolling. In a tough matchup, the Birds pitching came through - eeking out victories in quality starts and the ratios. Adam Wainwright came up big - providing two of the three quality outings. Back2Back Jax had another fantastic season, but ultimately fell short. Michael Pineda and Chris Flexen each having outings of 5 and 2/3rds doesn't help to ease the pain in this one.

### Maine Cobra Kai defeats Big League Chu
![Nathan Eovaldi](https://cdn.bignewsnetwork.com/flm1632045901.jpg)

While none of the categories were particularly close, Maine Cobra Kai moves to the championship after grabbing ahold of six of them. Cobra Kai's pitching volume continues to rack up the quality starts and Ks for days. Big League Chu's pitching was excellent and put up solid ratios, but lacked the volume to compete in all pitching categories. From there, Cobra Kai's offense has stayed piping hot.

Congrats to Back2Back Jax and Big League Chu on a great season.

## Championship Matchup - A Closer Look
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
</style>

<script>
export default {
    data() {
        return {
            weeks: [
                {
                    matchups: [
                        {
                            team1: "Torrano Beisbol Birds",
                            team1Img: "https://images.seattletimes.com/wp-content/uploads/2021/09/urn-publicid-ap-org-61c93ac625d27539f1ef39075136e32eRays_Blue_Jays_Baseball_84800.jpg?d=780x519",
                            team2: "Maine Cobra Kai",
                            team2Img: "https://www.journal-advocate.com/wp-content/uploads/2021/09/TDP-L-ROCKIES-PHILLIES_JAC4154x.jpg",
                            story: "The Maine Cobra Kai pitching volume attack continues as two-start weeks are on the slate for Keuchel, E-Rod, and A.J. Alexy. The Birds have no such scheduling luck, but have the pitching to take any and all categories. Cobra Kai has the hotter offense coming into this week and all those Rockie bats get to hit at home, but anything can happen. It's been an astounding season by both squads just to get here. Best of luck!"
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