<template>
    <section class="container">
        <my-header></my-header>
        <main>
            <div class="burst_info">
                <h1>Levels To It</h1>
                <table>
                    <tbody>
                        <tr>
                            <td>Location</td>
                            <td>Everyday life</td>
                        </tr>
                        <tr>
                            <td>Date</td>
                            <td>April 27, 2019</td>
                        </tr>
                    </tbody>
                </table>
            </div>
            <div class="burst_container">
                <div class="layer bottom">
                    <div class="layer middle">
                        <div class="layer top" />
                    </div>
                </div>
            </div>
        </main>
    </section>
</template>

<script>
import MyHeader from '~/components/MyHeader.vue'

export default {
    components: {
        MyHeader
    },
    data: function () {
        return {
        };
    },
    methods: {}
}
</script>

<style lang="scss" scoped>
.container {
    background: url('~/assets/img/levels.png') no-repeat center center;
    background-size: cover;
    min-height: 100vh;
    padding: 0 100px;
    header {
        display: flex;
        height: 70px;
        align-items: center;
        nav {
            margin-left: auto;
            ul {
                list-style: none;
                li {
                    display: inline;
                    a {
                        padding: 10px 20px;
                        font-family: 'Oswald', sans-serif;
                        color: #ffffff;
                        text-transform: uppercase;
                        text-decoration: none;
                    }
                }
            }
        }
    }
    main {
        min-height: calc(100vh - 90px);
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        .burst_info {
            flex: 1;
            h1 {
                font-size: 40px;
                font-family: 'Oswald', sans-serif;
                color: #ffffff;
                text-transform: uppercase;
                margin-bottom: 10px;
            }
            table {
                color: #dddddd;
                font-size: 15px;
                font-family: 'Oswald', sans-serif;
                tbody {
                    tr {
                        td {
                            &:first-of-type {
                                color: #aaaaaa;
                                padding-right: 10px;
                            }
                        }
                    }
                }
            }
        }
        .burst_container {
            flex: 2;
            display: flex;
            align-items: center;
            justify-content: center;
            min-height: 400px;
            // background-color: #FFFFFF;
            position: relative;
        }
    }
}

// $circleHeight: 80px;
// $circleWidth: 80px;

.layer {
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 50%;
    box-shadow: 3px 5px 12px 0 rgba(0, 0, 0, 0.3);

    &.bottom {
        height: 80px;
        width: 80px;
        background-color: rgb(194, 194, 194);
        transform: scale(0);
        animation: 6.0s scaleUpDown_bottom ease-in-out infinite;
    }
    &.middle {
        height: 60px;
        width: 60px;
        background-color: rgb(211, 211, 211);
        transform: scale(0);
        animation: 6.0s scaleUpDown_middle 0.5s ease-in-out infinite;
    }
    &.top {
        height: 40px;
        width: 40px;
        background-color: rgb(224, 224, 224);
        transform: scale(0);
        animation: 6.0s scaleUpDown_top 1.0s ease-in-out infinite;
    }
}

@keyframes scaleUpDown_bottom {
    0% { transform: scale(0); }
    20% { transform: scale(1); }
    65% { transform: scale(1); }
    100% { transform: scale(0); }
}

@keyframes scaleUpDown_middle {
    0% { transform: scale(0); }
    25% { transform: scale(1); }
    45% { transform: scale(1); }
    80% { transform: scale(0); }
    100% { transform: scale(0); }
}

@keyframes scaleUpDown_top {
    0% { transform: scale(0); }
    30% { transform: scale(1); }
    35% { transform: scale(1); }
    50% { transform: scale(0); }
    100% { transform: scale(0); }
}

</style>

