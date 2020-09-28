---
title: Season End 2020
date: 2020-09-28 06:00:00
type: post
blog: true
tags:
    - Newsletter
extras: true
---

## Congratulations to our 2020 UDL Champion - Beanetown Cruz Line!
<div class="imageGroup">
<div class="imageContainer" v-for="image in emporium1">
<img :src="image">
</div>
</div>
<img class="championLogo" src="https://i.ibb.co/LYNJdbP/40823296-s.jpg" />
<div class="imageGroup">
<div class="imageContainer" v-for="image in emporium2">
<img :src="image">
</div>
</div>

Beanetown Cruz Line sailed to victory by a large margin. The Cruz Line finished top 5 in all categories except for innings pitched and truly dominated the short season. In an unpredictable tsunami of a year, the Cruz Line stayed steady 'til the end.

<h2 class="titleHug">Category Leaders - End of UDL Season</h2>
*as of September 28th
<LeagueLeaders :categories="categories"/>

Thanks everyone for a great year!

<script>
export default {
    data() {
        return {
            emporium1: [
                "https://cdn.theathletic.com/app/uploads/2019/06/25232922/GettyImages-1158311572-1024x687.jpg",
                "https://arc-anglerfish-arc2-prod-tbt.s3.amazonaws.com/public/LBEGRQLANVCP5OVUSTUHL7MBUI.jpg",
                "https://images2.minutemediacdn.com/image/fetch/w_2000,h_2000,c_fit/https%3A%2F%2Frisingapple.com%2Fwp-content%2Fuploads%2Fgetty-images%2F2018%2F08%2F1273955372.jpeg",
                "https://s.yimg.com/uu/api/res/1.2/ib1KJgm6EPk1HsdN1C.vPg--~B/aD0yNzU0O3c9Mzk5NDtzbT0xO2FwcGlkPXl0YWNoeW9u/https://media-mbst-pub-ue1.s3.amazonaws.com/creatr-images/2019-08/63eb4300-b667-11e9-b87f-f88768f7c5f4"
            ],
            emporium2: [
                "https://s.yimg.com/ny/api/res/1.2/SazLswDkeGfCAVkZfEPjoQ--~A/YXBwaWQ9aGlnaGxhbmRlcjtzbT0xO3c9ODAw/https://media.zenfs.com/en/sny_articles_235/3a5efc8062cce4926070378bd61b2138",
                "https://img.kyodonews.net/english/public/images/posts/1a9e4042ab0828bf466a396272ea9520/photo_l.jpg",
                "https://www.dailyherald.com/storyimage/DA/20200819/SPORTS/200819140/AR/0/AR-200819140.jpg&updated=202008191409&MaxW=900&maxH=900&noborder&Q=80",
                "https://images2.minutemediacdn.com/image/fetch/w_736,h_485,c_fill,g_auto,f_auto/https%3A%2F%2Freviewingthebrew.com%2Fwp-content%2Fuploads%2Fgetty-images%2F2017%2F07%2F1266798925-850x560.jpeg"
            ],
            categories: [
                {
                    category: 'Runs',
                    value: 361,
                    udlTeam: 'Bringers of W.A.R.',
                    udlTeamLogo: 'https://i.imgur.com/removed.png',
                    playerName: 'Tim Anderson',
                    playerImage: 'https://article-file-photos.s3.amazonaws.com/l_he6kd118202022344PM.jpg'
                },
                {
                    category: 'Home Runs',
                    value: 109,
                    udlTeam: 'Maine Cobra Kai',
                    udlTeamLogo: 'https://g.espncdn.com/s/flblm/logos/At%20the%20Ballpark-Robb%20Harskamp/Ballpark-11.svg',
                    playerName: 'Marcell Ozuna',
                    playerImage: 'https://cdn.chatsports.com/thumbnails/328-73830-original.jpeg'
                },
                {
                    category: 'RBI',
                    value: 324,
                    udlTeam: 'Bringers of W.A.R.',
                    udlTeamLogo: 'https://i.imgur.com/removed.png',
                    playerName: 'Mike Trout',
                    playerImage: 'https://image.cnbcfm.com/api/v1/image/103528737-GettyImages-513787246.jpg?v=1586097315&w=1400&h=950'
                },
                {
                    category: 'Stolen Bases',
                    value: 52,
                    udlTeam: 'Hone Ron Runners',
                    udlTeamLogo: 'https://g.espncdn.com/lm-static/logo-packs/core/Solo/ESPN_Star_Wars_Lando-01.svg',
                    playerName: 'Adalberto Mondesi',
                    playerImage: 'https://www.kansascity.com/latest-news/ap3i15/picture228803114/alternates/FREE_1140/KCM_ROYALSTWINS040319JAT094F.JPG'
                },
                {
                    category: 'OBP',
                    value: .3584,
                    udlTeam: 'Bringers of W.A.R.',
                    udlTeamLogo: 'https://i.imgur.com/removed.png',
                    playerName: 'DJ LeMahieu',
                    playerImage: 'https://fivethirtyeight.com/wp-content/uploads/2019/10/GettyImages-1181740243-1-e1571375463328.jpg?w=575'
                },
                {
                    category: 'Strikeouts',
                    value: 524,
                    udlTeam: 'The Gamblers',
                    udlTeamLogo: 'https://i.imgur.com/y1qKgk1.jpg',
                    playerName: 'Luis Castillo',
                    playerImage: 'https://imagesvc.timeincapp.com/v3/fan/image?url=https://aroundthefoghorn.com/wp-content/uploads/getty-images/2016/04/976408576.jpeg&c=sc&w=1600&h=1067'
                },
                {
                    category: 'Innings Pitched',
                    value: 463.1,
                    udlTeam: 'The Gamblers',
                    udlTeamLogo: 'https://i.imgur.com/y1qKgk1.jpg',
                    playerName: 'Lance Lynn',
                    playerImage: 'https://calltothepen.com/wp-content/uploads/getty-images/2018/08/1158916682.jpeg'
                },
                {
                    category: 'ERA',
                    value: 3.312,
                    udlTeam: 'Back2Back Jax',
                    udlTeamLogo: 'https://larrybrownsports.com/wp-content/uploads/2016/07/max-scherzer-eyes.jpg',
                    playerName: 'Clayton Kershaw',
                    playerImage: 'https://ca-times.brightspotcdn.com/dims4/default/9284aa2/2147483647/strip/true/crop/4385x2923+0+0/resize/1486x991!/quality/90/?url=https%3A%2F%2Fcalifornia-times-brightspot.s3.amazonaws.com%2Fe4%2Fd0%2F21d103424e2da9d6eb7c7f78cc06%2Fdodgers-baseball-00686.jpg'
                },
                {
                    category: 'WHIP',
                    value: 1.137,
                    udlTeam: 'Mookie and The Betts',
                    udlTeamLogo: 'https://www.thewrap.com/wp-content/uploads/2019/02/rocket-1.jpg',
                    playerName: 'Brandon Woodruff',
                    playerImage: 'https://images2.minutemediacdn.com/image/fetch/w_2000,h_2000,c_fit/https%3A%2F%2Freviewingthebrew.com%2Fwp-content%2Fuploads%2Fgetty-images%2F2020%2F07%2F1227833183.jpeg'
                },
                {
                    category: 'Saves + Holds',
                    value: 43,
                    udlTeam: 'Beanetown Cruz Line and Mookie and The Betts (Tie)',
                    udlTeamLogo: 'https://i.ibb.co/LYNJdbP/40823296-s.jpg',
                    playerName: 'Liam Hendriks',
                    playerImage: 'https://ca-times.brightspotcdn.com/dims4/default/5d1cfbc/2147483647/strip/true/crop/3967x2645+0+0/resize/840x560!/quality/90/?url=https%3A%2F%2Fcalifornia-times-brightspot.s3.amazonaws.com%2F7e%2Fee%2Fce1237acd190d500bd1b56f5a735%2F518769ddd1904f57a2b39bda92e0e280'
                }
            ],
        };
    },
    filters: {
        newLines: function(str){
            return str.replace(/(\r\n|\n|\r)/gm, "<br><br>")
        }
    }
}
</script>

<style>
.authorName {
    font-size: 1rem;
}

.titleHug {
    margin-bottom: .3em;
}

.imageGroup {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr;
}

.imageContainer > img {
    display: block;
    width: 100%;
    height: 10em;
    object-fit: cover;
}

.championLogo {
    max-height: 20em;
    display: block;
    margin: auto;
}
</style>