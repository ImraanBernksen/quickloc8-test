<template>
    <footer>
        <div class="container text-center">
            <div class="row">
                <div class="col-lg-4 more">
                        <p><div class="A_N">Address:</div>Cnr Koeberg & Freedom Way Suite 50 & 51 Frazzitta Business Park,
                        Milnerton, 7441</p>
                        <p><div class="A_N">Phone number:</div>087 022 0814</p>
                </div>
                <div class="col-lg-4 m-auto">
                    <a class="quick" href="/">HOME</a>
                    <a class="quick" href="/message">MESSAGES</a>
                    <a class="quick" href="/contact">CONTACT US</a>
                </div>
                <div class="col-lg-4 m-auto">
                    <img class="img-fluid" src="https://i.postimg.cc/QtS1W9tS/Quicloc8-logo.png" style="width: 20rem;">
                </div>
            </div>
            <p class="more text-center">Copyright &copy; 2015 - 2023 | <a href="/" class="footer-mib">Quickloc8</a></p>
        </div>
    </footer>
</template>
<script>
export default {
    name: 'Footer'
}
</script>
<style scoped>
.more {
    font-size: 18px;
    text-align: start;
}
.A_N {
    color: var(--accentColor);
}

.footer-mib {
    text-decoration: none;
    color: var(--accentColor);
}

.footer-mib:hover {
    color: white;
}

footer {
    padding: 10px;
    box-shadow: 0px 0 19px rgba(1, 0, 0, 0.9);
    width: 100%;
    background-color: var(--primaryColor);
}

.quick:hover {
    color: var(--accentColor);
}

.quick {
    display: block;
    padding: 5px;
    color: white;
    font-size: 18px;
    text-decoration: none;
    font-family: 'Poppins', sans-serif;
}
</style>