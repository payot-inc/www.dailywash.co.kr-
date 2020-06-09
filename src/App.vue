<template>
  <v-app>
    <div class="wrap">
      <div ref="header" class="header" :class="{ ['scroll-header']: lightHeader }">
        <div class="inner">
          <div class="logo">
            <img src="@/assets/img/logo_icon.png">
            <span>데일리세탁</span>
          </div>
          <div class="nav">
            <v-btn text>Home</v-btn>
            <v-btn text href="#intro">데일리세탁</v-btn>
            <v-btn text href="#intro">이용가능지역</v-btn>
            <v-btn text href="#intro">자주묻는질문</v-btn>
            <v-btn text href="#intro">새로운 소식</v-btn>
          </div>
        </div>
      </div>
      <div class="contents">
        <div class="visual">
          <iframe 
            class="visual-video" 
            src="https://www.youtube.com/embed/Df2WyqQxidU?mute=0&autoplay=1&loop=1&playlist=Df2WyqQxidU&rel=0&controls=0&showinfo=0" 
            frameborder="0" 
            allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" 
            allowfullscreen
          >
          </iframe>

          <div class="visual-title">
            <span class="text1">Daily Wash</span>
            <span class="text2">가장 간편한 세탁서비스, <strong>데일리세탁</strong></span>
            <span class="text3">바쁜 현대인을 위한 세탁대행 서비스</span>
          </div>

          <div class="visual-filter" />
        </div>

        <div class="section01" id="intro">
          <div class="inner">
            <label></label>
            <img src="@/assets/img/logo_icon.png" class="icon">
            <span class="text1">세탁은 언제나 <strong>간편하게</strong></span>
            <span class="text2">바쁜 현대인들을 위한 세탁대행 서비스</span>
            <span class="text2">일반생활빨래에서 부터 드라이클리닝 까지!</span>
            <span class="text2">바쁜 일상속에 작은 여유를 찾아보세요</span>
            <img src="@/assets/img/slide-01.png" class="image">
          </div>
        </div>

        <div class="section02">
          <div class="inner">
            <v-row>
              <v-col cols="4">
                <div class="section-title">
                  <span class="text1">집에서 간편하게 수거배달을 <strong>예약하세요</strong></span>
                  <span class="text2">간편하게 터치 한번으로 빨래 없는 일상을 만날 수 있습니다 </span>
                  <div class="store">
                    <dl class="app-store">
                      <dt v-ripple>
                        <img src="@/assets/img/app.jpg">
                      </dt>
                      <dd>App Stroe</dd>
                    </dl>
                    <dl class="play-store">
                      <dt v-ripple>
                        <img src="@/assets/img/google.jpg">
                      </dt>
                      <dd>Google Play</dd>
                    </dl>
                  </div>
                </div>
              </v-col>
              <v-col cols="8">
                <div class="smart">
                  <img src="@/assets/img/phone.png">
                </div>
              </v-col>
            </v-row>
          </div>
        </div>

        <div class="section03">
          <div class="inner">
            <div class="section-title">
              <span class="text1"><strong>데일리세탁</strong> 이렇게 이용해보세요?</span>
              <span class="text2">모바일로 간편하게 빨래 없는 일상을 경험해 보세요</span>
            </div>
            <div class="section-cont">
              <v-row>
                <v-col cols="4">
                  <dl>
                    <dt>
                      <img src="@/assets/img/how01.png">
                    </dt>
                    <dd>
                      <label>1</label>
                      <span>데일리세탁 어플레케이션을 통해 원하는 세탁상품을 선택후 예약완료</span>
                    </dd>
                  </dl>
                </v-col>
                <v-col cols="4">
                  <dl>
                    <dt>
                      <img src="@/assets/img/how02.png">
                    </dt>
                    <dd>
                      <label>2</label>
                      <span>예약된 시간에 맞춰 기사가 방문하여 세탁물을 수거</span>
                    </dd>
                  </dl>
                </v-col>
                <v-col cols="4">
                  <dl>
                    <dt>
                      <img src="@/assets/img/how03.png">
                    </dt>
                    <dd>
                      <label>3</label>
                      <span>세탁이 완료된 세탁물은 예쁘게 패키징되어 고객님의 집으로 배달</span>
                    </dd>
                  </dl>
                </v-col>
              </v-row>
            </div> <!-- section-cont -->

            <div class="search-area">
              <div class="inBox">
                <label>
                  <v-icon>mdi-map-marker</v-icon>
                  <span>수거배달 가능지역 <strong>확인하기</strong></span>
                </label>
                <input type="text" placeholder="검색어를 입력해주세요" />
                <v-btn text>
                  <v-icon>mdi-magnify</v-icon>
                </v-btn>
              </div>
            </div>
          </div>
        </div> <!-- section03 -->

        <div class="section04">
          <div class="inner">
            <h4>자주묻는 질문</h4>
            <v-expansion-panels flat accordion>
              <v-expansion-panel
                v-for="(item,i) in 5"
                :key="i"
              >
                <v-expansion-panel-header>
                  <span>
                    <label>Q</label>현재 수거배달 가능한 지역은 어디인가요?
                  </span>
                </v-expansion-panel-header>
                <v-expansion-panel-content>
                  현재 리화이트는 서울, 경기 수도권 및 부산, 강원, 인천, 광주, 충북, 충남 등 일부지역에서 사용가능합니다. 현재 서비스 지역이 아니라면, 앱에서 '알림'을 신청해주세요!
                </v-expansion-panel-content>
              </v-expansion-panel>
            </v-expansion-panels>
          </div>
        </div>

        <div class="section05">
          <div class="inner">
            <div class="notice">
              <div class="section-title">
                <h4>데일리세탁</h4>
                <h4><strong>새로운 소식</strong></h4>
                <v-btn outlined>더 보기</v-btn>
              </div>
              <ul>
                <li v-ripple>
                  <span class="date">2020.06.09</span>
                  <span class="text">데일리세탁은 오픈준비중입니다</span>
                </li>
                <li v-ripple>
                  <span class="date">2020.06.08</span>
                  <span class="text">게시판 테스트</span>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div> <!-- contents -->

      <div class="footer">
        <div class="logo">
          <img src="@/assets/img/logo_b.png">
        </div>
        <span>(주)페이오티 | 서비스명: 데일리세탁 | 대표: 차경진 | 사업자등록번호: 599-81-00659 |  주소: 부산광역시 금정구 부산대학로 63번길 2 과학기술연구동 201호 </span>
        <span>이메일: cs@dailywash.co.kr | 전화: 070-7807-6857 | FAX: 0504-433-6857</span>
      </div>
    </div>
  </v-app>
</template>

<script>

export default {
  name: "App",

  components: {
    
  },

  data: () => ({
    //
    lightHeader: false,
  }),

  mounted() {
    const self = this;
    const headerHeight = document.getElementsByClassName('visual')[0].clientHeight;
    document.addEventListener('scroll', () => {
      const nowScrollPosition = window.scrollY || document.documentElement.scrollTop;
      self.lightHeader = nowScrollPosition > headerHeight - 70 ;
    });
  }
};
</script>

<style lang="scss" scoped>

.header{
  position: fixed;
  width:100%;
  display:flex;
  align-items: center;
  justify-content: center;
  border-bottom:1px solid rgba(255,255,255,0.2);
  align-items: center;
  padding:0 30px;
  height:70px;
  top:0px;
  left:0px;
  z-index:3;

  .inner{
    display:flex;
    flex-direction:row;
    justify-content:space-between;
  }
  

  .logo{
    display:flex;
    align-items: center;
    img{height:34px}
    span{font-size:24px;margin-left:15px;color:#fff;}
  }

  .nav{
    .v-btn{
      color:#fff;
      font-size:15px;
      font-weight:300;
      margin-left:10px;
    }
  }
}

.scroll-header{
    background:#fff;
    border-bottom:1px solid #e2e2e2;
    .logo{
      span{color:#292929;}
    }
    .nav{
      .v-btn{
        color:#494949;
        font-weight:500
      }
    }
}

.inner{
  width:1200px;
  margin:0px auto;
  display:flex;
  flex-direction: column;;
  justify-content: center;
  align-items: center;
}

.section01{
  display:flex;
  justify-content: center;
  align-items: center;
  padding:100px 0;
  min-height:600px;

  label{display:block;width:2px;;height:40px;background:#c2c2c2;}
  img.icon{height:60px;margin:30px 0}
  img.image{height:400px;}
  span{
    display:block;
    text-align: center;
  }

  span.text1{font-size:36px;margin-bottom:15px;}
  span.text2{font-size:16px;color:#888;margin-bottom:5px;}

}

.section02{
  display:flex;
  justify-content: center;
  height:750px;
  background:#01a1dd url('./assets/img/section02-bg.jpg') no-repeat center / 100%;
  background-attachment: fixed;

  .row{padding:0px;margin:0px;}
  .col{padding:0px;}


  .store{
    margin-top:50px;
    display:flex;
    dl{
      display:flex;
      flex-direction: column;
      flex:1;
      text-align:center;

      dt{
        width:100%;
        height:100px;
        background:#fff;
        border-radius:5px;
        padding:10px;
        overflow: hidden;
        img{height:100%;}
      }
      dd{color:#fff;margin-top:15px;}
    }
    dl.app-store{margin-right:10px;}
    dl.play-store{margin-left:10px;}
  }

  .section-title{
    display:flex;
    flex-direction: column;
    justify-content: center;
    height:100%;

    span{display:block;color:#fff}
    span.text1{
      font-size:36px;line-height:44px;font-weight:400;
      word-break: keep-all;
      strong{font-weight:600;}
    }
    span.text2{
      font-size:16px;
      margin-top:20px;
      word-break: keep-all;
      color:rgba(255,255,255,0.8)
    }
  }
  
  .smart{
    height:100%;
    display:flex;
    align-items: flex-end;
    justify-content: flex-end;
    img{height:635px;}
  }

}

.section03{
  display:flex;
  justify-content: center;
  align-items: center;
  padding:100px 0;

  .section-title{
    width:100%;
    display:flex;
    justify-content: flex-start;
    flex-direction: column;
    margin-bottom:50px;

    span{
      display:block;
    }
    span.text1{
      font-size:36px;
      strong{font-weight:600}
    }
    span.text2{font-size:16px;margin-top:10px;color:#888}
  }

  .section-cont{
    width:100%;

    .row{padding:0px;}
    .col{padding:0px;}

    dl{
      display:flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;;

      dt{
        display:flex;
        align-items: flex-end;
        text-align: center;
        justify-content: center;
        min-height:260px;

        img{width:260px;}
      }
      dd{
        display:flex;
        width:280px;
        margin-top:50px;
        

        label{
          display:Flex;
          justify-content: center;
          align-items: center;
          width:40px;
          height:40px;
          border-radius:20px;
          margin-right:15px;
          background:#01a1dd;
          color:#fff;
          font-weight:500;
        }
        span{
          flex:1;
          word-break: keep-all;
          font-weight:400;
          font-size:14px;
          color:#888;
        }
      }
    }
  }

  .search-area{
    width:100%;
    border:1px solid #e2e2e2;
    height:80px;
    margin-top:140px;
    box-shadow: 5px 5px 15px rgba(0,0,0,0.05);

    .inBox{
      width:100%;
      display:flex;
      align-items: center;
      padding-left:20px;

      label{
        display:flex;
        flex-direction: row;
        align-items: center;
        border-right:1px solid #e2e2e2;
        padding-right:20px;
        color:#01a1dd;

        .v-icon{font-size:32px;color:#01a1dd}
        span{
          font-size:24px;
          strong{color:#494949;}
        }
      }

      input{
        flex:1;
        outline: none;
        height:80px;
        padding:0 20px;
      }

      .v-btn{
        min-width:80px;
        height:80px;
        border-radius:0px;
        border-left:1px solid #e2e2e2;
        .v-icon{
          font-size:32px;
        }
      }
    }
  }
}

.section04{
  background: #eef4f6;
  padding:100px 0;

  .inner{
    align-items: flex-start;
  }

  h4{font-size:36px;text-align: left;font-weight:400;margin-bottom:40px;  }
  .theme--light.v-expansion-panels .v-expansion-panel{background:none;}
  .v-expansion-panel{border-bottom:1px solid #e2e2e2;}
  .v-expansion-panel-header{
    padding:0px;font-size:18px;height:60px;
    span{
      label{color:#01a1dd;margin-right:10px;}
    }
  }
  .v-expansion-panel-content{font-size:14px;color:#888;margin:0px;}
}

.section05{
  width:100%;
  min-height:800px;
  display:flex;
  flex-direction: column;
  background: url('./assets/img/notice-bg.png') no-repeat;
  background-position-y: center;
  background-position-x: 100%;
  padding:100px 0;

  .inner{
    align-items: flex-start;
    justify-content: flex-start;
  }

  .notice{
    flex:1;
    width:50%;
    height:100%;

    .section-title{
      h4{font-size:36px;font-weight:400;line-height:46px}
      .v-btn{height:30px;border:1px solid #e2e2e2;margin-top:20px;}
    }

    ul{
      list-style-type: none;
      padding:0px;
      margin-top:40px;
      width:320px;

      li{

        border-bottom:1px solid #e2e2e2;
        padding:20px 0;
        span.date{color:#01a1dd}
        span.text{margin-top:5px;}
        span{display:block;}
      }

    }
  }

  .row{padding:0;margin:0;}
  .col{padding:0;margin:0;}
}


.contents{
  padding:0px;
  
  .visual{
    display:flex;
    justify-content: center;
    align-items: center;
    height:800px;
    overflow:hidden;
    position: relative;


    .visual-video{
      width:100%;
      height:400%;
    }
    .visual-title{
      position:absolute;
      text-align:center;
      color:#fff;
      z-index:2;

      span{display:block;font-weight:400;}
      span.text1{letter-spacing: 20px;font-size:24px;color:#aaa}
      span.text2{
        font-size:42px;
        margin:10px 0;
        strong{font-weight:600;}
      }
      span.text3{font-size:24px;color:#aaa}
  }
    .visual-filter{
      position:absolute;
      width:100%;
      height:100%;
      background:rgba(0,0,0,0.6);
      background-image: url('./assets/img/visual-bg.png');
      z-index:1;
    }
  }
}

.footer{
  border-top:1px solid #e2e2e2;
  text-align: center;
  padding:50px 0 100px 0;
  
  .logo{
    margin-bottom:20px;
    img{height:50px;}
  }

  span{
    font-size:12px;
    display:block;
    color:#888;
    margin-bottom:5px;
  } 
}

</style>