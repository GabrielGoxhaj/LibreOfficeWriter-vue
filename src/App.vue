<script setup>
import { ref } from 'vue';
import MenuLibreOfficeWriter from './components/MenuLibreOfficeWriter.vue';
import FileDropdown from './components/MenuDropdowns/FileDropdown.vue';
import ModificaDropdown from './components/MenuDropdowns/ModificaDropdown.vue';
import VisualizzaDropdown from './components/MenuDropdowns/VisualizzaDropdown.vue';
import InserisciDropdown from './components/MenuDropdowns/InserisciDropdown.vue';
import FormatoDropdown from './components/MenuDropdowns/FormatoDropdown.vue';
import FinestraDropdown from './components/MenuDropdowns/FinestraDropdown.vue';
import AiutoDropdown from './components/MenuDropdowns/AiutoDropdown.vue';
import MenuIconLibreOfficeWriter from './components/MenuIconLibreOfficeWriter.vue';
import DocumentiRecentiDropdown from './components/MenuDropdowns/FileDropdowns/DocumentiRecentiDropdown.vue';
import TitleBar from './components/TitleBar.vue';
import Nascondi from './components/Nascondi.vue';
import MenuLaterale from './components/MenuLaterale.vue';

// titolo docx
const title_docx = ref('Senza Nome 1.docx');
const updateTitle = (title) => {
  title_docx.value = title;
  updatePagina(1);
};

// funzioni e costanti per dinamicizzare attuale pagina e il massimo di pagine per ciascun file
const paginaNumber = ref(1);
const maxPagina = ref(1);
const updatePagina = (pagina) => {
  paginaNumber.value = pagina;
};
const updateMaxPagina = (max) => {
  maxPagina.value = max;
};

// visibilità dei menu laterali alla pagina
const isMenuLateraleVisible = ref(true);
const hideMenuLaterale = () => {
  isMenuLateraleVisible.value = !isMenuLateraleVisible.value;
  console.log(isMenuLateraleVisible.value)
};
const isSubMenuLateraleVisible = ref(false);
const showSubMenuLaterale = () => {
  isSubMenuLateraleVisible.value = !isSubMenuLateraleVisible.value
}

// funzioni e costanti per i vari dropdown del menu superiore
const showDropdown = ref(null);
const dropdownPosition = ref({ top: 0, left: 0 });
const toggleDropdown = ({ type, position }) => {
  showDropdown.value = showDropdown.value === type ? null : type;
  dropdownPosition.value = position;
};
const closeDropdown = () => {
  showDropdown.value = null;
};

// funzioni e costanti per i vari dropdown dei dropdown (submenu)
const showSubDropdown = ref(null);
const subDropdownPosition = ref({ top: 0, left: 0 });
const toggleSubDropdown = ({ type, position }) => {
  console.log(showSubDropdown.value);
  showSubDropdown.value = showSubDropdown.value === type ? null : type;
  subDropdownPosition.value = position;
};
const closeSubDropdown = () => {
  showSubDropdown.value = null;
}

</script>

<template>
  <div class="libreOfficeWriter">
    <TitleBar :title_docx="title_docx" />
    <div class="menu">
      <MenuLibreOfficeWriter @toggle-dropdown="toggleDropdown" />
      <div id="dropdownsWrapper">
        <div id="fileWrapper">
          <FileDropdown @toggle-sub-dropdown="toggleSubDropdown" v-if="showDropdown === 'File'"
            :style="{ top: dropdownPosition.top + 'px', left: dropdownPosition.left + 'px' }" />
          <!-- Dropdown di File -->
          <DocumentiRecentiDropdown v-if="showSubDropdown === 'DocumentiRecenti'" @update-title="updateTitle"
            @toggle-dropdown="closeDropdown" @toggle-sub-dropdown="closeSubDropdown"
            :style="{ top: dropdownPosition.top + 'px', left: dropdownPosition.left + 'px' }" />
        </div>
        <ModificaDropdown v-if="showDropdown === 'Modifica'"
          :style="{ top: dropdownPosition.top + 'px', left: dropdownPosition.left + 'px' }" />
        <VisualizzaDropdown v-if="showDropdown === 'Visualizza'"
          :style="{ top: dropdownPosition.top + 'px', left: dropdownPosition.left + 'px' }" />
        <InserisciDropdown v-if="showDropdown === 'Inserisci'"
          :style="{ top: dropdownPosition.top + 'px', left: dropdownPosition.left + 'px' }" />
        <FormatoDropdown v-if="showDropdown === 'Formato'"
          :style="{ top: dropdownPosition.top + 'px', left: dropdownPosition.left + 'px' }" />
        <StiliDropdown v-if="showDropdown === 'Stili'"
          :style="{ top: dropdownPosition.top + 'px', left: dropdownPosition.left + 'px' }" />
        <TabellaDropdown v-if="showDropdown === 'Tabella'"
          :style="{ top: dropdownPosition.top + 'px', left: dropdownPosition.left + 'px' }" />
        <FormularioDropdown v-if="showDropdown === 'Formulario'"
          :style="{ top: dropdownPosition.top + 'px', left: dropdownPosition.left + 'px' }" />
        <StrumentiDropdown v-if="showDropdown === 'Formulario'"
          :style="{ top: dropdownPosition.top + 'px', left: dropdownPosition.left + 'px' }" />
        <FinestraDropdown v-if="showDropdown === 'Finestra'"
          :style="{ top: dropdownPosition.top + 'px', left: dropdownPosition.left + 'px' }" />
        <AiutoDropdown v-if="showDropdown === 'Aiuto'"
          :style="{ top: dropdownPosition.top + 'px', left: dropdownPosition.left + 'px' }" />
      </div>
      <MenuIconLibreOfficeWriter @update-title="updateTitle" />
    </div>
    <div id="mainWrapper" style="display: flex; align-items: center;">
      <div>
        <img id="righello" src="../src/assets/Writer/icons/righello.png">
      </div>
          <Nascondi @click="hideMenuLaterale" :style="isMenuLateraleVisible ? 'transform: rotate(180deg)' : 'transform: rotate(0deg)'" />
          <MenuLaterale v-if="isMenuLateraleVisible" />
      </div>


    <div class="footer">
      <div class="footer-top">
        <img src="./assets/Writer/footer/footer1.png"/>
      </div>
      <div class="footer-bottom" style="display: flex; align-items: center;">
        <img src="./assets/Writer/footer/footer2.png"/>
        <p class="numberPagina">Pagina {{paginaNumber}} di {{maxPagina}}</p>
        <img src="./assets/Writer/footer/footer3.png"/>
    </div>
    </div>
  </div>
</template>

<style scoped>
.libreOfficeWriter {
  width: 800px;
  height: 560px;
  background-color: #f0f0f0;
  font-family: 'Segoe UI', Tahoma, sans-serif;
}

.menu {
  background-color: #fdfdfd;
  border-bottom: 1px solid #b0b0b0;
}

.libreOfficeWriter {
  border: 1px solid black;
}

hr {
  display: block;
  margin-left: auto;
  margin-right: auto;
  margin-top: 0;
  margin-bottom: 0;
}

#mainWrapper {
  display: flex;
  flex-direction: row;
  width: 100%;
  height: 370px;
}

.footer-top {
  border-top: 1px solid #c4c4c4;
  height: 38px;
}

.footer-bottom {
  border-top: 1px solid #c4c4c4;
  height: 21px;
}

.numberPagina {
  margin: none;
  margin-left: 5px;
  font-size: 11px;
  margin-right: 6px;
  margin-bottom: 8px;
  cursor: default;
}

#righello {
  margin-left: 9px;
  margin-top: 4px;
}
</style>