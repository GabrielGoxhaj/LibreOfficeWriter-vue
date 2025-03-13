<template>
  <div class="menuIconLibreOfficeImpress">
    <div class="riga1">
      <button @click="changePPTX('Senza Nome 1.pptx')"><img src="../assets/Impress/icons/icons_menu/nuovo.png"></button><button @click="changePPTX('Senza Nome 1.pptx', 1)" class="dropdown" @mouseover="addHoverClass" @mouseout="removeHoverClass"><img src="../assets/Impress/icons/icons_menu/dropdown-icon.png"></button>
      <button><img src="../assets/Impress/icons/icons_menu/apri.png"></button><button class="dropdown" @mouseover="addHoverClass" @mouseout="removeHoverClass"><img src="../assets/Impress/icons/icons_menu/dropdown-icon.png"></button>
      <button><img src="../assets/Impress/icons/icons_menu/salva.png"></button><button class="dropdown" @mouseover="addHoverClass" @mouseout="removeHoverClass"><img src="../assets/Impress/icons/icons_menu/dropdown-icon.png"></button>
      <div class="vl"></div>
      <button><img src="../assets/Impress/icons/icons_menu/exportPDF.png"></button>
      <button><img src="../assets/Impress/icons/icons_menu/stampa.png"></button>
      <div class="vl"></div>
      <button><img src="../assets/Impress/icons/icons_menu/taglia.png"></button>
      <button><img src="../assets/Impress/icons/icons_menu/copia.png"></button>
      <button><img src="../assets/Impress/icons/icons_menu/incolla.png"></button><button class="dropdown" @mouseover="addHoverClass" @mouseout="removeHoverClass"><img src="../assets/Impress/icons/icons_menu/dropdown-icon.png"></button>
      <div class="vl"></div>
      <button><img src="../assets/Impress/icons/icons_menu/clona-formattazione.png"></button>
      <div class="vl"></div>
      <button><img src="../assets/Impress/icons/icons_menu/annulla.png"></button><button class="dropdown" @mouseover="addHoverClass" @mouseout="removeHoverClass"><img src="../assets/Impress/icons/icons_menu/dropdown-icon.png"></button>
      <button><img src="../assets/Impress/icons/icons_menu/ripristina.png"></button><button class="dropdown" @mouseover="addHoverClass" @mouseout="removeHoverClass"><img src="../assets/Impress/icons/icons_menu/dropdown-icon.png"></button>
      <div class="vl"></div>
      <button><img src="../assets/Impress/icons/icons_menu/trova-sostituisci.png"></button>
      <button><img src="../assets/Impress/icons/icons_menu/controllo-ortografico.png"></button>
      <div class="vl"></div>
      <button><img src="../assets/Impress/icons/icons_menu/mostra-griglia.png"></button>
      <button><img src="../assets/Impress/icons/icons_menu/cattura-griglia.png"></button>
      <button><img src="../assets/Impress/icons/icons_menu/mostra-viste.png"></button><button class="dropdown" @mouseover="addHoverClass" @mouseout="removeHoverClass"><img src="../assets/Impress/icons/icons_menu/dropdown-icon.png"></button>
      <button><img src="../assets/Impress/icons/icons_menu/diapositiva-schema.png"></button>
      <button class="espandi"><img src="../assets/Impress/icons/icons_menu/espandi.png"></button>
      <button class="espandi"><img src="../assets/Impress/icons/icons_menu/espandi.png"></button>
    </div>
    <div class="riga2">
      <button><img src="../assets/Impress/icons/icons_menu/seleziona.png"></button>
      <button><img src="../assets/Impress/icons/icons_menu/zoom.png"></button>
      <div class="vl"></div>
      <button><img src="../assets/Impress/icons/icons_menu/colore-linea.png"></button><button class="dropdown" @mouseover="addHoverClass" @mouseout="removeHoverClass"><img src="../assets/Impress/icons/icons_menu/dropdown-icon.png"></button>
      <button><img src="../assets/Impress/icons/icons_menu/colore-riempimento.png"></button><button class="dropdown" @mouseover="addHoverClass" @mouseout="removeHoverClass"><img src="../assets/Impress/icons/icons_menu/dropdown-icon.png"></button>
      <div class="vl"></div>
      <button><img src="../assets/Impress/icons/icons_menu/linea.png"></button>
      <button><img src="../assets/Impress/icons/icons_menu/rettangolo.png"></button>
      <button><img src="../assets/Impress/icons/icons_menu/ellisse.png"></button>
      <div class="vl"></div>
      <button><img src="../assets/Impress/icons/icons_menu/frecce.png"></button><button class="dropdown" @mouseover="addHoverClass" @mouseout="removeHoverClass"><img src="../assets/Impress/icons/icons_menu/dropdown-icon.png"></button>
      <button><img src="../assets/Impress/icons/icons_menu/curve-poligoni.png"></button><button class="dropdown" @mouseover="addHoverClass" @mouseout="removeHoverClass"><img src="../assets/Impress/icons/icons_menu/dropdown-icon.png"></button>
      <button><img src="../assets/Impress/icons/icons_menu/connettori.png"></button><button class="dropdown" @mouseover="addHoverClass" @mouseout="removeHoverClass"><img src="../assets/Impress/icons/icons_menu/dropdown-icon.png"></button>
      <div class="vl"></div>
      <button><img src="../assets/Impress/icons/icons_menu/forme-base.png"></button><button class="dropdown" @mouseover="addHoverClass" @mouseout="removeHoverClass"><img src="../assets/Impress/icons/icons_menu/dropdown-icon.png"></button>
      <button><img src="../assets/Impress/icons/icons_menu/forme-simbolo.png"></button><button class="dropdown" @mouseover="addHoverClass" @mouseout="removeHoverClass"><img src="../assets/Impress/icons/icons_menu/dropdown-icon.png"></button>
      <button><img src="../assets/Impress/icons/icons_menu/frecce-blocco.png"></button><button class="dropdown" @mouseover="addHoverClass" @mouseout="removeHoverClass"><img src="../assets/Impress/icons/icons_menu/dropdown-icon.png"></button>
      <button><img src="../assets/Impress/icons/icons_menu/flowchart.png"></button><button class="dropdown" @mouseover="addHoverClass" @mouseout="removeHoverClass"><img src="../assets/Impress/icons/icons_menu/dropdown-icon.png"></button>
      <button><img src="../assets/Impress/icons/icons_menu/forme-callout.png"></button><button class="dropdown" @mouseover="addHoverClass" @mouseout="removeHoverClass"><img src="../assets/Impress/icons/icons_menu/dropdown-icon.png"></button>
      <button><img src="../assets/Impress/icons/icons_menu/stella-banner.png"></button><button class="dropdown" @mouseover="addHoverClass" @mouseout="removeHoverClass"><img src="../assets/Impress/icons/icons_menu/dropdown-icon.png"></button>
      <button><img src="../assets/Impress/icons/icons_menu/oggetti-3d.png"></button><button class="dropdown" @mouseover="addHoverClass" @mouseout="removeHoverClass"><img src="../assets/Impress/icons/icons_menu/dropdown-icon.png"></button>
      <div class="vl"></div>
      <button><img src="../assets/Impress/icons/icons_menu/ruota.png"></button>
      <button class="espandi"><img src="../assets/Impress/icons/icons_menu/espandi.png"></button>
    </div>
  </div>
</template>

<script scoped>
export default {
  methods: {
    changePPTX(title) {
      this.updateTitleAndClose(title);
    },
    updateTitleAndClose(title) {
      this.$emit('update-title', title);
    },
    addHoverClass(event) {
      const prevButton = event.target.closest('.dropdown').previousElementSibling;
      if (prevButton && prevButton.tagName === 'BUTTON') {
        prevButton.classList.add('button-hover');
      }
    },
    removeHoverClass(event) {
      const prevButton = event.target.closest('.dropdown').previousElementSibling;
      if (prevButton && prevButton.tagName === 'BUTTON') {
        prevButton.classList.remove('button-hover');
      }
    }
  }
}
</script>

<style scoped>
button {
  border: 1px solid #fdfdfd;
  background-color: #fdfdfd;
  padding: 4px;
  height: 33.6px;
  margin-top: 2px;
  margin-bottom: 2px;
}

button:not(.dropdown) {
  width: 33.6px;
}

button:hover:not(.espandi) {
  background-color: #e4f2fe;
  border: 1px solid #d1eafe;
}

.dropdown {
  padding-top: 8px;
  padding-bottom: 8px;
}

button:hover:not(.espandi)+.dropdown,
button:hover:not(.espandi)+.dropdown:hover,
.dropdown:hover {
  background-color: #cbe5fc;
  border: 1px solid #b4dcfc;
}

.dropdown:hover,
.dropdown:hover:has(~ button) {
  background-color: #cbe5fc;
  border: 1px solid #b4dcfc;
}

.button-hover {
  background-color: #e4f2fe;
  border: 1px solid #d1eafe;
}

.riga1,
.riga2 {
  display: flex;
  align-items: center;
  margin-left: 4px;
}

.vl {
  border-left: 0.5px solid #dfdfdf;
  height: 15px;
  margin: 1px
}
</style>
