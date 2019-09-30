<template>
	<Layout :style="{padding: '0 24px 24px'}">
        <Breadcrumb :style="{margin: '10px 0'}">
        	<div class="yellow">
        		{{username}},欢迎使用由chrilwe开发的orangelala商城后台管理系统
        	</div>
        </Breadcrumb>
        <Content :style="{padding: '24px', minHeight: '530px', background: '#e8eaec'}">
            <div id="tabs">
            	<Row style="background:#eee;padding:3px">
			        <Col span="3">
			           <Card style="width:170px;height:90px;" :bordered="true">
					        <div style="text-align:center">
					            <Icon type="ios-home-outline" size="50" color="blue" /> <br>
					            <div class="blue">商城入口</div>
					        </div>
					    </Card> 
			        </Col>
			        <Col span="3" offset="2">
			            <Card style="width:170px;height:90px" :bordered="true">
					        <div style="text-align:center">
					            <Icon type="md-cart" size="50" color="blue"  /> <br>
					            <div class="blue">购物车入口</div>
					        </div>
					    </Card>
			        </Col>
					<Col span="3" offset="2">
			            <Card style="width:170px;height:90px" :bordered="true">
					        <div style="text-align:center">
					            <Icon type="ios-bookmarks-outline" size="50" color="blue"/> <br>
					            <div class="blue">订单中心入口</div>
					        </div>
					    </Card>
			        </Col>
			        <Col span="3" offset="2">
			            <Card style="width:170px;height:90px" :bordered="true">
					        <div style="text-align:center">
					            <Icon type="md-calendar" size="50" color="blue"/> <br>
					            <div class="blue">我的收藏入口</div>
					        </div>
					    </Card>
			        </Col>
			        <Col span="3" offset="2">
			            <Card style="width:170px;height:90px" :bordered="true">
					        <div style="text-align:center">
					            <Icon type="md-contacts" size="50" color="blue"/> <br>
					            <div class="blue">会员管理入口</div>
					        </div>
					    </Card>
			        </Col>
			    </Row>
			    <Row style="background:#eee;padding:3px">
			    	<Card style="width: auto;height:260px" :bordered="true">
				        <div style="text-align:center">
				            业务功能<br>
				        </div>
				    </Card>
			    </Row>
			    <Row style="background:#eee;padding:5px">
			    	<Card style="width: auto;height:150px" :bordered="true">
				        <Row style="background:#eee;padding:3px">
			        		<Col span="3">
			        			<Card style="width:170px;height:90px;" :bordered="true">
							        <div style="text-align:center">
							            <Icon type="ios-people" size="50" color="yellow" /> <br>
							            <div class="blue">会员数量</div><br>
							            1000000
							        </div>
							    </Card> 
			        		</Col>
			        		<Col span="3" offset="6">
			        			<Card style="width:170px;height:90px;" :bordered="true">
							        <div style="text-align:center">
							            <Icon type="ios-pulse-outline" size="50" color="yellow" /> <br>
							            <div class="blue">订单数量</div><br>
							            100000
							        </div>
							        
							    </Card> 
			        		</Col>
			       
			        		<Col span="3" offset="6">
			        			<Card style="width:170px;height:90px;" :bordered="true">
							        <div style="text-align:center">
							            <Icon type="ios-podium-outline" size="50" color="yellow" /> <br>
							            <div class="blue">商品数量</div><br>
							            100000
							        </div>
							    </Card> 
			        		</Col>
			        	</Row>
				    </Card>
			    </Row>
			    
            </div>
        </Content>
    </Layout>
</template>

<script>
	export default{
		data() {
			return {
				username: "admin"
			}
		}
	}
</script>

<style>
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