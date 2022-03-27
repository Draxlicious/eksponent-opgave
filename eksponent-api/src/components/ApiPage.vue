<template>
    <div>
       {{ text }}
        <div v-for="item in list" v-bind:key="item.id">
            <div>
                <p>{{item.id}}</p>
                <p>{{item.navn}}</p>
                <p>{{item.telefonnummer}}</p>
                <p>{{item.motto}}</p>
                <img :src="item.imageUrl" />
            </div>
        </div>
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
        fetch("https://shrouded-peak-36914.herokuapp.com/persons")
        .then( response => {
            return response.json();
        })
        .then( data => {
            this.list = data
            console.log(data)
            // console.log(data[0])
        })
        // .catch(err => console.log(err))
    }
}

</script>