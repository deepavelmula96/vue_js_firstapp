<template>
<h1>Form</h1>
<!-- 1. input -->
<input type="text" placeholder="enter email" v-model="email"><br> <br>
<input type="password" placeholder="enter password" v-model="password"> <br> <br>
<!--2. checkbox  -->
<h3>Technology :{{ technology }}</h3>
<label for="javascript">Javascript</label>
<input type="checkbox" value="javascript" id="javascript" v-model="technology"> <br>
<label for="nodejs">nodejs</label>
<input type="checkbox" value="nodejs" id="nodejs" v-model="technology"> <br>
<label for="expressjs">expressjs</label>
<input type="checkbox" value="expressjs" id="expressjs" v-model="technology"> <br>
<!-- 3. radio button -->
<h3>Profession {{ profession }}</h3>
<label for="student">student</label>
<input type="radio" value="student" id="student" v-model="profession" name="profession"> <br>
<label for="developer">developer</label>
<input type="radio" value="developer" id="developer" v-model="profession" name="profession"> <br>
<!-- checkbox vs radio===> radio ((((((same name ))))))need to take (RS) -->
<!-- 4. if-else condition -->
<h3 v-if="show">if conditions in Vue js</h3>
<h3 v-else>else condition </h3>
<button v-on:click="show=!show">condition</button>
<!-- 5. for Loop -->
<h3> for loop with array </h3>
<ul>
    <li v-for="item in availableTechnologies" :key="item">{{ item }}</li>
</ul>
<h3>for loop with object</h3>
<ul>
    <li v-for="item in users" :key="item.name">name is :{{ item.name }} and email is :{{ item.email }}</li>
</ul>
<button type="button" v-on:click="getDetails()">get Details</button>
</template>

<script>
export default {
    name: "FormInputs",
    data() {
        return {
            email: null,
            password: null,
            technology: [],
            profession: null,
            show: true,
            availableTechnologies: [
                "javascript", "node js", "express js", "mongo db", "vue js", "redux", "python"
            ],
            users: [{
                    name: "deepa",
                    email: "deepa@gmail.com"
                },
                {
                    name: "deepa1",
                    email: "deepa1@gmail.com"
                },
                {
                    name: "deepa2",
                    email: "deepa2@gmail.com"
                },
                {
                    name: "deepa3",
                    email: "deepa3@gmail.com"
                },
                {
                    name: "deepa4",
                    email: "deepa4@gmail.com"
                }
            ]
        }
    },
    methods: {
        getDetails() {
            console.log("your Details", this.email, this.password);
        }
    }
}
</script>
