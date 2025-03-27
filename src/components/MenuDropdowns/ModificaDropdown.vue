<template>
    <div id="dropdownModifica" class="dropdownModifica" :style="style">
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/modifica/modifica-annulla.png">Annulla</div></a>
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/modifica/modifica-ripristina.png">Ripristina</div></a>
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/modifica/modifica-ripeti.png">Ripeti</div></a>
        <hr />
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/modifica/modifica-taglia.png">Taglia</div></a>
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/modifica/modifica-copia.png">Copia</div></a>
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/modifica/modifica-incolla.png">Incolla</div></a>
        <a style="display: flex; justify-content: space-between;"><div><img src="../../assets/Writer/icons/icons_dropdown/modifica/modifica-incolla-speciale.png">Incolla speciale</div><g>&#x1F782;</g></a>
        <hr />
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/modifica/modifica-seleziona.png">Seleziona tutto</div></a>
        <a style="display: flex; justify-content: space-between;"><div><img src="../../assets/Writer/icons/icons_dropdown/vuoto-16x16.png">Modo selezione</div><g>&#x1F782;</g></a>
        <a class="disabled" style="display: flex; justify-content: space-between;"><div><img src="../../assets/Writer/icons/icons_dropdown/vuoto-16x16.png">Seleziona testo</div></a>
        <hr />
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/modifica/modifica-trova.png">Trova...</div></a>
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/modifica/modifica-trova-sostituisci.png">Trova e sostituisci...</div></a>
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/vuoto-16x16.png">Vai alla pagina</div></a>
        <hr />
        <a style="display: flex; justify-content: space-between;"><div><img src="../../assets/Writer/icons/icons_dropdown/vuoto-16x16.png">Revisioni</div><g>&#x1F782;</g></a>
        <a style="display: flex; justify-content: space-between;"><div><img src="../../assets/Writer/icons/icons_dropdown/vuoto-16x16.png">Commento</div><g>&#x1F782;</g></a>
        <hr />
        <a class="disabled"><div><img src="../../assets/Writer/icons/icons_dropdown/vuoto-16x16.png">Collegamento ipertestuale</div></a>
        <a class="disabled" style="display: flex; justify-content: space-between;"><div><img src="../../assets/Writer/icons/icons_dropdown/modifica/modifica-riferimento.png">Riferimento</div><g>&#x1F782;</g></a>
        <a class="disabled"><div><img src="../../assets/Writer/icons/icons_dropdown/vuoto-16x16.png">Campi...</div></a>
        <a class="disabled"><div><img src="../../assets/Writer/icons/icons_dropdown/vuoto-16x16.png">Collegamenti esterni...</div></a>
        <a class="disabled" style="display: flex; justify-content: space-between;"><div><img src="../../assets/Writer/icons/icons_dropdown/vuoto-16x16.png">Oggetto OLE</div><g>&#x1F782;</g></a>
        <a style="display: flex; justify-content: space-between;"><div><img src="../../assets/Writer/icons/icons_dropdown/modifica/modifica-database.png">Scambia database</div></a>
        <hr />
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/modifica/modifica-modo-cursore.png">Modo cursore diretto</div></a>
        <a class="disabled"><div><img src="../../assets/Writer/icons/icons_dropdown/vuoto-16x16.png">Modo Modifica</div></a>
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
.dropdownModifica {
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

.dropdownModifica a {
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

.dropdownModifica a div {
    display: flex;
    align-items: center;
    padding: auto;
}

.dropdownModifica a div img {
    margin-right: 14px;
    max-width: 16px;
    max-height: 16px;
}

.dropdownModifica a:hover:not(.disabled) {
    background-color: #95cdfb;
}

hr {
    margin: 0;
    color: #d7d7d7;
}

.dropdownModifica a:hover.disabled {
    background-color: #ececec;
}

a.disabled {
    color: #808080;
}
</style>