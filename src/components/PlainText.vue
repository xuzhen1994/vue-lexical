<template>
    <div id="vue-lexical-plaintext" contenteditable="true"><slot></slot></div>
</template>
<script>
import {createEditor} from 'lexical'
export default {
    props: {
        config: {
            type: Object,
            required: true,
            default: function () {
                return {}
            }
        },
        rootNode: {
            type: Object,
            required: false
        }
    },
    data() {
        return {
        }
    },
    mounted() {
        const editor = createEditor(this.config)
        const rootEle = this.rootNode ? this.rootNode : document.getElementById("vue-lexical-plaintext")
        editor.setRootElement(rootEle)
    },
}
</script>
<style scoped>
    
</style>