<template>
    <div class="titleBar">
        <div class="title">
            <img src="../assets/Impress/icons/icon-libreofficeimpress.png" />
            <span> {{ title_pptx }} — LibreOffice Impress</span>
        </div>
        <div class="buttons">
            <div class="minimize" id="impressMinimize"><img src="../assets/Impress/icons/icon-minimize.svg" /></div>
            <div class="restore" id="impressRestore"><img src="../assets/Impress/icons/icon-restore.svg" /></div>
            <div class="close" id="impressClose">&times;</div>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        title_pptx: {
            type: String,
            required: true
        }
    }
}
</script>

<style scoped>
.title {
    margin-left: 5px;
    display: flex;
    align-items: center;
    cursor: default;
}

.title>span {
    font-size: 12px;
    margin-left: 6px;
}

.titleBar {
    align-items: center;
    background-color: #fdfdfd;
}

.titleBar,
.buttons {
    display: flex;
    justify-content: space-between;
}

.restore:hover, .minimize:hover {
    background: #e5e5e5;
}

.close:hover {
    background: red;
    color: white;
}

.restore {
    display: inline;
    float: right;
    width: 60px;
    height: 26px;
    font-size: 20px;
    font-family: 'Times New Roman', Times, serif;
    margin: auto auto;
    text-align: center;
    transition: 0.2s;
}

.minimize {
    display: inline;
    float: right;
    width: 60px;
    height: 26px;
    font-family: 'Times New Roman', Times, serif;
    margin: auto auto;
    text-align: center;
    transition: 0.2s;
}

.close {
    display: inline;
    float: right;
    width: 60px;
    height: 26px;
    font-size: 25px;
    font-family: 'Times New Roman', Times, serif;
    margin: auto auto;
    text-align: center;
    transition: 0.2s;
    cursor: default;
}
</style>