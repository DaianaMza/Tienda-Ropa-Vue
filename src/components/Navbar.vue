<script>
export default {
    data() {
        return {
        };
    },
};
</script>

<template>
    <v-app-bar app color="white" flat>
        <v-badge color="#D5F0DB" dot>
            <v-toolbar-title class="m1-4">
                <span class="green--text">TU</span><strong>TIENDA </strong>
            </v-toolbar-title>
        </v-badge>
        <v-spacer></v-spacer>
        <v-badge  color="#white" >
            <v-badge overlap content="3" class="mr-2 mt-1" color="#41AB55">
                <v-avatar color="#FFF0EE" sixe="40">
                    <v-icon x-small color="#41AB55">fas fa-shopping-cart</v-icon>
                </v-avatar>
            </v-badge>
        </v-badge>
    </v-app-bar>
</template>
  

  
<style scoped></style>