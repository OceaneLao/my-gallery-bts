<script>
import MainNav from '../Layout/MainNav.vue'
import PictureCard from '../Content/PictureCard.vue'

export default {
    name:"HomePage",
    components : {
        MainNav,
        PictureCard
    }
}
</script>

<template>
    <header>
        <main-nav />
    </header>
    <h2 class="text-center m-3">
        ✨ Mon premier projet en VueJS ✨
    </h2>
    <section>
        <picture-card />
    </section>
</template>