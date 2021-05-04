<template>
  <div class="betting_field" >
    <div class="container">
      <div class="betting_field_row">
        <div class="betting_field_zero">
          <button
              class="betting_number_zero"
              :style="numbers[0].color"
          >
            {{numbers[0].num}}
          </button>
        </div>
        <div class="betting_field_center">
          <div class="betting_field_all_num">
            <div class="btn_num" v-for="number in numbers">
              <button class="betting_number"  v-if="number.id != 0" :style="number.color" >
                {{number.num}}
              </button>
            </div>
          </div>
          <div class="betting_field_dozen_column">
            <div class="wrapper_dozen_column1">
              <div class="dozen_column1">1 TO 12</div>
              <div class="outside_bets_dozen_column1">
                <div class="smaller_numbers">1 TO 18</div>
                <div class="even_numbers">EVEN</div>
              </div>
            </div>
            <div class="wrapper_dozen_column2">
              <div class="dozen_column2">1 TO 12</div>
              <div class="outside_bets_dozen_column2">
                <div class="red_numbers">RED</div>
                <div class="black_numbers">BLACK</div>
              </div>
            </div>
            <div class="wrapper_dozen_column3">
              <div class="dozen_column3">1 TO 12</div>
              <div class="outside_bets_dozen_column3">
                <div class="odd_numbers">ODD</div>
                <div class="large_numbers">19 TO 36</div>
              </div>
            </div>

          </div>

        </div>
        <div class="betting_field_column">
          <button class="betting_field_column1">2:1</button>
          <button class="betting_field_column2">2:1</button>
          <button class="betting_field_column3">2:1</button>
        </div>
      </div>
    </div>

  </div>
  <div class="test_div">

  </div>
</template>

<script>
import {fieldsNumber} from "../fieldsNumber";

export default {
  name: "BettingField",
  data(){
    return {
      numbers: fieldsNumber
    }
  },

}
</script>

<style scoped>

.betting_field {
  color: #FFF;
  display: flex;
  justify-content: center;
  margin-top: 20px;
}

.container {
  width: 680px;
  height: 240px;

}

.betting_field_row {
  display: flex;
}

.betting_field_zero {
  height: 100%;

}
.betting_number_zero{
  width: 44px;
  height: 140px;
  margin: 2px;
  border-radius: 3px;
}
.betting_number {
  width: 44px;
  height: 44px;
  color: #FFF;
  margin: 2px;
  border-radius: 3px;
  font-size: 14px;
}

.betting_field_center {
}

.betting_field_all_num {
  width: 593px;
  display: flex;
  flex-direction: column-reverse;
  flex-wrap: wrap;
  height: 145px;
}

.btn_num {
}

/*.betting_field_dozen_column {*/
/*  display: flex;*/
/*  justify-content: space-around;*/
/*  text-align: center;*/
/*  margin: 5px 0px 0px 0px;*/
/*}*/
.betting_field_dozen_column {
  margin-top: 5px;
  display: grid;
  grid-template-columns: repeat(3, 192px);
  gap: 8px;
  text-align: center;

}
.wrapper_dozen_column1,
.wrapper_dozen_column2,
.wrapper_dozen_column3{

}
.dozen_column1,
.dozen_column2,
.dozen_column3{
  padding: 12px 0;
  border-radius: 3px;
  border: 1px solid #323549;
}

.dozen_column1 {

}

.dozen_column2 {
}

.dozen_column3 {

}

.outside_bets_dozen_column1,
.outside_bets_dozen_column2,
.outside_bets_dozen_column3{
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 5px;
  text-align: center;
  margin-top: 5px;
}

.smaller_numbers,
.even_numbers,
.red_numbers,
.black_numbers ,
.odd_numbers,
.large_numbers{
  min-width: 93px;
  height: 44px;
  border: 1px solid #323549;
  border-radius: 3px;
  display: flex;
  justify-content: center;
  align-items: center;
}
.smaller_numbers {
}

.even_numbers {
}

.red_numbers {
  background: #FF114A;
}

.black_numbers {
  background: #4B5D86
}

.odd_numbers {
}

.large_numbers {
}

.betting_field_column {
  margin: 0px 2px 0px 3px;
}
.betting_field_column1,
.betting_field_column2,
.betting_field_column3{
  width: 44px;
  height: 44px;
  background: #131313;
  color: #FFF;
  margin: 2px 0px;
  border-radius: 3px;
  font-size: 14px;
  border: 1px solid #323549;
}
.betting_field_column1 {
}

.betting_field_column2 {
}

.betting_field_column3 {
}

.test_div{
  height: 150px;
}

</style>
