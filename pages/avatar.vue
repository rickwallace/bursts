<template>
    <section class="container">
        <my-header></my-header>
        <main>
            <div class="burst_info">
                <h1>Avatar</h1>
                <table>
                    <tbody>
                        <tr>
                            <td>Location</td>
                            <td>Animal Kingdom, Pandora - The World of Avatar</td>
                        </tr>
                        <tr>
                            <td>Date</td>
                            <td>August 15, 2018</td>
                        </tr>
                    </tbody>
                </table>
            </div>
            <div class="burst_container">                                
                
            </div>
        </main>
    </section>
</template>

<script>
import MyHeader from '~/components/MyHeader.vue'
import {TweenMax, TimelineLite} from "gsap";

export default {
    components: {
        MyHeader
    },
    data: function () {
        return {
        };
    },
    methods: {
        beginAnimation: function() {
            var tl = new TimelineLite();
            tl.from("#lower-rays", 10, {rotation:"+=360", transformOrigin:"50% 50%", ease:Linear.easeNone,repeat:-1});
        }
    },
    beforeMount: function() {
        this.beginAnimation()
    }
}
</script>

<style lang="scss" scoped>
.container {
    // background-color: #262626;
    background: url('~/assets/img/avatar.png') no-repeat center center;
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
        }
    }
}
</style>

