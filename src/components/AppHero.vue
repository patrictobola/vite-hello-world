<script>
export default {
    data() {
        return {
            image: 'tastiera'
        }
    },
    methods: {
        getImagePath(image) {
            const url = new URL(`../assets/img/${image}.jpg`, import.meta.url)
            return url.href
        }
    }
}
</script>
<template>
    <!-- Foto con indirizzo assoluto -->
    <img src="https://images.unsplash.com/photo-1517694712202-14dd9538aa97?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80"
        alt="Foto random">
    <span>Foto con indirizzo assoluto da internet</span>
    <img src="../assets/img/foto_pc.jpg" alt="Foto random">
    <span>Foto con indirizzo relativo dalla cartella</span>
    <img :src="getImagePath(this.image)" alt="Foto random">
    <span>Foto con indirizzo relativo ma con nome foto dinamico</span>
</template>
<style>
img {
    display: block;
    height: 300px;
}
</style>