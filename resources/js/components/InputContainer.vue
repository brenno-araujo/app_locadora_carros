<template>
    <div class="form-group">
         <label :for="id">{{title}}</label>
         <slot></slot>
         <small id="emailHelp" class="form-text text-muted">{{textHelp}}</small>
    </div>
</template>

<script>
    export default {
        props: ['id', 'title', 'idHlep', 'textHelp']
    }
</script>
