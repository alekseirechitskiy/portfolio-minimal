<template>
  <div class="case-card">
    <a class="case-card__link" href="#">
      <div class="case-card__link-hover">
        <span class="case-card__link-text">view project</span>
      </div>
      <img class="case-card__image" :src="caseImage" :alt="caseImageDescription">
    </a>
  </div>
</template>

<script>
export default {
  name: "CaseCard",
  props: ["caseImage", "caseImageDescription"]
}
</script>

<style scope lang="scss">
.case-card {
  width: 100%;
  height: auto;
}

.case-card__image {
  width: 100%;
  object-fit: cover;
  object-position: center;
  vertical-align: bottom;
}

.case-card__link {
  display: block;
  // height: 358px;
  position: relative;
}

.case-card__link-hover {
  display: flex;
  align-items: center;
  justify-content: center;
  opacity: 0;
  position: absolute;
  content: "";
  left: 0;
  right: 0;
  top: 0;
  bottom: 0;
  background-color: rgba(0,0,0, 0.5);
  transition: opacity 0.3s;
}

.case-card__link:hover {
  .case-card__link-hover {
    opacity: 1;
  }
}

.case-card__link-text {
  font-family: 'Space Grotesk';
  font-weight: 500;
  font-size: 20px;
  line-height: 28px;
  letter-spacing: -0.25px;
  color: #FFFFFF;
  padding-left: 32px;
  position: relative;

  @media #{$screen-1024} {
    font-size: 24px;
    line-height: 31px;
  }

  &::before {
    position: absolute;
    content: "";
    width: 24px;
    height: 24px;
    top: 4px;
    left: 0;
    background-image: url('../assets/icons/view-project.svg');
  }
}
</style>