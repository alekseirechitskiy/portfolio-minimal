<template>
  <div class="resume">
    <h1 class="resume__title title">Resume</h1>
    <p class="resume__text text">A summary of my education, work history, credentials, and other accomplishments and skills</p>
    <ul class="resume__list">
      <li class="resume__item">
        <span class="resume__years">2015-2016</span>
        <div class="resume__description">
          <h3 class="resume__description-title">IT Staff and Operations</h3>
          <h4 class="resume__description-subtitle">Burdeyn Hospital</h4>
          <ul class="resume__description-list">
            <li class="resume__description-list-item">Maintain the hospital network with CISCO-standards</li>
            <li class="resume__description-list-item">Mikrotik configurations on routers</li>
            <li class="resume__description-list-item">Troubleshoot the employeer’s computers</li>
          </ul>
        </div>
      </li>
      <li class="resume__item">
        <span class="resume__years">2016-2018</span>
        <div class="resume__description">
          <h3 class="resume__description-title">WordPress Developer</h3>
          <h4 class="resume__description-subtitle">Fortunel Studio</h4>
          <ul class="resume__description-list">
            <li class="resume__description-list-item">Create a SEO Plugin based on PHP 7.2</li>
            <li class="resume__description-list-item">Maintain clients website</li>
            <li class="resume__description-list-item">Build and deploy for client area services</li>
          </ul>
        </div>
      </li>
      <li class="resume__item">
        <span class="resume__years">2018-2020</span>
        <div class="resume__description">
          <h3 class="resume__description-title">UI Designer</h3>
          <h4 class="resume__description-subtitle">Matic Job Ltd.</h4>
          <ul class="resume__description-list">
            <li class="resume__description-list-item">Brainstorming ideas to design</li>
            <li class="resume__description-list-item">Create wireframe and design systems</li>
            <li class="resume__description-list-item">Create micro-interactions with Figma</li>
            <li class="resume__description-list-item">Create hand-off documents</li>
            <li class="resume__description-list-item">Redesign old website with minimalism style</li>
          </ul>
        </div>
      </li>
      <li class="resume__item">
        <span class="resume__years">2020-present</span>
        <div class="resume__description">
          <h3 class="resume__description-title">Senior Product Designer</h3>
          <h4 class="resume__description-subtitle">Kali Network Ltd.</h4>
          <ul class="resume__description-list">
            <li class="resume__description-list-item">Manage company PDM management system</li>
            <li class="resume__description-list-item">Design & rout HVAC ductwork using REVIT</li>
            <li class="resume__description-list-item">Create working prototypes for new concept designs</li>
            <li class="resume__description-list-item">Collaborate closely with developers, copywriters and UX designers</li>
            <li class="resume__description-list-item">Research on new design trends</li>
          </ul>
        </div>
      </li>
    </ul>
  </div>
</template>

<style lang="scss">
  .resume {
    width: 100%;
    padding: 15px;
    padding-bottom: 40px;
    text-align: left;
    font-family: 'Space Grotesk', Helvetica, Arial, sans-serif;
    
    @media #{$desktop}{
      padding: 24px;
      padding-top: 130px;
      // margin-left: 22%;
    }
  }

  .resume__title {
    font-family: Archivo, Helvetica, Arial, sans-serif;
    margin: 0;
    margin-bottom: 16px;
    font-weight: 900;
    font-size: 48px;
    line-height: 117%;
    letter-spacing: -0.8px;
    color: var(--title-color);
  }

  .resume__text {
    font-weight: 400;
    font-size: 24px;
    line-height: 150%;
    letter-spacing: -0.25px;
    max-width: 676px;
    margin: 0;
    margin-bottom: 40px;
    color: var(--text-color);

    & strong {
      color: var(--title-color);
    }
  }

  .resume__list {
    margin: 0;
    padding: 0;
    list-style: none;
  }

  .resume__item {
    display: flex;
    flex-direction: column;
    margin-bottom: 24px;
    
    @media #{$desktop}{
      flex-direction: row;
    }

    &:last-child {
      margin-bottom: 0;
    }
  }

  .resume__years {
    margin-bottom: 10px;
    width: 180px;
    font-weight: 600;
    font-size: 20px;
    line-height: 26px;
    color: var(--title-color);
    @media #{$desktop}{
      margin-bottom: 0;
    }
  }

  .resume__description-title {
    margin: 0;
    margin-bottom: 4px;
    font-weight: 600;
    font-size: 16px;
    line-height: 20px;
    letter-spacing: -0.25px;
    color: var(--title-color);
  }

  .resume__description-subtitle {
    margin: 0;
    margin-bottom: 16px;
    font-weight: 500;
    font-size: 14px;
    line-height: 18px;
    letter-spacing: -0.25px;
    color: var(--text-color);
  }

  .resume__description-list {
    list-style-type: disc;
    margin: 0;
    padding-left: 25px;
  }

  .resume__description-list-item {
    font-weight: 500;
    font-size: 14px;
    line-height: 157%;
    letter-spacing: -0.25px;
    color: var(--text-color);
  }
</style>
