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
				            <Tabs value="name6">
						        <TabPane label="全部订单" name="name6">
						        	<input type="hidden" value="name6" />
						        	订单号<Input v-model="input1" placeholder="订单号" style="width: 300px" />
						        	用户信息<Input v-model="input2" placeholder="用户信息" style="width: 300px" />
						        	支付方式 <Select v-model="model1" style="width:200px">
										        <Option v-for="item in cityList" :value="item.value" :key="item.value" size="small" style="height:20px">
										        	{{ item.label }}
										        </Option>
										    </Select><br><br>
						        	商品名称<Input v-model="input3" placeholder="商品名称" style="width: 300px" />
						        	商品编号<Input v-model="input3" placeholder="商品编号" style="width: 300px" />
						        	<Button type="primary" shape="circle" icon="ios-search" style="text-align:center">搜索</Button>
						        </TabPane>
						        <TabPane label="待收款" name="name7">
						        	<input type="hidden" value="name7" />
						        	订单号<Input v-model="input1" placeholder="订单号" style="width: 300px" />
						        	用户信息<Input v-model="input2" placeholder="用户信息" style="width: 300px" />
						        	支付方式 <Select v-model="model1" style="width:200px">
										        <Option v-for="item in cityList" :value="item.value" :key="item.value" size="small" style="height:20px">
										        	{{ item.label }}
										        </Option>
										    </Select><br><br>
						        	商品名称<Input v-model="input3" placeholder="商品名称" style="width: 300px" />
						        	商品编号<Input v-model="input3" placeholder="商品编号" style="width: 300px" />
						        	<Button type="primary" shape="circle" icon="ios-search" style="text-align:center">搜索</Button>
						        </TabPane>
						        <TabPane label="待发货" name="name8">
						        	<input type="hidden" value="name8" />
						        	订单号<Input v-model="input1" placeholder="订单号" style="width: 300px" />
						        	用户信息<Input v-model="input2" placeholder="用户信息" style="width: 300px" />
						        	支付方式 <Select v-model="model1" style="width:200px">
										        <Option v-for="item in cityList" :value="item.value" :key="item.value" size="small" style="height:20px">
										        	{{ item.label }}
										        </Option>
										    </Select><br><br>
						        	商品名称<Input v-model="input3" placeholder="商品名称" style="width: 300px" />
						        	商品编号<Input v-model="input3" placeholder="商品编号" style="width: 300px" />
						        	<Button type="primary" shape="circle" icon="ios-search" style="text-align:center">搜索</Button>
						        </TabPane>
						        <TabPane label="待收货" name="name9">
						        	<input type="hidden" value="name9" />
						        	订单号<Input v-model="input1" placeholder="订单号" style="width: 300px" />
						        	用户信息<Input v-model="input2" placeholder="用户信息" style="width: 300px" />
						        	支付方式 <Select v-model="model1" style="width:200px">
										        <Option v-for="item in cityList" :value="item.value" :key="item.value" size="small" style="height:20px">
										        	{{ item.label }}
										        </Option>
										    </Select><br><br>
						        	商品名称<Input v-model="input3" placeholder="商品名称" style="width: 300px" />
						        	商品编号<Input v-model="input3" placeholder="商品编号" style="width: 300px" />
						        	<Button type="primary" shape="circle" icon="ios-search" style="text-align:center">搜索</Button>
						        </TabPane>
						        <TabPane label="已完成" name="name10">
						        	<input type="hidden" value="name10" />
						        	订单号<Input v-model="input1" placeholder="订单号" style="width: 300px" />
						        	用户信息<Input v-model="input2" placeholder="用户信息" style="width: 300px" />
						        	支付方式 <Select v-model="model1" style="width:200px">
										        <Option v-for="item in cityList" :value="item.value" :key="item.value" size="small" style="height:20px">
										        	{{ item.label }}
										        </Option>
										    </Select><br><br>
						        	商品名称<Input v-model="input3" placeholder="商品名称" style="width: 300px" />
						        	商品编号<Input v-model="input3" placeholder="商品编号" style="width: 300px" />
						        	<Button type="primary" shape="circle" icon="ios-search" style="text-align:center">搜索</Button>
						        </TabPane>
						        <TabPane label="已关闭" name="name11">
						        	<input type="hidden" value="name11" />
						        	订单号<Input v-model="input1" placeholder="订单号" style="width: 300px" />
						        	用户信息<Input v-model="input2" placeholder="用户信息" style="width: 300px" />
						        	支付方式 <Select v-model="model1" style="width:200px">
										        <Option v-for="item in cityList" :value="item.value" :key="item.value" size="small" style="height:20px">
										        	{{ item.label }}
										        </Option>
										    </Select><br><br>
						        	商品名称<Input v-model="input3" placeholder="商品名称" style="width: 300px" />
						        	商品编号<Input v-model="input3" placeholder="商品编号" style="width: 300px" />
						        	<Button type="primary" shape="circle" icon="ios-search" style="text-align:center">搜索</Button>
						        </TabPane>
						    </Tabs>
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
		data() {
			return {
				orderstatus: 'name6',
				cityList: [
                    {
                        value: 'New York',
                        label: 'New York'
                    },
                    {
                        value: 'London',
                        label: 'London'
                    }
                ],
                model1 : "",
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
		},
		methods: {
			changeOrderStatus(name) {
				alert(name);
			}
		}
	}
</script>

<style >

</style>