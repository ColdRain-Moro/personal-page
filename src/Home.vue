<script setup lang="ts">
import Avatar from "./components/Avatar.vue";
import Button from "./components/Button.vue";

const getAssetsFile = () => {
    return new URL(`./assets/chino.jpg`, import.meta.url).href
}

function openBlog() {
    window.open("https://blog.coldrain.ink/", "_blank");
}

function openGitHub() {
    window.open("https://github.com/ColdRain-Moro", "_blank");
}

function openQQ() {
    window.open("tencent://message/?uin=1335014319&Site=&Menu=yes", "_blank");
}

function openBiliBili() {
    window.open("https://space.bilibili.com/29402561", "_blank");
}

</script>

<template>
    <div id="background">
        <div id="background-color">
            <div id="content-box">
                <div id="top-content">
                    <Avatar :src="getAssetsFile()" center />
                    <h1>Rain</h1>
                    <h2>Everything that kills me makes me feel alive.</h2>
                    <hr>
                    <p>
                        为有牺牲多壮志，敢教日月换新天。
                        <br>
                        -「<strong>七律·到韶山</strong>」
                    </p>
                </div>
                <Button name="Blog" @click="openBlog"></Button>
                <Button name="GitHub" @click="openGitHub"></Button>
                <Button name="QQ" @click="openQQ"></Button>
                <Button name="BiliBili" @click="openBiliBili"></Button>
            </div>
            <div id="bottom">
                <div>Copyright © by <a href="https://github.com/ColdRain-Moro" target="_blank">Rain</a> All Rights
                    Reserved.</div>
                <div>Powered by <a href="https://v3.vuejs.org/" target="_blank">Vue.js</a> framework.</div>
            </div>
        </div>
    </div>
</template>

<style scoped>
hr {
    margin: 15px 25%;
}

p {
    font-family: "ff-tisa-web-pro-1", "ff-tisa-web-pro-2", "Lucida Grande", "Hiragino Sans GB", "Hiragino Sans GB W3", "Microsoft YaHei", "WenQuanYi Micro Hei", sans-serif;
    color: white;
    line-height: 1.7em;
}

h1 {
    font-family: 'Old English Text MT', 'EngraversOldEnglishBT-Bold', 'Lato', "PingFang SC", "Microsoft YaHei", sans-serif;
    margin: 10px 0 5px 0;
    color: #fff;
    line-height: 1.2em;
    letter-spacing: 0.05em;
    font-size: 2.5em;
    font-weight: lighter;
    -webkit-font-smoothing: antialiased;
}

h2 {
    margin: 0 0 5px 0;
    font-weight: lighter;
    font-size: 1.2em;
    color: rgb(210, 210, 210);
    -webkit-font-smoothing: antialiased;
    font-family: "ff-tisa-web-pro-1", "ff-tisa-web-pro-2", "Lucida Grande", "Hiragino Sans GB", "Hiragino Sans GB W3", "Microsoft YaHei", "WenQuanYi Micro Hei", sans-serif;
}

#top-content {
    margin-bottom: 5%;
}

#bottom {
    display: flex;
    flex-direction: column;
    justify-content: center;
    height: 8%;
    box-sizing: border-box;
    text-align: center;
    background-color: #dddddd92;
}

#content-box {
    width: 100%;
    height: 92%;
    padding: 8% 20%;
    box-sizing: border-box;
}

#background-color {
    background-color: #68686892;
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
}

#background {
    user-select: none;
    width: 100%;
    height: 100%;
    background-image: url(https://api.fantasyzone.cc/tu);
    background-size: cover;
}
</style>