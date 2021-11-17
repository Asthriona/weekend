<template>
    <div class="footer">
        <p>
            Code hosted on GitHub. Hosting and DNS Powered by Cloudlfare. <br>
            Made by Asthriona, Inspired by <a href="https://estcequecestbientotleweekend.fr/" target="_blank" rel="noopener noreferrer">This website</a>
            My other websites and services: <br>
            <a href="http://" target="_blank" rel="noopener noreferrer">Asthriona.com</a> • <a href="http://" target="_blank" rel="noopener noreferrer">Yukiko.app</a> • <a href="http://" target="_blank" rel="noopener noreferrer">IMG-UP </a>
        </p>
        <div class="foot_logo">
            <p>Operating Company</p>
            <div class="figure">
                <img src="https://cdn.nishikino.xyz/asthriona/icons/footLogo.png" width="100%" alt="Not We">
            </div>
        </div>
    </div>
</template>

<style scoped>
.footer {
    position: fixed;
    bottom: 0;
    width: 100%;
    text-align: center;
    background-color: #0d0d0d;
    color: #ccc;
    padding: 10px;
    left: 0;
    right: 0;
}
a{
    color: #d86100;
}
.footer .foot_logo {
    max-width: 300px;
    width: 100%;
    margin: 0 auto 12px;
}
.footer .foot_logo p {
    display: table-cell;
    width: 9em;
    vertical-align: middle;
    font-size: 12px;
}
.footer .foot_logo .figure {
    display: table-cell;
    width: calc(100% - 7em);
}
</style>
