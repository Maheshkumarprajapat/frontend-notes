# Slick Carousel With Responsive

### Installation
```
npm install react-slick
npm install slick-carousel	
```

### Include CSS
```
import "slick-carousel/slick/slick.css"; 
import "slick-carousel/slick/slick-theme.css";
```

### Single Item
```
import React from "react";
import Slider from "react-slick";

export default function SlickSlider() {
  let settings = {
    dots: false,
    autoplay: true,
    autoplaySpeed: 3000,
    slidesToShow: 4,
    slidesToScroll: 4,
    nextArrow: ( <img src="" alt="IconRightArrow" />),
    prevArrow: ( <img src="" alt="IconLeftArrow" />),
    responsive: [
        {
          breakpoint: 1024,
          settings: {
            slidesToShow: 3,
            slidesToScroll: 3,
            infinite: true,
            dots: true
          }
        },
        {
          breakpoint: 600,
          settings: {
            slidesToShow: 2,
            slidesToScroll: 2,
            initialSlide: 2
          }
        },
        {
          breakpoint: 480,
          settings: {
            slidesToShow: 1,
            slidesToScroll: 1
          }
        }
      ]
  };
  return (
  	<Slider {...settings}>
       <div>
         <h3>1</h3>
          </div>
          <div>
            <h3>2</h3>
          </div>
          <div>
            <h3>3</h3>
          </div>
          <div>
            <h3>4</h3>
          </div>
          <div>
            <h3>5</h3>
          </div>
          <div>
            <h3>6</h3>
          </div>
      </Slider>
  );
}


```