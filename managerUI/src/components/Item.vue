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
		           <Card style="width:1050px;height:180px;" :bordered="true">
				        <div>
				            <Tabs value="name1">
						        <TabPane label="商品管理" name="name1">
						        	筛选<br>
						        	关键字<Input v-model="input1" placeholder="关键字" style="width: 300px" />
						        	状态<Input v-model="input2" placeholder="状态" style="width: 300px" />
						        	分类<Input v-model="input3" placeholder="分类" style="width: 300px" /><br><br>
						        	<Button type="primary" shape="circle" icon="ios-search" style="text-align:center">搜索</Button>
						        </TabPane>
						        <TabPane label="商品分类管理" name="name2">标签二的内容</TabPane>
						        <TabPane label="评价管理" name="name3">标签三的内容</TabPane>
						        <TabPane label="退货地址" name="name4">标签三的内容</TabPane>
						        <TabPane label="配送方式" name="name5">标签三的内容</TabPane>
						    </Tabs>
				        </div>
				    </Card>
				    <br> 
				    <Card style="width:1050px;height:50px;" :bordered="true">
				    	<div style="text-align:center">
				    		<Button type="warning" ghost>添加商品</Button>
				    	</div>
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
		data(){
			return{
				input1: "",
				input2: "",
				input3: "",
				columns1: [
                    {
                        title: 'Name',
                        key: 'name'
                    },
                    {
                        title: 'Age',
                        key: 'age'
                    },
                    {
                        title: 'Address',
                        key: 'address'
                    }
                ],
                data1: [
                    {
                        name: 'John Brown',
                        age: 18,
                        address: 'New York No. 1 Lake Park',
                        date: '2016-10-03'
                    },
                    {
                        name: 'Jim Green',
                        age: 24,
                        address: 'London No. 1 Lake Park',
                        date: '2016-10-01'
                    },
                    {
                        name: 'Joe Black',
                        age: 30,
                        address: 'Sydney No. 1 Lake Park',
                        date: '2016-10-02'
                    },
                    {
                        name: 'Jon Snow',
                        age: 26,
                        address: 'Ottawa No. 2 Lake Park',
                        date: '2016-10-04'
                    }
                ]
			}
		}
	}
</script>

<style>

</style>