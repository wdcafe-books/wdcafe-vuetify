# CH3.  Grid System

  

## 1\. 그리드 샘플

  

```
<template>
  <div class="home">
    <v-container>
      <v-row>
        <v-col><h1 class="text-center">Home Page</h1></v-col>
      </v-row>
      <v-row>
        <v-col>Box1</v-col>
        <v-col>Box2</v-col>
        <v-col>Box3</v-col>
      </v-row>
      <v-row>
        <v-col cols="12">Col 12</v-col>
      </v-row>
      <v-row>
        <v-col cols="3">Col 3</v-col>
        <v-col cols="3">Col 3</v-col>
        <v-col cols="3">Col 3</v-col>
        <v-col cols="3">Col 3</v-col>
      </v-row> 
      <v-row>
        <v-col cols="4">Col 1</v-col>
        <v-col cols="4">Col 2</v-col>
        <v-col cols="4">Col 3</v-col>
      </v-row>
      <v-row>
        <v-col cols="6">
          <v-row>
            <v-col>Box1</v-col>
            <v-col>Box2</v-col>
            <v-col>Box3</v-col>
          </v-row>
        </v-col>
        <v-col cols="6">Col 2</v-col>
      </v-row>      
    </v-container>

    <v-container>
      <v-row>
        <v-col cols="12" sm="6" md="4" lg="3" xl="3" xxl="3"><div class="box">Responsive</div></v-col>
        <v-col cols="12" sm="6" md="4" lg="3" xl="3" xxl="3"><div class="box">Responsive</div></v-col>
        <v-col cols="12" sm="6" md="4" lg="3" xl="3" xxl="3"><div class="box">Responsive</div></v-col>
        <v-col cols="12" sm="6" md="4" lg="3" xl="3" xxl="3"><div class="box">Responsive</div></v-col>
      </v-row>
    </v-container>

    <v-container fluid>
      <v-row>
        <v-col cols="12" class="text-center"><div class="purple-lighten-3">Col1</div></v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
// Components
// import HelloWorld from '../components/HelloWorld.vue';

export default ({
  name: 'HomeView',
});
</script>

<style scoped lang="scss">
  .v-container{
    margin-bottom: 50px;
    >.v-row{
      margin-bottom: 20px;
    }
    .v-col{
      border: 1px solid #000;
    }
    .box{
      border: 1px solid #000;
    }
  }
</style>
```