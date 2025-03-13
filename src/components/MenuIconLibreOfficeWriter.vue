<template>
  <div class="menuIconLibreOfficeWriter">
    <div class="riga1">
      <button @click="changePPTX('Senza Nome 1.pptx')"><img src="../assets/Writer/icons/icons_menu/nuovo.png"></button><button @click="changePPTX('Senza Nome 1.pptx', 1)" class="dropdown" @mouseover="addHoverClass" @mouseout="removeHoverClass"><img src="../assets/Writer/icons/icons_menu/dropdown-icon.png"></button>
      <button><img src="../assets/Writer/icons/icons_menu/apri.png"></button><button class="dropdown" @mouseover="addHoverClass" @mouseout="removeHoverClass"><img src="../assets/Writer/icons/icons_menu/dropdown-icon.png"></button>
      <button><img src="../assets/Writer/icons/icons_menu/salva.png"></button><button class="dropdown" @mouseover="addHoverClass" @mouseout="removeHoverClass"><img src="../assets/Writer/icons/icons_menu/dropdown-icon.png"></button>
      <div class="vl"></div>
      <button><img src="../assets/Writer/icons/icons_menu/exportPDF.png"></button>
      <button><img src="../assets/Writer/icons/icons_menu/stampa.png"></button>
      <button><img src="../assets/Writer/icons/icons_menu/anteprima-stampa.png"></button>
      <div class="vl"></div>
      <button><img src="../assets/Writer/icons/icons_menu/taglia.png"></button>
      <button><img src="../assets/Writer/icons/icons_menu/copia.png"></button>
      <button><img src="../assets/Writer/icons/icons_menu/incolla.png"></button><button class="dropdown" @mouseover="addHoverClass" @mouseout="removeHoverClass"><img src="../assets/Writer/icons/icons_menu/dropdown-icon.png"></button>
      <div class="vl"></div>
      <button><img src="../assets/Writer/icons/icons_menu/clona-formattazione.png"></button>
      <div class="vl"></div>
      <button><img src="../assets/Writer/icons/icons_menu/annulla.png"></button><button class="dropdown" @mouseover="addHoverClass" @mouseout="removeHoverClass"><img src="../assets/Writer/icons/icons_menu/dropdown-icon.png"></button>
      <button><img src="../assets/Writer/icons/icons_menu/ripristina.png"></button><button class="dropdown" @mouseover="addHoverClass" @mouseout="removeHoverClass"><img src="../assets/Writer/icons/icons_menu/dropdown-icon.png"></button>
      <div class="vl"></div>
      <button><img src="../assets/Writer/icons/icons_menu/trova-sostituisci.png"></button>
      <button><img src="../assets/Writer/icons/icons_menu/controllo-ortografico.png"></button>
      <button><img src="../assets/Writer/icons/icons_menu/segni-formattazione.png"></button>
      <div class="vl"></div>
      <button><img src="../assets/Writer/icons/icons_menu/tabella.png"></button>
      <button><img src="../assets/Writer/icons/icons_menu/immagine.png"></button>
      <button><img src="../assets/Writer/icons/icons_menu/grafico.png"></button>
      <button><img src="../assets/Writer/icons/icons_menu/casella-testo.png"></button>
      <button class="espandi"><img src="../assets/Writer/icons/icons_menu/espandi.png"></button>
    </div>
    <div class="riga2">
      <select>
        <option value="default">Stile del paragrafo predefinito</option>
        <option value="body">Corpo del testo</option>
        <option value="h1">Titolo principale</option>
        <option value="subtitle">Sottotitolo</option>
        <option value="h2">Titolo 1</option>
        <option value="h3">Titolo 2</option>
        <option value="h4">Titolo 3</option>
        <option value="h5">Titolo 4</option>
        <option value="blockquote">Citazione in blocco</option>
        <option value="pre">Testo preformattato</option>
        <option value="more">Altri stili...</option>
      </select>
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
select > option {
  font-size: 16px;
}

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
