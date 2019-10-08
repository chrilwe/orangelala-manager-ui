<template>
	<Layout :style="{padding: '0 24px 24px'}">
        <Breadcrumb :style="{margin: '10px 0'}">
        	<div class="yellow">
        		{{username}},欢迎使用由chrilwe开发的orangelala商城后台管理系统
        	</div>
        </Breadcrumb>
        <Content :style="{padding: '24px', minHeight: '530px', background: '#e8eaec'}">
        	<Row style="background:#eee;padding:3px">
		        <Col span="3">
		           <Card style="width:1050px;height:120px;" :bordered="true">
				        <div>
				            帅选条件
				        </div><br>
				        用户账号<Input ref="username" v-model="uname" placeholder="用户账号" style="width: 300px" />
			        	用户昵称<Input ref="nickName" v-model="nickName" placeholder="用户昵称" style="width: 300px" />
			        	<Button @click="userSearch()" type="primary" shape="circle" icon="ios-search" style="text-align:center">搜索</Button>
				    </Card>
				    
				    <br>
				    <Card style="width:1050px;height:260px;" :bordered="true">
				    	<div style="text-align:center">
				    		<Table border :columns="columns1" :data="data1"></Table>
				    	</div>
				    </Card>
		        </Col>
		    </Row>
        </Content>
    </Layout>
</template>

<script>
	export default{
		data() {
			return {
				uname: "",
				nickName: ""
			}
		},
		methods:{
			userSearch() {
				 this.$http.post('/someUrl', {username: this.uname,nickName: this.nickName}).then(response => {
				    this.someData = response.body;
				  }, response => {
				    alert("error");
				  });
			}
		}
	}
</script>

<style>


</style>