<template>
  <div>
    <ul id="v-for-object" class="demo">
      <li v-for="value in gString1" :key="value">
        {{ value.note }}
      </li>
    </ul>
    <ul id="v-for-object" class="demo">
      <li v-for="value in gString2" :key="value">
        {{ value.note }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "GuitarFretboard",
  data() {
    return {
      gString1: [],
      gString2: [],
      gString3: [],
      gString4: [],
      gString5: [],
      gString6: [],

      notesArray: [
        {
          number: 1,
          note: "A",
        },
        {
          number: 2,
          note: "A#",
        },
        {
          number: 3,
          note: "B",
        },
        {
          number: 4,
          note: "C",
        },
        {
          number: 5,
          note: "C#",
        },
        {
          number: 6,
          note: "D",
        },
        {
          number: 7,
          note: "D#",
        },
        {
          number: 8,
          note: "E",
        },
        {
          number: 9,
          note: "F",
        },
        {
          number: 10,
          note: "F#",
        },
        {
          number: 11,
          note: "G",
        },
        {
          number: 12,
          note: "G#",
        },
      ],

      standardTunning : { string1 : 7, string2 : 2, string3 : 10, string4 : 5, string5 : 0, string6 : 7 },


      offsetC: 0,
    };
  },

  methods: {
    stringPopulate(gstringArray, offsetValue) {
      while (gstringArray.length < 22) {

        for (let i = 0; i < this.notesArray.length; i++) {
          var offset = (i + offsetValue) % this.notesArray.length;
          gstringArray.push(this.notesArray[offset]);

          if (gstringArray.length == 22) {
            break;
          }
        }
      }

    },
  },

  beforeMount() {
    this.stringPopulate(this.gString1, this.offsetC);
    console.log(this.gString1);
  },
};
</script>