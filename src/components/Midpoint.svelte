<script>
    let currentState = 0;
  
    const changeState = () => {
      currentState = (currentState + 1) % 3;
      setTimeout(changeState, 6000);
    }
  
    setTimeout(changeState, 6000);
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
    <div class="float-right">  
        <img class="midcolor" src="/src/assets/Midcolor.svg" alt="" />
      {#if currentState === 0}
      <div id="oneimg">
        <img class="freseight" src="/src/assets/freseight.png" alt="" />  
        <img class="strawberry" src="/src/assets/strawberry.svg" alt="" />
          <img class="midstrawberry" src="/src/assets/midstrawberry.svg" alt="" />
          <img class="platepan" src="src/assets/platepan.png" alt="" />
          <img class="vectorone" src="src/assets/vectorone.png" alt="" />
          <img class="nutellaglass" src="src/assets/nutellaglass.png" alt="" />
          <img class="twostrawberry" src="/src/assets/twostrawberry.svg" alt="" />
        </div>
        {:else if currentState === 1}
        <div id="twoimg">
          <img src="/src/assets/twostrawberry.svg" alt="">
        </div>
        {:else}
        <div>
            <img src="/src/assets/midstrawberry.svg" alt="">
        </div>
      {/if} </div>
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
    width: 88.78px;
    height: 56.67px;
    animation-name: freselocal;  
    animation-duration: 1s;
    animation-fill-mode: forwards; /* Animasyon bitiminde son durumu korur */
    animation-timing-function: ease-in-out; /* Animasyonun başlangıç ve sonunda yavaşlama */
}

@keyframes freselocal {
    0% {left: -570px; top: -550px;}
    100% {left: -450px; top: -220px;} 
}

.strawberry {
    position: relative;
    float: right;
    width: 100px;
    height: 135px;
    top: -285px;
    left: 250px;
    animation-name: strawlocal;
    animation-duration: 1s;
    animation-fill-mode: forwards; /* Animasyon bitiminde son durumu korur */
    animation-timing-function: ease-in-out; /* Animasyonun başlangıç ve sonunda yavaşlama */
}

@keyframes strawlocal {
    0% {left: 250px; top: -285px;}
    100% {left: 180px; top: -100px;}
}

.midstrawberry {
    position: relative;
    float: right; /* Yeni eklenen özellik */
    width: 123px;
    height: 110px;
    animation-name: midstrawlocal;
    animation-duration: 1s;
    animation-fill-mode: forwards; /* Animasyon bitiminde son durumu korur */
    animation-timing-function: ease-in-out;
}

@keyframes midstrawlocal {
    0% {left: 150px; top:50px;}
    100% {left: 180px; top:100px;}
}
/* iç içe geçimiş yapı */
.twostrawberry {
    position: relative;
    float: right; /* Yeni eklenen özellik */
    width: 125px;
    height: 110px;
    animation-name: twostrawlocal;
    animation-duration: 1s;
    animation-fill-mode: forwards; /* Animasyon bitiminde son durumu korur */
    animation-timing-function: ease-in-out;
}
 
@keyframes twostrawlocal {
    0% {left: 700px; top: -100px;}
     100% {left: 580px; top: -320px;}  
} 

.platepan {
    position: relative;    
    width: 366px; /* Başlangıçta genişlik */
    height: 315px; /* Başlangıçta yükseklik */
    float: right;
    opacity: 0; /* Başlangıçta opasiteyi ayarlayın */
    animation: platepanlocal 1s forwards ease-in-out; /* Döndürme animasyonu */
}

@keyframes platepanlocal {
    0% {
        opacity: 0; /* %0'da opasiteyi ayarlayın */
        width: 366px; /* %0'da genişlik */
        height: 315px; /* %0'da yükseklik */
        left: 800px;
        top: -100px;
        transform: rotate(45deg); /* %0'da 45 derece dönüş */
        animation-timing-function: ease-out; /* Başlangıçta yavaş */
    }
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



</style>