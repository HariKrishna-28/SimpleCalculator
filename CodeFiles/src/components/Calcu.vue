<template>
  <div class = title >Simple Calculator</div>
      <table border="1">
         <tr>
            <td colspan="3"><input type="text" id="result"/></td>
            <!-- clr() function will call clr to clear all value -->
            <td><input type="button" value="c" @click="clr()"/> </td>
         </tr>
         <tr>
            <!-- create button and assign value to each button -->
            <!-- dis("1") will call function dis to display value -->
            <td><input type="button" value="1" @click="dis('1')"/> </td>
            <td><input type="button" value="2" @click="dis('2')"/> </td>
            <td><input type="button" value="3" @click="dis('3')"/> </td>
            <td><input type="button" value="/" @click="dis('/')"/> </td>
         </tr>
         <tr>
            <td><input type="button" value="4" @click="dis('4')"/> </td>
            <td><input type="button" value="5" @click="dis('5')"/> </td>
            <td><input type="button" value="6" @click="dis('6')"/> </td>
            <td><input type="button" value="-" @click="dis('-')"/> </td>
         </tr>
         <tr>
            <td><input type="button" value="7" @click="dis('7')"/> </td>
            <td><input type="button" value="8" @click="dis('8')"/> </td>
            <td><input type="button" value="9" @click="dis('9')"/> </td>
            <td><input type="button" value="+" @click="dis('+')"/> </td>
         </tr>
         <tr>
            <td><input type="button" value="." @click="dis('.')"/> </td>
            <td><input type="button" value="0" @click="dis('0')"/> </td>
            <!-- solve function call function solve to evaluate value -->
            <td><input type="button" value="=" @click="solve()"/> </td>
            <td><input type="button" value="*" @click="dis('*')"/> </td>
         </tr>
      </table>
</template>

<script>
export default {
  name: 'Calcu',
  props: {
    msg: String
  },
  methods : {
    dis(val)
         {
             document.getElementById("result").value+=val
         },
    solve()
         {
             let x = document.getElementById("result").value
             let y = eval(x)
             document.getElementById("result").value = y
         },
    clr()
         {
             document.getElementById("result").value = ""
         }

  }
}
</script>


<style>

.title{
         margin-bottom: 10px;
         text-align:center;
         width: 210px;
         color:green;
         border: solid black 2px;
         }
  
         input[type="button"]
         {
         background-color:green;
         color: black;
         border: solid black 2px;
         width:100%
         }
  
         input[type="text"]
         {
         background-color:white;
         border: solid black 2px;
         width:100%
         }

</style>
