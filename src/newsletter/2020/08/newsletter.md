---
title: August 2020 Newsletter
date: 2020-08-28 06:00:00
type: post
blog: true
tags:
    - Newsletter
---

We're still playing baseball somehow!

![giolito](https://media.giphy.com/media/8FxCjHFhn5hnz1CiLO/giphy.gif)

This Giolito dude ruined all the #TorkWatch fun, but roto has been a fun switch-up and boy is that Cruz Line Cruzin'.

<h2 class="titleHug">Category Leaders - End of August</h2>
*as of the morning of August 27th
<LeagueLeaders :categories="categories"/>

<script>
export default {
  data() {
    return {
        categories: [
            {
                category: 'Runs',
                value: 193,
                udlTeam: 'Bringers of W.A.R.',
                udlTeamLogo: 'https://i.imgur.com/removed.png',
                playerName: 'Mike Yastrzemski',
                playerImage: 'https://www.mercurynews.com/wp-content/uploads/2019/08/1168500505.jpg'
            },
            {
                category: 'Home Runs',
                value: 61,
                udlTeam: 'Maine Cobra Kai',
                udlTeamLogo: 'https://g.espncdn.com/s/flblm/logos/At%20the%20Ballpark-Robb%20Harskamp/Ballpark-11.svg',
                playerName: 'Anthony Santander',
                playerImage: 'https://s.yimg.com/uu/api/res/1.2/wP0HXe5Y2WXQ8f02GeAZ1g--~B/aD0yOTE2O3c9NDM3MztzbT0xO2FwcGlkPXl0YWNoeW9u/https://media-mbst-pub-ue1.s3.amazonaws.com/creatr-images/2019-07/22971ab0-aee6-11e9-aefb-ae0c8c1185fe'
            },
            {
                category: 'RBI',
                value: 172,
                udlTeam: 'Bringers of W.A.R.',
                udlTeamLogo: 'https://i.imgur.com/removed.png',
                playerName: 'Charlie Blackmon',
                playerImage: 'https://i.cbc.ca/1.5625501.1593020920!/fileImage/httpImage/image.jpg_gen/derivatives/16x9_780/blackmon-charlie-190818-1180.jpg'
            },
            {
                category: 'Stolen Bases',
                value: 26,
                udlTeam: 'Hone Ron Runners',
                udlTeamLogo: 'https://g.espncdn.com/lm-static/logo-packs/core/Solo/ESPN_Star_Wars_Lando-01.svg',
                playerName: 'Fernando Tatis Jr.',
                playerImage: 'https://ca-times.brightspotcdn.com/dims4/default/df3da93/2147483647/strip/true/crop/2417x1611+0+0/resize/840x560!/quality/90/?url=https%3A%2F%2Fcalifornia-times-brightspot.s3.amazonaws.com%2Ff6%2F1a%2F8c1a22ab4567a0b85613e9b7067b%2Fpadres-dodgers-baseball-35938.jpg'
            },
            {
                category: 'OBP',
                value: .3646,
                udlTeam: 'Beanetown Cruz Line',
                udlTeamLogo: 'https://i.ibb.co/LYNJdbP/40823296-s.jpg',
                playerName: 'Michael Conforto',
                playerImage: 'https://images2.minutemediacdn.com/image/fetch/w_736,h_485,c_fill,g_auto,f_auto/https%3A%2F%2Frisingapple.com%2Fwp-content%2Fuploads%2Fgetty-images%2F2017%2F07%2F1174327119-850x560.jpeg'
            },
            {
                category: 'Strikeouts',
                value: 286,
                udlTeam: 'The Gamblers',
                udlTeamLogo: 'https://i.imgur.com/y1qKgk1.jpg',
                playerName: 'Sonny Gray',
                playerImage: 'https://cdn.vox-cdn.com/thumbor/aNL6WZMkEecYRwYu3X0h0jiUCxM=/0x0:4924x3144/1200x800/filters:focal(1864x722:2650x1508)/cdn.vox-cdn.com/uploads/chorus_image/image/66348566/1169253440.jpg.0.jpg'
            },
            {
                category: 'Innings Pitched',
                value: 251.2,
                udlTeam: 'The Gamblers',
                udlTeamLogo: 'https://i.imgur.com/y1qKgk1.jpg',
                playerName: 'Lance Lynn',
                playerImage: 'https://images2.minutemediacdn.com/image/fetch/c_fill,g_auto,f_auto,h_560,w_850/https%3A%2F%2Ffansided.com%2Fwp-content%2Fuploads%2Fgetty-images%2F2018%2F08%2F1228113700-850x560.jpeg'
            },
            {
                category: 'ERA',
                value: 3.022,
                udlTeam: 'Preston Perennials',
                udlTeamLogo: 'http://vandenberg.id.au/uploads/images/PP-small.jpg',
                playerName: 'Terry Francona',
                playerImage: 'https://i.insider.com/581a7590b28a642b0f8b5cf9?width=1100&format=jpeg&auto=webp'
            },
            {
                category: 'WHIP',
                value: 1.079,
                udlTeam: 'Team Riptide',
                udlTeamLogo: 'https://img.fantrax.com/logos/tmLogo_q9qkntnviwcl7gnr_512.jpg',
                playerName: 'Tyler Duffey',
                playerImage: 'https://www.fccnn.com/sports/article808945.ece/alternates/BASE_LANDSCAPE/Minnesota%20Twins%20starting%20pitcher%20Tyler%20Duffey%20%2856%29%20pitches%20during%20a%20game%20last%20season%20against%20the%20Kansas%20City%20Royals%20at%20Target%20Field.%20Brad%20Rempel%20%20USA%20TODAY%20Sports'
            },
            {
                category: 'Saves + Holds',
                value: 24,
                udlTeam: 'Mookie and The Betts',
                udlTeamLogo: 'https://www.thewrap.com/wp-content/uploads/2019/02/rocket-1.jpg',
                playerName: 'Taylor Rogers',
                playerImage: 'https://cdn.vox-cdn.com/thumbor/SMHRilCwt_Sts8OGu1ZCOYRW67c=/0x0:3000x2157/1200x800/filters:focal(774x620:1254x1100)/cdn.vox-cdn.com/uploads/chorus_image/image/63734842/1139718342.jpg.0.jpg'
            }
        ]
    };
  },
}
</script>