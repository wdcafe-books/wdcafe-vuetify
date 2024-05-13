# CH8.  Cards

  

  

  

##  1. Font Icons 사용하기

  

The `v-card` component is a stylish way to wrap different types of content; such as tables, images, or user actions.

  

  

## API

| Component | Description |
| --- | --- |
| [v-card](https://vuetifyjs.com/en/api/v-card/) | Primary Component |
| [v-card-item](https://vuetifyjs.com/en/api/v-card-item/) | Sub-component used to wrap the Card’s `v-card-title` and `v-card-subtitle` components. |
| [v-card-title](https://vuetifyjs.com/en/api/v-card-title/) | Sub-component used to display the Card’s title. Wraps the `#title` slot |
| [v-card-subtitle](https://vuetifyjs.com/en/api/v-card-subtitle/) | Sub-component used to display the Card’s subtitle. Wraps the `#subtitle` slot. |
| [v-card-text](https://vuetifyjs.com/en/api/v-card-text/) | Sub-component used to display the Card’s text. Wraps the `#text` slot. |
| [v-card-actions](https://vuetifyjs.com/en/api/v-card-actions/) | Sub-component that modifies the default styling of [v-btn](https://vuetifyjs.com/en/components/buttons/). Wraps the `#actions` slot |

  

| Element / Area | Description |
| --- | --- |
| 1\. Container | The Card container holds all `v-card` components. Composed of 3 major parts: `v-card-item`, `v-card-text`, and `v-card-actions` |
| 2\. Title (optional) | A heading with increased **font-size** |
| 3\. Subtitle (optional) | A subheading with a lower emphasis text color |
| 4\. Text (optional) | A content area with a lower emphasis text color |
| 5\. Actions (optional) | A content area that typically contains one or more [v-btn](https://vuetifyjs.com/en/components/buttons/) components |

  

  

## Variants

  

The **variant** prop gives you easy access to several different card styles. Available variants are: **elevated**(default), **flat**, **tonal**, **outlined**, **text**, and **plain**.

| Value | Description |
| --- | --- |
| **elevated** | Elevates the card with a shadow |
| **flat** | Removes card shadow and border |
| **tonal** | Background color is a lowered opacity of the color |
| **outlined** | Applies a thin border and card has zero elevation |
| **text** | Removes the background and removes shadow |
| **plain** | Removes the background and lowers the opacity until hovered |

  

  

  

  

* * *

  

  

## 1\. 예시 샘플(1)

  

```
<template>
  <div class="cards">
    <h1 class="text-center mb-10">Cards Page</h1>

    <v-container>
      <div class="v-row">
        <div class="v-col" v-for="num in 4" :key="num">
          <v-card variant="outlined" border="dashed thin" hover>
            <v-card-title>This is Title</v-card-title>
            <v-card-subtitle>This is Sub Title</v-card-subtitle>
            <v-card-text>Lorem ipsum dolor sit amet consectetur adipisicing elit. Harum accusamus hic mollitia ad illum cupiditate dicta ipsam error repellat, et ullam numquam ex expedita cumque quasi temporibus iusto maiores consectetur!</v-card-text>

            <v-divider></v-divider>

            <v-card-actions class="d-flex justify-lg-space-between">
              <v-btn>
                <v-icon>mdi:mdi-delete</v-icon>
                <v-icon>mdi:mdi-share</v-icon>
              </v-btn>

              <v-chip>my chip</v-chip>
            </v-card-actions>
          </v-card>
        </div>
      </div>
      <v-row>
        <v-col class="d-flex">
          <v-card
            class="mx-auto"
            width="344"
            max-width="344"
          >
            <v-img
              height="200px"
              src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
              cover
            ></v-img>

            <v-card-title>
              Top western road trips
            </v-card-title>

            <v-card-subtitle>
              1,000 miles of wonder
            </v-card-subtitle>

            <v-card-actions>
              <v-btn
                color="orange-lighten-2"
                text="Explore"
              ></v-btn>

              <v-spacer></v-spacer>

              <v-btn
                :icon="show ? 'mdi:mdi-chevron-up' : 'mdi:mdi-chevron-down'"
                @click="show = !show"
              ></v-btn>
            </v-card-actions>

            <v-expand-transition>
              <div v-show="show">
                <v-divider></v-divider>

                <v-card-text>
                  I'm a thing. But, like most politicians, he promised more than he could deliver. You won't have time for sleeping, soldier, not with all the bed making you'll be doing. Then we'll go with that data file! Hey, you add a one and two zeros to that or we walk! You're going to do his laundry? I've got to find a way to escape.
                </v-card-text>
              </div>
            </v-expand-transition>
          </v-card>

          <v-card
            class="mx-auto"
            width="344"
            max-width="400"
          >
            <v-img
              class="align-end text-white"
              height="200"
              src="https://cdn.vuetifyjs.com/images/cards/docks.jpg"
              cover
            >
              <v-card-title>Top 10 Australian beaches</v-card-title>
            </v-img>

            <v-card-subtitle class="pt-4">
              Number 10
            </v-card-subtitle>

            <v-card-text>
              <div>Whitehaven Beach</div>

              <div>Whitsunday Island, Whitsunday Islands</div>
            </v-card-text>

            <v-card-actions>
              <v-btn color="orange" text="Share"></v-btn>

              <v-btn color="orange" text="Explore"></v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  name: 'CardView',
  data: () => ({
    show: false,
  }),
};
</script>

<style scoped lang="scss">
  .v-container{
    >.v-row{
      margin-bottom: 50px;
    }
  }
</style>
```