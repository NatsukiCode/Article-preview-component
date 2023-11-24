<script setup lang="ts">
import { Ref, ref } from 'vue';
const showTooltip: Ref<boolean> = ref(false);
const toggleTooltip = () => {
showTooltip.value = !showTooltip.value;
};
</script>

<template>
  <main>
    <article class="article">
      <div id="mainimage">
        <img src="images/drawers.jpg" alt="A green drawer">
      </div>

      <div class="article__content">
        <section id="headline" >
          <h2 class="article__headline">Shift the overall look and feel by adding these wonderful touches to furniture in your home</h2>
        </section>

        <section id="maintext" >
          <p>Ever been in a room and felt like something was missing? Perhaps it felt slightly bare and uninviting. I've got some simple tips to help you make any room feel complete</p>
        </section>

        <section id="profile">
          <div class="article__profile">
            <img src="images/avatar-michelle.jpg" alt="avatar-michelle">
            <div class="about">
              <h3 class="name">Michelle Appleton</h3>
              <p>28 Jun 2020</p>
            </div>
            <div class="share-icon" @click="toggleTooltip">
              <img src="images/icon-share.svg" alt="a share icon">
             </div>
          </div>
        </section>
      </div>
    </article>
    <div class="share-tooltip" v-if="showTooltip" @click="toggleTooltip">
      <div class="share">
        <p>share</p>
      </div>
      <div class="sns-icons" > 
        <img src="images/icon-facebook.svg" alt="facebook icon">
        <img src="images/icon-twitter.svg" alt="twitter icon">
        <img src="images/icon-pinterest.svg" alt="pinterest icon">
      </div>
      <div class="share-icon">
        <img src="images/icon-share.svg" alt="a share icon">
      </div>
    </div>
  </main>
</template>


<style>
  @import url('https://fonts.googleapis.com/css2?family=Manrope:wght@500;700&display=swap');

  :root {
    --clr-veryDarkGrayishBlue: hsl(217, 19%, 35%);
    --clr-desaturatedDarkBlue: hsl(214, 17%, 51%);
    --clr-grayishBlue: hsl(212, 23%, 69%);
    --clr-lightGrayishBlue: hsl(210, 46%, 95%);

    --ff: 'Manrope', sans-serif;

    --fw-regular: 500;
    --fw-bold: 700;
  }

  main {
    font-family: var(--ff);
    font-weight: var(--fw-regular);
    color: var(--clr-desaturatedDarkBlue);
    font-size: 0.8rem;
    background-color: var(--clr-lightGrayishBlue);
    padding: 4.5rem 1.6rem;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 700px;
  }

  .article {
    background-color: white;
    border-radius: 0.8rem;
    overflow: hidden;
    max-width: 600px;
    display: grid;
  }

  .article__content {
    padding: 0 2.2rem;
  }

  #headline .article__headline {
    color: var(--clr-veryDarkGrayishBlue);
    font-weight: var(--fw-bold);
    font-size: 1rem;
    letter-spacing: 0.001rem;
    padding: 2.3rem 0 1rem 0;
  }

  #profile {
    margin: 1.8rem 0 1rem;
  }

  #profile .article__profile {
    display: flex;
    justify-content: space-between;
    box-sizing: border-box;
  }

  .article__profile img {
    border-radius: 50%;
    max-width: 40px;
  }

  #profile .about {
    margin-right: auto;
    margin-left: 0.5rem;
  }

  #profile .name {
    color: var(--clr-veryDarkGrayishBlue);
    font-size: 0.8rem;
  }

  .share-icon {
    background-color: var(--clr-lightGrayishBlue);
    border-radius: 50%;
    width: 30px;
    height: 30px;
    display: grid;
    place-content: center;
  }

/* For the desktop ver styling */
  @media(min-width: 600px) {
    .article {
      grid-template-columns: 1.5fr 2fr;
      overflow: visible;
    }

    #mainimage {
      background-image: url(images/drawers.jpg);
      background-size: cover;
      margin-right: 1.8rem;
      border-radius: 0.8rem 0 0 0.8rem;
    }

    #mainimage img {
      display: none;
    }

    .article__content {
      display: grid;
      padding: 1.3rem 1.3rem 1.3rem 0;
    }

    #headline .article__headline {
      padding: 0;
      font-size: 1.1rem;
    }

    #maintext {
      font-size: 0.6rem;
      line-height: 1rem;
      padding-top: 0.5rem;
    }

    #profile {
      margin: 0;
      padding-top: 1rem;
    }

    .article__profile img {
      max-width: 30px;
      max-height: 30px;
    }

    #profile .name, p {
      font-size: 0.7rem;
    }
    /* For the pop up bubble styling */
    .share-tooltip {  
      left: 61%;
      position: absolute;
      background: #1a62bc;
      border-radius: 0.8rem;
      /* left: 170%; */
      /* bottom: 200%; */
      overflow: visible;
    }

    .share-tooltip::before {
      content: "";
      position: absolute;
      top: 100%;
      border: 12px solid transparent;
      border-top: 10px solid var(--clr-veryDarkGrayishBlue);
    }

    .share-tooltip .share-icon {
      display: none;
    }
  }

  /* For the mobile active state styling. */
  @media(max-width: 375px) {
    .share-tooltip {
      position: absolute;
      width: 325px;
      border-radius: 0 0 10px 10px;
    }
  }

  .share-tooltip {
    display: flex;
    justify-content: center;
    background-color: var(--clr-veryDarkGrayishBlue);
    padding: 0.8rem;
    margin-top: 1.2rem;
  }

  .share {
    display: flex;
    align-items: center;
    text-transform: uppercase;
    letter-spacing: 0.5rem;
  }

  .sns-icons {
    display: flex;
    margin-top: 0.3rem;
    margin-left: 1rem;
    gap: 0.8rem;
    height: 1.3rem;
  }

  .share-tooltip .share-icon {
    background-color: var(--clr-desaturatedDarkBlue);
    margin-left: 2.3rem;
  }

  .share-tooltip .share-icon img {
    filter: invert(100%);
  }
  
</style>
