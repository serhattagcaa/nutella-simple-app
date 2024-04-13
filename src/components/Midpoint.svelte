<script>
  let currentState = 0;

  const changeState = () => {
    currentState = (currentState + 1) % 3;
    setTimeout(changeState, 6000);
  }

  setTimeout(changeState, 6000);

  
  import Midcolor from  "../assets/Midcolor.svg";
  import Freseight from "../assets/freseight.png";
  import Strawberry from "../assets/strawberry.svg";
  import Midstrawberry from "../assets/midstrawberry.svg";
  import Platepan from "../assets/platepan.png";
  import Vectorone from "../assets/vectorone.png";
  import Nutellaglass from "../assets/nutellaglass.png";
  import Twostrawberry from "../assets/twostrawberry.svg";
  import Onfreelight from "../assets/onfreelight.svg";
  import Rightfreelight from "../assets/rightfreelight.svg";
  import Topfrelight from "../assets/topfrelight.svg"
</script>

<main>
  <div>
    <div class="relative pl-28 top-[200px]">
      {#if currentState === 0}
        <h1 class="font-montserrat font-[600] text-[64px] text-[#1F1F1F]" id="onetext">Pankek Keyfini</h1>
      {:else if currentState === 1}
        <h1 class="font-montserrat font-[600] text-[64px] text-[#1F1F1F]" id="twotext">Ramazan Keyfini</h1>
      {:else}
        <h1 class="font-montserrat font-[600] text-[64px] text-[#1F1F1F]" id="threetext">Kahve Keyfini</h1>
      {/if}
      <h1 class="font-montserrat font-[600] text-[64px] text-[#1F1F1F]">Nutella İle Taçlandır</h1>
      <p class="relative top-[15px] font-montserrat font-[500] text-[#1F1F1F] text-[20px]">
        Nutella ile eğlenceli günler için hazırlayabileceğiniz <br> daha o kadar çok yaratıcı tarif var ki!
      </p>
      <button class="relative top-[60px] font-montserrat font-[500] w-52 h-14 rounded-[15px] text-white bg-[#E3001A]">
        Tarifi Görüntüle
      </button>
      <div class="relative top-[200px] flex space-x-8">
        <p class="w-[50px] h-2 {currentState === 0 ?  'bg-red-800': 'bg-gray-200'} rounded-lg" />
        <p class="w-[50px] h-2 {currentState === 1 ?  'bg-red-800': 'bg-gray-200'} rounded-lg" />
        <p class="w-[50px] h-2 {currentState === 2 ?  'bg-red-800': 'bg-gray-200'} rounded-lg" />
      </div>
    </div>   
    <div class="float-right" >  
      <img class="midcolor" src={Midcolor} alt="" />
      {#if currentState === 0}
        <div id="oneimg">
          <img class="freseight" src={Freseight} alt="" />  
          <img class="strawberry" src={Strawberry} alt="" />
          <img class="midstrawberry" src={Midstrawberry} alt="" />
        
          <img class="platepan" src={Platepan} alt="" />
          <img class="vectorone" src={Vectorone} alt="" />
          <img class="nutellaglass" src={Nutellaglass} alt="" />
        
          <img class="twostrawberry" src={Twostrawberry} alt="" />
          <img class="onfreelight" src={Onfreelight} alt="" />
          <img class="rightfreelight" src={Rightfreelight} alt="" />         
          <img class="topfrelight" src={Topfrelight} alt="" />
        </div>
      {:else if currentState === 1}
        <div id="twoimg">
          <img src={Twostrawberry} alt="">
        </div>
      {:else}
        <div>
          <img src={Midstrawberry} alt="">
        </div>
      {/if}
    </div>
  </div>
</main>

  
<style>


.midcolor {
    position: relative;
    float: right;
    top:-300px;
}

.freseight {
    position: relative;
    float: right; /* Yeni eklenen özellik */
    left: -570px; 
    top: -550px;
    width: 88.78px;
    height: 56.67px;
    animation: freseightone ease-in 0.7s forwards, freseighttwo 0.7s ease-out 5s forwards;
  }

  @keyframes freseightone {
      100% {
        left: -450px; top: -220px;
      }
    }

    @keyframes freseighttwo {
      100% {
        left: -550px;
         top: -220px;
         transform: rotate(33deg);
         opacity:0.5;
      }
    }

    .strawberry {
  position: relative;
  float: right;
  width: 100px;
  height: 135px;
  top: -285px;
  left: 250px;
  animation: strawberryone ease-in 0.7s forwards, strawberrytwo 0.7s ease-out 5s forwards;
}

@keyframes strawberryone {
  100% {
    left: 180px;
    top: -100px;
  }
}

@keyframes strawberrytwo {
  100% {
    left: 550px;
    top: -550px;
    transform: rotate(66deg);
    width: 57.14px;
    height: 77.14px;
  }
}
.midstrawberry {
    position: relative;
    float: right; /* Yeni eklenen özellik */
    width: 123px;
    height: 110px;
    animation: midstrawone ease-in 0.7s forwards, midstrawtwo 1s ease-out 5s forwards;
    left: 150px; top:50px;

}

@keyframes midstrawone {
    
    100% {left: 180px; top:100px;}
}

@keyframes midstrawtwo {
    
    100% {
      transform: rotate(-60deg);
      left: 90px;
      top: 990px; 
      width: 49.2px;
      height: 45px;
    }
}

/* iç içe geçimiş yapı */
.twostrawberry {
    position: relative;
    float: right; /* Yeni eklenen özellik */
    width: 125px;
    height: 110px;
    animation: twostrawone ease-in 0.7s forwards, twostrawtwo 1s ease-out 5s forwards;
    left: 700px;
    top: -100px;
}
 
@keyframes twostrawone {
     100% {left: 580px; top: -320px;}  
} 

@keyframes twostrawtwo{
     100% {
      transform: rotate(60deg);
      left: 1000px;
      top: 500px;
      width:50px; 
      height: 44px;
    }  
}

.platepan {
    position: relative;    
    width: 366px; /* Başlangıçta genişlik */
    height: 315px; /* Başlangıçta yükseklik */
    float: right;
    opacity: 0; /* Başlangıçta opasiteyi ayarlayın */
    opacity: 0; /* %0'da opasiteyi ayarlayın */
    left: 800px;
    top: -100px;
    transform: rotate(45deg); /* %0'da 45 derece dönüş */
    animation-timing-function: ease-out; /* Başlangıçta yavaş */
    animation: platepanone ease-in 0.7s forwards, platepantwo 1s ease-out 5s forwards;
}

@keyframes platepanone{
    100% {
        opacity: 1; /* %100'de opasiteyi ayarlayın */
        width: 523px; /* %100'de genişlik */
        height: 450px; /* %100'de yükseklik */
        left: 800px;
        top: -100px;
        transform: rotate(0deg); /* %100'de 0 derece dönüş */
        animation-timing-function: ease-in; /* Sonunda hızlı */
    }
  }

  @keyframes platepantwo{
    100% {
        opacity: 1; /* %100'de opasiteyi ayarlayın */
        width: 523px; /* %100'de genişlik */
        height: 450px; /* %100'de yükseklik */
        left: 800px;
        top: -100px;
        transform: rotate(0deg); /* %100'de 0 derece dönüş */
        animation-timing-function: ease-in; /* Sonunda hızlı */
    }
  }

.nutellaglass{
    position: relative;
    float: right;
    width: 75.85116px; 
    height: 88.13012px;
    animation-name:nutellaglasslocal;
    animation-duration: 1s;
    animation-fill-mode: forwards; /* Animasyon bitiminde son durumu korur */
    animation-timing-function: ease-in-out;
}
@keyframes nutellaglasslocal {
    0% {
        opacity: 0;
        width: 75.85116px; 
        height: 88.13012px;
        left: 810px;
        top: -340px;
        transform: rotate(45deg);
        animation-timing-function: ease-out;
    }
    100% {
        opacity: 1;
        width: 108.3588px;
        height: 125.9016px;
        left: 810px;
        top: -340px;
        transform: rotate(0deg);
        animation-timing-function: ease-in;
    }
}

.vectorone{
    position: relative;
    float: right;
    width: 243.6px;
    height: 237.3px;
    animation-name:vectoronelocal;
    animation-duration: 1s;
    animation-fill-mode: forwards; /* Animasyon bitiminde son durumu korur */
    animation-timing-function: ease-in-out;
}
@keyframes vectoronelocal{
    0% {
        opacity: 0; /* %0'da opasiteyi ayarlayın */
        width: 243.6px;
        height: 237.3px;
        left: 450px;
        top: -520px;
        transform: rotate(45deg); /* %0'da 45 derece dönüş */
        animation-timing-function: ease-out; /* Başlangıçta yavaş */
    }
    100% {
        opacity: 1; /* %100'de opasiteyi ayarlayın */
        width: 348px;
        height: 339px; /* %0'da yükseklik */
        left: 450px;
        top: -520px;
        transform: rotate(0deg); /* %100'de 0 derece dönüş */
        animation-timing-function: ease-in; /* Sonunda hızlı */
    }
}
.onfreelight{
  position: relative;
    float: right; /* Yeni eklenen özellik */
    width: 95px;
    height: 85px;
    animation-name: onfreelightlocal;
    animation-duration: 1s;
    animation-fill-mode: forwards; /* Animasyon bitiminde son durumu korur */
    animation-timing-function: ease-in-out;
}

@keyframes onfreelightlocal {
     0% {left: 1400px; top: -560px;}
     100% {left: 1121px; top: -560px;}  
} 

.topfrelight{
  position: relative;
    float: right; /* Yeni eklenen özellik */
    width:106.875px;
    height: 136.875px;
    animation-name: topfrelightlocal;
    animation-duration: 1s;
    animation-fill-mode: forwards; /* Animasyon bitiminde son durumu korur */
    animation-timing-function: ease-in-out;
}
@keyframes topfrelightlocal{
     0% {left: 1050px; top: 500px;}  
     100% {left: 1050px; top: -180px;}  
} 

.rightfreelight{
  position: relative;
    float: right; /* Yeni eklenen özellik */
    width: 73px;
    height: 67px;
    animation-name: rightfreelightlocal;
    animation-duration: 1s;
    animation-fill-mode: forwards; /* Animasyon bitiminde son durumu korur */
    animation-timing-function: ease-in-out;
}
@keyframes rightfreelightlocal{  
  0% {left: 1500px; top: -160px;}     
  100% {left: 1216px; top: -160px;}  
} 


</style>