<script>
  let currentState = 0;

  const changeState = () => {
    currentState = (currentState + 1) % 3;
    setTimeout(changeState, 6000);
  }

  setTimeout(changeState, 6000);

  
  import Midcolor from  "../assets/Midcolor.png";
  import Freseight from "../assets/freseight.png";
  import Strawberry from "../assets/strawberry.svg";
  import Midstrawberry from "../assets/midstrawberry.svg";
  import Platepan from "../assets/platepan.png";
  import Vectorone from "../assets/vectorone.png";
  import Nutellaglass from "../assets/nutellaglass.png";
  import Twostrawberry from "../assets/twostrawberry.svg";
  import Onfreelightsvg from "../assets/onfreelight.svg";
  import Onfreelightpng from "../assets/onfreelight.png" ;
  import Rightfreelightsvg from "../assets/rightfreelight.svg";
  import Rightfreelightpng from "../assets/rightfreelight.png";
  import Topfrelight from "../assets/topfrelight.svg";
  import Rightramadanlight from "../assets/rightramadanlight.png";
  import Leftramamdanlight from "../assets/leftramadanlight.png";
  import Vectortwo from "../assets/vectortwo.png";
  import Ramadanhurma from "../assets/ramadanhurma.png";
  import Kahveone from "../assets/kahveone.png";
  import Kahvebardak from "../assets/kahvebardak.png";
  import Kahvekayip from "../assets/kahvekayip.png";
  import Duman from "../assets/duman.png";
  import Kakvealt from "../assets/kahvealt.png";
  import HardDeepkahve from "../assets/boşlukhardcoffe.png"
  import App from "../App.svelte";
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
        <button
          class="w-[50px] h-2 rounded-lg {currentState === 0 ? 'bg-red-800' : 'bg-gray-200'}"
          on:click={() => currentState = 0}
        ></button>
        <button
          class="w-[50px] h-2 rounded-lg {currentState === 1 ? 'bg-red-800' : 'bg-gray-200'}"
          on:click={() => currentState = 1}
        ></button>
        <button
          class="w-[50px] h-2 rounded-lg {currentState === 2 ? 'bg-red-800' : 'bg-gray-200'}"
          on:click={() => currentState = 2}
        ></button>
      </div>
    </div>   
    <div class="float-right" >  
      {#if currentState === 0}
        <div class="twoimg">
          <div class="midcolortwo">
          <img class="midcolortwolite" src={Midcolor} alt="" />
          <img class="onfreelight" src={Onfreelightpng} alt="" />
          <img class="rightfreelightpp" src="{Rightfreelightpng}"  alt="">
          </div>
          <div class="twoimgin">
            <img class="topfrelightppfirst" src="{Topfrelight}"  alt=""> 
            <img class="freseight" src={Freseight} alt="" />  
            <img class="strawberry" src={Strawberry} alt="" />
            <img class="midstrawberry" src={Midstrawberry} alt="" />
            <img class="platepan" src={Platepan} alt="" />
            <img class="vectorone" src={Vectorone} alt="" />
            <img class="nutellaglass" src={Nutellaglass} alt="" /> 
            <img class="twostrawberry" src={Twostrawberry} alt="" />
          </div>
        </div>
      {:else if currentState === 1}
        <div class="twoimg">
          <div class="midcolortwo">
          <img class="midcolortwolite" src={Midcolor} alt="" />
          <img class="leftramadanlight" src={Leftramamdanlight} alt="">
          <img class="rightramadanlight" src={Rightramadanlight} alt="">
          <img src="{Onfreelightpng}" class="onramadanlight" alt="">
          <img src="{Rightfreelightpng}"  class="rightfreeramadanlight" alt="">
          <img src="{Topfrelight}" class="topramadanlight" alt="">  
        </div>
        <div class="twoimgin">
          <img class="ramadanhurma" src="{Ramadanhurma}" alt=""/>
          <img class="vectortwo" src="{Vectortwo}" alt=""/>
        </div>
           <div>
         <img class="frestwoeight" src={Freseight} alt="" />
        </div>
        </div>
      {:else}
        <div class="twoimg">
          <div class="midcolortwo">
            <img class="midcolortwolite" src={Midcolor} alt="" />
            <img src={Kahveone} alt="" class="kahveone">
            <img src={Kahvekayip} alt="" class="kahvekayip">
            <img src={Kakvealt} alt="" class="kahvealt">
          </div>
        </div>
        <div class="twoimgin">
          <img src={Kahvebardak} class="kahvebardak" alt="">
          <img src={Duman} class="duman" alt="">
          <img src={HardDeepkahve} class="hardcoffe" alt="">
        </div>
      {/if}
    </div>
  </div>
</main>

  
<style>

.freseight{
  position: relative;
    transform: rotate(10deg);
    left: -750px;
    top: -1700px;
    width: 88.78px;
    height: 56.67px;
    animation: 
    freseightone 0.7s cubic-bezier(0.66, 0, 0.34, 1) forwards,
    freseighttwo 0.7s cubic-bezier(0.25, 0.1, 0.25, 1) 5s forwards;
  }

  @keyframes freseightone {
    100% {
      left: -640px;
      top: -1359px;
    }
}

.strawberry{
  position: absolute;
  top: -1450px;
  left: 50px;
  animation: 
  strawberryone 0.7s cubic-bezier(0.66, 0, 0.34, 1) forwards,
  strawberrytwo 0.7s cubic-bezier(0.25, 0.1, 0.25, 1) 5s forwards; 
}
 @keyframes strawberryone {
  100% { 
  top: -1280px;
  left: -30px;
    }
}

@keyframes strawberrytwo {
  100% { 
  top: -1800px;
  left: 170px;
  transform: rotate(400deg) scale(0.001) ;
  }
}

.midstrawberry{
 position: absolute;
 top: -1170px;
 left: -150px;
 animation: 
 midstrawberryone 0.7s cubic-bezier(0.66, 0, 0.34, 1) forwards,
 midstrawberrytwo 0.7s cubic-bezier(0.25, 0.1, 0.25, 1) 5s forwards; 
}
 @keyframes midstrawberryone {
  100% { 
    top: -1100px;
    left: -130px;
  }
}

@keyframes midstrawberrytwo {
  100% {
  top: 500px;
  left: -500px;
  transform: rotate(-400deg) scale(0.001);
  }
}

.twostrawberry{
  position: absolute;
  top: -900px;
  left: 90px;
 animation: 
 twostrawberryone 0.7s cubic-bezier(0.66, 0, 0.34, 1) forwards,
 twostrawberrytwo 0.7s cubic-bezier(0.25, 0.1, 0.25, 1) 5s forwards;   
}

@keyframes twostrawberryone {
  100% { 
   top: -1070px;
   left: 10px;
   }
}

@keyframes twostrawberrytwo {
  100% {
  top: 500px;
  left: 600px;
  transform: rotate(400deg) scale(0.001);
  }
}
.platepan{
 position: absolute;
 top: -1290px;
 left: -40px;
}

.nutellaglass{
position: absolute;
 top: -1065px;
 left: 325px;
}

.vectorone{
position: absolute;
 top: -1263px;
 left: 100px;
}

.topfrelightppfirst{
  position: absolute;
  top: 1500px;
  left: 10px;
  z-index: 2;
  transform: scale(1.1);
  animation: 
  topfrelightppfirstone 0.7s cubic-bezier(0.66, 0, 0.34, 1) forwards,
  topfrelightpptwo 0.7s cubic-bezier(0.25, 0.1, 0.25, 1) 5s forwards; 
}

@keyframes topfrelightppfirstone{
  100%{
  top: -866px;
  left: 200px;
  }
}

@keyframes topfrelightpptwo{
  100%{
  top: -866px;
  left: 200px;
  }
}
.topfrelightpp{
  position: absolute;
  top: 600px;
  left: 200px;
  z-index: 2;
  transform: scale(1.1);
  
}

.rightfreelightpp{
  position: absolute;
  top: 800px;
  left: 500px;
  z-index: 2;
  transform: scale(0.5);
  animation: 
  rightfreelightone 0.7s cubic-bezier(0.66, 0, 0.34, 1) forwards,
  rightfreelighttwo 0.7s cubic-bezier(0.25, 0.1, 0.25, 1) 5s forwards;     
  }

@keyframes rightfreelightone{
  100%{
    top: 600px;
    left: 465px;
  }
}
 
@keyframes rightfreelighttwo{
  100%{
    top: 600px;
    left: 465px;
  }
}
.onfreelight{
  position: absolute;
  left: 500px;
  top: 120px;
  z-index: 2;
  transform: scale(0.55);
  opacity: 0.5;
  animation: 
  onfreelightone 0.7s cubic-bezier(0.66, 0, 0.34, 1) forwards,
  onfreelighttwo 0.7s cubic-bezier(0.25, 0.1, 0.25, 1) 5s forwards;   
}

@keyframes onfreelightone {
  100% { 
    opacity: 1;
    top: 120px; 
    left: 420px;
  }
}

@keyframes onfreelighttwo {
  100% {
    top: 120px; 
    left: 420px;
    opacity: 1;
  }
}


.leftramadanlight {
  position: absolute;
  transform: rotate(15deg);
  top: -160px;
  left: 210px;
  width: 170.57px;
  height: 323.14px;
  z-index: 2;
  animation: 
    leftramadanlightone 0.7s cubic-bezier(0.66, 0, 0.34, 1) forwards,
    leftramadanlighttwo 0.7s cubic-bezier(0.25, 0.1, 0.25, 1) 5s forwards;
}

@keyframes leftramadanlightone {
  100% {
    transform: rotate(0deg);
    top: 20px;
    left: 165px;
    width: 170.57px;
    height: 323.14px;
  }
}

@keyframes leftramadanlighttwo {
  100% {
    top: -250px;
    left: 165px;
    width: 170.57px;
    height: 323.14px;
  }
}


.frestwoeight {
    position: relative;
    transform: rotate(10deg);
    left: -640px;
    top: -1086px;
    width: 88.78px;
    height: 56.67px;
    opacity: 0.5;
    animation: 
    frestwoightone 0.7s cubic-bezier(0.66, 0, 0.34, 1) forwards,
    frestwoighttwo 0.7s cubic-bezier(0.25, 0.1, 0.25, 1) 5s forwards;
    filter: sepia(1.5) saturate(2.5) hue-rotate(-3deg) brightness(0.9);
}

@keyframes frestwoightone {
    100% {
        transform: rotate(33deg) scale(0.8);
        opacity: 1;
        left: -800px;
        top: -1086px;
    }
}

/* @keyframes frestwoighttwo {
    100% {
        transform: rotate(33deg);
        opacity: 0.7;
    }
} */
.twoimg{
position: relative;
width: 100%;
height: 100%;
}

.midcolortwo{
  position: relative;
  top:-300px;
  -webkit-mask-image: url(src/assets/Midcolor.png);
  mask-image: url(src/assets/Midcolor.png);
  mask-image: url(src/assets/Midcolor.png);
  -webkit-mask-repeat: no-repeat;
  mask-repeat: no-repeat;    
  z-index:1;
}

.midcolortwolite{
position: relative;
z-index: 1;
}
.leftramadanlight {
  position: absolute;
  transform: rotate(15deg);
  top: -160px;
  left: 210px;
  width: 170.57px;
  height: 323.14px;
  z-index: 2;
  animation: 
    leftramadanlightone 0.7s cubic-bezier(0.66, 0, 0.34, 1) forwards,
    leftramadanlighttwo 0.7s cubic-bezier(0.25, 0.1, 0.25, 1) 5s forwards;
}

@keyframes leftramadanlightone {
  100% {
    transform: rotate(0deg);
    top: 20px;
    left: 165px;
    width: 170.57px;
    height: 323.14px;
  }
}

@keyframes leftramadanlighttwo {
  100% {
    top: -250px;
    left: 165px;
    width: 170.57px;
    height: 323.14px;
  }
}

/* Real Left */
.rightramadanlight {
  position: absolute;
  transform: rotate(-40deg);
  top: -400px;
  left: -50px;
  width: 195.8px;
  height: 630.3px;
  z-index: 2;
  animation: 
    rightramadanlightone 0.7s cubic-bezier(0.66, 0, 0.34, 1) forwards,
    rightramadanlighttwo 0.7s cubic-bezier(0.25, 0.1, 0.25, 1) 5s forwards;
}

@keyframes rightramadanlightone {
  100% {
    transform: rotate(0deg);
    top: -350px;
    left: 20px;
    width: 195.8px;
    height: 630.3px;
  }
}

@keyframes rightramadanlighttwo {
  100% {
    top: -600px;
    left: 20px;
    width: 195.8px;
    height: 630.3px;
  }
}
.twoimgin{
  position: relative;
  top:300px;
  z-index: 2;
}
.ramadanhurma{
  position: absolute;
  top: -1060px;
  left: -170px;
  transform: scale(1.8);
}
.vectortwo{
  position: absolute;
  top: -1290px;
  left: -190px;
  transform: rotate(-117deg) scale(0.72);
}
/* .lightfamilytwo{
  position: relative;
  top:-200px;
  left: 200px;
  z-index: 3;
} */
.onramadanlight{
  position: absolute;
  transform:  rotate(100deg) scale(0.45);
  top: 580px;
  left: 450px;
  filter: sepia(1.5) saturate(2.5) hue-rotate(-3deg) brightness(0.9);
  z-index: 2;
  animation: 
  onramadanlightone 0.7s cubic-bezier(0.66, 0, 0.34, 1) forwards,
  onramadanlighttwo 0.7s cubic-bezier(0.25, 0.1, 0.25, 1) 5s forwards; 
}

@keyframes onramadanlightone{
  100% {
    top: 580px;
    left: 450px;
    transform: rotate(5deg) scale(0.40);
  }
}
/* @keyframes onramadanlighttwo{
  100% {
    top: 580px;
    left: 450px;
  transform: scale(0.55);
  }
} */



.rightfreeramadanlight{
  top: 135px; 
  left: 445px;
  transform: rotate(-100deg) scale(0.70);
  filter: sepia(1.5) saturate(2.5) hue-rotate(-3deg) brightness(0.9);
  position: absolute;
  opacity: 0.5;
  z-index: 2;
  animation: 
  rightfreeramadanlightone 0.7s cubic-bezier(0.66, 0, 0.34, 1) forwards,
  rightfreeramadanlighttwo 0.7s cubic-bezier(0.25, 0.1, 0.25, 1) 5s forwards; 
}
@keyframes rightfreeramadanlightone{
  100% {
  top: 120px;
  left: 400px;
  opacity: 1;
  transform: scale(0.55);
  }
}

@keyframes rightfreeramadanlighttwo{
  100%{
  opacity: 1;
  top: 120px;
  left: 400px;
  transform: scale(0.55);
  }
}

.topramadanlight{
  position: absolute;
  top: 600px;
  left: 200px;
  z-index: 2;
  transform: scale(1.1);
  filter: sepia(1.5) saturate(2.5) hue-rotate(-3deg) brightness(0.9);
  opacity: 0.5;
  animation: 
  topramadanlightone 0.7s cubic-bezier(0.66, 0, 0.34, 1) forwards,
  topramadanlighttwo 0.7s cubic-bezier(0.25, 0.1, 0.25, 1) 5s forwards; 
}

@keyframes topramadanlightone {
  100% {
  opacity: 1;
  top: 650px;
  left: 300px;
  transform: rotate(101deg);

  }
}

@keyframes topramadanlighttwo {
  100% {
  top: 650px;
  left: 300px;

  }
}

.kahveone{
  position: absolute;
  top: 160px;
  left: 450px;
  z-index: 2;
  opacity: 0.5;
  animation: 
  kahveoneone 0.7s cubic-bezier(0.66, 0, 0.34, 1) forwards,
  kahveonetwo 0.7s cubic-bezier(0.25, 0.1, 0.25, 1) 5s forwards; 
}

@keyframes kahveoneone {
  100% {
    opacity: 1;
    top: 160px;
    left: 450px;
  }
}@keyframes kahveonetwo {
  100% {
    opacity: 1;
    top: 160px;
    left: 450px;
  }
}
.kahvekayip{
  position: absolute;
  z-index: 2;
  top: 650px;
  left: 510px;
  opacity: 0.5;
  animation: 
  kahvekayipone 0.7s cubic-bezier(0.66, 0, 0.34, 1) forwards,
  kahvekayiptwo 0.7s cubic-bezier(0.25, 0.1, 0.25, 1) 5s forwards; 
}
@keyframes kahvekayipone {
  100% {
  top: 650px;
  left: 510px;
  opacity: 1;

  }
}
@keyframes kahvekayiptwo {
  100% {
  top: 650px;
  left: 510px;
  opacity: 1;

  }
}
.kahvebardak{
  position: absolute;
  top:-1430px;
  left: -30px;
}

.duman{
  position: absolute;
  top:-1430px;
  left: -90px;
}

.kahvealt{
  position: absolute;
  z-index: 2;
  opacity: 0.5;
  top: 660px;
  left: 310px;
  animation: 
  kahvealtone 0.7s cubic-bezier(0.66, 0, 0.34, 1) forwards,
  kahvealttwo 0.7s cubic-bezier(0.25, 0.1, 0.25, 1) 5s forwards; 
  
}
@keyframes kahvealtone {
  100% {
  top: 660px;
  left: 310px;
  opacity: 1;
  }
}
@keyframes kahvealttwo {
  100% {
  top: 660px;
  left: 310px;
  opacity: 1;

  }
}
.hardcoffe{
  position: relative;
  left: -780px;
  top: -1360px;
  transform: scale(1.2);
  opacity: 0.5;
  animation: 
  hardcoffeone 0.7s cubic-bezier(0.66, 0, 0.34, 1) forwards,
  hardcoffetwo 0.7s cubic-bezier(0.25, 0.1, 0.25, 1) 5s forwards; 
  
}
@keyframes hardcoffeone {
  100% {
    left: -780px;
    top: -1360px;
  opacity: 1;
  }
}
@keyframes hardcoffetwo {
  100% {
    left: -780px;
    top: -1360px;
  opacity: 1;

  }
}
</style>