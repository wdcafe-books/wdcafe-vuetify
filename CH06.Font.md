# CH6.  Font

  

Control text size, alignment, wrapping, overflow, transforms and more. By default, Vuetify uses the Material Design specification [Roboto Font](https://fonts.google.com/specimen/Roboto).

  

## 1. Typography

  

Control the size and style of text using the Typography helper classes. These values are based upon the [Material Design type specification](https://material.io/design/typography/the-type-system.html).

  

- Heading 1  text-h1
- Heading 2  text-h2
- Heading 3  text-h3
- Heading 4  text-h4
- Heading 5  text-h5
- Heading 6  text-h6
- Subtitle 1    text-subtitle-1
- Subtitle 2    text-subtitle-2
- Body 1    text-body-1
- Body 2    text-body-2
- BUTTON   text-button
- Caption   text-caption
- OVERLINE  text-overline

  

  

## 2. Font Weight

  

```
<template>
  <div>
    <p class="font-weight-black">
      Black text.
    </p>
    <p class="font-weight-bold">
      Bold text.
    </p>
    <p class="font-weight-medium">
      Medium weight text.
    </p>
    <p class="font-weight-regular">
      Normal weight text.
    </p>
    <p class="font-weight-light">
      Light weight text.
    </p>
    <p class="font-weight-thin">
      Thin weight text.
    </p>
    <p class="font-italic">
      Italic text.
    </p>
  </div>
</template>
```

  

  

## 3\. Text Align

  

```
<template>
  <div>
    <p class="text-left">
      Left aligned on all viewport sizes.
    </p>
    <p class="text-center">
      Center aligned on all viewport sizes.
    </p>
    <p class="text-right">
      Right aligned on all viewport sizes.
    </p>

    <p class="text-sm-left">
      Left aligned on viewports SM (small) or wider.
    </p>
    <p class="text-right text-md-left">
      Left aligned on viewports MD (medium) or wider.
    </p>
    <p class="text-right text-lg-left">
      Left aligned on viewports LG (large) or wider.
    </p>
    <p class="text-right text-xl-left">
      Left aligned on viewports XL (extra-large) or wider.
    </p>
  </div>
</template>
```

  

  

## 4\. Text Abbreviation (말줄임...)

```
<template>
  <div>
    <span
      class="d-inline-block text-truncate"
      style="max-width: 150px;"
    >
      Suspendisse faucibus, nunc et pellentesque egestas, lacus ante convallis tellus.
    </span>
  </div>
</template>
```

  

  

  

* * *

  

  

## 5\. 예시 샘플

  

- Font Sample1

```
<template>
  <div class="grid">
    <v-container>
      <v-row>
        <v-col><h1 class="text-center">Font Page</h1></v-col>
      </v-row>   
      <v-row>
        <v-col class="d-flex flex-column border">
          <h3 class="text-h4">Text</h3>
          <h3 class="text-subtitle-1">Text</h3>
          <h3 class="text-subtitle-2">Text</h3>
          <h3 class="text-body-1">Text</h3>
          <h3 class="text-body-3">Text</h3>
          <h3 class="text-button">Text</h3>
          <h2 class="text-left">Text</h2>
          <h2 class="text-center">Text</h2>
          <h2 class="text-right">Text</h2>
          <h2 class="text-center font-weight-light">This is homepage</h2>
          <p class="text-center font-weight-bold">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Adipisci veniam sequi eligendi facere unde? Sint deleniti nobis, aspernatur aliquid, rem aut similique id architecto asperiores harum labore, quaerat quas consectetur.</p>
        </v-col>
      </v-row>
    </v-container>

  </div>
</template>

<script>
// Components
// import HelloWorld from '../components/HelloWorld.vue';

export default ({
  name: 'GridView',
});
</script>

<style scoped lang="scss">
  .v-container{
    margin-bottom: 50px;
    >.v-row{
      margin-bottom: 20px;

      h2, h3, p{
        margin-bottom: 30px;
      }
    }
  }
</style>
```

  

  

- Font Weight Sample

```
<template>
  <div>
    <p class="font-weight-black">
      Black text.
    </p>
    <p class="font-weight-bold">
      Bold text.
    </p>
    <p class="font-weight-medium">
      Medium weight text.
    </p>
    <p class="font-weight-regular">
      Normal weight text.
    </p>
    <p class="font-weight-light">
      Light weight text.
    </p>
    <p class="font-weight-thin">
      Thin weight text.
    </p>
    <p class="font-italic">
      Italic text.
    </p>
  </div>
</template>
```

  

  

- Align Sample

```
<template>
  <div>
    <p class="text-left">
      Left aligned on all viewport sizes.
    </p>
    <p class="text-center">
      Center aligned on all viewport sizes.
    </p>
    <p class="text-right">
      Right aligned on all viewport sizes.
    </p>

    <p class="text-sm-left">
      Left aligned on viewports SM (small) or wider.
    </p>
    <p class="text-right text-md-left">
      Left aligned on viewports MD (medium) or wider.
    </p>
    <p class="text-right text-lg-left">
      Left aligned on viewports LG (large) or wider.
    </p>
    <p class="text-right text-xl-left">
      Left aligned on viewports XL (extra-large) or wider.
    </p>
  </div>
</template>
```

  

  

- Text Decoration Sample

```
<template>
  <div class="d-flex justify-space-between flex-row">
    <a
      class="text-decoration-none"
      href="#"
    >
      Non-underlined link
    </a>

    <div class="text-decoration-line-through">
      Line-through text
    </div>

    <div class="text-decoration-overline">
      Overline text
    </div>

    <div class="text-decoration-underline">
      Underline text
    </div>
  </div>
</template>
```

  

  

- Teansform

```
<template>
  <div>
    <p class="text-lowercase">
      Lowercased text.
    </p>
    <p class="text-uppercase">
      Uppercased text.
    </p>
    <p class="text-capitalize">
      capitalized text.
    </p>
  </div>
</template>
```