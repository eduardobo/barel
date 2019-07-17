<template>
    <div>
        <h1>Productos</h1>
        <h2>Quesos</h2>
        <b-row>
            <b-col class="pt-3" cols="12" set="12" sm="12" md="6" lg="4" xl="4" v-for="(cheese, index) of cheeses" :key=index>
                <b-card :title='cheese.name' :img-src="require(`../${cheese.image}`)" img-top>
                    <b-card-text>
                        {{cheese.description}}
                    </b-card-text>
                </b-card>
            </b-col>
        </b-row>
    </div>
</template>

<script>
export default {
    name:'Products',
    data(){
        return{
            cheeses:[
                {name:'Manchego', description:'Queso puramente manchego', image: 'assets/manchego.png' },
                {name:'Enchilado', description:'Queso manchego cubierto con chile abanero', image: 'assets/enchilado.png' },
                {name:'Chipotle', description:'Queso manchego cubierto con chile abanero', image: 'assets/chipotle.png' },
                {name:'Epazote', description:'Queso manchego cubierto con chile abanero', image: 'assets/logo.png' }
            ]
        }
    },
    methods: {
        getImagePath(imageName){
            return imageName ? require(`../assets/${imageName}.png`): ''
        }
    },
}
</script>