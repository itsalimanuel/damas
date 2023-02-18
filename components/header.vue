<script setup lang="ts">
import { ref } from "#imports";
const menuRef = ref<Boolean>(false);

const toggleMneu = () => {
    menuRef.value = !menuRef.value;
}
</script>

<template>
  <header class="header">
    <div id="burger">
      <Menu @click="toggleMneu" />
    </div>
    <div :class="{'active': menuRef}" class="header-list">
      <div class="header-links">
        <router-link to="/">Team</router-link>
        <router-link to="/">Works</router-link>
        <router-link to="/">Blog</router-link>
      </div>
      <div class="header-contact">
        <a href="#" class="btn"
          >Contact
          <span>&#8594;</span>
        </a>
      </div>
    </div>
    <div class="header-brand">
      <h2>Damas</h2>
    </div>
  </header>
</template>

<style lang="sass" scoped>
.header
    position: fixed
    width: 100%
    display: flex
    z-index: 2
    align-items: center
    justify-content: space-between
    padding: 40px 50px
    #burger
        display: none
    @media (max-width: 1200px)
        padding: 20px 25px
    @media (max-width: 820px)
        padding: 10px 20px
        #burger
            display: block
            z-index: 5
    .active
        display: flex
        flex-direction: column
        position: absolute
        top: 0
        left: 0
        width: 100%
        height: 100vh
        justify-content: space-evenly
        align-items: center
        background-color: var(--backgroundColor)
    &-list
        display: flex
        justify-content: space-between
        max-width: 400px
        width: 100%
        @media (max-width: 820px)
            display: none
            max-width: 100%
    &-links
        display: block
        a
            display: block
            color: var(--main-color)
            text-decoration: none
            font-size: var(--fontSize)
            margin-top: var(--space-top)
            &:hover
                color: var(--color-white)
    &-contact
        
        a
            position: relative
            width: 200px
            height: 40px
            display: grid
            place-items: center
            background: var(--main-color)
            color: var(--backgroundColor)
            border-radius: 80px
            font-size: var(--fontSize)
            font-weight: 700
            letter-spacing: 1px
            text-decoration: none
            border-top: 2px solid #e6e6fa
            border-left: 2px solid #e6e6fa
            padding-left: var(--space-top)
            overflow: hidden
            transition: 0.5s ease-in-out

            &:hover
                padding-left: 0
                padding-right: var(--space-top)
                color: var(--backgroundColor)
                span
                    left: calc(100% - (var(--space-top)*4))
                    transform: rotate(180deg)

            span
                position: absolute
                display: grid
                place-items: center
                left: 5px
                width: 30px
                height: 30px
                background: var(--backgroundColor)
                color: var(--main-color)
                border-radius: 50%
                font-size: var(--fontSize)
                font-weight: 900
                transition: 0.5s cubic-bezier(0.4, 0, 1, 1)
    &-brand
        h2
            font-size: 72px
            color: var(--main-color)
            @media (max-width: 1200px)
                font-size: 36px
            @media (max-width: 820px)
                font-size: 22px
</style>
