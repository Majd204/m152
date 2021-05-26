<template>
  <div class="content">
    <div>
   <ul>
   <li v-for="note in noten">Fach: {{note.name}} <br> Noten: {{note.grades}} <br> 
   Durchschnitt: {{subjectAverage(note.grades)}}<br> Gesamtdurchschnitt: {{overallAverage()}}</li>
    </ul>
</div>
</div>
</template>



<script>

export default {
  name: 'App',
  data: function(){
    return{


  noten:[

    {
        name: "Mathematik",
        grades: [5,4.7,3.5,4.1] 
    },
    {
        name: "Geschichte",
        grades: [5.5,4.9,5.75] 
    },
    {
        name: "Physik",
        grades: [2,2.7,4.3] 
    },
    {
        name: "Deutsch",
        grades: [4.25,4.1,3.5] 
    },
],
 newschoolGrade: '',
         }
     },
     methods: {
         subjectAverage: function (grades) {
             var sum = 0;
             for (var grade of grades) {
                 sum += grade;
             }
             return Math.round((sum / grades.length) * 2) / 2;
         },
    overallAverage: function () {
      var total = 0;
      this.noten.forEach((note) => {
        total += parseFloat(this.subjectAverage(note.grades));
      });
      return (total / this.noten.length).toFixed(2);
         },
     }
}
</script>

<style lang="scss">
.content{
width: 100px;
margin: 0 auto;
} 
</style>
