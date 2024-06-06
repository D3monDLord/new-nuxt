<template>
  <v-app class="blue-lighten-3">
    <navbar />

    <section class="py-10">
      <v-container>
        <v-row class="align-center">
          <v-col md="6" cols="12">
            <v-img
              height="400"
              cover
              rounded
              src="https://th.bing.com/th/id/OIP.qLWyLYtT84QM91zO8AI1cwHaH0?rs=1&pid=ImgDetMain"
            ></v-img>
          </v-col>

          <v-col col="12" md="6">
            rimuru tempest In their normal form — referred to as slime form
            ｢スライム形態フォーム, suraimu fōmu｣ — Rimuru takes the appearance of a
            spherical — sometimes amorphous — mass of slightly blue and translucent ooze.
            Rimuru's initial slime form has a diameter of around 40 cm and it increases as
            they get stronger across the series, becoming around 80 cm after reincarnating
            into an ultimate slime.
          </v-col>
        </v-row>
      </v-container>

      <section>
        <v-container>
          <v-row> 
            <v-col
             cols="12" 
            md="6" 
            lg="4"
             v-for="meal in product.meals" 
             :key="meal">

             <v-card height="300" hover>
              <v-img height="250" cover :src="meal.strMealThumb"></v-img>
            </v-card>
            <v-card-title>{{ meal.strMeal }}</v-card-title>
       

            </v-col>
           </v-row>
        </v-container>

    
      </section>
    </section>
  </v-app>
</template>

<script setup>

const { data: product } = useFetch(
  "http://www.themealdb.com/api/json/v1/1/filter.php?c=Seafood"
);
</script>

<style lang="scss" scoped></style>
