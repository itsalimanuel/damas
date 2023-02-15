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
</template>

<style lang="sass">
.footer
    position: relative
    padding: 50px
    width: var(--width)
    display: grid
    grid-template-columns: 2fr 5fr
    &-social
        &-title
            padding-bottom: var(--space-top)
            h3
                font-size: 20px
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
        p
            padding-bottom: calc( var(--space-top) * 4 )
            font-size: 36px
        a
            padding: var(--space-top) calc( var(--space-top) * 4 )
            background: var(--main-color)
            color: var(--backgroundColor)
            text-decoration: none
            border-radius: calc( var(--space-top) * 3  )
</style>