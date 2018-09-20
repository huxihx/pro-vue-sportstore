<template>
    
</template>

<script>
export default {
    props: ["line"],
    data: function () {
        return {
            qvalue: this.line.quantity
        }
    },
    methods: {
        sendChangeEvent($event) {
            if ($event.target.value > 0) {
                this.$emit("quantity", Number($event.target.value))
                this.qvalue = $event.target.value
            } else {
                this.$emit("quantity", 1)
                this.qvalue = 1
                $event.target.value = this.qvalue
            }
        },
        sendRemoveEvent() {
            this.$emit("remove", this.line)
        }
    }
}
</script>

