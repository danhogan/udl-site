---
title: June 2019 Matchups To Watch
date: 2019-07-04 06:00:00
type: post
tags:
    - Matchups
---

# June 2019 Matchups To Watch
<!-- http://static1.comicvine.com/uploads/original/11112/111129141/5440487-1122329314-52705.png -->

Here are some good matchups to watch as we near the All-Star break.

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
<p>{{matchup.story}}</p>

</div>

</div>

<script>
export default {
    data() {
        return {
            weeks: [
                {
                    week: 14,
                    matchups: [
                        {
                            team1: "Hone Ron Runners",
                            team1Img: "https://imagesvc.timeincapp.com/v3/fan/image?url=https://sodomojo.com/wp-content/uploads/getty-images/2017/07/1136588957.jpeg&",
                            team2: "Discount Bob's Couch Emporium",
                            team2Img: "https://cdn.vox-cdn.com/thumbor/skPmCumgtbt--fL1I5ULDKvds3M=/0x0:3119x2152/1200x800/filters:focal(1035x81:1533x579)/cdn.vox-cdn.com/uploads/chorus_image/image/61719557/1027371596.jpg.0.jpg",
                            story: "A cross-league matchup between top teams."
                        }
                    ]
                },
                {
                    week: 15,
                    matchups: [
                        {
                            team1: "Back2Back Jax",
                            team1Img: "https://www.washingtonpost.com/resizer/ipO_A39dXL2mK_BtbjldiBdNmW4=/1385x0/arc-anglerfish-washpost-prod-washpost.s3.amazonaws.com/public/HJWOJ4A2OAI6RGHVZ3WPVB2BWY.jpg",
                            team2: "Bringers of W.A.R.",
                            team2Img: "https://thumbor.forbes.com/thumbor/960x0/https%3A%2F%2Fspecials-images.forbesimg.com%2Fdam%2Fimageserve%2F1143874470%2F960x0.jpg%3Ffit%3Dscale",
                            story: "A cross-league matchup between top teams."
                        },
                        {
                            team1: "The Gamblers",
                            team1Img: "https://cdn.vox-cdn.com/thumbor/8XCJfPgQ-o1HX0bZQIMbvKVGBVc=/0x0:4371x2915/1200x800/filters:focal(1023x145:1721x843)/cdn.vox-cdn.com/uploads/chorus_image/image/63645506/usa_today_12543456.0.jpg",
                            team2: "Hone Ron Runners",
                            team2Img: "https://thenypost.files.wordpress.com/2019/03/jacob-degrom-4.jpg?quality=90&strip=all",
                            story: "Good teams in a cross-league matchup. Plus I'm listing them here in hopes they'll publicly fight in Slack."
                        },
                        {
                            team1: "Discount Bob's Couch Emporium",
                            team1Img: "https://www.denverpost.com/wp-content/uploads/2019/03/6edebb2cccd14ce094fb367ace9e0d7b.jpg?w=541",
                            team2: "Forgot About Trea",
                            team2Img: "https://cdnph.upi.com/svc/sv/upi/4341529362612/2018/1/f9de5257cbaea16a77e5d8078af94857/Nats-rookie-Juan-Soto-smashes-homer-before-MLB-debut.jpg",
                            story: "The cross-league matchups continue. We need a Koufax vs Aaron matchup tracker."
                        }
                    ]
                },
                {
                    week: 16,
                    matchups: [
                        {
                            team1: "Hone Ron Runners",
                            team1Img: "https://imagesvc.timeincapp.com/v3/fan/image?url=https://aroundthefoghorn.com/wp-content/uploads/getty-images/2016/04/1158320881.jpeg&c=sc&w=850&h=560",
                            team2: "Big League Chu",
                            team2Img: "https://www.mercurynews.com/wp-content/uploads/2019/03/Matt-Chapman1.jpg?w=620",
                            story: "Does Mario ever get an easy matchup?"
                        },
                        {
                            team1: "Forgot About Trea",
                            team1Img: "https://www.washingtonpost.com/resizer/mOXdtcHJc3vrP0yhT_SNJ4YBWqk=/1484x0/arc-anglerfish-washpost-prod-washpost.s3.amazonaws.com/public/F27YOWWEJII6RFCR5B4PS27BTM.jpg",
                            team2: "The Gamblers",
                            team2Img: "https://image.nj.com/home/njo-media/width600/img/yankees_main/photo/mlb-new-york-yankees-at-houston-astros-ae5d1ed491867b26.jpg",
                            story: "Both teams with 68 wins and clinging to a wild card spot at the time of this writing."
                        }
                    ]
                }
            ]
        };
    }
};
</script>

<style>
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