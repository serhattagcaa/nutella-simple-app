<script>
 import Nutella from "../assets/nutella.png" 
 
</script>
<main>
  <nav class="flex items-center justify-between h-36">
    <div class="pl-28">
      <a href="/">
        <img src={Nutella} alt="A jar of Nutella" width="178" height="133">

      </a>
    </div>
    <div class="flex pr-40 pt-11 space-x-8 relative">
      <div class="searchBox">
        <input id="searchInput" class="font-montserrat font-[500]" type="text" name="İnput" placeholder="Search">
        <img class="searchButton" src="/src/assets/search.svg" alt="">
      </div>
      <a class="font-montserrat font-[500]" href="/nutellacontent">Nutella'nın içinde</a>
      <a class="font-montserrat font-[500]" href="/recipes">Tarifler</a>
      <a class="font-montserrat font-[500]" href="/discover">Keşfet</a>
      <a class="font-montserrat font-[500] text-[#f70000]" href="/products">Ürünler</a>
    </div>
  </nav>
</main>

<style>
  .searchBox {
    position: relative;
    top: -20px;
    right: -25px;
    border-bottom: 2px solid transparent;
    height: 50px;
    padding: 10px;
    background-color: transparent;
  }
  .searchBox:hover {
    border-bottom-color: black;
  }
  .searchBox:hover #searchInput {
    width: 240px;
    padding: 0 6px;
  }
  #searchInput {
    border: none;
    background: none;
    outline: none;
    float: right;
    padding: 0;
    color: black;
    font-size: 16px;
    transition: width 0.4s, padding 0.4s;
    height: 45px;
    width: 0;
    border-bottom: none;
  }
  .searchButton {
    margin-top: 10px;
  }
  @media screen and (max-width: 620px) {
    .searchBox:hover #searchInput {
      width: 150px;
      padding: 0 6px;
    }
  }
</style>
