<template>
    <div class="layout">
        <Layout>
            <div :is="Oheader"></div>
            <Layout>
                <Sider hide-trigger :style="{background: '#fff'}">
                   <Menu :theme="theme3" active-name="1" :style="{width: auto}"> 
                   		<MenuItem name="1">
                   			<div @click="openTabs(IndexTabs)">
				                <Icon type="md-chatbubbles" />
				                首页
				            </div>
			            </MenuItem>
			            <MenuItem name="item">
			                <div @click="openTabs(Item)">
			                	<Icon type="md-document" />
			                	商品管理
			                </div>
			            </MenuItem>
			            <MenuItem name="2">
			                <Icon type="md-chatbubbles" />
			                会员管理
			            </MenuItem>
			            <MenuItem name="3">
			                <Icon type="md-heart" />
			                订单管理
			            </MenuItem>
			            <MenuItem name="4">
			                <Icon type="md-leaf" />
			                数据统计
			            </MenuItem>
			            <MenuItem name="4">
			                <Icon type="md-leaf" />
			                店铺装修
			            </MenuItem>
			            <MenuItem name="4">
			                <Icon type="md-leaf" />
			                文章营销
			            </MenuItem> 
			            <MenuItem name="4">
			                <Icon type="md-leaf" />
			                分权系统
			            </MenuItem> 
			            <MenuItem name="4">
			                <Icon type="md-leaf" />
			                系统设置
			            </MenuItem>
			            <MenuItem name="4">
			                <Icon type="md-leaf" />
			                快递助手
			            </MenuItem>
			            <MenuItem name="4">
			                <Icon type="md-leaf" />
			                优惠券管理
			            </MenuItem>
			            <MenuItem name="4">
			                <Icon type="md-leaf" />
			                经销商管理
			            </MenuItem>     
				    </Menu>
                </Sider>
                <div :is="currentTabs"></div>
            </Layout>
        </Layout>
    </div>
</template>

<script>
	import Oheader from "./components/Oheader.vue";
	import IndexTabs from "./components/IndexTabs.vue";
	import Item from "./components/Item.vue";
    export default {
       data() {
   	 		return {
   	 			IndexTabs: "IndexTabs",
   	 			Oheader: "Oheader",
   	 			currentTabs: "IndexTabs",
   	 			Item: "Item"
   	 		}
       },
       components: {
	 		Oheader,
	 		IndexTabs,
	 		Item
	   },
	   methods: {
	   		openTabs(name) {
	   			this.currentTabs = name;
	   		}
	   },
	   mounted() {
	  		
	  }
    }
</script>

<style scoped>
	.layout{
	    border: 1px solid #d7dde4;
	    background: #f5f7f9;
	    position: relative;
	    border-radius: 4px;
	    overflow: hidden;
	}
	.layout-logo{
	    width: 100px;
	    height: 30px;
	    background: #5b6270;
	    border-radius: 3px;
	    float: left;
	    position: relative;
	    top: 15px;
	    left: 20px;
	}
	.layout-nav{
	    width: 420px;
	    margin: 0 auto;
	    margin-right: 20px;
	}
	.layout-footer-center{
	    text-align: center;
	}
	.blue{
		color: blue;
	}
	.yellow{
		color: #ed4014;
	}
</style>