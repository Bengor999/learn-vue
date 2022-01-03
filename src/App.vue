<template>
<div class="general">


<div id="eventBasedApp">
    <b> the event-based component </b> <br/>
    first input: <input type="text"  @input="onFirstInput($event.target.value)"/> <br/>
    second input: <input type="text" @input="onSecondInput($event.target.value)"/> <br/>
    result: <span>{{ text }}</span>
</div>
<hr>

<!-- <div id="watchesApp">
    <b>for watches based component</b> <br/>
    first input: <input type="text" v-model="firstInput"/> <br/>
    second input: <input type="text" v-model="secondInput"/> <br/>
    result: <span>{{ text }}<span/>  
</div>
<hr> -->

<!-- <div id="computedApp">
    <b> for computed based component</b> <br/>
    first input: <input type="text" v-model="firstInput"/> <br/>
    second input: <input type="text" v-model="secondInput"/> <br/>
    result: <span>{{ computedText }}<span/>    
</div> -->
<hr>
</div>
</template>
<script>

export default {
    data() {
        return {
            text: '',
            textFirst: '',
            textSecond: '',
        }
    },
    methods: {
        onFirstInput(ei) {
            this.textFirst = ei;
            this.text = this.textFirst + this.textSecond;
        },
        onSecondInput(ei) {
            this.textSecond = ei;
            this.text = this.textFirst + this.textSecond;
        }


    }


}
</script>
<style>
* {
    margin: 0;
    padding: 0;
    border: 0;
    box-sizing: border-box;
}
.general {
    padding: 10px;
}
button {
    padding: 10px 20px;
    background-color: aqua;
    margin: 20px;
    border-radius: 10px;
}
input {
    background-color: goldenrod;
    border: hotpink 1px solid;
    padding: 5px 10px;
    margin: 20px;
}
#eventBasedApp span {
    text-transform: uppercase;
}

</style>