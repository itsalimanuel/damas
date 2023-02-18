<script setup>
import { ref } from "#imports";
import gsap from "gsap";

const refItem = ref(null);

const mouseEnter = () => {
  let mouse = gsap.timeline();
  let targets = gsap.utils.toArray(refItem.value);
  targets.forEach((item) => {
    console.log(item);
    mouse.to(item, {
      color: "red",
      ease: "none",
    });
  });
};
</script>

<template>
  <div class="home">
    <div class="home-about">
      <div class="home-about-title">
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequuntur,
          asperiores?
        </p>
      </div>
      <div class="home-about-image">
        <img
          src="https://images.pexels.com/photos/90333/pexels-photo-90333.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1"
          alt=""
        />
      </div>
    </div>
    <div class="home-service">
      <div class="home-service-title">
        <h3>Services:</h3>
      </div>
      <div class="home-service-list">
        <div
          v-for="(index, i) in 3"
          :key="i"
          ref="refItem"
          @mouseenter="mouseEnter(i)"
          class="--item"
        >
          <div class="--item-data">
            <span>19 April 2022 {{ index }}</span>
          </div>
          <div class="--item-title">
            <h3>
              Lorem ipsum dolor sit amet consectetur adipisicing elit.
              Repellendus nobis commodi tenetur dolores sapiente eum, iure rerum
              ut nesciunt ducimus.
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
            <h3>name</h3>
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
    @media (max-width: 820px)
        margin-top: 20px
    &-about
        width: 65%
        margin-left: var(--auto)
        @media (max-width: 1200px)
            width: 87.5%
        @media (max-width: 820px)
            width: 100%
        @media (max-width: 480px)
            margin-left: unset
            width: 100%
        &-title
            max-width: 60%
            @media (max-width: 1200px)
                max-width: 100%
            @media (max-width: 820px)
                max-width: 100%
            p
                font-size: 38px
                @media (max-width: 1200px)
                    font-size: 28px
                @media (max-width: 820px)
                    font-size: 18px
        &-image
            margin-top: calc( var(--space-top) * 2 )
            width: 100%
            height: 600px
            @media (max-width: 1200px)
                height: var(--auto)
            @media (max-width: 820px)
                height: var(--auto)
            @media (max-width: 480px)
                margin-top: var(--space-top)
                height: 300px
            img
                width: var(--width)
                height: var(--height)
    &-service
        margin-top: calc( var(--space-top) * 4 )
        width: 65%
        margin-left: var(--auto)
        @media (max-width: 1200px)
            width: 87.5%
        @media (max-width: 820px)
            width: 100%
        @media (max-width: 480px)
            width: 100%
            margin-top: calc( var(--space-top) * 2 )
        &-title
            h3
                font-size: 38px
                font-weight: 400
                @media (max-width: 820px)
                    font-size: 22px
                    font-weight: bold
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
                @media (max-width: 820px)
                    grid-template-columns: 1fr
                    padding: 20px 0 20px
                &-data
                    span
                        font-size: 14px
                        @media (max-width: 820px)
                            font-size: 18px
                &-title
                    h3
                        font-size: 28px
                        font-weight: 300
                        @media (max-width: 820px)
                            font-size: 18px
    &-works
        margin-top: calc( var(--space-top) * 4 )
        width: 65%
        margin-left: var(--auto)
        @media (max-width: 1200px)
            width: 87.5%
        @media (max-width: 820px)
            width: 100%
        @media (max-width: 480px)
            width: 100%
            margin-top: calc( var(--space-top) * 2 )

        &-title
            h3
                font-size: 38px
                font-weight: 400
                @media (max-width: 820px)
                    font-size: 22px
                    font-weight: bold
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
                @media (max-width: 820px)
                    grid-template-columns: unset
                    display: flex
                    justify-content: space-between
                    align-items: center
                    padding: 20px 0 20px
                &-data
                    span
                        font-size: 14px
                        @media (max-width: 820px)
                            font-size: 18px
                &-title
                    text-align: right
                    @media (max-width: 820px)
                        text-align: left
                    h3
                        font-size: 28px
                        font-weight: 300
                        @media (max-width: 820px)
                            font-size: 18px
</style>
