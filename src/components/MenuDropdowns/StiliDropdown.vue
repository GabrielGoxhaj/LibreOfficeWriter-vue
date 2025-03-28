<template>
    <div id="dropdownStili" class="dropdownStili" :style="style">
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/stili/stile-corpo.png">Corpo del testo</div></a>
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/stili/stile-titolo.png">Titolo</div></a>
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/stili/stile-sottotitolo.png">Sottotitolo</div></a>
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/stili/stile-h1.png">Titolo 1</div></a>
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/stili/stile-h2.png">Titolo 2</div></a>
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/stili/stile-h3.png">Titolo 3</div></a>
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/stili/stile-citazione-blocco.png">Citazione blocco</div></a>
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/stili/stile-preformattato.png">Testo preformattato</div></a>
        <hr />
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/stili/stile-senza.png">Senza stile di carattere</div></a>
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/stili/stile-enfasi.png">Enfasi</div></a>
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/stili/stile-enfasi-forte.png">Enfasi forte</div></a>
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/stili/stile-cit.png">Citazione</div></a>
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/stili/stile-sorgente.png">Testo sorgente</div></a>
        <hr />
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/stili/stile-nessun-elenco.png">Nessun elenco</div></a>
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/stili/stile-puntato.png">Stile elenco puntato •</div></a>
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/stili/stile-123.png">Stile elenco 123</div></a>
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/stili/stile-ABC-maiusc.png">Stile elenco ABC</div></a>
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/stili/stile-abc.png">Stile elenco abc</div></a>
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/stili/stile-IVX-maiusc.png">Stile elenco IVX</div></a>
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/stili/stile-ivx.png">Stile elenco ivx</div></a>
        <hr />
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/stili/stile-modifica.png">Modifica stile</div></a>
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/stili/stile-aggiorna.png">Aggiorna lo stile selezionato</div></a>
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/stili/stile-nuovo.png">Nuovo stile dalla selezione</div></a>
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/vuoto-16x16.png">Carica stili da modello</div></a>
        <hr />
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/stili/stile-gestisci.png">Gestisci gli stili</div></a>
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
.dropdownStili {
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

.dropdownStili a {
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

.dropdownStili a div {
    display: flex;
    align-items: center;
    padding: auto;
}

.dropdownStili a div img {
    margin-right: 14px;
    max-width: 16px;
    max-height: 16px;
}

.dropdownStili a:hover:not(.disabled) {
    background-color: #95cdfb;
}

hr {
    margin: 0;
    color: #d7d7d7;
}

.dropdownStili a:hover.disabled {
    background-color: #ececec;
}

a.disabled {
    color: #808080;
}
</style>