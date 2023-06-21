<template>
  <section id="imagesSection" :class="attr">
    <h3>Recommend Music Best 3</h3>
    <p>상황별로 꼭 권유하고 싶은 노래 TOP 3</p>
    <div class="images__inner container">
      <div class="image">
        <figure class="image__header">
          <img src="../../assets/images/img/image01.png" alt="drive" />
        </figure>
        <div class="image__body">
          <h4>
            Green Green Grass <br />
            George Ezra<br /><br />
          </h4>
          <p>
            -화창한 여름, 창문을 열고 시원한 바람을 만끽하며 드라이브 할 때<br />-실내지만
            드라이브 하는 기분을 내고 싶을 때
          </p>
          <a href="https://www.youtube.com/watch?v=VQeW62X8rEA" class="btn"
            ><br />Listen<br
          /></a>
        </div>
      </div>
      <div class="image">
        <figure class="image__header">
          <img src="../../assets/images/img/image02.png" alt="brunout" />
        </figure>
        <div class="image__body">
          <h4>
            Breathe In Breathe Out <br />
            Blanks<br /><br />
          </h4>
          <p>
            -현대인이라면 한 번쯤 겪는 번아웃을 이겨낼 때<br />-지치는 하루,
            훌쩍 여행을 떠나고 싶을 때
          </p>
          <a href="https://www.youtube.com/watch?v=UvaafKCTrvM" class="btn"
            ><br />Listen<br
          /></a>
        </div>
      </div>
      <div class="image">
        <figure class="image__header">
          <img src="../../assets/images/img/image03.png" alt="hopes" />
        </figure>
        <div class="image__body">
          <h4>
            High Hopes <br />
            Panic! At The Disco<br /><br />
          </h4>
          <p>
            포기하고 싶고, 지쳐서 넘어질 것 같지만 지금까지 걸어온 길을 생각하며
            마음을 다잡을 때<br />
          </p>
          <a href="https://www.youtube.com/watch?v=IPXIgEAGe4U" class="btn"
            ><br />Listen<br
          /></a>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    attr: String,
  },
};
</script>

<style lang="scss">
.images__inner {
  @include flex-between;

  .image {
    width: 32%;
    border: 2px solid var(--color_body);

    .image__header {
      margin-top: -20px;

      img {
        width: 100%;
        margin-top: 20px;
      }
    }
    .image__body {
      margin-top: -80px;
      padding: 15px 10px;
      background: #000;
      color: #fff;
      z-index: 100;
      position: relative;

      h4 {
        font-size: 23px;
      }

      p {
        font-size: 20px;
        word-break: keep-all;
      }

      a {
        color: #fff;
        line-height: 1.5;
        font-size: 18px;

        &:hover {
          text-decoration: underline;
          text-underline-position: under;
        }
      }
    }
  }
}
</style>
