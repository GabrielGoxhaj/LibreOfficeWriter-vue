<template>
    <div class="menuLaterale">
        <button><img src="../assets/Writer/icons/icons_menu_laterale/impostazioni.png"></button>
        <button @click="openMenuLaterale('proprietà', $event)"><img src="../assets/Writer/icons/icons_menu_laterale/proprietà.png"></button>
        <button @click="openMenuLaterale('galleria', $event)"><img src="../assets/Writer/icons/icons_menu_laterale/galleria.png"></button>
        <button @click="openMenuLaterale('navigatore', $event)"><img src="../assets/Writer/icons/icons_menu_laterale/navigatore.png"></button>
        <button @click="openMenuLaterale('forme', $event)"><img src="../assets/Writer/icons/icons_menu_laterale/forme.png" ></button>
        <button @click="openMenuLaterale('pagina', $event)"><img src="../assets/Writer/icons/icons_menu_laterale/pagina.png" ></button>
        <button @click="openMenuLaterale('ispettore-stili', $event)"><img src="../assets/Writer/icons/icons_menu_laterale/ispettore-stili.png" ></button>
        <button @click="openMenuLaterale('gestisci-modifiche', $event)"><img src="../assets/Writer/icons/icons_menu_laterale/gestisci-modifiche.png" ></button>
        <button @click="openMenuLaterale('controllo-accesso', $event)"><img src="../assets/Writer/icons/icons_menu_laterale/controllo-accesso.png" ></button>
        </div>
</template>

<script>
export default {
    methods: {
        assignSelected(event) {
            const buttons = document.querySelectorAll('.menuLaterale button');
            const button = event.target.closest('button');
            if (button.classList.contains('selected')) {
                button.classList = '';
            } else {
                buttons.forEach(btn => btn.classList.remove('selected'));
                button.classList.add('selected');
            }
        },
        openMenuLaterale(menu, event) {
            this.assignSelected(event);
        }
    }
}
</script>

<style scoped>
.menuLaterale {
    display: flex;
    flex-direction: column;
    border-left: 1px solid #b0b0b0;
    height: 370px;
}

button {
    border: 1px solid #f0f0f0;
    background-color: #f0f0f0;
    padding: 4px;
    margin: 2px;
}

button:hover {
    background-color: #e4f2fe;
    border: 1px solid #d1eafe;
}

.selected {
    border: 1px solid #99d1ff; 
    background-color: #cce8ff;
}
</style>