<template>
  <v-layout row wrap class="pa-3">
    <v-flex v-for="item in items" :key="item.id" sm6 md4>
      <v-card flat class="text-xs-center ma-2">
        <v-card-title class="headline"> {{ item.name }} </v-card-title>
        <v-responsive>
          <v-img :src="item.image" />
        </v-responsive>
        <v-card-text class="subheading">
          <div class="text--primary">Description: {{ item.description }}</div>
          <br />
          <div class="text--primary">Price: {{ item.price }} $</div>
        </v-card-text>
        <v-card-actions class="text-xs-center mx-2">
          <v-spacer />
          <v-btn color="success">
            <v-icon left>mdi-cart</v-icon>
            Add to Cart
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          id: '516',
          name: 'Unisex Thermal Vest',
          description:
            'Our thermal vest, made from organic bamboo with recycled plastic down filling, is a favorite of both men and women. You will help the environment, and have a wear-easy piece for many occasions.',
          price: '95',
          image_title: 'unisex-thermal-vest_lynda_29944',
          image:
            'https://hplussport.com/wp-content/uploads/2016/12/unisex-thermal-vest_LYNDA_29944.jpg',
        },
        {
          id: '514',
          name: 'Grunge Skater Jeans',
          description:
            'Our boy-cut jeans are for men and women who appreciate that skate park fashions are not just for skaters. Made from the softest and most flexible organic cotton denim.',
          price: '68',
          image_title: 'unisex-grunge-jeans_lynda_29937',
          image:
            'https://hplussport.com/wp-content/uploads/2016/12/unisex-grunge-jeans_LYNDA_29937.jpg',
        },
        {
          id: '520',
          name: 'V-Neck Sweater',
          description:
            'This medium-weight sweater, made from organic knitted cotton and bamboo, is the perfect solution to a chilly night at the campground or a misty walk on the beach.',
          price: '65',
          image_title: 'v-neck-sweater-for-men_lynda_29947',
          image:
            'https://hplussport.com/wp-content/uploads/2016/12/v-neck-sweater-for-men_LYNDA_29947.jpg',
        },
        {
          id: '518',
          name: 'V-Neck Pullover',
          description:
            'This organic hemp jersey pullover is perfect in a pinch. Wear for casual days at the office, a game of hoops after work, or running your weekend errands.',
          price: '65',
          image_title: 'v-neck-long-sleeved-pullover_lynda_29946',
          image:
            'https://hplussport.com/wp-content/uploads/2016/12/v-neck-long-sleeved-pullover_LYNDA_29946.jpg',
        },
        {
          id: '500',
          name: 'Thermal Fleece Jacket',
          description:
            'Our thermal organic fleece jacket, is brushed on both sides for ultra softness and warmth. This medium-weight jacket is versatile all year around, and can be worn with layers for the winter season.',
          price: '60',
          image_title: 'thermal-jacket_lynda_29943',
          image:
            'https://hplussport.com/wp-content/uploads/2016/12/thermal-jacket_LYNDA_29943.jpg',
        },
      ],
    }
  },
}
</script>
