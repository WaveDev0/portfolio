<template>

    <section class="presentation">
        <div class="content_img">
            <div class="container" :style="{maxWidth : maxwdt}">
                <div class="text"  :style="{maxWidth : maxwdt}">
                    <slot name="textepresentation"></slot>
                </div>
                <div class="image"  :style="{maxWidth : maxwdt}">
                    <img :src="image" alt="Description de l'image">
                </div>
            </div>
        </div>     
    </section>

</template>


<script>
    export default {
        props : ["maxwdt", 'image']
    }
</script>

<style>
    
    /* presentation */


 

    .content_img {
        padding: 10px 0px;
        background-color: rgb(82, 82, 82);
    }

    .container {
        display: flex;
        flex-wrap: wrap;
        gap: 20px;
        padding: 20px;
        
        justify-content: center;
        margin: 0 auto;
    }

    .image, .text {
        flex: 1 1 300px; 
        width: 100%; 
    }

    .image img {
        width: 100%;
        display: block;
        object-fit: cover;
        border-radius: 10px;
    }

    .text {
        /* padding: 20px; */
        /* background-color: #f4f4f4; */
        border-radius: 10px;
        display: flex;
        flex-direction: column;
        justify-content: center;
    }

   
</style>


