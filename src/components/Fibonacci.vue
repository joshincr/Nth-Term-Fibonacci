<template>
  <div class="container">
    <div class="header">
      <h1> N<sup>th</sup> term of Fibonacci Sequence</h1>
    </div> <br>
    <h6 style="font-family:montserrat">Developed by Joshin Rexy</h6>
    <form class="input-bar" onSubmit="return false">
      <div class="input-group">
        <input
          type="number"
          class="form-control"
          placeholder="Enter value of n..."
          v-model="nth"
        />
        <button @click="getValue(nth)" type="button" class="btn">
          <i class="material-icons">calculate</i>
        </button>
      </div>
    </form>
    <div class="resultdiv" v-if="result !== ''">
      <div class="col-md-12">
      <p><strong> Result:</strong></p>
      <p> Contains <strong>{{this.len}}</strong> digit(s)</p>
      <p class="result">{{this.result}}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Fibonacci',
  props: {
    msg: String
  },
  data () {
    return {
      nth: "",
      result: "",
      isNeg: false,
      len: null
    }
  },
  methods: {
    getValue(nth) {
      let first = 0n, second = 1n, sum;
      if (nth == 0) {
        this.result = 0;
        this.len = 0
      }
      else if (nth % 1 != 0) {
        alert('Please Enter Integers only')
      }
      else {
        if (nth < 0) {
          this.isNeg = true,
          nth *= -1
        }
        for(var i = 2; i <= nth; i++)
        {
          sum = first + second; first = second; second = sum;
        }
        if (this.isNeg && nth % 2 == 0) {
          this.result = "-" + second
          this.len = this.result.length - 1
          this.isNeg = false
        }
        else {
          this.result = "" + second
          this.len = this.result.length
        }
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.header {
  font-family: 'Montserrat', sans-serif;
  background-color: #ccfcfa;
}
button {
  height: 38px;
  width: 50px;
}
p { 
  margin:5px;
  word-wrap: break-word;
}
.input-bar {
  width: 30%;
  margin-top: 35px;
  margin-left: auto;
  margin-right: auto;
  border: solid #00bdb6;
}
.result {
  margin-top: 10px;
  border: solid #00bdb6;
}
.resultdiv {
  margin-top: 25px;
}
.form-control {
  border-right: solid #00bdb6;
}
</style>
