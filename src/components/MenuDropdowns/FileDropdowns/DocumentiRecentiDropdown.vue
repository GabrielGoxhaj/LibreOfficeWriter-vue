<template>
    <div id="dropdownDocumentiRecenti" class="dropdownDocumentiRecenti" :style="style">
        <a @click="changePPTX('Il Sistema Solare.pptx')"><div><img src="../../../assets/Impress/icons/icons_dropdown/file/file-presentazione.png"> <u>1</u>. Il Sistema Solare.pptx</div></a>
        <a @click="changePPTX('IVA.pptx')"><div><img src="../../../assets/Impress/icons/icons_dropdown/file/file-presentazione.png"> <u>2</u>. IVA.pptx</div></a>
        <a @click="changePPTX('Social Media Marketing.pptx')"><div><img src="../../../assets/Impress/icons/icons_dropdown/file/file-presentazione.png"> <u>3</u>. Social Media Marketing.pptx</div></a>
    </div>
</template>

<script>
export default {
    props: {
        style: {
            type: Object,
            default: () => ({})
        }
    },
    methods: {
        changePPTX(title) {
            console.log('changePPTX called with:', title);
            this.updateTitleAndClose(title);
            this.closeDropdown();
        },
        updateTitleAndClose(title) {
            this.$emit('update-title', title);
        },
        closeDropdown() {
            this.$emit('toggle-dropdown', { type: null, position: { top: 0, left: 0 } });
        }
    }
}
</script>

<style scoped>
.dropdownDocumentiRecenti {
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

.dropdownDocumentiRecenti a {
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

.dropdownDocumentiRecenti a div {
    display: flex;
    align-items: center;
    padding: auto;
}

.dropdownDocumentiRecenti a div img {
    margin-right: 14px;
    max-width: 16px;
    max-height: 16px;
}

.dropdownDocumentiRecenti a:hover:not(.disabled) {
    background-color: #95cdfb;
}

hr {
    margin: 0;
    color: #d7d7d7;
}

.dropdownDocumentiRecenti a:hover.disabled {
    background-color: #ececec;
}

a.disabled {
    color: #808080;
}
</style>