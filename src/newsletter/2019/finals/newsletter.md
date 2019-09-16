---
title: Championship Final 2019
date: 2019-09-16 06:00:00
type: post
blog: true
tags:
    - Newsletter
extras: true
---

Championship week is here! Congrats to Forgot About Trea and Big League Chu on a great season.

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
                            team1: "The Emporium",
                            team1Img: "http://www.trbimg.com/img-5ab9a0e2/turbine/ct-spt-cubs-yu-darvish-notes-20180326",
                            team2: "Team !Ponche!",
                            team2Img: "https://img.mlbstatic.com/mlb-images/image/private/t_2x1/t_w1536/mlb/zzcpwjsc8jwdlnxyuxo6.jpg",
                            story: "The Emporium had a busy week winning a close matchup and simultaneously rebranding the team. The injury bug has also been busy lately taking out Emporium stars Christian Yelich, Jose Ramirez, and Anthony Rizzo. Nevertheless, the team is lifted by their new full-priced status. Team !Ponche! snuck past Big League Chu with the tiebreaker and some stellar pitching. The offense cooled off just a touch, but there is still some healthy firepower there. The tantalizing luck charms of David Peralta and Jake Arrieta remain entrenched in the lineup and ready for the championship bout. \n The Emporium is limping into the final. Has the Team !Ponche! offense cooled enough for things to stay close? The matchup could be another close one as both rotations and bullpens could easily swing the fate of the 2019 UDL champion."
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