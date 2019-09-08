<template>
    <div class="container">

        <!-- hello world -->
        <div>{{ message }}</div>

        <!-- v-bind -->
        <div style="margin-top: 20px; border-top: 1px solid;">
            <a :href="url" target="_blank">click me to go to Google</a>
        </div>

        <!-- v-on -->
        <div style="margin-top: 20px; border-top: 1px solid;">
            <button @click="flag = !flag">Toggle flag blow</button>
            <div>{{ flag }}</div>
        </div>

        <!-- computed -->
        <div style="margin-top: 20px; border-top: 1px solid;">
            computed message
            <div>{{ computedShowMessage }}</div>
            <button @click="message += ' clicked'">Change message</button>
        </div>

        <!-- metohd -->
        <div style="margin-top: 20px; border-top: 1px solid;">
            metohd message
            <div v-text="showMessage()"></div>
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
        },
        computed: {
            computedShowMessage: function () {
                console.log('executed computed showMessage')
                return this.message
            }
        },
        methods: {
            showMessage: function () {
                console.log('executed method showMessage')
                return this.message
            }
        },
    }
</script>
