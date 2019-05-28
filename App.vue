<template>
  <div id = "app">
    <Tree :node="root"/>
  </div>
</template>
<script>
import Tree from './components/Tree';
export default {
  components: {
    Tree
  },
  name: 'app',
  data(){
    return {
      root:
      {
        name: 'show',
        children:[{
              name:'furniture',
              children:[
                {name: 'srk',children:[{name:'sofa',children:[{name:'2'},{name:'3'}]},{name:'chair',children:[{name:'2'},{name:'3'}]}]},
                {name: 'br',children:[{name:'dt',children:[{name:'2'},{name:'3'}]},{name:'bd',children:[{name:'2'},{name:'3'}]}]}]
        },
        {
              name:'electronics',
              children:[
                {name: 'mobile',children:[{name:'samsung',children:[{name:'sam1'},{name:'sam2'}]},{name:'vivo',children:[{name:'vivoy81'},{name:'vivopro'}]}]},
                {name: 'laptops',children:[{name:'lenovo',children:[{name:'lenovo1'},{name:'lenovo i7'}]},{name:'apple',children:[{name:'macbook1'},{name:'macbook2'}]}]}]
        },
        {
              name:'cosmetics',
              children:[
                {name: 'revlon',children:[{name:'mb',children:[{name:'mb1'},{name:'mb2'}]},{name:'el',children:[{name:'el1'},{name:'el2'}]}]},
                {name: 'dazler',children:[{name:'mb',children:[{name:'mb1'},{name:'mb2'}]},{name:'el',children:[{name:'el1'},{name:'el2'}]}]}]
        },
                
              ]
        
      }
    }
  }
}
</script>
