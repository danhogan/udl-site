---
title: April 2021 Newsletter
date: 2021-04-02 06:00:00
type: post
blog: true
tags:
    - Newsletter
extras: true
---

Hey! Say hello to a full 162 games ahead of us!

![lindor-hi](https://media.giphy.com/media/U8OVgqRHc4lYCFTFes/giphy.gif)

## Matchups To Watch

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

## Opening Day Power Rankings (AKA, Last Year's Roto Results)

1. Beanetown Cruz Line	
2. Bringers of W.A.R.	
3. Back2Back Jax	
4. Preston Perennials	
5. Torrano Beisbol Birds	
6. Mookie and The Betts	
7. The Emporium	
8. Maine Cobra Kai	
9. The Gamblers	
10. Big League Chu	
11.	Springfield Isotopes	
12.	Team Riptide	
13.	Hone Ron Runners	
14.	Wayne's Hardware	
15.	Fried Chicken Sandwich	
16.	Forgot About Trea	
17.	CT Clippers	
18.	Vengeful Tuna	
19.	Cat Scratch Fever	
20.	The Royal Rooters	


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
                week: 1,
                matchups: [
                    {
                        team1: "Beanetown Cruz Line",
                        team1Img: "https://cdn.vox-cdn.com/thumbor/qdpE14bnSjCpjSN-tuNY3HATylQ=/1400x1400/filters:format(jpeg)/cdn.vox-cdn.com/uploads/chorus_asset/file/22381995/1305190710.jpg",
                        team2: "Big League Chu",
                        team2Img: "https://img.bleacherreport.net/img/images/photos/003/864/377/hi-res-59621c5acd5382b651a24b22ff7aa146_crop_north.jpg?1587524820&w=3072&h=2048",
                        story: "Beanetown Cruz Line begins their title defense against Big League Chu in a battle of stacked rotations."
                    },
                    {
                        team1: "Torrano Beisbol Birds",
                        team1Img: "https://tipofthetower.com/wp-content/uploads/getty-images/2017/07/1171787674.jpeg",
                        team2: "Back2Back Jax",
                        team2Img: "https://pressboxonline.com/wp-content/uploads/2019/11/orioles19-625-trey-mancini-1-800x445.jpg",
                        story: "Both teams finished in the top 5 last year and will battle all year for the Aaron East title."
                    }
                ]
            }
        ]
    };
  },
}
</script>