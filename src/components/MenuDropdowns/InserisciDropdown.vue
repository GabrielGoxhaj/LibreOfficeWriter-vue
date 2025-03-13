<template>
    <div id="dropdownInserisci" class="dropdownInserisci" :style="style">
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/inserisci/inserisci-immagine.png">Immagine...</div></a>
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/inserisci/inserisci-audio-video.png">Audio o video...</div></a>
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/inserisci/inserisci-grafico.png">Grafico...</div></a>
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/inserisci/inserisci-tabella.png">Tabella...</div></a>
        <a style="display: flex; justify-content: space-between;"><div><img src="../../assets/Impress/icons/icons_dropdown/inserisci/inserisci-media.png">Media</div><g>&#x1F782;</g></a>
        <a style="display: flex; justify-content: space-between;"><div><img src="../../assets/Impress/icons/icons_dropdown/vuoto-16x16.png">Oggetto OLE</div><g>&#x1F782;</g></a>
        <a style="display: flex; justify-content: space-between;"><div><img src="../../assets/Impress/icons/icons_dropdown/inserisci/inserisci-forma.png">Forma</div><g>&#x1F782;</g></a>
        <hr />
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/vuoto-16x16.png">Linea guida di cattura...</div></a>
        <hr />
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/inserisci/inserisci-casella-testo.png">Casella di testo</div></a>
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/inserisci/inserisci-commento.png">Commento</div></a>
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/inserisci/inserisci-fontwork.png">Fontwork...</div></a>
        <hr />
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/inserisci/inserisci-collegamento.png">Collegamento...</div></a>
        <a class="disabled"><div><img src="../../assets/Impress/icons/icons_dropdown/inserisci/inserisci-carattere-speciale.png">Carattere speciale...</div></a>
        <a class="disabled" style="display: flex; justify-content: space-between;"><div><img src="../../assets/Impress/icons/icons_dropdown/vuoto-16x16.png">Segno di formattazione</div><g>&#x1F782;</g></a>
        <hr />
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/inserisci/inserisci-numero.png">Numero diapositiva</div></a>
        <a style="display: flex; justify-content: space-between;"><div><img src="../../assets/Impress/icons/icons_dropdown/inserisci/inserisci-comando.png">Comando di campo</div><g>&#x1F782;</g></a>
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/vuoto-16x16.png">Intestazione e piè di pagina...</div></a>
        <hr />
        <a style="display: flex; justify-content: space-between;"><div><img src="../../assets/Impress/icons/icons_dropdown/inserisci/inserisci-controlli.png">Controlli per formulario</div><g>&#x1F782;</g></a>
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
.dropdownInserisci {
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

.dropdownInserisci a {
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

.dropdownInserisci a div {
    display: flex;
    align-items: center;
    padding: auto;
}

.dropdownInserisci a div img {
    margin-right: 14px;
    max-width: 16px;
    max-height: 16px;
}

.dropdownInserisci a:hover:not(.disabled) {
    background-color: #95cdfb;
}

hr {
    margin: 0;
    color: #d7d7d7;
}

.dropdownInserisci a:hover.disabled {
    background-color: #ececec;
}

a.disabled {
    color: #808080;
}
</style>