<template>
    <div class="home">
        <div class="home-about">
            <div class="home-about-title">
                <p>
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequuntur, asperiores?
                </p>
            </div>
            <div class="home-about-image">
                <img src="https://images.pexels.com/photos/90333/pexels-photo-90333.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1"
                    alt="">
            </div>
        </div>
        <div class="home-service">
            <div class="home-service-title">
                <h3>Services:</h3>
            </div>
            <div class="home-service-list">
                <div class="--item">
                    <div class="--item-data">
                        <span>19 April 2022</span>
                    </div>
                    <div class="--item-title">
                        <h3>
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Repellendus nobis commodi tenetur
                            dolores sapiente eum, iure rerum ut nesciunt ducimus.
                        </h3>
                    </div>
                </div>
                <div class="--item">
                    <div class="--item-data">
                        <span>19 April 2022</span>
                    </div>
                    <div class="--item-title">
                        <h3>
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Repellendus nobis commodi tenetur
                            dolores sapiente eum, iure rerum ut nesciunt ducimus.
                        </h3>
                    </div>
                </div>
                <div class="--item">
                    <div class="--item-data">
                        <span>19 April 2022</span>
                    </div>
                    <div class="--item-title">
                        <h3>
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Repellendus nobis commodi tenetur
                            dolores sapiente eum, iure rerum ut nesciunt ducimus.
                        </h3>
                    </div>
                </div>
            </div>
        </div>
        <div class="home-works">
            <div class="home-works-title">
                <h3>Works:</h3>
            </div>
            <div class="home-works-list">
                <div class="--item" v-for="i in 10">
                    <div class="--item-data">
                        <span>19 April 2022</span>
                    </div>
                    <div class="--item-title">
                        <h3>
                            name
                        </h3>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="sass">
.home
    position: relative
    margin-top: 50px
    &-about
        width: 65%
        margin-left: var(--auto)
        &-title
            max-width: 60%
            p
                font-size: 38px
        &-image
            margin-top: calc( var(--space-top) * 2 )
            width: 100%
            height: 600px
            img
                width: var(--width)
                height: var(--height)
    &-service
        margin-top: calc( var(--space-top) * 4 )
        width: 65%
        margin-left: var(--auto)
        &-title
            h3
                font-size: 38px
                font-weight: 400
        &-list
            margin-top: calc( var(--space-top) * 2 )
            display: block
            .--item
                margin-top: var(--space-top)
                cursor: pointer
                padding: var(--space-top)
                padding-bottom: calc( var(--space-top) * 3 )
                display: grid
                grid-template-columns: 1fr 3fr
                border-top: 5px solid var(--main-color)
                &-data
                    span
                        font-size: 14px
                &-title
                    h3
                        font-size: 28px
                        font-weight: 300
    &-works
        margin-top: calc( var(--space-top) * 4 )
        width: 65%
        margin-left: var(--auto)
        &-title
            h3
                font-size: 38px
                font-weight: 400
        &-list
            margin-top: calc( var(--space-top) * 2 )
            display: block
            .--item
                margin-top: var(--space-top)
                cursor: pointer
                padding: var(--space-top)
                padding-bottom: calc( var(--space-top) * 3 )
                display: grid
                grid-template-columns: 1fr 3fr
                border-top: 5px solid var(--main-color)
                &-data
                    span
                        font-size: 14px
                &-title
                    text-align: right
                    h3
                        font-size: 28px
                        font-weight: 300
</style>