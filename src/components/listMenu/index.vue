<template>
    <List :header="title" size="small" split="false">
        <ListItem v-for="item in menu">
        	
        	<span>{{item}}</span> 
        	<slot name="left"></slot>        	
        	<slot name="right"></slot>        	
        </ListItem>
        <ListItem><img :src="src"/></ListItem>        
    </List>
</template>

<script>
export default {
  name: 'ListMenu',
  props:['title','menu','src']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>