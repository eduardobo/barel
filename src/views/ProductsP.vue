<template>
    <div>
        <h1>Productos</h1>
        <h2>Quesos</h2>
        <b-row>
            <b-col cols="12" set="12" sm="12" md="6" lg="4" xl="4" v-for="(cheese, index) of cheeses" :key=index>
                <b-card :title='cheese.name' :img-src="require('@/assets/logo.png')" img-top>
                    <b-card-text>
                        {{cheese.description}}
                    </b-card-text>
                </b-card>
                <b-card :title='cheese.name' :img-src="getImagePath(cheese.image)" img-top>
                    <b-card-text>
                        {{cheese.description}}
                    </b-card-text>
                </b-card>
                <b-card :title='cheese.name' :img-src="require(`../assets/${cheese.image}.png`)" img-top>
                    <b-card-text>
                        {{cheese.description}}
                    </b-card-text>
                </b-card>
                <b-card :title='cheese.name' :img-src="require(`../${cheese.image2}`)" img-top>
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
                {name:'Manchego', description:'Queso puramente manchego', image:'logo', image2: 'assets/logo.png' },
                {name:'Enchilado', description:'Queso manchego cubierto con chile abanero', image:'logo', image2: 'assets/logo.png' }
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