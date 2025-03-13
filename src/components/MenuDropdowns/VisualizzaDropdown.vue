<template>
  <div id="dropdownVisualizza" class="dropdownVisualizza" :style="style">
    <a><div><img src="../../assets/Impress/icons/icons_dropdown/visualizza/visualizza-normale.png">Normale</div></a>
    <a><div><img src="../../assets/Impress/icons/icons_dropdown/visualizza/visualizza-struttura.png">Struttura</div></a>
    <a><div><img src="../../assets/Impress/icons/icons_dropdown/visualizza/visualizza-note.png">Note</div></a>
    <a><div><img src="../../assets/Impress/icons/icons_dropdown/visualizza/visualizza-ordine.png">Ordine diapositive</div></a>
    <a><div><img src="../../assets/Impress/icons/icons_dropdown/visualizza/visualizza-diapositiva-schema.png">Diapositiva schema</div></a>
    <a><div><img src="../../assets/Impress/icons/icons_dropdown/visualizza/visualizza-note-schema.png">Note dello schema</div></a>
    <a><div><img src="../../assets/Impress/icons/icons_dropdown/visualizza/visualizza-stampato.png">Stampato dello schema</div></a>
    <hr />
    <a><div><img src="../../assets/Impress/icons/icons_dropdown/vuoto-16x16.png">Interfaccia Utente</div></a>
    <a style="display: flex; justify-content: space-between;"><div><img src="../../assets/Impress/icons/icons_dropdown/vuoto-16x16.png">Barre degli strumenti</div><g>&#x1F782;</g></a>
    <hr />
    <a><div><img src="../../assets/Impress/icons/icons_dropdown/vuoto-16x16.png">Barra di stato</div></a>
    <a><div><img src="../../assets/Impress/icons/icons_dropdown/vuoto-16x16.png">Pannello diapositive</div></a>
    <a><div><img src="../../assets/Impress/icons/icons_dropdown/vuoto-16x16.png">Barra a schede delle viste</div></a>
    <hr />
    <a><div><img src="../../assets/Impress/icons/icons_dropdown/visualizza/visualizza-righelli.png">Righelli</div></a>
    <a style="display: flex; justify-content: space-between;"><div><img src="../../assets/Impress/icons/icons_dropdown/visualizza/visualizza-griglia.png">Griglia e linee guida</div><g>&#x1F782;</g></a>
    <a style="display: flex; justify-content: space-between;"><div><img src="../../assets/Impress/icons/icons_dropdown/vuoto-16x16.png">Linee guida</div><g>&#x1F782;</g></a>
    <hr />
    <a><div><img src="../../assets/Impress/icons/icons_dropdown/visualizza/visualizza-commenti.png">Commenti</div></a>
    <a style="display: flex; justify-content: space-between;"><div><img src="../../assets/Impress/icons/icons_dropdown/vuoto-16x16.png">Colore/Toni di grigio</div><g>&#x1F782;</g></a>
    <hr />
    <a><div><img src="../../assets/Impress/icons/icons_dropdown/visualizza/visualizza-barra.png">Barra laterale</div></a>
    <a><div><img src="../../assets/Impress/icons/icons_dropdown/visualizza/visualizza-layout.png">Layout diapositiva</div></a>
    <a><div><img src="../../assets/Impress/icons/icons_dropdown/visualizza/visualizza-cambio.png">Cambio diapositiva</div></a>
    <a><div><img src="../../assets/Impress/icons/icons_dropdown/visualizza/visualizza-animazione.png">Animazione</div></a>
    <a><div><img src="../../assets/Impress/icons/icons_dropdown/visualizza/visualizza-stili.png">Stili</div></a>
    <a><div><img src="../../assets/Impress/icons/icons_dropdown/visualizza/visualizza-galleria.png">Galleria</div></a>
    <a><div><img src="../../assets/Impress/icons/icons_dropdown/visualizza/visualizza-navigatore.png">Navigatore</div></a>
    <a><div><img src="../../assets/Impress/icons/icons_dropdown/vuoto-16x16.png">Barra dei colori</div></a>
    <hr />
    <a><div><img src="../../assets/Impress/icons/icons_dropdown/visualizza/visualizza-sposta.png">Sposta</div></a>
    <a style="display: flex; justify-content: space-between;"><div><img src="../../assets/Impress/icons/icons_dropdown/vuoto-16x16.png">Zoom</div><g>&#x1F782;</g></a>
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
.dropdownVisualizza {
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

.dropdownVisualizza a {
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

.dropdownVisualizza a div {
  display: flex;
  align-items: center;
  padding: auto;
}

.dropdownVisualizza a div img {
  margin-right: 14px;
  max-width: 16px;
  max-height: 16px;
}

.dropdownVisualizza a:hover:not(.disabled) {
  background-color: #95cdfb;
}

hr {
  margin: 0;
  color: #d7d7d7;
}

.dropdownVisualizza a:hover.disabled {
  background-color: #ececec;
}

a.disabled {
  color: #808080;
}
</style>