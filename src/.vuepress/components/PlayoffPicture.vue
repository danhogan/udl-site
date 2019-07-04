<template>
    <div class="wrapper">
        <div class="item">
            <div class="item-parent">
                <p>UDL Championship</p>
            </div>
            <div class="item-childrens">
                <div class="item-child">
                    <div class="item">
                        <div class="item-parent">
                            <p>KLCS</p>
                        </div>
                        <div class="item-childrens">
                            <div class="item-child">
                                <div class="item">
                                    <div class="item-parent">
                                        <p>KLDS</p>
                                    </div>
                                    <div class="item-childrens">
                                        <div class="item-child">
                                            <div class="block">
                                                <img :src="playoffs.koufax[1].udlTeamLogo">
                                                <div>
                                                    <h2>{{playoffs.koufax[1].title}}</h2>
                                                    <p>1. {{playoffs.koufax[1].udlTeam}}</p>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="item-child">
                                            <div class="block">
                                                <img :src="playoffs.koufax[4].udlTeamLogo">
                                                <div>
                                                    <h2>{{playoffs.koufax[4].title}}</h2>
                                                    <p>4. {{playoffs.koufax[4].udlTeam}}</p>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                            <div class="item-child">
                                <div class="item">
                                    <div class="item-parent">
                                        <p>KLDS</p>
                                    </div>
                                    <div class="item-childrens">
                                        <div class="item-child">
                                            <div class="block">
                                                <img :src="playoffs.koufax[2].udlTeamLogo">
                                                <div>
                                                    <h2>{{playoffs.koufax[2].title}}</h2>
                                                    <p>2. {{playoffs.koufax[2].udlTeam}}</p>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="item-child">
                                            <div class="block">
                                                <img :src="playoffs.koufax[3].udlTeamLogo">
                                                <div>
                                                    <h2>{{playoffs.koufax[3].title}}</h2>
                                                    <p>3. {{playoffs.koufax[3].udlTeam}}</p>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="item-child">
                    <div class="item">
                        <div class="item-parent">
                            <p>ALCS</p>
                        </div>
                        <div class="item-childrens">
                            <div class="item-child">
                                <div class="item">
                                    <div class="item-parent">
                                        <p>ALDS</p>
                                    </div>
                                    <div class="item-childrens">
                                        <div class="item-child">
                                            <div class="block">
                                                <img :src="playoffs.aaron[1].udlTeamLogo">
                                                <div>
                                                    <h2>{{playoffs.aaron[1].title}}</h2>
                                                    <p>1. {{playoffs.aaron[1].udlTeam}}</p>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="item-child">
                                            <div class="block">
                                                <img :src="playoffs.aaron[4].udlTeamLogo">
                                                <div>
                                                    <h2>{{playoffs.aaron[4].title}}</h2>
                                                    <p>4. {{playoffs.aaron[4].udlTeam}}</p>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                            <div class="item-child">
                                <div class="item">
                                    <div class="item-parent">
                                        <p>ALDS</p>
                                    </div>
                                    <div class="item-childrens">
                                        <div class="item-child">
                                            <div class="block">
                                                <img :src="playoffs.aaron[2].udlTeamLogo">
                                                <div>
                                                    <h2>{{playoffs.aaron[2].title}}</h2>
                                                    <p>2. {{playoffs.aaron[2].udlTeam}}</p>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="item-child">
                                            <div class="block">
                                                <img :src="playoffs.aaron[3].udlTeamLogo">
                                                <div>
                                                    <h2>{{playoffs.aaron[3].title}}</h2>
                                                    <p>3. {{playoffs.aaron[3].udlTeam}}</p>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: ["playoffs"],
    data() {
        return {
            
        };
    }
};
</script>

<style>
    .wrapper {
        background-color: DarkSalmon;
        display: flex;
        height: 1000px;
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