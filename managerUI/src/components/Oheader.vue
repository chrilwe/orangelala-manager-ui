<template>
    <Header>
        <Menu mode="horizontal" theme="dark" active-name="1">
            <div>
                <img class="layout-logo" src="../images/logo.png"></img>
            </div>
            
            <div class="demo-avatar">
                <a @click="modal1=true">
                    <Avatar style="background-color: #5cadff;float: right;right: 15px;top: 12px" icon="ios-person" size="large" title="admin"/>
                </a>
                <Modal
                    title="系统消息"
                    v-model="modal1"
                    :styles="{float: center}" @on-ok="ok()" @on-cancel="cancel()">
                    <p>是否离开当前系统</p>
                </Modal>
            </div>
        </Menu>
    </Header>

</template>

<script>
    export default {
        data(){
            return{
                modal1: false
            }
        },
        methods: {
            logout() {
                this.modal1=true;
                alert("是否退出登录"+modal1);
            },
            ok() {
                alert("ok");
            }
        }
    }
</script>

<style scoped>
    .layout{
        border: 1px solid #d7dde4;
        background: #17233d;
        position: relative;
        border-radius: 4px;
        overflow: hidden;
    }
    .layout-logo{
        width: 120px;
        height: 50px;
        background: #515a6e;
        border-radius: 3px;
        float: left;
        position: relative;
        top: 6px;
        left: 20px;
    }
    .layout-nav{
        width: 420px;
        margin: 0 auto;
        margin-right: 20px;
    }
    .yellow{
        float: right;
        right: 40px;
        top: 12px
    }
</style>