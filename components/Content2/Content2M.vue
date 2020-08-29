<template>
  <section
    id="content2-frame-sm"
    class="hidden-md-and-up hidden-xs-only information-frame-content2-sm"
  >
    <div class="content-frame">
      <div class="content-right-sm">
        <div class="content-sec02">
          <h1>
            {{ $t("content2Topic") }}
            <hr class="hr-content-sec02" />
          </h1>
          <ul>
            <li>
              <div style="margin-left: 2rem;">
                <span style="color: #0c1351;">{{ $t("graduated") }}</span>
                {{ $t("graduatedToppic") }}
              </div>
            </li>
            <li>
              <div style="margin-left: 2rem;">
                <span style="color: #0c1351;">{{ $t("skillsToppic") }}</span>
                | Javascript, Vue.js, CSS, HTML5, Nuxt.js, Node.js, MySQL,
                MongoDB, Mongoose, Git.
              </div>
            </li>
            <li>
              <div style="margin-left: 2rem;">
                <div style="margin: 1rem 0rem;color: #0c1351;">
                  Front-end Developer at Bookallaround Co., Ltd. |
                  {{ $t("bookaa.rangeWork") }}
                </div>
                {{ $t("bookaa.workExperienceContent") }}
              </div>
            </li>
            <li>
              <div style="margin-left: 2rem;">
                <div style="margin: 1rem 0rem;color: #0c1351;">
                  Full Stack Developer at The Existing Co., Ltd. |
                  {{ $t("existing.rangeWork") }}
                </div>
                <div>{{ $t("existing.workExperienceContent.one") }}</div>
                <div>{{ $t("existing.workExperienceContent.two") }}</div>
              </div>
            </li>
            <li>
              <div style="margin-left: 2rem;">
                <div style="margin: 1rem 0rem;color: #0c1351;">
                  Back-end Developer at Vonde Co., Ltd. |
                  {{ $t("vonder.rangeWork") }}
                </div>
                <div>{{ $t("vonder.workExperienceContent.one") }}</div>
                <div>{{ $t("vonder.workExperienceContent.two") }}</div>
              </div>
            </li>
          </ul>
          <div class="hr-under-content">
            <hr />
          </div>
        </div>
      </div>
      <div class="text-section">
        <hr />
        03.
      </div>
    </div>
  </section>
</template>

<script>
import $ from "jquery";

export default {
  mounted() {
    var contentFrame2 = $("#content2-frame-sm").offset().top;
    var footerFrame = $("#footer-frame-sm").offset().top;

    var getHeightOfHeader = $("#header-menu-sm").height();
    var getHeightOfContentFrame = $(".information-frame-content2-sm").height();
    $(".information-frame-content2-sm").css({
      height: getHeightOfContentFrame + getHeightOfHeader + "px",
      //   "padding-top": getHeightOfHeader + "px",
    });

    var $w = $(window).scroll(function(event) {
      if (
        $w.scrollTop() >= contentFrame2 - 400 &&
        $w.scrollTop() < footerFrame + 400
      ) {
        $(".content-right-sm").addClass("add-animation-sm");
        $(".content-right-sm").css({
          display: "flex",
        });
      }
    });
  },
};
</script>

<style scoped>
.add-animation-sm {
  animation: fadeIn 0.5s ease-out;
}

.information-frame-content2-sm {
  height: 125vh;
  display: flex;
  justify-content: center;
  font-size: 2.5rem;
  background-color: #ffff;
}

.content-frame {
  position: relative;
  height: 100%;
  width: 100%;
}

.content-right-sm {
  height: 63%;
  width: 100%;
  display: none;
  align-items: flex-end;
  justify-content: flex-start;
  padding-left: 4rem;
}

.content-sec02 {
  width: 100%;
  height: 100%;
}

.content-sec02 h1 {
  display: flex;
  align-items: center;
  color: #be4d08;
  letter-spacing: 3px;
  font-size: 1.6rem;
  margin-bottom: 10px;
}

.hr-content-sec02 {
  width: 9rem;
  margin-left: 2rem;
}

.content-sec02 h2 {
  color: #a9946e;
  letter-spacing: 2px;
  font-size: 1.3rem;
  line-height: 1.1em;
}

.content-sec02 h3 {
  color: #0c1351;
  text-align: justify;
  width: 59%;
  font-size: 0.8rem;
}

.content-sec02 ul {
  margin-left: 5rem;
  color: #a9946e;
  font-size: 1.3rem;
  line-height: 1.1em;
  font-weight: 700;
  width: 68%;
  text-align: justify;
}

.content-sec02 li {
  margin-top: 2rem;
  letter-spacing: 1.2px;
}

.hr-under-content {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-left: 5rem;
  width: 68%;
  margin-top: 1rem;
}

.hr-under-content hr {
  width: 4rem;
  border: 2px solid #a9946e;
}

.text-section {
  position: absolute;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  bottom: 10%;
  right: 19%;
  height: 4rem;
  font-size: 1rem;
  font-weight: 700;
}

.text-section hr {
  transform: rotate(90deg);
  width: 4rem;
  border: 2px solid #a9946e;
}

@keyframes fadeIn {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
</style>
