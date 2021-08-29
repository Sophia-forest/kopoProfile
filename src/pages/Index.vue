<template>
  <q-layout view="lHh lpr lfr">
    <div v-bind:class="{'main': $q.platform.is.desktop, 'mobile_main': $q.platform.is.ipad || $q.platform.is.mobile}"
         class="full-height" style="background-color:rgba(0, 0, 0, 0.7);">

      <q-header elevated class="bg-darkgray" style="background-color:rgba(0, 0, 0, 0.7);">
        <q-toolbar class="text-h3">
          <q-space></q-space>
          <q-tabs v-model="selected_tab" shrink>
            <q-tab name="about_me" :style="[selected_tab == 'about_me' ? {backgroundColor: 'rgba(0, 0, 0, 0.33)'} : {}]" class="q-mr-sm q-py-xs custom_tab"
                   @click="scrollToElement('id_about_me')" style="width:120px;min-height:auto !important;color: pink"
                   label="About Me"/>

            <q-tab name="works" :style="[selected_tab == 'works' ? {backgroundColor: 'rgba(0, 0, 0, 0.33)'} : {}]" class="q-mr-sm q-py-xs custom_tab"
                   @click="scrollToElement('id_projects')" style="width:120px;min-height:auto !important;color: pink"
                   label="learned"/>

            <!-- <q-tab name="pubs" :style="[selected_tab == 'pubs' ? {backgroundColor: 'rgba(0, 0, 0, 0.33)'} : {}]" class="q-mr-sm q-py-xs custom_tab"
                   @click="scrollToElement('id_publications')" style="width:120px;min-height:auto !important;color: pink"
                   label="Publications"/> -->

            <!-- <q-tab name="photo" :style="[selected_tab == 'photo' ? {backgroundColor: 'rgba(0, 0, 0, 0.33)'} : {}]" class="q-mr-sm q-py-xs custom_tab"
                   @click="scrollToElement('id_photo')" style="width:120px;min-height:auto !important;color: pink"
                   label="Photo"/> -->

            <q-tab name="contact" :style="[selected_tab == 'contact' ? {backgroundColor: 'rgba(0, 0, 0, 0.33)'} : {}]" class="q-mr-sm q-py-xs custom_tab"
                   @click="scrollToElement('contact_us')"
                   style="width:120px;min-height:auto !important;color: pink" label="Contact Me"/>

          </q-tabs>
        </q-toolbar>
      </q-header>
      <section>
        <div class="full-height full-width flex flex-center text-center"
           style="background-color: grey !important;z-index:0;height: 100vh !important;">
        <div class="">
          <!-- <div class="text-h6 text-pink-5">WELCOME TO MY PAGE</div> -->
          <div class="text-h2 text-pink q-py-sm q-my-md my-font"
               style="">WELCOME TO MY PAGE
          </div>
          <div class="text-h4 my-font" style="color:pink;">
            I'M A LEARNER
          </div>
          <div style="color: black !important;" class="text-h4 q-mt-md text-grey-2 my-font">
            Ahlim Lee
          </div>
        </div>
      </div>
      </section>
    </div>

    <div style="background-color:black	" id="id_about_me">
      <div class="row">
        <div class="col-md-4 col-lg-4 col-xs-12 col-sm-12">
          <div style="background-color:black" class="q-pa-md text-center text-pink text-weight-bolder text-h4">
            ABOUT ME
          </div>
          <div style="background-color: rgba(0, 0, 0, 0.68) !important;">
            <!-- <div style="background-color: rgba(0, 0, 0, 0.68) !important;">
              <q-img style="height:300px"
                     class="col-5"
                     src="/statics/images/my_2.jpg"
              />
            </div> -->
          </div>
        </div>
        <div class="col-md-8 col-lg-8 col-xs-12 col-sm-12 q-px-md q-pt-sm">
          <!-- <div class="text-h4 text-center text-white q-py-xs q-my-xs"
               style="border-top:3px solid #bdbdbd;border-bottom: 3px solid #bdbdbd;">HELLO
          </div> -->
          <!-- <h5 class="q-my-none text-caption" style="color: #20ffff;">
            2017.06 ~ Current : Korea Polytechnic College Professor<br>
            - dept. of Smart Finance : blockchain & IT tech
            <br>
            <br>
            2011.03 ~ 2017.05.26 Principal Engineer, Samsung SDS<br>
            - Participated in Several BPM(Business Process Management) Projects<br>
            - Developing Interface Module (SAP, SharePoint, ESB)<br>
            - Project Leader, EFSS(Enterprise File Sync & Share) Development Team<br>
            (https://www.youtube.com/watch?v=Wy6xK1D-Icg)<br>
            - Strategic Planning at Samsung Global Strategy & Operations (GSO, '14.1 ~ '15.8)
            <br>
            <br>
            2007.3 ~ 2008.12 Research Engineer, Precision Guided Munition R&D Center, LIG Nex1<br>
            - Developing Mission Critical Land-To-Air Missile Defense System<br>
            (https://www.youtube.com/watch?v=yP_ST_CaLlA)
            <br>
            <br>
            2004.3 ~ 2007.2 Research Engineer, Java Team, Mobile Communication R&D Lab, LG Electronics<br>
            - Porting Java Virtual Machine to Mobile Platforms(TI condat, Infineon apoxi)<br>
            - Performance Tuning and Country Adaptation of GSM mobile phones
          </h5> -->
          
        </div>
      </div>
    </div>

<!-- <div id="q-app" style="min-height: 100vh;"> -->
  <div id="q-app" style="background-color:#FFD2D2	">
  <!-- <div class="q-pa-md row justify-center"> -->
    <div class="q-pa-md row justify-center">
    <div style="width: 100%; max-width: 1000px">
      
        <q-chat-message
        name="Pepper"
        bg-color="yellow"
        
        avatar="/statics/images/robot1.png"
        :text="['Hello ahlim! how are you?']"
      ></q-chat-message>
      <q-chat-message
        name="Ahlim"
        bg-color="grey"
        avatar="/statics/images/arim.png"
        :text="['Great! how r U?']"
        sent
      ></q-chat-message>
      <q-chat-message
      bg-color="yellow"
        name="Pepper"
        avatar="/statics/images/robot1.png"
        :text="['Good! I heard you have been studying IT at the Polytechnic University since March 2021']"
      ></q-chat-message>
            <q-chat-message
        name="aAhlimhlim"
        bg-color="grey"
        avatar="/statics/images/arim.png"
        :text="['I am learning computer languages and programming :)']"
        sent
        z
      ></q-chat-message>
            <q-chat-message
      bg-color="yellow"
        name="Pepper"
        avatar="/statics/images/robot1.png"
        :text="['Can you tell me what you learned?']"
      ></q-chat-message>
            <q-chat-message
        name="Ahlim"
        bg-color="grey"
        avatar="/statics/images/arim.png"
        :text="['Of course, i will show you']"
        sent
        z
      ></q-chat-message>

    </div>
  </div>
</div>

 


    <div style="background-color:#FFD2D2" id="id_projects">
      <div class="row q-px-xl">
        
        <!-- <div class="text-h4 text-center text-white q-py-sm q-my-md full-width"
             style="border-top:3px solid #bdbdbd;border-bottom: 3px solid #bdbdbd;">MY Works
        </div> -->
        <div class="col-md-12 col-md-12 col-xs-12 col-sm-12 q-mb-xl flex flex-center">
          <q-card class="my-card" flat bordered style="background:radial-gradient(circle, #bebebe 0%, #828282 100%)">
            <q-card-section>
              <!-- <q-ribbon class="github-text" position="top-right" type="corner" color="white" background-color="#eb4f71">
                <a href="https://github.com/wonyongHwang/KopoBlockchain" target="_blank">FORK ME ON GITHUB!</a>
              </q-ribbon> -->
              <div class="row">
                <div class="col-lg-6 col-md-6 col-xs-12 col-sm-12">
                  <q-card-section class="q-py-xs">
                    <div class="text-h5 text-bold text-white">PYTHON</div>
                                        <div class="text-caption text-white">
                      <ul class="text-h8">
                        <li>내/외부 데이터 연동 및 데이터 처리기술 학습 <br>(웹크롤링, 공공데이터 수집)</li>
                        <li>SQL을 활용하여 DB(oracle, postgresql, MariaDB) 테이블 CRUD</li>
                        <li>데이터 전처리 : 데이터 타입 통합, 불량 데이터 처리</li>
                        <li>코드 리뷰를 통한 블록체인 이해</li>
                        <li>머신 러닝(데이터의 상관관계 분석)(DecisionTreeRegressor모델 적용)</li>
                        <li>주식 매수, 매도 예측 프로그램 <br> 다양한 라이브러리들 사용(FinanceDataReader, matplotlib등)<br>KIND에서 기업정보 불러오기 <br>함수와 클래스 생성 후 사용 <br> Matplotlib를 활용하여 추출한 데이터를 그래프로 시각화 </li>
                      </ul>
                    </div>
                    <!-- <div class="text-h5 q-mt-sm q-mb-xs">
                      <a class="project_link" style="text-decoration: none;color: #eb4f71;"
                         href="https://github.com/wonyongHwang/KopoBlockchain" target="_blank">Kopo BlockChain</a>
                    </div> -->
                  </q-card-section>
                </div>

                <!-- <div id="q-app" style="min-height: 100vh;">
  <div class="q-pa-md">
    <q-carousel
      animated
      v-model="slide"
      arrows
      navigation
      infinite
    >
      <q-carousel-slide :name="1" img-src="/statics/images/blockchain.png"></q-carousel-slide>
      <q-carousel-slide :name="2" img-src="https://cdn.quasar.dev/img/parallax1.jpg"></q-carousel-slide>
      <q-carousel-slide :name="3" img-src="https://cdn.quasar.dev/img/parallax2.jpg"></q-carousel-slide>
      <q-carousel-slide :name="4" img-src="https://cdn.quasar.dev/img/quasar.jpg"></q-carousel-slide>
    </q-carousel>
  </div>
</div> -->


                <div class="col-lg-6 col-md-6 col-xs-12 col-sm-12">
                  <q-card-section class="col-5 flex flex-center">
                    <q-img
  class="rounded-borders"
                      style="border:1px solid darkgrey"
                      src="/statics/images/crawling.png"
                    />
                  </q-card-section>
                </div>
                               <div class="col-lg-6 col-md-6 col-xs-12 col-sm-12">
                  <q-card-section class="col-5 flex flex-center">
                    <q-img
                      href="google.com"
                      class="rounded-borders"
                      style="border:1px solid darkgrey"
                      src="/statics/images/stock.png"
                    />
                  </q-card-section>
                </div>
                               <!-- <div class="col-lg-6 col-md-6 col-xs-12 col-sm-12">
                  <q-card-section class="col-5 flex flex-center">
                    <q-img
                      href="google.com"
                      class="rounded-borders"
                      style="border:1px solid darkgrey"
                      src="/statics/images/blockchain.png"
                    />
                  </q-card-section>
                </div> -->
              </div>
            </q-card-section>

            <q-separator/>

            <!-- <q-card-actions class="block">
              <a style="font-size: 25px;" class="q-py-sm q-pl-sm" href="https://www.slideshare.net/SuJeongShim/blockchain-implementation-by-python"
                 target="_blank" title="SlideShare"><i class="fab fa-slideshare" style="color: #eb5daa"></i></a>
              <div class="float-right q-py-sm">
                <iframe class="float-right"
                        src="https://ghbtns.com/github-btn.html?user=wonyongHwang&repo=KopoBlockchain&type=fork&count=true&size=large"
                        frameborder="0" scrolling="0" width="136" height="30" title="GitHub"></iframe>
              </div>
            </q-card-actions> -->
          </q-card>
        </div>


                <div class="col-md-12 col-md-12 col-xs-12 col-sm-12 q-mb-xl flex flex-center">
          <q-card class="my-card" flat bordered style="background:radial-gradient(circle, #bebebe 0%, #828282 100%)">
            <q-card-section>
              <!-- <q-ribbon class="github-text" position="top-right" type="corner" color="white" background-color="#eb4f71">
                <a href="https://github.com/wonyongHwang/KopoBlockchain" target="_blank">FORK ME ON GITHUB!</a>
              </q-ribbon> -->
              <div class="row">
                <div class="col-lg-6 col-md-6 col-xs-12 col-sm-12">
                  <q-card-section class="q-py-xs">
                    <div class="text-h5 text-bold text-white">JAVA</div>
                                        <div class="text-caption text-white">
                      <ul class="text-h8">
                        <li>Eclipse에 Spring, tomcat 등 개발 환경 구축</li>
                        <li>Model, View, Controller에 대한 이해 </li>
                        <li>jsp파일, css파일 생성과 관계 이해</li>
                        <li>SQLite와 Spring 연동 </li>
                        <li>입주자 명단 테이블 페이지 생성(CREATE)</li>
                        <li>입주자 등록 페이지 생성</li>
                        <li>입주자 목록 조회 및 수정,삭제 페이지 생성(READ, UPDATE, DELETE)</li>
                      </ul>
                    </div>
                  </q-card-section>
                </div>


                <div class="col-lg-6 col-md-6 col-xs-12 col-sm-12">
                  <q-card-section class="col-5 flex flex-center">
                    <q-img

                      style="border:1px solid darkgrey"
                      src="/statics/images/java.png"
                    />
                  </q-card-section>
                </div>
                            
                               <!-- <div class="col-lg-6 col-md-6 col-xs-12 col-sm-12">
                  <q-card-section class="col-5 flex flex-center">
                    <q-img
                      href="google.com"
                      class="rounded-borders"
                      style="border:1px solid darkgrey"
                      src="/statics/images/blockchain.png"
                    />
                  </q-card-section>
                </div> -->
              </div>
            </q-card-section>

            <q-separator/>

            <!-- <q-card-actions class="block">
              <a style="font-size: 25px;" class="q-py-sm q-pl-sm" href="https://www.slideshare.net/SuJeongShim/blockchain-implementation-by-python"
                 target="_blank" title="SlideShare"><i class="fab fa-slideshare" style="color: #eb5daa"></i></a>
              <div class="float-right q-py-sm">
                <iframe class="float-right"
                        src="https://ghbtns.com/github-btn.html?user=wonyongHwang&repo=KopoBlockchain&type=fork&count=true&size=large"
                        frameborder="0" scrolling="0" width="136" height="30" title="GitHub"></iframe>
              </div>
            </q-card-actions> -->
          </q-card>
        </div>


                <div class="col-md-12 col-md-12 col-xs-12 col-sm-12 q-mb-xl flex flex-center">
          <q-card class="my-card" flat bordered style="background:radial-gradient(circle, #bebebe 0%, #828282 100%)">
            <q-card-section>
              <!-- <q-ribbon class="github-text" position="top-right" type="corner" color="white" background-color="#eb4f71">
                <a href="https://github.com/wonyongHwang/KopoBlockchain" target="_blank">FORK ME ON GITHUB!</a>
              </q-ribbon> -->
              <div class="row">
                <div class="col-lg-6 col-md-6 col-xs-12 col-sm-12">
                  <q-card-section class="q-py-xs">
                    <div class="text-h5 text-bold text-white">JAVASCRIPT</div>
                                        <div class="text-caption text-white">
                      <ul class="text-h8">
                        <li>nodeJs를 활용한 backend 웹 어플리케이션 서버 구축</li>
                        <li>jquery를 활용한 frontEnd 개발</li>

                      </ul>
                    </div>
                   
                  </q-card-section>
                </div>
    
              </div>
            </q-card-section>

            <q-separator/>

            <!-- <q-card-actions class="block">
              <a style="font-size: 25px;" class="q-py-sm q-pl-sm" href="https://www.slideshare.net/SuJeongShim/blockchain-implementation-by-python"
                 target="_blank" title="SlideShare"><i class="fab fa-slideshare" style="color: #eb5daa"></i></a>
              <div class="float-right q-py-sm">
                <iframe class="float-right"
                        src="https://ghbtns.com/github-btn.html?user=wonyongHwang&repo=KopoBlockchain&type=fork&count=true&size=large"
                        frameborder="0" scrolling="0" width="136" height="30" title="GitHub"></iframe>
              </div>
            </q-card-actions> -->
          </q-card>
        </div>

         <div class="col-md-12 col-md-12 col-xs-12 col-sm-12 q-mb-xl flex flex-center">
          <q-card class="my-card" flat bordered style="background:radial-gradient(circle, #bebebe 0%, #828282 100%)">
            <q-card-section>
              <!-- <q-ribbon class="github-text" position="top-right" type="corner" color="white" background-color="#eb4f71">
                <a href="https://github.com/wonyongHwang/KopoBlockchain" target="_blank">FORK ME ON GITHUB!</a>
              </q-ribbon> -->
              <div class="row">
                <div class="col-lg-6 col-md-6 col-xs-12 col-sm-12">
                  <q-card-section class="q-py-xs">
                    <div class="text-h5 text-bold text-white">DATABASE</div>
                                        <div class="text-caption text-white">
                      <ul class="text-h8">
                        <li>데이터 모델링의 이해</li>
                        <li>Oracle, MySQL, PostgreSQL, MariaDB 조회 쿼리 학습</li>
                        <li>GROUPBY/JOIN 등 함수 위주 실습</li>

                      </ul>
                    </div>
                   
                  </q-card-section>
                </div>
    
              </div>
            </q-card-section>

            <q-separator/>

            <!-- <q-card-actions class="block">
              <a style="font-size: 25px;" class="q-py-sm q-pl-sm" href="https://www.slideshare.net/SuJeongShim/blockchain-implementation-by-python"
                 target="_blank" title="SlideShare"><i class="fab fa-slideshare" style="color: #eb5daa"></i></a>
              <div class="float-right q-py-sm">
                <iframe class="float-right"
                        src="https://ghbtns.com/github-btn.html?user=wonyongHwang&repo=KopoBlockchain&type=fork&count=true&size=large"
                        frameborder="0" scrolling="0" width="136" height="30" title="GitHub"></iframe>
              </div>
            </q-card-actions> -->
          </q-card>
        </div>


 <div class="col-md-12 col-md-12 col-xs-12 col-sm-12 q-mb-xl flex flex-center">
          <q-card class="my-card" flat bordered style="background:radial-gradient(circle, #bebebe 0%, #828282 100%)">
            <q-card-section>
              <!-- <q-ribbon class="github-text" position="top-right" type="corner" color="white" background-color="#eb4f71">
                <a href="https://github.com/wonyongHwang/KopoBlockchain" target="_blank">FORK ME ON GITHUB!</a>
              </q-ribbon> -->
              <div class="row">
                <div class="col-lg-6 col-md-6 col-xs-12 col-sm-12">
                  <q-card-section class="q-py-xs">
                    <div class="text-h5 text-bold text-white">LINUX</div>
                                        <div class="text-caption text-white">
                      <ul class="text-h8">
                        <li>vi 편집기 학습</li>
                        <li>쉘을 활용한 자동화 학습</li>
                        <li>VirtualBox환경에서의 네트워크 환경 학습</li>

                      </ul>
                    </div>
                   
                  </q-card-section>
                </div>
    
              </div>
            </q-card-section>

            <!-- <q-separator/> -->

            <!-- <q-card-actions class="block">
              <a style="font-size: 25px;" class="q-py-sm q-pl-sm" href="https://www.slideshare.net/SuJeongShim/blockchain-implementation-by-python"
                 target="_blank" title="SlideShare"><i class="fab fa-slideshare" style="color: #eb5daa"></i></a>
              <div class="float-right q-py-sm">
                <iframe class="float-right"
                        src="https://ghbtns.com/github-btn.html?user=wonyongHwang&repo=KopoBlockchain&type=fork&count=true&size=large"
                        frameborder="0" scrolling="0" width="136" height="30" title="GitHub"></iframe>
              </div>
            </q-card-actions> -->
          </q-card>
        </div>



        


        
      </div>
    </div>


<!-- 
    <div style="background-color:#14104e" id="id_publications">
      <div class="row row q-px-xl">
        <div class="text-h4 text-center text-white q-py-sm q-my-md full-width"
             style="border-top:3px solid #bdbdbd;border-bottom: 3px solid #bdbdbd;">Current Publications
        </div>
        <div class="col-md-12 col-md-12 col-xs-12 col-sm-12 q-mb-xl flex flex-center">
          <q-card class="my-card" flat bordered>
            <q-card-section class="q-py-xs">
              <div class="text-overline text-pink">Current Publications</div>

                <div class="text-h5 q-mt-sm q-mb-xs">
                  <div style="text-decoration: none;color: #eb4f71;">Application Development Using BlockChain</div>
                </div>
                <div class="text-caption text-grey-9">
                  Dec 10, 2019 Korea Polytechnics college<br>
                  <br>
                  - learn the characteristics of blockchain architecture through bitcoin<br>
                  - ethereum and its application development<br>
                  ISBN : 978-89-6440-531-4 (13500)<br>
                </div>

                <div class="text-h5 q-mt-sm q-mb-xs">
                  <div style="text-decoration: none;color: #eb4f71;">Development of Industrial Electronic Hardware</div>
                </div>
                <div class="text-caption text-grey-9">
                  Dec 31, 2018 Korea Research Institute for Vocational Education & Training (KRIVET)<br>
                  ISBN : 979-11-339-6977-7 (95560), 979-11-339-6976-0 (95560), 979-11-339-6979-1 (95560), 979-11-339-6975-3 (95560),<br>
                   979-11-339-6978-4 (95560) <br><br>
                </div>

                <div class="text-h5 q-mt-sm q-mb-xs">
                  <div style="text-decoration: none;color: #eb4f71;">A Study on Implementation of BlockChain Voting System using Hyperledger Fabric</div>
                </div>
                <div class="text-caption text-grey-9">
                  Journal of Korea institute of information, electronics, and communication technology v.13 no.4 , 2020, pp.298 - 305<br>
                  <br>
                  This paper deals with the implementation of electronic voting system using permissioned block chain technology.<br>
                  Cases studies have recently been under way in many industrial areas to review the application of the blockchain<br>
                  based electronic voting system. The existing electronic voting system was easily exposed by hacking because of<br>
                  its centralized characteristics, making it difficult to ensure the reliability and transparency of the voting<br>
                  system itself. In this study, we proposed key considerations and concepts to ensure the reliability and<br>
                  transparency of voters and voting stakeholder by utilizing a hyperledger fabric which is nowadays widely<br>
                   used as a permissioned blockchain.
                   <br><br>
                   
                   and more ...
                </div>

            </q-card-section>
          </q-card>
        </div>
      </div>
    </div> -->


    <!-- <section id="id_photo">
      <div style="background-color:#206b73;z-index:0;" class="content">
        <div class="row row q-px-xl">
          <div class="text-h4 text-center text-white q-py-sm q-my-md full-width"
               style="border-top:3px solid #bdbdbd;border-bottom: 3px solid #bdbdbd;">Photo
          </div>
          <div class="col-md-12 col-md-12 col-xs-12 col-sm-12 q-mb-xl">
            <div class="q-pa-md">
              <div class="q-col-gutter-md row">
                <div class="col-md-6 col-md-6 col-xs-12 col-sm-12 text-center flex flex-center">
                  <q-img
                    src="statics/images/pic1.png"
                    v-bind:class="{'sketch_desktop': $q.platform.is.desktop, 'sketch_mobile': $q.platform.is.ipad || $q.platform.is.mobile}"
                  >
                  </q-img>
                </div>
              
                <div class="col-md-6 col-md-6 col-xs-12 col-sm-12 text-center flex flex-center">
                  <q-img src="statics/images/pic2.png"
                         v-bind:class="{'sketch_desktop': $q.platform.is.desktop, 'sketch_mobile': $q.platform.is.ipad || $q.platform.is.mobile}">
                  </q-img>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <!-- <canvas id="canvas2" style="height: 100%;width:100%;"></canvas>
    </section> --> 

      <div id="q-app" style="background-color:#FFD2D2	">
  <!-- <div class="q-pa-md row justify-center"> -->
    <div class="q-pa-md row justify-center">
    <div style="width: 100%; max-width: 1000px">
      
        <q-chat-message
        name="Pepper"
        bg-color="yellow"
        
        avatar="/statics/images/robot1.png"
        :text="['Wow! It is interesting']"
      ></q-chat-message>
      <q-chat-message
        name="Ahlim"
        bg-color="grey"
        avatar="/statics/images/arim.png"
        :text="['Thank you :) How about visiting my github?']"
        sent
      ></q-chat-message>

            <q-chat-message
        name="Ahlim"
        bg-color="grey"
        avatar="/statics/images/arim.png"
        :text="['And if you have a question, just send email to me :)']"
        
        sent
        z
      ></q-chat-message>
            <q-chat-message
      bg-color="yellow"
        name="Pepper"
        avatar="/statics/images/robot1.png"
        :text="['Thank you ! :)']"
      ></q-chat-message>
            <q-chat-message
        name="Ahlim"
        bg-color="grey"
        avatar="/statics/images/arim.png"
        :text="['It is my pleasure :)']"
        sent
        z
      ></q-chat-message>

    </div>
  </div>
</div>

    <div id="contact_us">
      <div style="background-color: rgba(0, 0, 0, 0.6) !important;">
        <form
          action="https://formspree.io/f/xwkaakkd"
          method="POST"
        >
          <div class="row text-center flex flex-center q-py-lg">
            <div class="col-md-6 col-lg-6 col-sx-12 col-sm-12 q-gutter-lg q-px-xl q-pb-none q-ma-none">
              <q-input required v-model="name" name="name" bg-color="grey" outlined label="Your Name *">
                <template v-slot:append>
                  <q-icon name="list" style="color:pink"/>
                </template>
              </q-input>
              <q-input type="email" required v-model="email" name="_replyto" bg-color="grey" outlined label="Your Email *">
                <template v-slot:append>
                  <q-icon name="email" style="color:pink"/>
                </template>
              </q-input>
            </div>
            <div class="col-md-6 col-lg-6 col-sx-12 col-sm-12 q-gutter-lg q-px-xl q-pb-none q-ma-none">
              <q-input required v-model="message" name="message" class="" type="textarea" bg-color="grey" outlined
                       label="Your Message *">
                <template v-slot:append>
                  <q-icon name="comment" style="color:pink"/>
                </template>
              </q-input>
            </div>
          </div>
          <div class="row flex flex-center text-center q-pb-xl q-mt-md">
            <div class="col-md-12 col-lg-12 col-sx-12 col-sm-12">
              <q-btn type="submit" size="lg" style="background:pink;color: grey;bold" label="Send Message" glossy/>
            </div>
          </div>
        </form>
      </div>


    </div>


    <q-toolbar class="flex flex-center text-white" style="background-color: #F56E6E;border-top: 2px solid grey"
               id="id_contact_me">
      <div class="q-pa-sm q-gutter-sm">

               <q-btn color="secondary"  label="Visit to my github" href="https://github.com/Sophia-forest" glossy></q-btn>

        <q-btn target="_blank" style="border: 2px solid white" round type="a"
               href="https://github.com/Sophia-forest"
               glossy
               icon="fab fa-github"/>

        <!-- <q-btn target="_blank" style="border: 2px solid black;" round type="a"
               href="https://www.facebook.com/wonyong.hwang"
               glossy
               icon="fab fa-facebook"/> -->
        <!-- <q-btn target="_blank" style="border: 2px solid green;" round type="a"
               href="https://www.linkedin.com/in/justino/"
               glossy
               icon="fab fa-linkedin"/> -->
      </div>
    </q-toolbar>
  </q-layout>
</template>

<script>

    import {scroll} from 'quasar'

    const {getScrollTarget, setScrollPosition} = scroll
    export default {
        name: 'PageIndex',
        data() {
            return {
                name: "",
                email: "",
                message: "",
                selected_tab: 'about_me',
            }
        },
        methods: {
            scrollToElement(id) {
                let el = document.getElementById(id)
                const target = getScrollTarget(el)
                const offset = el.offsetTop - 65
                const duration = 800
                setScrollPosition(target, offset, duration)
            }
        },
        mounted: function () {
            // let canvas2Settings = {
            //     "target": "canvas2",
            //     "max": "120",
            //     "animate": true,
            //     "props": ["circle", "square", "triangle", "line"],
            //     "colors": [[165, 104, 246], [230, 61, 135], [0, 199, 228], [253, 214, 126]],
            //     "clock": "20"
            // };
            // let canvas2 = new ConfettiGenerator(canvas2Settings);
            // canvas2.render();
        }
    }
</script>

<style>
  .main {

    background: url() no-repeat center center fixed;
    -webkit-background-size: cover;
    -moz-background-size: cover;
    -o-background-size: cover;
    background-size: cover;
    height: 100vh !important;
  }

  .mobile_main {
    /* background: url(/statics/images/my_1_2.jpg) no-repeat center center fixed; */
    -webkit-background-size: cover;
    -moz-background-size: cover;
    -o-background-size: cover;
    background-size: cover;
    height: 100vh !important;
  }

  .my-card {
    width: 100%;
    max-width: 800px;
    border: none;
    border-radius: 0px;
  }

  .sponsor-card {
    width: 100%;
    max-width: 240px;
    border: none;
    border-radius: 6px;
  }

  .project_link:hover {
    text-decoration: underline !important;
  }

  .sketch_desktop {
    width: 100%;
    height: 100%;
    display:block; 
    margin:auto;
    border: 5px solid #30313b;
  }

  .sketch_mobile {
    width: 100%;
    height: 100% !important;
    border: 20px solid #30313b;
  }

  #contact_us {
    /* background: url(/statics/images/muje.jpg); */
    background-size: contain;
      /* background-size: 1000px;
  width: 1000px;
  height: 1000px; */
    background-position: right;
    background-attachment: fixed;
    background-repeat: no-repeat;
  }

  .custom_tab {
    width: 130px;
  }

  body {
    overflow-x: hidden;
  }

  section {
    position: relative;
  }

  section > * {
    z-index: 9;
    position: relative;
    top: 0;
  }

  section > canvas {
    z-index: 1;
    position: absolute;
    left: 0;
  }
</style>
