<script scoped>
export default {
  methods: {
    dropdownToggle(event, dropdownType) {
      const buttonRect = event.target.getBoundingClientRect();
      this.$emit('toggle-dropdown', {
        type: dropdownType,
        position: {
          top: buttonRect.bottom,
          left: buttonRect.left
        }
      });
    }
  }
}
</script>

<template>
  <div class="menuLibreOfficeImpress">
    <button @click="dropdownToggle($event, 'File')">
      <u>F</u>ile
    </button>
    <button @click="dropdownToggle($event, 'Modifica')">
      <u>M</u>odifica
    </button>
    <button @click="dropdownToggle($event, 'Visualizza')">
      <u>V</u>isualizza
    </button>
    <button @click="dropdownToggle($event, 'Inserisci')">
      <u>I</u>nserisci
    </button>
    <button @click="dropdownToggle($event, 'Formato')">
      F<u>o</u>rmato
    </button>
    <button @click="dropdownToggle($event, 'Stili')">
      <u>S</u>tili
    </button>
    <button @click="dropdownToggle($event, 'Tabella')">
      T<u>a</u>bella
    </button>
    <button @click="dropdownToggle($event, 'Formulario')">
      Fo<u>r</u>mulario
    </button>
    <button @click="dropdownToggle($event, 'Strumenti')">
      St<u>r</u>umenti
    </button>
    <button @click="dropdownToggle($event, 'Finestra')">
      Fi<u>n</u>estra
    </button>
    <button @click="dropdownToggle($event, 'Aiuto')">
      Ai<u>u</u>to
    </button>
  </div>
</template>

<style scoped>
button {
  border: 1px solid #fdfdfd;
  background-color: #fefefe;
  font-size: 12px;
}

button:hover {
  background-color: #e4f2fe;
  border: 1px solid #d1eafe;
}
</style>