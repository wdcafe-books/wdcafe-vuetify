# CH9.  Expansion panels

  

  

  

##  1. Expansion panels 사용하기

  

The `v-expansion-panel` component is useful for reducing vertical space with large amounts of information. The default functionality of the component is to only display one expansion-panel body at a time; however, with the `multiple` property, the expansion-panel can remain open until explicitly closed.

  

  

## API

| Component | Description |
| --- | --- |
| [v-expansion-panels](https://vuetifyjs.com/en/api/v-expansion-panels/) | Primary component |
| [v-expansion-panel](https://vuetifyjs.com/en/api/v-expansion-panel/) | Sub-component that wraps `v-expansion-panel-text` and `v-expansion-panel-title` |
| [v-expansion-panel-title](https://vuetifyjs.com/en/api/v-expansion-panel-title/) | Sub-component used to display the Expansion Panel’s title. Wraps the `#title` slot |
| [v-expansion-panel-text](https://vuetifyjs.com/en/api/v-expansion-panel-text/) | Sub-component used to display the Expanion Panel’s text. Wraps the `#text` slot |

  

  

```
<v-expansion-panels>
  <v-expansion-panel
    title="Title"
    text="Lorem ipsum dolor sit amet consectetur adipisicing elit. Commodi, ratione debitis quis est labore voluptatibus! Eaque cupiditate minima"
  >
  </v-expansion-panel>
</v-expansion-panels>
```

  

  

* * *

  

  

## 1\. 예시 샘플(1)

  

```
<template>
  <div class="expansion-panels">
    
    <h1 class="text-center mb-10">Cards Page</h1>

    <v-container>
      <v-row>
        <v-col>
          <h3>Default</h3>
          <v-expansion-panels>
            <v-expansion-panel
              v-for="i in 3"
              :key="i"
              text="Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat."
              title="Item" 
              expand-icon="mdi:mdi-menu-down"
            ></v-expansion-panel>
          </v-expansion-panels>
        </v-col>
      </v-row>
      <v-row>
        <v-col>
          <h3>Accordion</h3>

          <v-expansion-panels variant="accordion">
            <v-expansion-panel
              v-for="i in 3"
              :key="i"
              text="Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat."
              title="Item" 
              expand-icon="mdi:mdi-menu-down"
            ></v-expansion-panel>
          </v-expansion-panels>
        </v-col>
      </v-row>
      <v-row>
        <v-col>
          <v-expansion-panels>
            <v-expansion-panel>
              <v-expansion-panel-title collapse-icon="mdi:mdi-minus" expand-icon="mdi:mdi-plus">
                Item
              </v-expansion-panel-title>
              <v-expansion-panel-text>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
              </v-expansion-panel-text>
            </v-expansion-panel>

            <v-expansion-panel>
              <v-expansion-panel-title>
                Item
                <template v-slot:actions="{ expanded }">
                  <v-icon :color="!expanded ? 'teal' : ''" :icon="expanded ? 'mdi:mdi-pencil' : 'mdi:mdi-check'"></v-icon>
                </template>
              </v-expansion-panel-title>
              <v-expansion-panel-text>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
              </v-expansion-panel-text>
            </v-expansion-panel>

            <v-expansion-panel>
              <v-expansion-panel-title disable-icon-rotate>
                Item
                <template v-slot:actions>
                  <v-icon color="error" icon="mdi:mdi-alert-circle">
                  </v-icon>
                </template>
              </v-expansion-panel-title>
              <v-expansion-panel-text>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
              </v-expansion-panel-text>
            </v-expansion-panel>
          </v-expansion-panels>
        </v-col>
      </v-row>
    </v-container>

  </div>
</template>

<script>
export default {
  name: 'ExpansionPanels',
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