<template>
    <div id="dropdownPresentazione" class="dropdownPresentazione" :style="style">
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/presentazione/presentazione-prima.png">Inizia dalla prima diapositiva</div></a>
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/presentazione/presentazione-corrente.png">Inizia dalla diapositiva corrente</div></a>
        <hr />
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/presentazione/presentazione-cronometrata.png">Presentazione cronometrata</div></a>
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/presentazione/presentazione-personalizzata.png">Presentazione personalizzata...</div></a>
        <hr />
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/presentazione/presentazione-impostazioni.png">Impostazioni presentazione...</div></a>
    </div>
</template>

<script>
export default {
    props: {
        style: {
            type: Object,
            default: () => ({})
        }
    }
}
</script>

<style scoped>
.dropdownPresentazione {
    position: absolute;
    background-color: #F2F2F2;
    width: 255px;
    height: auto;
    overflow: auto;
    box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.2);
    border: lightgray;
    border-width: 1px;
    border-style: solid;
    z-index: 10;
}

.dropdownPresentazione a {
    color: black;
    text-decoration: none;
    font-family: 'Segoe UI', Tahoma, sans-serif;
    font-size: 9pt;
    display: block;
    margin-top: 1px;
    margin-left: 2px;
    padding-left: 7px;
    padding-top: 3px;
    padding-bottom: 3px;
    padding-right: 10px;
    transition: 0.1s;
    cursor: default;
}

.dropdownPresentazione a div {
    display: flex;
    align-items: center;
    padding: auto;
}

.dropdownPresentazione a div img {
    margin-right: 14px;
    max-width: 16px;
    max-height: 16px;
}

.dropdownPresentazione a:hover:not(.disabled) {
    background-color: #95cdfb;
}

hr {
    margin: 0;
    color: #d7d7d7;
}

.dropdownPresentazione a:hover.disabled {
    background-color: #ececec;
}

a.disabled {
    color: #808080;
}
</style>