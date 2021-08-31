<template>
  <v-app id="inspire">
    <v-navigation-drawer
      v-model="drawer"
      :mini-variant.sync="mini"
      permanent
    >
      <v-list-item class="px-2">
        <v-list-item-avatar color="primary">
          <!-- <v-img src="https://randomuser.me/api/portraits/men/85.jpg"></v-img> -->
          Sk
        </v-list-item-avatar>

        <v-list-item-title>Web Application</v-list-item-title>

        <v-btn
          icon
          @click.stop="mini = !mini"
        >
          <v-icon>mdi-chevron-left</v-icon>
        </v-btn>
      </v-list-item>

      <v-divider></v-divider>

      <v-list dense>
        <v-list-item
          v-for="item in items"
          :key="item.title"
          link
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
            <!-- <i :class=""></i> -->
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-main>
      <!--  -->
    </v-main>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  components: {
  },

  data () {
    return {
      drawer: true,
      items: [
        { title: 'Home', icon: 'mdi-home-variant', f_icon: 'fas fa-atom fa-lg'},
        { title: 'Target Structure', icon: 'mdi-atom', f_icon: 'fas fa-atom fa-lg' },
        { title: 'ADMET Prediction', icon: 'mdi-chart-scatter-plot', f_icon: 'fas fa-atom fa-lg' },
        { title: 'Drug-Target Interaction', icon: 'mdi-needle', f_icon: 'fas fa-atom fa-lg' },
      ],
      mini: true,
    }
  },
};
</script>
