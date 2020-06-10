<template>
  <v-app>
    <div class="wrap" id="home">
      <div ref="header" class="header" :class="{ ['scroll-header']: lightHeader }">
        <div class="inner">
          <div class="logo">
            <img src="@/assets/img/logo_icon.png">
            <span>데일리세탁</span>
          </div>
          <div class="nav">
            <v-btn text href="#home">Home</v-btn>
            <v-btn text href="#intro">데일리세탁</v-btn>
            <v-btn text href="#how">이용방법</v-btn>
            <v-btn text href="#faq">자주묻는질문</v-btn>
            <v-btn text href="#customer">고객센터</v-btn>
          </div>
          <div class="nav-mobile">
            <v-btn text @click="$refs.navSide.sideOpen(true)">
              <v-icon >mdi-menu</v-icon>
            </v-btn>
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
              <v-col cols="12" md="4" sm="6" xs="12">
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
              <v-col cols="12" md="8" sm="6" xs="12">
                <div class="smart">
                  <img src="@/assets/img/phone.png">
                </div>
              </v-col>
            </v-row>
          </div>
        </div>

        <div class="section03" id="how">
          <div class="inner">
            <div class="section-title">
              <span class="text1"><strong>데일리세탁</strong> 이렇게 이용해보세요?</span>
              <span class="text2">모바일로 간편하게 빨래 없는 일상을 경험해 보세요</span>
            </div>
            <div class="section-cont">
              <v-row>
                <v-col cols="12" md="4" sm="6">
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
                <v-col cols="12" md="4" sm="6">
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
                <v-col cols="12" md="4" sm="6">
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
              <label>
                <v-icon>mdi-map-marker</v-icon>
                <span>수거배달 가능지역 <strong>확인하기</strong></span>
              </label>
              <div class="inBox">
                <input type="text" placeholder="검색어를 입력해주세요" />
                <v-btn text>
                  <v-icon>mdi-magnify</v-icon>
                </v-btn>
              </div>
            </div>
          </div>
        </div> <!-- section03 -->

        <div class="section04" id="faq">
          <div class="inner">
            <h4>자주묻는 질문</h4>
            <v-expansion-panels flat accordion>
              <v-expansion-panel
                v-for="item in qna" 
                :key="item"
              >
                <v-expansion-panel-header>
                  <span>
                    <label>Q</label>{{item.question}}
                  </span>
                </v-expansion-panel-header>
                <v-expansion-panel-content>
                  {{item.answer}}
                </v-expansion-panel-content>
              </v-expansion-panel>
            </v-expansion-panels>
          </div>
        </div>

        <div class="section05" id="customer">
          <div class="inner">
      
            <div class="section-title">
              <h4>데일리세탁에 대해</h4>
              <h4><strong>아직 궁금한 점이 남으셨나요?</strong></h4>
              <p>아래로 번호로 전화주시면 친절하게 안내드릴게요!</p>
            </div>
            <div class="section-cont">
              <strong>070-7807-6857</strong>
              <p>오전10시 ~ 오후 6시 / 공휴일 휴무</p>
            </div>
            <!-- <ul>
              <li v-ripple>
                <span class="date">2020.06.09</span>
                <span class="text">데일리세탁은 오픈준비중입니다</span>
              </li>
              <li v-ripple>
                <span class="date">2020.06.08</span>
                <span class="text">게시판 테스트</span>
              </li>
            </ul> -->
          </div>
       
        </div>
      </div> <!-- contents -->

      <div class="footer">
        <div class="logo">
          <img src="@/assets/img/logo_b.png">
        </div>
        <div class="btns">
          <v-btn text>데일리세탁 이용약관</v-btn>
          <v-btn text>개인정보 취급방침</v-btn>
        </div>
        <span>(주)페이오티 | 서비스명: 데일리세탁 | 대표: 차경진 | 사업자등록번호: 599-81-00659 |  주소: 부산광역시 금정구 부산대학로 63번길 2 과학기술연구동 201호 </span>
        <span>이메일: cs@dailywash.co.kr | 전화: 070-7807-6857 | FAX: 0504-433-6857</span>
      </div>
    </div>

    <NavSide ref="navSide"/>
  </v-app>
</template>

<script>
import NavSide from '@/components/nav-side.vue';

export default {
  name: "App",

  components: {
    NavSide
  },

  data: () => ({
    lightHeader: false,
    qna:[
      {
        question:'현재 수거배달 가능한 지역은 어디인가요?',
        answer:'현재 데일리세탁은 부산 일부지역에서 사용가능합니다. 현재 서비스 지역이 아니라면, 앱에서 알림을 신청해주세요!'
      },
      {
        question:'세탁가격은 어떻게 되나요?',
        answer:'앱을 통해 예약할때 상품의 가격을 확인 할 수 있습니다'
      },
      {
        question:'세탁요금 결제는 어떻게 하나요?',
        answer:'앱 사용시 결제할 카드를 등록해주시면 예약 주문시 등록된 카드로 자동결제됩니다.'
      },
      {
        question:'최소 주문금액은 얼마인가요?',
        answer:'세탁요금은 14,900원부터 서비스를 이용 하실 수 있습니다. 하나의 상품만 주문하여도 최소 14,900원이 결제되니 주의해주세요'
      },

    ]
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
    }
  }

  .nav-mobile{
    display:none;

    .v-btn{
      min-width:50px;
      border-color:#fff;

      .v-icon{color:#fff;}
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
    .nav-mobile{
      .v-btn{
        .v-icon{color:#494949}
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

      span{display:block;font-weight:400;word-break: keep-all;}
      span.text1{letter-spacing: 20px;font-size:24px;color:#aaa;}
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
  background:#01a1dd url('./assets/img/section02-bg.jpg') no-repeat center / 100%;
  background-attachment: fixed;

  .row{padding:0px;margin:0px;}
  .col-md-4{padding:0px;margin:0px;}
  .col-sm-6{padding:0px;}

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

  .store{
    margin-top:50px;
    display:flex;

    dl{
      display:flex;
      flex-direction: column;
      flex-basis:120px;
      text-align:center;

      dt{
        width:100%;
        height:70px;;
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
    display:flex;
    align-items: center;

    label{
        display:flex;
        flex-direction: row;
        align-items: center;
        border-right:1px solid #e2e2e2;
        color:#01a1dd;
        padding:0 20px;

        .v-icon{font-size:32px;color:#01a1dd}
        span{
          font-size:24px;
          strong{color:#494949;}
        }
      }

    .inBox{
      flex:1;
      display:flex;
      align-items: center;

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
  display:flex;
  min-height:600px;
  flex-direction: column;
  background: url('./assets/img/notice-bg.png') no-repeat right center;
  padding:100px 0;

  .inner{
    flex:1;
    align-items: flex-start;
    justify-content: center;
  }

    .section-title{
      h4{font-size:36px;font-weight:400;line-height:46px}
      p{margin-top:20px;color:#888;font-size:16px}
    }

    .section-cont{
      margin-top:40px;
      strong{font-size:36px;color:#01a1dd}
      p{color:#888}
    }



  .row{padding:0;margin:0;}
  .col{padding:0;margin:0;}
}




.footer{
  border-top:1px solid #e2e2e2;
  text-align: center;
  padding:50px 20px 100px 20px;;
  
  .logo{
    margin-bottom:20px;
    img{height:50px;}
  }

  .btns{
    margin-bottom:20px;
    .v-btn{
      height:30px;
      border:1px solid #e2e2e2;
      margin:0 5px;
      font-size:12px;
      font-weight:500;
      margin-bottom:10px;
    }
  }

  span{
    font-size:12px;
    display:block;
    color:#888;
    margin-bottom:5px;
  } 
}


@media screen and(max-width:1200px){
  .header{
    padding:0px;
    .logo{padding-left:20px;}
    .nav{display:none}
    .nav-mobile{
      display:block;

      .v-btn{
        min-width:70px;
        height:70px;
        padding:0px;margin:0px;
      }
    }
    .inner{padding:0px}
  }
  .inner{
    width:100%;
    padding:0 20px;
  }

  .contents{
    .visual{
      background:url('./assets/img/visual-bg.jpg') no-repeat right center;

      iframe{display:none;}
    }
  }

  .section01{
    span.text1{font-size:32px;line-height:42px;}
  }

  .section02{
    .smart{
      img{width:100%;height:auto;}
    }
    .section-title{
      padding:70px 0;
      span.text1{font-size:32px;line-height:42px;}
    }
    .store{margin-top:20px;}
  }

  .section03{
    .section-title{
      span.text1{
        font-size:32px;line-height:42px;
        word-break: keep-all;
      }
    }
    .section-cont{
      dl{
        margin-bottom:50px;
        dt{
          flex:1;
          min-height:200px;
          img{width:100%;}
        }
        dd{
          width:100%;
          margin-top:30px;
          align-items: center;

          label{
            width:30px;
            height:30px;
            border-radius:15px;
            margin-right:10px;
          }
        }
      }
    }

    .search-area{
      border:0px;
      box-shadow: none;
      flex-direction: column;
      padding-bottom:150px;

      label{
        flex:1;
        border-right:0px;
        margin-bottom:20px;
        span{}
        strong{}
      }

      .inBox{
        flex:1;
        width:100%;
        border:1px solid #e2e2e2;

        input{height:60px;}
        .v-btn{
          min-width:60px;
          height:60px;
        }
        
      }
    }
  }

  .section04{
    h4{font-size:32px;}
    .v-expansion-panel-header{
      font-size:16px;
    }    
  }

  .section05{
    background: none;;
    .section-title{
      h4{font-size:32px;line-height:42px;word-break: break-all;}
    }
  }

}


@media screen and(max-width:720px){
  .contents{
    .visual{
      height:720px;

      .visual-title{
        span.text1{font-size:18px;color:#aaa;letter-spacing: 10px;}
        span.text2{
          font-size:32px;
          margin:10px 0;
          strong{font-weight:600;}
        }
        span.text3{font-size:18px;color:#aaa}
      }
    }
  }
  

  .section01{
    img.image{
      width:100%;
      height:auto;
    }
  }
  .section02{
    .store{
      margin-top:40px;
      dl{
        flex-basis:100px;
        dt{height:50px;}
      }
    }
  }

  .section03{
    .section-cont{
      dl{
        dt{
          width:80%;
        }
        dd{width:80%}
      }
    }
  }

  .section05{
    .section-cont{
      strong{font-size:28px;}
      p{font-size:14px;}
    }
  }

  .section04{
    .v-expansion-panel-header{
      font-size:14px;
      line-height:21px;
    }
    .v-expansion-panel-content{
      margin:0 -10px;
    }
  }
}

</style>