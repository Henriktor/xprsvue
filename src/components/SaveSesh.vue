<template>
    <div class="saveboi" align="right">
        <p>bla bla</p>
    </div>
</template>
<script>
export default {
    props: {
        msg: String
    },
    render: function(createElement) {

        return createElement('p', this.msg)
    }
}
</script>