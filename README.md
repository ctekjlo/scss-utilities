# SCSS

### Retina Sprites (_retina.scss)

```scss
    $sprites: sprite-map("sprites/*.png", $spacing: 40px); // $layout: diagonal;
    $sprites2x: sprite-map("sprites-retina/*.png", $spacing: 80px); // $layout: diagonal;

    // @include retina(button-add);
    // @include x2(button-add);

    //                 .button-add .button-add:hover .button-add:active + retina
    // $classes: true  .button-add .button-add.hover .button-add.active + retina
    .button-add {
        @include x2(button-add, $hover: true, $active: true, $classes: false);
    }

    //                 .button-add .button-add:hover + retina
    // $classes: true  .button-add .button-add.hover + retina
    .button-add {
        @include x2(button-add, $hover: true);
    }

    //                 .button-add .button-add:active + retina
    // $classes: true  .button-add .button-add.active + retina
    .button-add {
        @include x2(button-add, $active: true);
    }

    //                 .button-add + retina
    // $classes: true  .button-add + retina
    .button-add {
        @include x2(button-add);
    }
