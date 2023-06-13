<template>
    <div :class="{ loader: true, fadeout: !isLoading }">
        Loading ...
        <div class="image">
            <img class="logo img-fluid animate__animated animate__bounceIn" src="https://i.postimg.cc/QtS1W9tS/Quicloc8-logo.png">
        </div>
    </div>
</template>
  
<script>
export default {
    name: "Welcome",
    props: ["isLoading"]
};
</script>
  
<style scoped>
.loader {
    background-color: var(--primaryColor );
    bottom: 0;
    color: white;
    display: block;
    font-size: 32px;
    left: 0;
    overflow: hidden;
    padding-top: 10vh;
    position: fixed;
    right: 0;
    text-align: center;
    top: 0;
}

.fadeout {
    animation: fadeout 3.5s forwards;
}

@keyframes fadeout {
    to {
        opacity: 0;
        visibility: hidden;
    }
}

.logo {
    width: 40rem;
}

.image {
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 60vh;
}
</style>