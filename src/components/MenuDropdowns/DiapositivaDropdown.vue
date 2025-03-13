<template>
    <div id="dropdownDiapositiva" class="dropdownDiapositiva" :style="style">
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/diapositiva/diapositiva-nuova-diapositiva.png">Nuova diapositiva</div></a>
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/diapositiva/diapositiva-duplica.png">Duplica diapositiva</div></a>
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/vuoto-16x16.png">Inserisci diapositiva da Diapositiva...</div></a>
        <a style="display: flex; justify-content: space-between;"><div><img src="../../assets/Impress/icons/icons_dropdown/vuoto-16x16.png">Layout</div><g>&#x1F782;</g></a>
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/diapositiva/diapositiva-elimina-diapositiva.png">Elimina diapositiva</div></a>
        <hr />
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/diapositiva/diapositiva-salva.png">Salva immagine di sfondo</div></a>
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/diapositiva/diapositiva-imposta.png">Imposta immagine di sfondo...</div></a>
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/diapositiva/diapositiva-proprietà.png">Proprietà della diapositiva...</div></a>
        <hr />
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/diapositiva/diapositiva-cambia-schema.png">Cambia schema diapositiva...</div></a>
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/diapositiva/diapositiva-nuovo-schema.png">Nuovo schema</div></a>
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/diapositiva/diapositiva-elimina-schema.png">Elimina schema</div></a>
        <hr />
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/diapositiva/diapositiva-sfondo.png">Sfondo dello schema</div></a>
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/diapositiva/diapositiva-oggetti.png">Oggetti dello schema</div></a>
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/diapositiva/diapositiva-elementi.png">Elementi dello schema...</div></a>
        <hr />
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/diapositiva/diapositiva-mostra.png">Mostra diapositiva</div></a>
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/diapositiva/diapositiva-nascondi.png">Nascondi diapositiva</div></a>
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/diapositiva/diapositiva-rinomina.png">Rinomina la diapositiva...</div></a>
        <hr />
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/vuoto-16x16.png">Vai all'ultima diapositiva modificata</div></a>
        <a style="display: flex; justify-content: space-between;"><div><img src="../../assets/Impress/icons/icons_dropdown/vuoto-16x16.png">Sposta</div><g>&#x1F782;</g></a>
        <a style="display: flex; justify-content: space-between;"><div><img src="../../assets/Impress/icons/icons_dropdown/vuoto-16x16.png">Naviga</div><g>&#x1F782;</g></a>
        <hr />
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/vuoto-16x16.png">Diapositiva sommario</div></a>
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/vuoto-16x16.png">Pagina da struttura</div></a>
        <a><div><img src="../../assets/Impress/icons/icons_dropdown/diapositiva/diapositiva-cambio-diapositiva.png">Cambio diapositiva</div></a>
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
.dropdownDiapositiva {
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

.dropdownDiapositiva a {
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

.dropdownDiapositiva a div {
    display: flex;
    align-items: center;
    padding: auto;
}

.dropdownDiapositiva a div img {
    margin-right: 14px;
    max-width: 16px;
    max-height: 16px;
}

.dropdownDiapositiva a:hover:not(.disabled) {
    background-color: #95cdfb;
}

hr {
    margin: 0;
    color: #d7d7d7;
}

.dropdownDiapositiva a:hover.disabled {
    background-color: #ececec;
}

a.disabled {
    color: #808080;
}
</style>