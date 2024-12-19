<script>
    
</script>

<div class="background">
    <div class="quad-circle-2"></div>
    <div class="triangle-1"></div>
    <div class="quad-circle-2"></div>
    <div class="triangle-2"></div>

    <div class="quad-circle-1"></div>
    <div class="square-1"></div>
    <div class="triangle-2"></div>
    <div class="square-1"></div>
    
    <div class="quad-circle-1"></div>
    <div class="triangle-1"></div>
    <div class="quad-circle-2"></div>
    <div class="quad-circle-1"></div>

    <div class="quad-circle-3"></div>
    <div class="quad-circle-4"></div>
    <div class="quad-circle-2"></div>
    <div class="triangle-3"></div>

    <div class="square-1"></div>
    <div class="triangle-4"></div>
    <div class="square-1"></div>
    <div class="quad-circle-1"></div>


</div>

<style>
.background {
    background-color: #ffd97d;
    width: 100%;
    height: 100%;
    position: fixed;
    z-index: 99;
    view-transition-name: background;
    /* transform: translateX(101%); */
}

.quad-circle-1 {
  width: 100px;
  height: 100px;
  background: red;
  border-radius: 50%
}

.quad-circle-2 {
    width: 100px;
    height: 100px;
    display: block;
    background-color: aqua;
    border-radius: 0 0 240px 0;
}

.triangle-3 {
    width: 0;
    height: 0;
    border-top: 100px solid red;
    border-right: 100px solid transparent;
}
</style>