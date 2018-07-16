# Custom collection of handy sass mixins for Boostrap 4.

Dome extra handy classes for Boostrap 4. I commited it for personal usage. But if you find it handy - feel free to use it as well.

## System Requirements

* [Boostrap 4](https://github.com/twbs/bootstrap)


## Installation

To install enter the following command, second "npm instal" command is used to download files from repository:

```
npm install --save Omi0/boostrap-mixins#master
npm install
```

To update enter the following command. Which removed local files and reupload them from repository again

```
npm uninstall @omio/boostrap-mixins && npm install
```

To use you need to add this line to your styles.scss file.

```
@import "./node_modules/@omio/boostrap-mixins/scss/mixins.scss";
or
@import "~@omio/boostrap-mixins/scss/mixins.scss";
```

which must be placed after you import your variables.scss

```
@import "./variables.scss";
@import "~bootstrap/scss/bootstrap.scss";

```

So the result is something like

```
@import "./variables.scss";
@import "~bootstrap/scss/bootstrap.scss";
@import "~@omio/boostrap-mixins/scss/mixins.scss";
```

After that you can use custom generated classes in your project.

## Mixins

### Responsive Border

border-{breakpoint}-{side}
border-{breakpoint}-{side}-none
sides: top, right, bottom, left, x, y

Classes Examples:

```
border-md-right
border-lg-x-none
```

### Responsive Negative Margings

Very handy when you need to removed spaces based on resulution. Expecially remove top and bottom gaps.

mn{side}-{breakpoint}-{size}
sides: t, b, r, l
sizes used $spacers array (can be extended). By defaults they are 1-5.

Classes Examples:

```
mnt-sm-1
mnb-xl-5
```

### Responsive Headings

Usefull when you need to change the size of the text

{heading}-{breakpoint}
headings: h1-h6

Classes Examples:

```
h1-sm
h5-lg
```

### Responsive Displays

Displays is super large heading. Thus it must be responsive. Otherwise you will end up having a hude text for a small display

display-{breakpoint}-{size}
sizes: 1-4

Classes Examples:

```
display-md-4
display-lg-1
```

### Responsive Width, Height, Min-Height

Displays is super large heading. Thus it must be responsive. Otherwise you will end up having a hude text for a small display

w-{breakpoint}-{size}
h-{breakpoint}-{size}
hm-{breakpoint}-{size}

sizes inherits $sizes array and it can be extended. By default it has: 25, 50, 75, 100, auto. There is extra size: 'gutter' (only for width) which limits a width minus $grid-gutter-width property. Ideally it need to be used with horizontal margins 'mx-auto'

For height $sizes array must be modified. Because relative persentages can't be used for height property

To add extra options to $sizes you need to add following into your variables.scss:

```
$sizes: (
  100px: 100px,
  200px: 200px,
  300px: 300px,
  400px: 400px,
  500px: 500px,
  600px: 600px
);
```

Classes Examples:

```
w-sm-gutter
w-xl-75 (75% of the width for xl)
h-md-500px
hm-200px (min-height to 200px for xs)
hm-lg-500px (min-height to 500px to lg)
```

### Responsive Font-Weight

Implements $font-weight-light, $font-weight-normal, $font-weight-bold properties

fw-{breakpoint}-{size}
sizes: light, normal, bold

Classes Examples:

```
fw-normal
fw-md-bold
```

### Responsive Line-Height

lh-{breakpoint}-{size}
sizes: initial, md (for 1.5), lg (for 2)

Classes Examples:

```
lh-initial
lh-sm-md
lh-lg-lg
```

### Responsive Buttons

Default boostrap has only btn-sm or btn-lg classes. We also addes extra btn-md class which is something in the between btn-sm or btn-lg.
Idea of this is to be able to make action buttons responsive

btn-{breakpoint}-{size}
sizes: sm, md, lg

Classes Examples:

```
btn-sm
btn-md-md
btn-lg-lg
```
