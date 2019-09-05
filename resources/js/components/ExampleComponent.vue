<template>
    <div class="container">
        <div>Hello World</div>

        <div><a :href="url" target="_blank">click me</a></div>

        <div>
            <button @click="flag = !flag">Change flag</button>
            <div>{{ flag }}</div>
        </div>
    </div>
</template>

<script>
    export default {
        data: function () {
            return {
                message: 'hello world',
                url: 'https://google.com',
                flag: true,
            }
        },
        mounted() {
            console.log('Component mounted.')
        }
    }
</script>
