<script setup>
//It is just a move function;
let hrefName=  [{'name':'首页',href:'#main'},{'name':'资讯',href:'#news'},{'name':'共鸣者',href:'#esonators'},{'name':'情报',href:'#lore'},{'name':'世界',href:'#regions'},{'name':'储值中心',href:'#'}]
let moveName=  [{'name':'首页',href:'#main'},{'name':'资讯',href:'#news'},{'name':'共鸣者',href:'#esonators'},{'name':'情报',href:'#lore'},{'name':'世界',href:'#regions'},{'name':'结尾',href:'#end'},{'name':'结尾2',href:'#end2'}]
let number = 1;
let time = 0;



window.addEventListener('wheel',e=>{
  if(e.deltaY > 0){
    if(number < 6){
      number = number + 0.5;
    }
  }else{
    if(number > 0) {
      number = number - 0.5;
    }
  }
  if(number%0.5!=0){
    console.log('不满足条件啊');
  }else{
    window.open(`${moveName[number]['href']}`, '_self');
  }
});

</script>

<template>

</template>

<style scoped>

</style>