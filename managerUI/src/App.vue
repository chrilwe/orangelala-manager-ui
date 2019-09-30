<template>
    <div class="layout">
        <Layout>
            <v-Oheader></v-Oheader>
            <Layout>
                <Sider hide-trigger :style="{background: '#fff'}">
                   <Menu :theme="theme3" active-name="1" :style="{width: auto}"> 
			            <MenuItem name="1">
			                <div @click="openTabs(1)">
			                	<Icon type="md-document" />
			                	文章管理
			                </div>
			            </MenuItem>
			            <MenuItem name="2">
			                <Icon type="md-chatbubbles" />
			                评论管理
			            </MenuItem>
			            <MenuItem name="3">
			                <Icon type="md-heart" />
			                用户留存
			            </MenuItem>
			            <MenuItem name="4">
			                <Icon type="md-leaf" />
			                流失用户
			            </MenuItem> 
				    </Menu>
                </Sider>
                <v-IndexTabs></v-IndexTabs>
            </Layout>
        </Layout>
    </div>
</template>

<script>
	import Oheader from "./components/Oheader.vue";
	import IndexTabs from "./components/IndexTabs.vue";
    export default {
       data() {
   	 		return {

   	 		}
       },
       components: {
	 		"v-Oheader": Oheader,
	 		"v-IndexTabs": IndexTabs
	   },
	   methods: {
	   		openTabs(name) {
	   			alert("open"+name);
	   		}
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