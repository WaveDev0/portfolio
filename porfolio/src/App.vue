<script setup>
  // import HelloWorld from './components/HelloWorld.vue'
  import presentation from './components/presentation.vue'

  import imagepresentation from './assets/img/img.png'

</script>


<template>
    <nav>
        <section class="container_nav" :style="{maxWidth : style.MaxWidth}">
            <h1>Mathéo Thierry</h1>
            <ul>
                <li><a href="#">Accueil</a></li>
                <li><a href="#">A propos</a></li>
                <li><a href="#">Competences</a></li>
                <li><a href="#">Project</a></li>
                <li><a href="#">Contact</a></li>

                <li><a href="#" class="btn_nav">Telecharger Cv</a></li>
            </ul>
        </section>
    </nav>    

    <div class="separation"></div>

    <header>
        <presentation :maxwdt="style.MaxWidth" :image="imagepresentation">
            <template #textepresentation>
                <h2>Titre du Texte</h2>
                <p>Ceci est un exemple de texte à côté d'une image. Vous pouvez personnaliser ce texte, ainsi que l'image, en modifiant le CSS associé.</p>
            </template>
        </presentation>
    </header>
</template>


<script>
    export default {
        data() {
            return {
                Number : 0, 

                style : {
                    MaxWidth : '1100px',  
                }
            }
        }
    }
</script>

<style>
    body  {
        background-color: rgba(17, 17, 17, 1);
    }
    /* nav */
    h1 {
        color: white;
        font-weight: normal;
        font-size: 1rem;
    }
    nav {
        background-color: rgba(15, 15, 15, 1);
        display: flex; 
        position: fixed;
        width: 100%;
        border-bottom: solid 1px rgba(255, 255, 255, 0.082);
        padding: 25px 0px; 
        justify-content: center;
        align-items: center; 
    }
    nav .container_nav {
        display: flex;
        width: 100%;
        align-items: center;
        justify-content: space-between;
        /* background: rgb(79, 79, 80); */
    } 
    nav .container_nav ul {
        align-items: center;
        display: flex;
        height: 19px;
        /* background-color: red;   */
        width: 600px; 
        justify-content: space-between;
    }
    nav .container_nav ul li {
        list-style: none;
    }
    nav .container_nav ul li a {
        text-decoration: none; 
        font-size: 0.7rem; 
        transition: 0.2s;
        font-family: 'font-Regular';
        color: rgba(255, 255, 255, 0.71);
    }
    nav .container_nav ul li a:hover {
        color: white;
    }
    .btn_nav {
        background-color: rgba(40, 233, 140, 1);
        color: black !important;
        padding: 10px; 
        transition: 0.2s;
        border-radius: 4px;
        font-family: 'font-medium' !important;
    }
    .btn_nav:hover {
        opacity: 80%;
    }

    /* separation */

    .separation {
        /* background-color: red; */
        height: 71.6px;
    }
</style>
