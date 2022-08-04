<template>
    <footer class="footer">
        <p>Author: Laura Rodríguez Castillo</p>
        <p><a href="mailto:laura.rodriguez.castillo@gmail.com">laura.rodriguez.castillo@gmail.com</a></p>
    </footer>
</template>

<script>
export default {
    name: 'FooterC',
}
</script>

<style lang="scss">
.footer {
    display: flex;
    justify-content: space-between;
    max-width: 600px;
    width: 100%;
    margin: 20px auto;
    padding: 20px 50px;
    background-color: green;
    color: white;

    a {
        color: white;
    }
}
</style>