let slideIndex = 1;

function plusSlides(n) {
  $('mySlides1').click(function (e) { 
    alert('bo')
  });
}

function currentSlide(n) {
  showSlider((slideIndex = n));
}

function showSlider(n) {
  let slides = document.getElementsByClassName("mySlides");
  let dots = document.getElementsByClassName("dot");
  if (n > slides.length) {
    slideIndex = 1;
  }
  if (n < 1) {
    slideIndex = slides.length;
  }
  // 全部輪撥隱藏先行隱藏
  // 條件[i]到達該屬性時添加
  for (i = 0; i < slides.length; i++) {
    // slides[i].style.display = "none";
  }
  // 該[i]dot給予置換為空class
  for (i = 0; i < dots.length; i++) {
    dots[i].className = dots[i].className.replace("active", "");
  }

  slides[slideIndex - 1].setAttribute("style", "display:block");
}

// showSlides();

function showSlides() {
  var i;
  var slides = document.getElementsByClassName("mySlides");
  let dots = document.getElementsByClassName("dot");
  for (i = 0; i < slides.length; i++) {
    slides[i].style.display = "none";
  }
  for (i = 0; i < dots.length; i++) {
    dots[i].className = dots[i].className.replace("active", "");
  }
  slideIndex++;
  if (slideIndex > slides.length) {
    slideIndex = 1;
  }
  slides[slideIndex - 1].style.display = "block";
  setTimeout(showSlides, 2000); // Change image every 2 seconds
}
// 輪播數量
let imgNub = document.getElementsByClassName("mySlides").length; //轮播图片数量
console.log(imgNub);
// show();

function show() {
  let img = document.getElementsByClassName("mySlides");
  console.log(img);
  //获取轮播图片数量
  for (i = 0; i < imgNub; i++) {
    img[i].setAttribute("id", i);
  }

  //根据轮播图片数量设定图片位置对应的class
  //img3为中央展示位
  //img2 && img 4分别为左右
  if (imgNub == 1) {
    //img3
    for (i = 0; i < imgNub; i++) {
      document
        .getElementsByClassName(`mySlides .mySlides${i}`)
        .addClass("mySlides2");
    }
  }
  if (imgNub == 2) {
    //img 3、4
    for (i = 0; i < imgNub; i++) {
      $(".carousel .img:eq(" + i + ")").addClass("img" + (i + 3));
    }
  }
  if (imgNub == 3) {
    //img 2、3、4
    for (i = 0; i < imgNub; i++) {
      img[i].classList.add(`mySlides${i + 1}`);
    }
  }
}

// setInterval
var sliderTimes = null;
function sliderRight(){
   let i = 3;
  $(`.mySlides3`)
    .removeClass(`mySlides3`)
    .addClass(`mySlides4`);
  $(`.mySlides2`)
    .removeClass(`mySlides2`)
    .addClass(`mySlides3`);
  $(`.mySlides1`)
    .removeClass(`mySlides1`)
    .addClass(`mySlides2`);
  $(`.mySlides4`)
    .removeClass(`mySlides4`)
    .addClass(`mySlides1`);
}
function sliderLeft(){
  let i = 3;
  $(`.mySlides3`)
    .removeClass(`mySlides3`)
    .addClass(`mySlides4`);
  $(`.mySlides2`)
    .removeClass(`mySlides2`)
    .addClass(`mySlides3`);
  $(`.mySlides1`)
    .removeClass(`mySlides1`)
    .addClass(`mySlides2`);
  $(`.mySlides4`)
    .removeClass(`mySlides4`)
    .addClass(`mySlides1`);
}
function loopSlider(){
     if(sliderTimes){
	     window.clearInterval(sliderTimes)
	 }
	sliderRight()
	sliderTimes = window.setInterval(() => {
	  sliderRight()
	}, 5000);
}
loopSlider()
$("#arrow-right").click(function(){
   loopSlider()
})
$("#arrow-left").click(function(){
     if(sliderTimes){
	     window.clearInterval(sliderTimes)
	 }
	sliderLeft()
   loopSlider()
})