<template>
    <Dropdown>
        <a href="javascript:void(0)">
            {{txt}}
            <Icon type="ios-arrow-down"></Icon>
        </a>
        <DropdownMenu slot="list">
            <DropdownItem v-for="item in list">{{item}}</DropdownItem>
            
        </DropdownMenu>
    </Dropdown>
     
</template>

<script>
export default {
  name: 'DropMenu',
  props:['txt','list']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>