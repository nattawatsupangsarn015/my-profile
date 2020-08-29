<template>
  <section
    id="sub-content-mobile"
    class="hidden-sm-and-up information-frame-content2-xs"
  >
    <div class="content-frame">
      <div class="content-right-xs">
        <div class="content-sec02">
          <h1 style="text-align: end;">
            {{ $t("content2Topic") }}
            <hr class="hr-content-sec02" />
          </h1>
          <ul>
            <li>
              <div style="margin-left: 1rem;">
                <span style="color: #0c1351;">{{ $t("graduated") }}</span>
                {{ $t("graduatedToppic") }}
              </div>
            </li>
            <li>
              <div style="margin-left: 1rem;">
                <span style="color: #0c1351;">{{ $t("skillsToppic") }}</span>
                | Javascript, Vue.js, CSS, HTML5, Nuxt.js, Node.js, MySQL,
                MongoDB, Mongoose, Git.
              </div>
            </li>
            <li>
              <div style="margin-left: 1rem;">
                <div style="margin: 1rem 0rem;color: #0c1351;">
                  Front-end Developer at Bookallaround Co., Ltd. |
                  {{ $t("bookaa.rangeWork") }}
                </div>
                <div>{{ $t("bookaa.workExperienceContent") }}</div>
              </div>
            </li>
            <li>
              <div style="margin-left: 1rem;">
                <div style="margin: 1rem 0rem;color: #0c1351;">
                  Full Stack Developer at The Existing Co., Ltd. |
                  {{ $t("existing.rangeWork") }}
                </div>
                <div>{{ $t("existing.workExperienceContent.one") }}</div>
                <div>{{ $t("existing.workExperienceContent.two") }}</div>
              </div>
            </li>
            <li>
              <div style="margin-left: 1rem;">
                <div style="margin: 1rem 0rem;color: ##0c1351;">
                  Back-end Developer at Vonder Co., Ltd. |
                  {{ $t("vonder.rangeWork") }}
                </div>
                <div>{{ $t("vonder.workExperienceContent.one") }}</div>
                <div>{{ $t("vonder.workExperienceContent.one") }}</div>
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
    var contentFrame2 = $("#sub-content-mobile").offset().top;
    var footerFrame = $("#footer-frame-xs").offset().top;

    var getHeightOfHeader = $("#header-menu-xs").height();
    var getHeightOfContentFrame = $(".information-frame-content2-xs").height();
    $(".information-frame-content2-xs").css({
      height: getHeightOfContentFrame + getHeightOfHeader + "px",
      "padding-top": getHeightOfHeader + "px",
    });

    var $w = $(window).scroll(function(event) {
      if (
        $w.scrollTop() >= contentFrame2 - 400 &&
        $w.scrollTop() < footerFrame + 400
      ) {
        $(".content-right-xs").addClass("add-animation-xs");
        $(".content-right-xs").css({
          display: "flex",
        });
      }
    });
  },
};
</script>

<style scoped>
.add-animation-xs {
  animation: fadeIn 0.5s ease-out;
}

.information-frame-content2-xs {
  height: 100vh;
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

.content-right-xs {
  height: 63%;
  width: 100%;
  display: none;
  align-items: flex-end;
  justify-content: flex-end;
}

.content-sec02 {
  padding: 2rem;
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
  text-align: end;
}

.hr-content-sec02 {
  position: absolute;
  width: 6rem;
  right: 3rem;
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
  color: #a9946e;
  font-size: 12px;
  line-height: 1.1em;
  font-weight: 700;
  width: 90%;
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
  width: 60%;
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
  /*  */
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
