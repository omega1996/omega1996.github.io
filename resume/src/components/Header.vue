<template>
    <div>

        <div class="app__name mobile">
            <p class="app__header">
                {{ nameSymbolsMobile }}
            </p>
        </div>
        <div class="app__name desktop">
            <p class="app__header">
                {{ nameSymbols }}
            </p>
        </div>
    </div>
</template>

<script setup lang='ts'>
const nameSymbols = `d888888b db    db  .d8b.  d8b   db   d8888b. d888888b  .d8b.  d88888D  .d8b.  d8b   db  .d88b.  db    db \n  \`88\'   88    88 d8\' \`8b 888o  88   88  \`8D   \`88\'   d8\' \`8b YP  d8\' d8\' \`8b 888o  88 .8P  Y8. 88    88 \n   88    Y8    8P 88ooo88 88V8o 88   88oobY\'    88    88ooo88    d8\'  88ooo88 88V8o 88 88    88 Y8    8P \n   88    \`8b  d8\' 88~~~88 88 V8o88   88\`8b      88    88~~~88   d8\'   88~~~88 88 V8o88 88    88 \`8b  d8\' \n  .88.    \`8bd8\'  88   88 88  V888   88 \`88.   .88.   88   88  d8\' db 88   88 88  V888 \`8b  d8\'  \`8bd8\'  \nY888888P    YP    YP   YP VP   V8P   88   YD Y888888P YP   YP d88888P YP   YP VP   V8P  \`Y88P\'     YP`

const nameSymbolsMobile = `d888888b db    db  .d8b.  d8b   db \n  \`88\'   88    88 d8\' \`8b 888o  88 \n   88    Y8    8P 88ooo88 88V8o 88 \n   88    \`8b  d8\' 88~~~88 88 V8o88 \n  .88.    \`8bd8\'  88   88 88  V888 \nY888888P    YP    YP   YP VP   V8P \n                                   \n                                   \nd8888b. d888888b  .d8b.  d88888D  .d8b.  d8b   db  .d88b.  db    db \n88  \`8D   \`88\'   d8\' \`8b YP  d8\' d8\' \`8b 888o  88 .8P  Y8. 88    88 \n88oobY\'    88    88ooo88    d8\'  88ooo88 88V8o 88 88    88 Y8    8P \n88\`8b      88    88~~~88   d8\'   88~~~88 88 V8o88 88    88 \`8b  d8\' \n88 \`88.   .88.   88   88  d8\' db 88   88 88  V888 \`8b  d8\'  \`8bd8\'  \n88   YD Y888888P YP   YP d88888P YP   YP VP   V8P  \`Y88P\'     YP`

</script>

<style scoped lang='scss'>
.app {


    &__header {
        text-wrap: nowrap;
        white-space: pre;
    }

    &__name {
        z-index: 2;
        position: relative;
        font-family: 'Roboto Mono';
        font-weight: 600;
        padding: 2rem;
        padding-bottom: 0;
        width: calc(100% - 4em);

        color: #98d6f7;

    }
}


.mobile {



    @media only screen and (max-width: 1100px) {
        display: block;
    }

    @media only screen and (min-width: 1101px) {
        display: none;
    }

    @media only screen and (max-width: 700px) {
        font-size: 0.75em;
    }

    @media only screen and (max-width: 520px) {
        font-size: 0.5em;
    }

    @media only screen and (max-width: 350px) {
        font-size: 0.4em;
    }
}

.desktop {
    @media only screen and (max-width: 1100px) {
        display: none;
    }

    @media only screen and (min-width: 1101px) {
        display: block;
    }
}
</style>