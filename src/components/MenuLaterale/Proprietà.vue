<template>
    <div class="proprietà" style="overflow-y: auto; overflow-x: hidden;">
        <p>Proprietà</p>
        <details>
            <summary>Diapositiva</summary>
            <div class="select_wrapper">
                <label for="formato"><u>F</u>ormato:</label>
                <select name="formato" id="formato">
                    <option value="A6">A6</option>
                    <option value="A5">A5</option>
                    <option value="A4">A4</option>
                    <option value="A3">A3</option>
                    <option value="A2">A2</option>
                    <option value="A1">A1</option>
                    <option value="A0">A0</option>
                    <option value="B6_ISO">B6 (ISO)</option>
                    <option value="B5_ISO">B5 (ISO)</option>
                    <option value="B4_ISO">B4 (ISO)</option>
                    <option value="Lettera">Lettera</option>
                    <option value="Legale">Legale</option>
                    <option value="Folio">Folio</option>
                    <option value="Tabloid">Tabloid</option>
                    <option value="B6_JIS">B6 (JIS)</option>
                    <option value="B5_JIS">B5 (JIS)</option>
                    <option value="B4_JIS">B4 (JIS)</option>
                    <option value="16_Kai">16 Kai</option>
                    <option value="32_Kai">32 Kai</option>
                    <option value="32_Kai_grande">32 Kai grande</option>
                    <option value="Utente">Utente</option>
                    <option value="Busta_DL">Busta DL</option>
                    <option value="Busta_C6">Busta C6</option>
                    <option value="Busta_C6_5">Busta C6/5</option>
                    <option value="Busta_C5">Busta C5</option>
                    <option value="Busta_C4">Busta C4</option>
                    <option value="Diapositiva">Diapositiva</option>
                    <option value="Schermo_4_3">Schermo 4:3</option>
                    <option selected value="Schermo_16_9">Schermo 16:9</option>
                    <option value="Schermo_16_10">Schermo 16:10</option>
                    <option value="Schermo_panoramico">Schermo panoramico</option>
                    <option value="Presentazione_schermo_4_3">Presentazione su schermo (4:3)</option>
                    <option value="Presentazione_schermo_16_9">Presentazione su schermo (16:9)</option>
                    <option value="Presentazione_schermo_16_10">Presentazione su schermo (16:10)</option>
                    <option value="Cartolina_giapponese">Cartolina giapponese</option>
                </select>
            </div>
            <div class="select_wrapper">
                <label for="orientazione">Orientazione</label>
                <select name="formato" id="formato">
                    <option selected value="Orizzontale">Orizzontale</option>
                    <option value="Verticale">Verticale</option>
                </select>
            </div>
            <div class="select_wrapper">
                <label for="sfondo">Sfondo:</label>
                <select name="sfondo" id="sfondo">
                    <option selected value="nessuno">Nessuno</option>
                    <option value="colore">Colore</option>
                    <option value="sfumatura">Sfumatura</option>
                    <option value="tratteggio">Tratteggio</option>
                    <option value="bitmap">Bitmap</option>
                    <option value="motivo">Motivo</option>
                    <option value="usa_sfondo_diapositiva">Usa sfondo della diapositiva</option>
                </select>
            </div>
            <button>Inserisci immagine...</button>
            <div class="select_wrapper">
                <label for="diapositiva_schema">Diapositiva schema:</label>
                <select name="diapositiva_schema" id="diapositiva_schema">
                    <option selected value="predefinito">Predefinito</option>
                </select>
            </div>
            <input checked type="checkbox" id="sfondo_schema" name="sfondo_schema" value="sfondo_schema">
            <label for="sfondo_schema"> Sfondo dello schema</label><br>
            <input checked type="checkbox" id="oggetti_schema" name="oggetti_schema" value="oggetti_schema">
            <label for="oggetti_schema"> Oggetti dello schema</label><br>
            <button>Vista schema</button>
        </details>
        <details>
            <summary>Layout</summary>
            <div class="layout">
                <a><img src="../../assets/Impress/icons/icons_menu_laterale/proprietà-layout/layout-vuoto.png"></a>
                <a class="selected"><img src="../../assets/Impress/icons/icons_menu_laterale/proprietà-layout/layout-testo-centrato.png"></a>
                <a><img src="../../assets/Impress/icons/icons_menu_laterale/proprietà-layout/layout-titolo-contenuto.png"></a>
                <a><img src="../../assets/Impress/icons/icons_menu_laterale/proprietà-layout/layout-titolo-2contenuti.png"></a>
                <a><img src="../../assets/Impress/icons/icons_menu_laterale/proprietà-layout/layout-titolo.png"></a>
                <a><img src="../../assets/Impress/icons/icons_menu_laterale/proprietà-layout/layout-testo-centrato.png"></a>
                <a><img src="../../assets/Impress/icons/icons_menu_laterale/proprietà-layout/layout-titolo-2contenuti-contenuto.png"></a>
                <a><img src="../../assets/Impress/icons/icons_menu_laterale/proprietà-layout/layout-titolo-contenuto-2contenuti.png"></a>
                <a><img src="../../assets/Impress/icons/icons_menu_laterale/proprietà-layout/layout-titolo-2contenutisopra-contenuto.png"></a>
                <a><img src="../../assets/Impress/icons/icons_menu_laterale/proprietà-layout/layout-titolo-contenutosopra-contenuto.png"></a>
                <a><img src="../../assets/Impress/icons/icons_menu_laterale/proprietà-layout/layout-titolo-4contenuti.png"></a>
                <a><img src="../../assets/Impress/icons/icons_menu_laterale/proprietà-layout/layout-titolo-6contenuti.png"></a>
            </div>
        </details>
    </div>
</template>

<style scoped>
.layout {
    display: flex;
    flex-wrap: wrap;
}

.selected {
    border: 1px solid #0078d7 !important;
}

.select_wrapper {
    display: flex;
    align-items: center;
}

.layout>a {
    height: 47px;
    width: 61px;
    padding-left: 20px;
    padding-right: 20px;
    padding-top: 8px;
    padding-bottom: 8px;
    border: 1px solid #f0f0f0;
    margin-bottom: 1px;
}

.layout>a:hover:not(.selected) {
    border: 1px solid #85bae5;
}

summary {
    background-color: #e1e1e1;
    margin-bottom: 1px;
    font-weight: 500;
    font-size: 12px;
    cursor: pointer;
    list-style: none;
}

p {
    margin-bottom: 7px;
    font-weight: 500;
    font-size: 12px;
    cursor: default;
}

label {
    font-size: 12px;
    cursor: default;
    margin-right: 8px;
}

summary::before {
  content: url("../../assets/Impress/icons/icons_menu_laterale/open.png");
  margin-right: 5px;
}

details[open] summary::before {
  content: url("../../assets/Impress/icons/icons_menu_laterale/close.png");
  margin-right: 5px;
}
</style>