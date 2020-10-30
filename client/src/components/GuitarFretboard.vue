<template>
  <div>
    <h1>Hey there</h1>
    <ul id="v-for-object" class="demo">
      <li v-for="value in notesArray" :key="value">
        {{ value.note }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      notesArray : [{
        number: 1,
        note: "a"
      },
        {
        number: 2,
        note: "b"
      },
      ],
    };
  },
}
</script>