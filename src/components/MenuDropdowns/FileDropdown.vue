<template>
    <div id="dropdownFile" class="dropdownFile" :style="style">
        <a style="display: flex; justify-content: space-between;"><div><img src="../../assets/Writer/icons/icons_dropdown/file/file-nuovo.png">Nuovo</div><g>&#x1F782;</g></a>
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/file/file-apri.png">Apri...</div></a>
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/vuoto-16x16.png">Apri in remoto...</div></a>
        <a @click="subDropdownToggle($event, 'DocumentiRecenti')" style="display: flex; justify-content: space-between;"><div><img src="../../assets/Writer/icons/icons_dropdown/file/file-documenti-recenti.png">Documenti recenti</div><g>&#x1F782;</g></a>
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/file/file-chiudi.png">Chiudi</div></a>
        <hr />
        <a style="display: flex; justify-content: space-between;"><div><img src="../../assets/Writer/icons/icons_dropdown/vuoto-16x16.png">Procedure guidate</div><g>&#x1F782;</g></a>
        <a style="display: flex; justify-content: space-between;"><div><img src="../../assets/Writer/icons/icons_dropdown/file/file-modelli.png">Modelli</div><g>&#x1F782;</g></a>
        <hr />
        <a class="disabled"><div><img src="../../assets/Writer/icons/icons_dropdown/vuoto-16x16.png">Ricarica</div></a>
        <a class="disabled"><div><img src="../../assets/Writer/icons/icons_dropdown/vuoto-16x16.png">Versioni</div></a>
        <hr />
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/file/file-salva.png">Salva</div></a>
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/file/file-salva-con-nome.png">Salva con nome...</div></a>
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/vuoto-16x16.png">Salva in remoto...</div></a>
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/vuoto-16x16.png">Salva una copia...</div></a>
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/vuoto-16x16.png">Salva tutto</div></a>
        <hr />
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/file/file-esporta.png">Esporta</div></a>
        <a style="display: flex; justify-content: space-between;"><div><img src="../../assets/Writer/icons/icons_dropdown/file/file-esporta.png">Esporta come</div><g>&#x1F782;</g></a>
        <a style="display: flex; justify-content: space-between;"><div><img src="../../assets/Writer/icons/icons_dropdown/vuoto-16x16.png">Invia</div><g>&#x1F782;</g></a>
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/vuoto-16x16.png">Anteprima nel browser web</div></a>
        <hr />
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/file/file-stampa.png">Stampa</div></a>
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/vuoto-16x16.png">Impostazioni stampante...</div></a>
        <hr />
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/file/file-proprietà.png">Proprietà</div></a>
        <a style="display: flex; justify-content: space-between;"><div><img src="../../assets/Writer/icons/icons_dropdown/vuoto-16x16.png">Firme digitali</div><g>&#x1F782;</g></a>
        <hr />     
        <a><div><img src="../../assets/Writer/icons/icons_dropdown/file/file-esci.png">Esci da Libre Office</div></a>
    </div>
</template>

<script>
export default {
    props: {
        style: {
            type: Object,
            default: () => ({})
        }
    },
    methods: {
        subDropdownToggle(event, subDropdownType) {
            const aElement = event.target.closest('a'); // Find the closest <a> element
            const aRect = aElement.getBoundingClientRect(); // Get the bounding rectangle of the <a> element
            console.log('Emitting toggle-sub-dropdown with:', subDropdownType, aRect); // Add this line for debugging
            this.$emit('toggle-sub-dropdown', {
                type: subDropdownType,
                position: {
                    top: aRect.top,
                    left: aRect.right,
                }
            });
        }
    }
}
</script>

<style scoped>
.dropdownFile {
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

.dropdownFile a {
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

.dropdownFile a div {
    display: flex;
    align-items: center;
    padding: auto;
}

.dropdownFile a div img {
    margin-right: 14px;
    width: 16px;
    max-height: 16px;
}

.dropdownFile a:hover:not(.disabled) {
    background-color: #95cdfb;
}

hr {
    margin: 0;
    color: #d7d7d7;
}

.dropdownFile a:hover.disabled {
    background-color: #ececec;
}

a.disabled {
    color: #808080;
}
</style>