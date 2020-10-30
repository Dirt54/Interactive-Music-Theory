<template>
  <div>
    <ul id="v-for-object" class="demo">
      <li v-for="value in notesArray" :key="value">
        {{ value.note }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'GuitarFretboard',
  data() {
    return {
      notesArray: [
        {
          number: 1,
          note: "A",
        },
        {
          number: 2,
          note: "B",
        },
        {
          number: 3,
          note: "C",
        },
        {
          number: 4,
          note: "D",
        },
        {
          number: 5,
          note: "E",
        },
        {
          number: 6,
          note: "F",
        },
      ],
    };
  },
};
</script>