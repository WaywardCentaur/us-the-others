<template>
  <v-app>
    <div class="container mx-auto text-center px-8"> 
      <h2 class="text-h2 font-weight-bold mb-2 text-green-200">
        Presenting
        <span
          class="font-weight-bold ">Us the Others</span>
      </h2>
      <h3 class="text-h3 font-weight-bold mb-2 text-white">Description</h3>

      <div class="flex justify-center space-x-2 mt-6 lg:mt-10">
       

        <v-btn
        color="primary"
        @click="dialog1 = true"
        >
          Concept Art
        </v-btn>

        <v-dialog
          v-model="dialog1"
          width="auto"
        >
          <v-card>
            <img :src="image" alt="Concept art 1" />
            <v-card-actions>
              <v-btn color="primary" block @click="dialog1 = false">Close Dialog</v-btn>
            </v-card-actions>
          </v-card>
        </v-dialog>

        <v-btn
        color="primary"
        @click="dialog2 = true"
        >
          PBS
        </v-btn>

        <v-dialog
          v-model="dialog2"
          width="auto"
        >
          <v-card>
            <img :src="pbs" alt="PBS" />
            <v-card-actions>
              <v-btn color="primary" block @click="dialog2 = false">Close Dialog</v-btn>
            </v-card-actions>
          </v-card>
        </v-dialog>
        <!-- <a
          href="https://cloud.digitalocean.com/apps"
          class="inline-block py-2 lg:py-4 px-4 lg:px-8 rounded bg-yellow-400 hover:bg-yellow-300 text-yellow-800 shadow hover:shadow-2xl transition duration-300"
        >View Your Dashboard</a> -->
      </div>
    </div>
  </v-app>
</template>

<script>
import Image from '@/assets/image.png'; 
import PBS from '@/assets/pbs.png'; 
export default {
  name: "App",
  data() {
    return {
      image: Image,
      pbs: PBS,
      dialog1: false,
      dialog2: false,
    };
  },
};
</script>

<style>
#app {
  background-color: #268351;
  background: url("http://www.w3.org/2000/svg'%3E%3Cg fill='none' fill-rule='evenodd'%3E%3Cg fill='%232c945c' fill-opacity='0.4'%3E%3Cpath d='M36 34v-4h-2v4h-4v2h4v4h2v-4h4v-2h-4zm0-30V0h-2v4h-4v2h4v4h2V6h4V4h-4zM6 34v-4H4v4H0v2h4v4h2v-4h4v-2H6zM6 4V0H4v4H0v2h4v4h2V6h4V4H6z'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E");
}
</style>