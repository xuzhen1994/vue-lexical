<template>
    <div id="vue-lexical-richtext" contenteditable="true"><slot></slot></div>
</template>
<script>
import {createEditor} from 'lexical'
import {registerRichText} from '@lexical/rich-text'
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
        registerRichText(editor, undefined)
        const rootEle = this.rootNode ? this.rootNode : document.getElementById("vue-lexical-richtext")
        editor.setRootElement(rootEle)
    },
}
</script>
<style scoped>
    #vue-lexical-richtext {
        min-height: 120px;
        background: #ddd;
    }
</style>