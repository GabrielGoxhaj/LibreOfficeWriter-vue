<template>
    <div id="dropdownFormato" class="dropdownFormato" :style="style">
        <a style="display: flex; justify-content: space-between;"><div><img src="../../assets/Writer/icons/icons_dropdown/formato/formato-testo.png">Testo</div><g>&#x1F782;</g></a>
        <a style="display: flex; justify-content: space-between;"><div><img src="../../assets/Writer/icons/icons_dropdown/formato/formato-spaziatura.png">Spaziatura</div><g>&#x1F782;</g></a>
        <a style="display: flex; justify-content: space-between;"><div><img src="../../assets/Writer/icons/icons_dropdown/formato/formato-allinea.png">Allinea testo</div><g>&#x1F782;</g></a>
        <hr />
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/formato/formato-clona.png">Clona formattazione</div></a>
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/formato/formato-cancella.png">Cancella formattazione diretta</div></a>
        <a style="display: flex; justify-content: space-between;"><div><img src="../../assets/Writer/icons/icons_dropdown/vuoto-16x16.png">Evidenzia stili</div><g>&#x1F782;</g></a>
        <hr />
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/formato/formato-carattere.png">Carattere...</div></a>
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/formato/formato-paragrafo.png">Paragrafo...</div></a>
        <a style="display: flex; justify-content: space-between;"><div><img src="../../assets/Writer/icons/icons_dropdown/formato/formato-elenchi.png">Elenchi</div><g>&#x1F782;</g></a>
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/formato/formato-elenchi-puntati.png">Elenchi puntati e numerati...</div></a>
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/vuoto-16x16.png">Tema...</div></a>
        <hr />
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/formato/formato-stile.png">Stile di pagina...</div></a>
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/formato/formato-sommario.png">Pagina sommario...</div></a>
        <a class="disabled"><div><img src="../../assets/Writer/icons/icons_dropdown/vuoto-16x16.png">Commenti...</div></a>
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/formato/formato-colonne.png">Colonne...</div></a>
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/vuoto-16x16.png">Filigrana...</div></a>
        <a class="disabled"><div><img src="../../assets/Writer/icons/icons_dropdown/vuoto-16x16.png">Sezioni...</div></a>
        <hr />
        <a class="disabled" style="display: flex; justify-content: space-between;"><div><img src="../../assets/Writer/icons/icons_dropdown/formato/formato-immagine.png">Immagine</div><g>&#x1F782;</g></a>
        <a class="disabled" style="display: flex; justify-content: space-between;"><div><img src="../../assets/Writer/icons/icons_dropdown/formato/formato-casella-testo.png">Casella di testo e forma</div><g>&#x1F782;</g></a>
        <a class="disabled" style="display: flex; justify-content: space-between;"><div><img src="../../assets/Writer/icons/icons_dropdown/formato/formato-cornice.png">Cornice e oggetto</div><g>&#x1F782;</g></a>
        <a class="disabled"><div><img src="../../assets/Writer/icons/icons_dropdown/vuoto-16x16.png">Nome...</div></a>
        <a class="disabled"><div><img src="../../assets/Writer/icons/icons_dropdown/vuoto-16x16.png">Alt Text...</div></a>
        <hr />
        <a class="disabled" style="display: flex; justify-content: space-between;"><div><img src="../../assets/Writer/icons/icons_dropdown/formato/formato-ancoraggio.png">Ancoraggio</div><g>&#x1F782;</g></a>
        <a class="disabled" style="display: flex; justify-content: space-between;"><div><img src="../../assets/Writer/icons/icons_dropdown/formato/formato-scorrimento.png">Scorrimento</div><g>&#x1F782;</g></a>
        <a class="disabled" style="display: flex; justify-content: space-between;"><div><img src="../../assets/Writer/icons/icons_dropdown/formato/formato-disponi.png">Disponi</div><g>&#x1F782;</g></a>
        <a class="disabled" style="display: flex; justify-content: space-between;"><div><img src="../../assets/Writer/icons/icons_dropdown/formato/formato-ruota-ribalta.png">Ruota o ribalta</div><g>&#x1F782;</g></a>
        <a class="disabled" style="display: flex; justify-content: space-between;"><div><img src="../../assets/Writer/icons/icons_dropdown/formato/formato-gruppo.png">Gruppo</div><g>&#x1F782;</g></a>
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
.dropdownFormato {
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

.dropdownFormato a {
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

.dropdownFormato a div {
    display: flex;
    align-items: center;
    padding: auto;
}

.dropdownFormato a div img {
    margin-right: 14px;
    max-width: 16px;
    max-height: 16px;
}

.dropdownFormato a:hover:not(.disabled) {
    background-color: #95cdfb;
}

hr {
    margin: 0;
    color: #d7d7d7;
}

.dropdownFormato a:hover.disabled {
    background-color: #ececec;
}

a.disabled {
    color: #808080;
}
</style>