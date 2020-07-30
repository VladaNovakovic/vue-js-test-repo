<template>
    <div>
        <form v-on:submit.prevent="submitValue">
            <input
                type="text"
                name="usernameInput"
                title="usernameInput"
                v-model="user"
            />
            <input
                type="text"
                name="tweetInput"
                title="tweetInput"
                v-model="tweetText"
            />
            <input type="submit" name="submitButton"/>
        </form>
    </div>
</template>

<script>
    export default {
        name: 'TweetForm',
        props: {},
        data: () => ({
            user: 'Username',
            tweetText: 'hello there, what\'s on your mind',
        }),
        methods: {
            submitValue: function(event) {
                event.preventDefault();
                console.log({
                    event,
                    target: {...event.target},
                    // helloThis: this,
                    user: this.user,
                    tweetText: this.tweetText,
                });
            }
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    input {
        display: block;
    }

    a {
        color: #42b983;
    }
</style>
