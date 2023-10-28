<template>
    <div class="sticky-top" style="height: 100%; z-index:-1">
      <img src="../assets/Frame_5.png" alt="logo" style="width: 100%; height: 100%; object-fit:cover;">
    </div>
    <div class="sticky-top" style="height: 100%; z-index:-1">
      <img src="../assets/Frame_6.png" alt="logo" style="width: 100%; height: 100%; object-fit:cover;">
    </div>
    <div class="sticky-top" style="height: 100%; z-index:-1">
      <img src="../assets/Frame_7.png" alt="logo" style="width: 100%; height: 100%; object-fit:cover;">
    </div>
    <div class="sticky-top" style="height: 100%; z-index:-1">
      <img src="../assets/Frame_31.png" alt="logo" style="width: 100%; height: 100%; object-fit:cover;">
    </div>
    <div  style="height: 100%; z-index:1">
      <img src="../assets/Frame_15.png" alt="logo" style="width: 100%; height: 100%; object-fit:cover;">
    </div>

    <div class="frame">
        <div class="group"><div class="text-wrapper">TESTIMONIALS</div></div>
        <div class="div">
            <div class="group-wrapper">
                <div class="div-wrapper" onmouseover="showText(1)" onmouseout="hideText(1)" ><div class="text-wrapper-2" id="text-1"></div></div>
            </div>
            <div class="overlap-group-wrapper">
                <div class="overlap-group">
                    <div class="group-2" onmouseover="showText(2)" onmouseout="hideText(2)" ><div class="text-wrapper-2" id="text-2"></div></div>
                </div>
            </div>
            <div class="overlap-wrapper">
                <div class="overlap">
                    <div class="group-3" onmouseover="showText(3)" onmouseout="hideText(3)" ><div class="text-wrapper-2" id="text-3"></div></div>
                </div>
            </div>
            <div class="group-wrapper-2">
                <div class="group-4" onmouseover="showText(0)" onmouseout="hideText(0)" ><div class="text-wrapper-2" id="text-0"></div></div>
            </div>
        </div>
    </div>
            
</template>

<script>
/* eslint-disable */
export default {
    name: 'Main',
    methods: {
        showText(index) {
            const textElement = document.getElementById(`text-${index}`);
            fetch("https://elitefit4you.com/test-api/testimonials.json")
              .then((response) => response.json())
              .then((data) => {
                  //console.log(data);
                  //textElement.textContent = data["testimonials"][index]["message"];
              });
            textElement.style.display = 'block';
        },
        hideText(index) {
            const textElement = document.getElementById(`text-${index}`);
            textElement.style.display = 'none';
        }
    }
};

</script>
<style scoped>
.frame {
    position: relative;
    width: 100%;
    height: 552px;
    background-color: #ffffff;
    z-index: 5;
}

.frame .group {
  margin-bottom: 10px;
}

.frame .text-wrapper {
  font-size: 24px;
  font-weight: bold;
}

.frame .div {
  flex-wrap: wrap;
}

.frame .group-wrapper {
  width: 25%;
  padding: 10px;
  background-image: url(../assets/emily-image.jpg);
}

.frame .div-wrapper {
  background-color: #fff;
  border-radius: 5px;
  padding: 20px;
  box-shadow: 0px 0px 5px rgba(0, 0, 0, 0.1);
  cursor: pointer;
}

.frame .text-wrapper-2 {
  display: block;
}

.frame .overlap-group-wrapper {
    left: 640px;
    position: absolute;
    width: 277px;
    height: 277px;
    top: 0;
    border-radius: 20px;
    overflow: hidden;
    box-shadow: 0px 4px 4px #00000040;
}

.frame .overlap-group {
    width: 352px;
    height: 626px;
    top: -253px;
    left: -38px;
    background-image: url(../assets/david-image.jpg);
    position: relative;
    background-size: cover;
    background-position: 50% 50%;
}

.frame .group-2 {
    width: 143px;
    top: 369px;
    left: 107px;
    position: relative;
    height: 45px;
}

.frame .overlap-wrapper {
    left: 954px;
    position: absolute;
    width: 277px;
    height: 277px;
    top: 0;
    border-radius: 20px;
    overflow: hidden;
    box-shadow: 0px 4px 4px #00000040;
}

.frame .overlap {
    width: 331px;
    height: 441px;
    top: -164px;
    left: -27px;
    background-image: url(../assets/lisa-image.jpg);
    position: relative;
    background-size: cover;
    background-position: 50% 50%;
}

.frame .group-3 {
    width: 119px;
    top: 280px;
    left: 108px;
    position: relative;
    height: 45px;
}

.frame .group-wrapper-2 {
    left: 0;
    background-image: url(../assets/alex-image.jpg);
    background-size: 100% 100%;
    position: absolute;
    width: 277px;
    height: 277px;
    top: 0;
    border-radius: 20px;
    overflow: hidden;
    box-shadow: 0px 4px 4px #00000040;
}

.frame .group-4 {
    width: 116px;
    top: 116px;
    left: 82px;
    position: relative;
    height: 45px;
}

#div-wrapper:hover{
    filter: brightness(20%);
}
#group-2:hover{
    filter: brightness(20%);
}
#group-3:hover{
    filter: brightness(20%);
}
#group-4:hover{
    filter: brightness(20%);
}

.div {
  flex-wrap: wrap;
}
</style>


