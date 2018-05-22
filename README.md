# revolution-slider
Preload Revolution Slider- solved preload problem with a fullscreen revolution slider.


preloadImages = function(imageIndex) {
      var image = $(".tp-bgimg .tp-bgimg[src=" + imageIndex + "]");
      var preloadedImage = jQuery(new Image()).attr("src", image.attr("data-full-url"));
      preloadedImage.load(function() {
        preloadImages(imageIndex + 1);
      });
    }
    preloadImages(1)


});

