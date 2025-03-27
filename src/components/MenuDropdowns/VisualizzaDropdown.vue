<template>
  <div id="dropdownVisualizza" class="dropdownVisualizza" :style="style">
    <a><div><img src="../../assets/Writer/icons/icons_dropdown/visualizza/visualizza-normale.png">Normale</div></a>
    <a><div><img src="../../assets/Writer/icons/icons_dropdown/visualizza/visualizza-web.png">Web</div></a>
    <hr />
    <a><div><img src="../../assets/Writer/icons/icons_dropdown/vuoto-16x16.png">Interfaccia Utente</div></a>
    <a style="display: flex; justify-content: space-between;"><div><img src="../../assets/Writer/icons/icons_dropdown/vuoto-16x16.png">Barre degli strumenti</div><g>&#x1F782;</g></a>
    <a style="display: flex; justify-content: space-between;"><div><g class="selected check-mark">&#x2713;</g>Barra di stato</div></a>
    <hr />
    <a style="display: flex; justify-content: space-between;"><div><img src="../../assets/Writer/icons/icons_dropdown/visualizza/visualizza-righelli.png">Righelli</div><g>&#x1F782;</g></a>
    <a style="display: flex; justify-content: space-between;"><div><img src="../../assets/Writer/icons/icons_dropdown/visualizza/visualizza-barre-scorrimento.png">Barre di scorrimento</div><g>&#x1F782;</g></a>
    <a style="display: flex; justify-content: space-between;"><div><img src="../../assets/Writer/icons/icons_dropdown/visualizza/visualizza-griglia.png">Griglie e linee guida</div><g>&#x1F782;</g></a>
    <hr />
    <a style="display: flex; justify-content: space-between;"><div><img src="../../assets/Writer/icons/icons_dropdown/visualizza/visualizza-formattazione.png">Segni di formattazione</div></a>
    <a style="display: flex; justify-content: space-between;"><div><g class="selected check-mark">&#x2713;</g>Margini del testo</div></a>
    <a style="display: flex; justify-content: space-between;"><div><g class="selected check-mark">&#x2713;</g>Contorni tabella</div></a>
    <a style="display: flex; justify-content: space-between;"><div><g class="selected check-mark">&#x2713;</g>Margini sezione</div></a>
    <a style="display: flex; justify-content: space-between;"><div><g class="selected check-mark">&#x2713;</g>Immagini e grafici</div></a>
    <a style="display: flex; justify-content: space-between;"><div><img src="../../assets/Writer/icons/icons_dropdown/visualizza/visualizza-spazio-vuoto.png">Spazio vuoto</div></a>
    <hr />
    <a style="display: flex; justify-content: space-between;"><div><g class="selected check-mark">&#x2713;</g>Mostra le revisioni</div></a>
    <a class="disabled"><div><img src="../../assets/Writer/icons/icons_dropdown/vuoto-16x16.png">Commenti</div></a>
    <a class="disabled"><div><img src="../../assets/Writer/icons/icons_dropdown/vuoto-16x16.png">Commenti risolti</div></a>
    <hr />
    <a style="display: flex; justify-content: space-between;"><div><g class="selected check-mark">&#x2713;</g>Sfondo dei campi</div></a>
    <a><div><img src="../../assets/Writer/icons/icons_dropdown/vuoto-16x16.png">Nomi di campo</div></a>
    <a><div><img src="../../assets/Writer/icons/icons_dropdown/vuoto-16x16.png">Campo paragrafi nascosti</div></a>
    <hr />
    <a><div><img src="../../assets/Writer/icons/icons_dropdown/visualizza/visualizza-barra.png">Barra laterale</div></a>
    <a><div><img src="../../assets/Writer/icons/icons_dropdown/visualizza/visualizza-stili.png">Stili</div></a>
    <a><div><img src="../../assets/Writer/icons/icons_dropdown/visualizza/visualizza-galleria.png">Galleria</div></a>
    <a><div><img src="../../assets/Writer/icons/icons_dropdown/visualizza/visualizza-navigatore.png">Navigatore</div></a>
    <a><div><img src="../../assets/Writer/icons/icons_dropdown/visualizza/visualizza-sorgente-dati.png">Sorgenti dati</div></a>
    <hr />
    <a><div><img src="../../assets/Writer/icons/icons_dropdown/visualizza/visualizza-schermo-intero.png">Schermo intero</div></a>
    <a style="display: flex; justify-content: space-between;"><div><img src="../../assets/Writer/icons/icons_dropdown/vuoto-16x16.png">Zoom</div><g>&#x1F782;</g></a>
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

.dropdownVisualizza a div .check-mark {
  margin-right: 14px;
  width: 16px;
  height: 16px;
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