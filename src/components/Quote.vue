<template>
    <div class="col-sm-6 col-md-4 col-lg-3">
        <div class="panel panel-deafult">
            <slot></slot>
        </div>
    </div>
</template>
<script>
</script>
<style scoped>
    .panel-body {
        font-family: 'Arizonia', cursive;
        font-size: 24px;
        color: #6e6e6e;
    }

    .quote {
        cursor: pointer;
    }

    .quote:hover {
        background-color: #ffe2e2;
    }
</style>