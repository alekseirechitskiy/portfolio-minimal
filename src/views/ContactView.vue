<template>
  <div class="contact">
    <h1 class="contact__title title">Contact</h1>
    <p class="contact__text text">Let’s Chat!</p>
    <form class="contact__form form" action="#">
      <label class="form__input-box">
        <p class="form__input-text">Name</p>
        <input class="form__input-field" type="text" placeholder="Enter your name" required>
      </label>
      <label class="form__input-box">
        <p class="form__input-text">Email</p>
        <input class="form__input-field" type="email" placeholder="Enter your email" required>
      </label>
      <label class="form__input-box">
        <p class="form__input-text">Message</p>
        <textarea class="form__textarea-field" placeholder="Anything I can help? Let me know" required></textarea>
      </label>
      <button class="form__button button">Send</button>
    </form>
  </div>
</template>

<style lang="scss">
  .contact {
    width: 100%;
    padding: 15px;
    text-align: left;

    @media #{$screen-1024} {
      padding: 24px;
      padding-top: 130px;
      height: auto;
    }
  }

  .contact__title {
    margin: 0;
  }

  .contact__text {
    margin-bottom: 60px;
    font-family: 'Space Grotesk', Arial, sans-serif;
  }

  .form {
    font-family: 'Space Grotesk', Arial, sans-serif;
    max-width: 580px;

    .form__input-box {
      display: block;
      margin-bottom: 24px;
    }

    .form__input-text {
      font-family: 'Space Grotesk', Arial, sans-serif;
      font-weight: 500;
      font-size: 18px;
      line-height: 23px;
      letter-spacing: -0.25px;
      color: var(--title-color);
      margin: 0;
      position: relative;

      &::after {
        position: absolute;
        content: "*";
        color: var(--required-field-mark);
      }
    }

    .form__input-field,
    .form__textarea-field {
      box-sizing: border-box;
      display: block;
      border: 1px solid transparent;
      background-color: var(--input-field-bg);
      padding: 16px;
      outline: none;
      width: 100%;
      font-family: inherit;
      font-weight: 400;
      font-size: 18px;
      line-height: 23px;
      letter-spacing: -0.25px;

      &::placeholder {
        color: #9D9690;
      }

      &:focus {
        border: 1px solid #D3902A;
      }
    }

    .form__textarea-field {
      height: 240px;
      resize: none;
    }

    .form__button {
      width: 164px;
      height: 55px;
      outline: none;
      border: 2px solid var(--bg-color);
      color: var(--bg-color);
      background-color: var(--title-color);


      &:focus{
        border: 2px solid #D3902A;
        color: #D3902A;
      }
    }
  }

  .button {
    font-family: 'Space Grotesk';
    font-style: normal;
    font-weight: 400;
    font-size: 18px;
    line-height: 23px;
    letter-spacing: -0.25px;
    color: #F8F4F0;
    background-color: #000201;
    border: none;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
  }
</style>
