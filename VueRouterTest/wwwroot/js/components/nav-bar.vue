<template>
    <div>
        <nav>
            <router-link v-for="item in items" v-bind:to="{ path: `${item.path}` }">{{ item.name }}</router-link>
        </nav>
    </div>
</template>

<script>
    module.exports = {
        props: ['items']        
    };
</script>

<style>
    * {
        margin: 0;
        padding: 0;
    }

    body {
        font: 15px/1.3 'Open Sans', sans-serif;
        color: #5e5b64;
        text-align: center;
    }

    a, a:visited {
        outline: none;
        color: #389dc1;
    }

        a:hover {
            text-decoration: none;
        }

    section, footer, header, aside, nav {
        display: block;
    }

    /*-------------------------
        The menu
    --------------------------*/

    nav {
        display: inline-block;
        margin: 60px auto 45px;
        background-color: #5597b4;
        box-shadow: 0 1px 1px #ccc;
        border-radius: 2px;
    }

        nav a {
            display: inline-block;
            padding: 18px 30px;
            color: #fff !important;
            font-weight: bold;
            font-size: 16px;
            text-decoration: none !important;
            line-height: 1;
            background-color: transparent;
            -webkit-transition: background-color 0.25s;
            -moz-transition: background-color 0.25s;
            transition: background-color 0.25s;
        }

            nav a.router-link-active {
                background-color: #e35885;
            }

            nav a:first-child {
                border-radius: 2px 0 0 2px;
            }

            nav a:last-child {
                border-radius: 0 2px 2px 0;
            }
</style>