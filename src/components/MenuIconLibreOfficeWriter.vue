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
      <button style="width: 46.25px;"><img src="../assets/Writer/icons/icons_menu/tabella.png"></button>
      <button><img src="../assets/Writer/icons/icons_menu/immagine.png"></button>
      <button><img src="../assets/Writer/icons/icons_menu/grafico.png"></button>
      <button><img src="../assets/Writer/icons/icons_menu/casella-testo.png"></button>
      <div class="vl"></div>
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
      <button><img src="../assets/Writer/icons/icons_menu/aggiorna-stile.png"></button>
      <button><img src="../assets/Writer/icons/icons_menu/nuovo-stile.png"></button>
      <div class="vl" style="margin-left: 8px;"></div>
      <select id="font-select">
        <option style="font-family: Arial;" value="Arial">Arial</option>
        <option style="font-family: Verdana;" value="Verdana">Verdana</option>
        <option style="font-family: Tahoma;" value="Tahoma">Tahoma</option>
        <option style="font-family: Georgia;" value="Georgia">Georgia</option>
        <option style="font-family: Times;" value="Times New Roman">Times New Roman</option>
        <option style="font-family: 'Courier New';" value="Courier New">Courier New</option>
        <option style="font-family: 'Comic Sans MS';" value="Comic Sans MS">Comic Sans MS</option>
        <option style="font-family: Impact;" value="Impact">Impact</option>
        <option style="font-family: 'Trebuchet MS';" value="Trebuchet MS">Trebuchet MS</option>
        <option style="font-family: Helvetica" value="Helvetica">Helvetica</option>
      </select>
      <select id="font-size" style="margin-left">
        <option value="6">6 pt</option>
        <option value="7">7 pt</option>
        <option value="8">8 pt</option>
        <option value="9">9 pt</option>
        <option value="10">10 pt</option>
        <option value="10.5">10,5 pt</option>
        <option value="11">11 pt</option>
        <option value="12">12 pt</option>
        <option value="13">13 pt</option>
        <option value="14">14 pt</option>
        <option value="15">15 pt</option>
        <option value="16">16 pt</option>
        <option value="18">18 pt</option>
        <option value="20">20 pt</option>
        <option value="21">21 pt</option>
        <option value="22">22 pt</option>
        <option value="24">24 pt</option>
        <option value="26">26 pt</option>
        <option value="28">28 pt</option>
        <option value="32">32 pt</option>
        <option value="36">36 pt</option>
        <option value="40">40 pt</option>
        <option value="42">42 pt</option>
        <option value="44">44 pt</option>
        <option value="48">48 pt</option>
        <option value="54">54 pt</option>
        <option value="60">60 pt</option>
        <option value="66">66 pt</option>
        <option value="72">72 pt</option>
        <option value="80">80 pt</option>
        <option value="88">88 pt</option>
        <option value="96">96 pt</option>
    </select>
    <div class="vl"></div>
    <button><img src="../assets/Writer/icons/icons_menu/grassetto.png"></button>
    <button><img src="../assets/Writer/icons/icons_menu/italic.png"></button>
    <button><img src="../assets/Writer/icons/icons_menu/underline.png"></button><button class="dropdown" @mouseover="addHoverClass" @mouseout="removeHoverClass"><img src="../assets/Writer/icons/icons_menu/dropdown-icon.png"></button>
    <button><img src="../assets/Writer/icons/icons_menu/barrato.png"></button>
    <div class="vl"></div>
    <button><img src="../assets/Writer/icons/icons_menu/apice.png"></button>
    <button><img src="../assets/Writer/icons/icons_menu/pedice.png"></button>
    <div class="vl"></div>
    <button><img src="../assets/Writer/icons/icons_menu/cancella-formattazione-diretta.png"></button>
    <div class="vl"></div>
    <button class="espandi"><img src="../assets/Writer/icons/icons_menu/espandi.png"></button>
    </div>
  </div>
</template>

<script scoped>
export default {
  methods: {
    changeDOCX(title) {
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
select {
  border: 1px solid #ececec;
  border-bottom: 1px solid #838383;
  margin-left: 4px;
}

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
