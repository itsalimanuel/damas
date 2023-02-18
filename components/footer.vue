<script setup lang="ts">
import {ref , onMounted} from '#imports'

const data = ref<Number>()

const getYear = () => {
    data.value = new Date().getFullYear()
}

onMounted(() => {
    getYear()
})

</script>

<template>
    <footer class="footer">
        <div class="footer-social">
            <div class="footer-social-title">
                <h4>Follow on social</h4>
            </div>
            <div class="footer-social-links">
                <a href="">facebook</a>
                <a href="">twitter</a> 
            </div>
        </div>
        <div class="footer-contact">
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. At veniam accusamus, nobis totam error nisi aspernatur soluta incidunt id voluptas!</p>
            <a href="">hi@email.com</a>
        </div>
    </footer>
    <div class="copyright">
        Made with love using <a href="">Nuxt</a> - {{ data }}
    </div>
</template>

<style lang="sass" scoped>
.footer
    position: relative
    padding: 50px
    width: var(--width)
    display: grid
    grid-template-columns: 2fr 5fr
    @media (max-width: 820px)
        grid-template-columns: unset
        display: flex
        flex-direction: column
        padding: 20px
    &-social
        &-title
            padding-bottom: var(--space-top)
            h3
                font-size: 20px
                @media (max-width: 820px)
                    font-size: 22px
        &-links
            display: block
            a
                display: block
                font-size: var(--fontSize)
                color: var(--main-color)
                text-decoration: none
                margin-top: var(--space-top)
    &-contact
        padding-bottom: calc( var(--space-top) * 12 )
        @media (min-width: 820px)
            padding-bottom: var(--space-top)
        p
            padding-bottom: calc( var(--space-top) * 4 )
            font-size: 36px
            @media (max-width: 820px)
                padding-bottom: calc( var(--space-top) * 4 )
                padding-top: var(--space-top)
                font-size: 18px
        a
            padding: var(--space-top) calc( var(--space-top) * 4 )
            background: var(--main-color)
            color: var(--backgroundColor)
            text-decoration: none
            border-radius: calc( var(--space-top) * 3  )
            @media (max-width: 820px)
                width: var(--width)
                display: block
                font-weight: bold
                text-align: center
.copyright
    padding: 0 50px
    text-align: center
    @media (max-width: 820px)
        padding-bottom: 20px
    a
        color: var(--main-color)
        text-decoration: none
        font-weight: bold
</style>