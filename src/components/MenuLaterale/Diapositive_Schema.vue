<template>
    <div style="overflow-y: auto;" class="diapositive_schema">
        <div class="title" style="display: flex; justify-content: space-between;">
            <p>Diapositive schema</p>
            <div style="display: flex; justify-content: space-between;">
                <p class="buttons">&quest;</p>
                <p class="buttons">&times;</p>
            </div>
        </div>
        <details>
            <summary>Usate in questa presentazione</summary>
        </details>
        <details>
            <summary>Usate recentemente</summary>
        </details>
        <details>
            <summary>Dispoinibili per l'uso</summary>
            <div>
                <img src="../../assets/Impress/icons/icons_menu_laterale/diapositiva-schema-modelli.png">
            </div>
        </details>
    </div>
</template>

<style scoped>
.diapositive_schema {
    border-left: 1px solid #a0a0a0;
    padding-left: 8px;
    padding-right: 8px;
}

summary {
    background-color: #e1e1e1;
    margin-bottom: 1px;
    font-weight: 500;
    font-size: 12px;
    cursor: default;
}

p {
    margin-bottom: 7px;
    font-weight: 500;
    font-size: 12px;
    cursor: default;
}

.buttons {
    border: 1px solid white;
    cursor: default;
}

.buttons:hover {
    border: 1px solid #d1eafe;
    background-color: #e4f2fe;
    cursor: default;
}

summary::before {
  content: url("../../assets/Impress/icons/icons_menu_laterale/open.png"); /* Icona di apertura */
}

details[open] summary::before {
  content: url("../../assets/Impress/icons/icons_menu_laterale/close.png");; /* Icona di chiusura */
}
</style>