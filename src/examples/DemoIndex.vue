<template>
    <div>
        <div>
            <h3>Plain Text Demo</h3>
            <plain-text-demo></plain-text-demo>
            <h3>Rich Text Demo</h3>
            <rich-text-demo></rich-text-demo>
        </div>
    </div>
</template>
<script>
import PlainTextDemo from './PlainTextDemo.vue'
import RichTextDemo from './RichTextDemo.vue'
export default {
  components: { PlainTextDemo, RichTextDemo },
    
}
</script>
<style scoped>
    
</style>