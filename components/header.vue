<template>
    <header class="header">
        <div class="header-list">
            <div class="header-links">
                <router-link to="/">Team</router-link>
                <router-link to="/">Works</router-link>
                <router-link to="/">Blog</router-link>
            </div>
            <div class="header-contact">
                <a href="#" class="btn">Contact
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
    &-list
        display: flex
        justify-content: space-between
        max-width: 400px
        width: 100%
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
                
</style>