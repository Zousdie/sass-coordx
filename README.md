# sass-coordx

Sass basic toolbox. Make writing CSS less boring...

## Install

```
npm i sass-coordx -D
```

```scss
@import "~sass-coordx";
```

## BEM

write BEM

From [waynecz/Watson](https://github.com/waynecz/Watson)

## Responsive

Default breakpoint:

- xs: 0 - 575
- sm: 576 - 767
- md: 768 - 991
- lg: 992 - 1199
- xl: 1200 - Inf

Default defined breakpoints:

```scss
$--res-breakpoints: (
  "xs": "max-width: #{$--sm}",
  "sm": "min-width: #{$--sm}",
  "md": "min-width: #{$--md}",
  "lg": "min-width: #{$--lg}",
  "xl": "min-width: #{$--xl}"
) !default;

$--res-breakpoints-spec: (
  "xs-only": "max-width: #{$--sm - 1}",
  "sm-and-up": "min-width: #{$--sm}",
  "sm-only": "min-width: #{$--sm}) and (max-width: #{$--md} - 1",
  "sm-and-down": "max-width: #{$--md - 1}",
  "md-and-up": "min-width: #{$--md}",
  "md-only": "min-width: #{$--md}) and (max-width: #{$--lg } - 1",
  "md-and-down": "max-width: #{$--lg - 1}",
  "lg-and-up": "min-width: #{$--lg}",
  "lg-only": "min-width: #{$--lg}) and (max-width: #{$--xl } - 1",
  "lg-and-down": "max-width: #{$--xl - 1}",
  "xl-only": "min-width: #{$--xl}"
) !default;

$--res-breakpoints-orientation: (
  "landscape": "orientation: landscape",
  "portrait": "orientation: portrait"
) !default;
```

How to use:

```scss
$height: (
  "sm-and-down": 20px,
  "md-and-up": 30px
);

.demo {
  @include resl($height, flex-basis, $--res-breakpoints-spec);
}
```

## Others

to be continued...
