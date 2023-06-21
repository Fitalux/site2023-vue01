<template>
  <section id="introSection" :class="attr">
    <h3 class="blind">추천 음악 소개</h3>
    <div class="intro__inner container">
      <div class="intro__title">
        <span>Recommend Music</span>
        <h3 v-html="title"></h3>
        <p v-html="desc"></p>
      </div>
      <div class="intro__desc">
        <div v-for="(text, index) in texts" :key="index">
          <h4 :class="'icon-bg' + (index + 1)">{{ text.title }}</h4>
          <p>{{ text.desc }}</p>
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
  data: function () {
    return {
      title: "아 진짜 뭐 듣지?",
      desc: "일상의 한 부분을 채워줄<br /> 지극히 주관적인 취향의 음악 장르 추천",
      texts: [
        {
          title: "JAZZ",
          desc: "차분하고 부드러운 음향과 길고 선형적인 멜로디를 가진 음악이 많아 독서, 공부, 명상, 작업 등 집중력이 필요하고, 안락한 분위기를 느끼고 싶을 때 듣기 좋습니다.",
        },
        {
          title: "EDM",
          desc: "클럽이나 페스티벌 같은 상업적인 파티 문화에서 쓰이는 전자 음악들을 통칭하는 단어로, 즐겁고 신나는 분위기를 느끼고 싶을 때 듣기  좋습니다.",
        },
        {
          title: "POP SONG",
          desc: "대중적인 음악이라는 뜻으로, 다양한 장르를 통칭합니다. 영미권 대중음악이라는 뜻도 있죠. 장르를 아우르기 때문에 분위기에 따라 골라듣기 좋습니다.",
        },
        {
          title: "OST",
          desc: "오리지널 사운드트랙(Original SoundTrack)'의 약자로, 해당 작품을 위해 새로 작곡된 음악을 뜻합니다. 몇 번이고 다시 보게 되는 작품을 떠올리게 합니다.",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
.intro__inner {
  display: flex;
  justify-content: space-between;
}
.intro__title {
  width: 33%;

  span {
    background-color: #ff3344;
    font-size: 14px;
    padding: 4px 30px 2px;
    color: #fff;
    border-radius: 40px;
    text-transform: uppercase;
    margin-bottom: 10px;
    display: inline-block;
  }

  h3 {
    font-size: 50px;
    font-weight: 700;
    line-height: 1.2;
    margin-bottom: 30px;
  }

  p {
    font-size: 18px;
    line-height: 1.5;
    font-weight: 500;
  }
}

.intro__desc {
  width: 66%;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;

  > div {
    width: 48%;
    margin-bottom: 40px;

    h4 {
      font-size: 24px;
      margin-bottom: 15px;
    }

    &:nth-child(3) {
      margin-bottom: 0;
    }

    &:nth-child(4) {
      margin-bottom: 0;
    }
  }
}
</style>
