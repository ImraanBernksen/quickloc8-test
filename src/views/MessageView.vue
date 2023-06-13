<template>
    <NavBar/>
    <h1>Messages</h1>
    <div class="message-section">
        <div class="message">
            <div class="card p-1" v-for="message in messages" :key="message.id">
                <div class="row g-0">
                    <div class="col-md-2 m-auto">
                        <div class="eee">
                            E
                        </div>
                    </div>
                    <div class="col-md-8">
                        <div class="card-body">
                            <p class="text-start">{{ message.message }}</p>
                            <p class="text-start">{{ message.subject }}</p>
                        </div>
                    </div>
                    <div class="col-md-2 m-auto text-center">
                        <p>{{ message.display }}</p>
                        <i class="bi bi-star"></i>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <Footer/>
</template>
<script>
import NavBar from '../components/NavBar.vue';
import MessageData from '../messages.json';
import Footer from '@/components/Footer.vue';
export default {
    components: {
        NavBar,
        Footer
    },
    data() {
        return { messages: MessageData }
    }
}
</script>
<style scoped>
.bi-star {
    font-size: 30px;
}

.bi-star:hover {
    color: yellow;
}

.message {
    padding-top: 30px;
}

.message-section {
    padding-bottom: 20px;
}

.card {
    border: 2px solid black;
}

.eee {
    background-color: var(--primaryColor);
    border: 3px solid black;
    height: 100px;
    border-radius: 50%;
    width: 100px;
    margin: auto;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 40px;
}
</style>