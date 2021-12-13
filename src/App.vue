<template>
    <h1 :style="{color:couleur}">Coucou</h1>
    <TextInput msg="" />
    <DateInput msg="" />
    <TextArea msg="" />
    <MenuSelect msg="" />
    <MenuRadio msg="" />
    <Button msg="" />
    <bouttoncoul msg=""/>
    <SearchAutocomplete msg=""/>
    <ChangeColor msg="" v-on:validation="step='step2'"/>
    <div v-if="step === 'step1'">
      <h1>Etape:1</h1>
    </div>
    <div v-if="step === 'step2'">
      <h1>Etape:2</h1>
      <div>
        <button>Vers Etape 3</button>
      </div>
    </div>
    <div v-if="step === 'step3'">
      <h1>Etape:3</h1>
    </div>
    <div id="app">
    <SearchAutocomplete
      :items="[
        'Apple',
        'Banana',
        'Orange',
        'Mango',
        'Pear',
        'Peach',
        'Grape',
        'Tangerine',
        'Pineapple'
      ]"
    />
  </div>

</template>

<script>
import TextInput from "./components/TextInput.vue";
import DateInput from "./components/DateInput.vue";
import TextArea from "./components/TextArea.vue";
import MenuSelect from "./components/MenuSelect.vue";
import MenuRadio from "./components/MenuRadio.vue";
import Button from "./components/Button.vue";
import ChangeColor from "./components/ChangeColor.vue";
import bouttoncoul from "./components/bouttoncoul.vue";
import SearchAutocomplete from "./components/SearchAutocomplete.vue";
export default {
  name: "App",
  components: {
    TextInput,
    DateInput,
    TextArea,
    MenuSelect,
    MenuRadio,
    Button,
    ChangeColor,
    bouttoncoul,
    SearchAutocomplete,
  },
  data() {
    return {
      colorie: 'red',
      step: 'step1',
      couleur:'yellow'
  }
    }
    
  }


</script>

<style>
.temp {
  margin: 1em;
}
</style>