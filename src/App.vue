<script setup lang="ts"></script>

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
        <p>Ever been in a room and felt like something was missing? Perhaps it felt slightly bare and uninviting. I've got some simple tips to help you make any room feel complete.</p>
      </section>

      <section id="profile">
        <div class="article__profile">
          <img src="images/avatar-michelle.jpg" alt="avatar-michelle">
          <div class="about">
            <h3 class="name">Michelle Appleton</h3>
            <p>28 Jun 2020</p>
          </div>
          <div class="share-icon">
            <img src="images/icon-share.svg" alt="a share icon">
          </div>
        </div>
      </section>
    </div>
  </article>
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
  }

  .article {
    background-color: white;
    border-radius: 1rem;
    overflow: hidden;
    max-width: 375px;
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
 
</style>
