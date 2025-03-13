<template>
    <div id="dropdownStrumenti" class="dropdownStrumenti" :style="style">
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/strumenti/strumenti-controllo.png">Controllo ortografico...</div></a>
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/strumenti/strumenti-controllo-auto.png">Controllo ortografico automatico</div></a>
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/vuoto-16x16.png">Sinonimi...</div></a>
        <a style="display: flex; justify-content: space-between;"><div><img src="../../assets/Impress/icons/icons_dropdown/strumenti/strumenti-lingua.png">Lingua</div><g>&#x1F782;</g></a>
        <hr />
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/strumenti/strumenti-opzioni-correzione.png">Opzioni di correzione automatica...</div></a>
        <hr />
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/vuoto-16x16.png">Oscura</div></a>
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/vuoto-16x16.png">Oscura in automatico</div></a>
        <hr />
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/strumenti/strumenti-minimizza.png">Minimizza presentazione...</div></a>
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/strumenti/strumenti-mappa.png">Mappa immagine</div></a>
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/strumenti/strumenti-sostituzione.png">Sostituzione colore</div></a>
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/strumenti/strumenti-lettore.png">Lettore multimediale</div></a>
        <hr />
        <a style="display: flex; justify-content: space-between;"><div><img src="../../assets/Impress/icons/icons_dropdown/vuoto-16x16.png">Formulari</div><g>&#x1F782;</g></a>
        <a style="display: flex; justify-content: space-between;"><div><img src="../../assets/Impress/icons/icons_dropdown/strumenti/strumenti-macro.png">Macro</div><g>&#x1F782;</g></a>
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/strumenti/strumenti-strumenti.png">Strumenti per lo sviluppo</div></a>
        <hr />
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/strumenti/strumenti-xml.png">Impostazioni filtro XML...</div></a>
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/vuoto-16x16.png">Estensioni...</div></a>
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/vuoto-16x16.png">Personalizza...</div></a>
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/strumenti/strumenti-opzioni.png">Opzioni...</div></a>
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
.dropdownStrumenti {
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

.dropdownStrumenti a {
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

.dropdownStrumenti a div {
    display: flex;
    align-items: center;
    padding: auto;
}

.dropdownStrumenti a div img {
    margin-right: 14px;
    max-width: 16px;
    max-height: 16px;
}

.dropdownStrumenti a:hover:not(.disabled) {
    background-color: #95cdfb;
}

hr {
    margin: 0;
    color: #d7d7d7;
}

.dropdownStrumenti a:hover.disabled {
    background-color: #ececec;
}

a.disabled {
    color: #808080;
}
</style>