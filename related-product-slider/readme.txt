After extension installation follow below steps :

Open this file : templae/catalog/product/list/related.phtml

>> raplace two div tag :

1) <!-- <ol class="mini-products-list" id="block-related"> -->
        <ol class="bxslider" id="block-related">
2) <!-- <li class="item"> -->
         <li class="crsl-item">

>> Add this code at bottom of the page :

  <script type="text/javascript" src="<?php echo $this->getSkinUrl('js/jquery.bxslider.js', array('_secure'=>true));?>"></script>
  <script type="text/javascript" src="<?php echo $this->getSkinUrl('js/jquery.bxslider.min.js', array('_secure'=>true));?>"></script>
  <link rel="stylesheet" href="<?php echo $this->getSkinUrl(); ?>css/related.css" type="text/css" />
  <script>
      $j = jQuery.noConflict();
      $j(document).ready(function(){
      $j('.bxslider').bxSlider({
          minSlides: 4,
          maxSlides: 4,
          slideWidth: 245,
          slideMargin: 5
  });
      });
  </script>

