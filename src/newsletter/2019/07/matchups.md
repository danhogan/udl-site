---
title: July 2019 Matchups To Watch
date: 2019-07-29 06:00:00
type: post
tags:
    - Matchups
---

# July 2019 Matchups To Watch

Here are some good matchups in the midst of the UDL playoff race.

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
                    week: 17,
                    matchups: [
                        {
                            team1: "Back2Back Jax",
                            team1Img: "https://www.washingtonpost.com/resizer/ipO_A39dXL2mK_BtbjldiBdNmW4=/1385x0/arc-anglerfish-washpost-prod-washpost.s3.amazonaws.com/public/HJWOJ4A2OAI6RGHVZ3WPVB2BWY.jpg",
                            team2: "Team !Ponche!",
                            team2Img: "https://imagesvc.timeincapp.com/v3/mm/image?url=https%3A%2F%2Fcdn-s3.si.com%2Fs3fs-public%2Fstyles%2Fmarquee_large_2x%2Fpublic%2F2015%2F06%2F15%2Fnolan-arenado-ap2.jpg%3Fitok%3Dakr6D9Sb&w=1000&q=70",
                            story: "!Ponche! clings to their playoff spot while going up against the winningest team in the UDL."
                        },
                        {
                            team1: "Forgot About Trea",
                            team1Img: "https://cdnph.upi.com/svc/sv/upi/4341529362612/2018/1/f9de5257cbaea16a77e5d8078af94857/Nats-rookie-Juan-Soto-smashes-homer-before-MLB-debut.jpg",
                            team2: "Big League Chu",
                            team2Img: "https://www.mercurynews.com/wp-content/uploads/2019/03/Matt-Chapman1.jpg?w=620",
                            story: "Cross-league matchup of teams looking to hold on to their playoff spots."
                        },
                        {
                            team1: "Discount Bob's Couch Emporium",
                            team1Img: "https://img.bleacherreport.net/img/images/photos/003/800/551/hi-res-4fbd79987d6034eb2baf85886179f57b_crop_north.jpg?h=533&w=800&q=70&crop_x=center&crop_y=top",
                            team2: "Preston Perennials",
                            team2Img: "https://media.wkyc.com/assets/WKYC/images/1bbfec8f-6068-4958-97c7-e973df8d75b3/1bbfec8f-6068-4958-97c7-e973df8d75b3_750x422.jpg",
                            story: "The team from down under has that dark-horse vibe and we all know it."
                        }
                    ]
                },
                {
                    week: 18,
                    matchups: [
                        {
                            team1: "Preston Perennials",
                            team1Img: "https://shepherdexpress.com/downloads/44567/download/HiuraKeston19PS0008.jpg?cb=5a52d55f82b1877efacdb377b6631e22&w=640",
                            team2: "The Gamblers",
                            team2Img: "https://cdn.vox-cdn.com/thumbor/8XCJfPgQ-o1HX0bZQIMbvKVGBVc=/0x0:4371x2915/1200x800/filters:focal(1023x145:1721x843)/cdn.vox-cdn.com/uploads/chorus_image/image/63645506/usa_today_12543456.0.jpg",
                            story: "Teams living on the fringe of the playoffs."
                        }
                    ]
                },
                {
                    week: 19,
                    matchups: [
                        {
                            team1: "Wayne's Hardware",
                            team1Img: "https://a.espncdn.com/combiner/i?img=%2Fphoto%2F2018%2F0526%2Fr376053_1296x729_16%2D9.jpg",
                            team2: "Big League Chu",
                            team2Img: "https://sportshub.cbsistatic.com/i/r/2019/07/23/9dca44aa-042f-4401-989a-cd4d61fb65ef/thumbnail/1200x675/3ae8996bb615042a030fdca3f238e7f4/travis-darnaud-1400.jpg",
                            story: "Wayne's Hardware holds on to playoff hopes in a tough matchup."
                        },
                        {
                            team1: "Team !Ponche!",
                            team1Img: "https://s22927.pcdn.co/wp-content/uploads/2019/07/cody-bellinger-3.jpeg",
                            team2: "The Gamblers",
                            team2Img: "https://img.bleacherreport.net/img/images/photos/003/800/217/hi-res-ee1635a57d17a83dbcc3c6c5b873a082_crop_north.jpg?h=533&w=800&q=70&crop_x=center&crop_y=top",
                            story: "Playoff contenders both trying to cling to their spots."
                        }
                    ]
                },
                {
                    week: 20,
                    matchups: [
                        {
                            team1: "Big League Chu",
                            team1Img: "https://img.bleacherreport.net/img/images/photos/003/808/812/hi-res-dc047e8baf46ec8fdc8cf705a3d2b638_crop_north.jpg?h=533&w=800&q=70&crop_x=center&crop_y=top",
                            team2: "Team !Ponche!",
                            team2Img: "https://cdn-s3.si.com/styles/marquee_large_2x/s3/images/walker-buehler-topper.jpg?itok=MVRgQPG9",
                            story: "Matchup between two playoff contenders that have a tough schedule to close out the season."
                        }
                    ]
                },
                {
                    week: 21,
                    matchups: [
                        {
                            team1: "Bringers of W.A.R.",
                            team1Img: "https://cdn.vox-cdn.com/thumbor/LA50LvheoSlbB3F3QT4jRjzV4lg=/0x0:5067x3347/1200x800/filters:focal(1845x176:2655x986)/cdn.vox-cdn.com/uploads/chorus_image/image/59765607/952558268.jpg.0.jpg",
                            team2: "Discount Bob's Couch Emporium",
                            team2Img: "https://thespun.com/wp-content/uploads/2019/07/GettyImages-1157611870-775x465.jpg",
                            story: "Has the potential for a championship preview."
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