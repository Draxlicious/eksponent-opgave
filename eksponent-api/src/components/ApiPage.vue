<template>
    <div>
       {{ text }}
        <!-- <div v-for="item in list" v-bind:key="item.id">
            </div>
                <p>{{item.employee_name}}<p>
                <p>{{item.employee_employee_salary}}<p>
                <p>{{item.employee_age}}<p>
                <p>{{item.id}}<p>
            </div>
        </div> -->
    </div>
</template>

<script>
export default {
    data(){
        return{
            text: 'Welcome to eksponent'
        }
    },
    created(){
        // fetch("http://dummy.restapiexample.com/api/v1/employees")
        fetch("https://shrouded-peak-36914.herokuapp.com/")
        .then( response => {
            return response.json();
        })
        .then( data => {
            this.list = data
            // console.log(data)
            console.log(data[0])
        })
        // .catch(err => console.log(err))
    }
}

</script>