<template>
    <div class="register">
        <div class="header">
            <HeaderSign>
                <Col span="4">
                    <div class="info">
                    注册
                    </div>
                </Col>
            </HeaderSign>
        </div>
       
        <div class="content">
            <Row>
                <Col span="8">
                </Col>
                <Col span="8">
                    <div class="form">
                    <Form ref="formInline" :model="formInline" :rules="ruleInline">
                        <FormItem prop="user">
                            <Input type="text" v-model="formInline.user" placeholder="Username">
                                <Icon type="ios-person-outline" slot="prepend"></Icon>
                            </Input>
                        </FormItem>
                        <FormItem prop="password">
                            <Input type="password" v-model="formInline.password" placeholder="Password">
                                <Icon type="ios-lock-outline" slot="prepend"></Icon>
                            </Input>
                        </FormItem>
                        <FormItem>
                            <Button type="primary" @click="handleSubmit('formInline')">Signin</Button>
                        </FormItem>
                    </Form>
                    </div>
                </Col>
            </Row>
           
        </div>
    </div>
</template>

<script>
import HeaderSign from './../../components/headerSign';
export default{
    data(){
        return{
             formInline: {
                    user: '',
                    password: ''
                },
            ruleInline: {
                user: [
                    { required: true, message: 'Please fill in the user name', trigger: 'blur' }
                ],
                password: [
                    { required: true, message: 'Please fill in the password.', trigger: 'blur' },
                    { type: 'string', min: 6, message: 'The password length cannot be less than 6 bits', trigger: 'blur' }
                ]
            }
        }
    },
    methods:{

    },
    components:{
      HeaderSign
  }  
}
</script>

<style scoped>
.header{
    padding:20px  80px;
    background:rgb(250,250,250);
}
.info{
    font-size:18px;
    line-height:50px;
    margin-left:10px;
}
.content{
    padding:40px 80px;
    background-color:rgb(230,230,230);
}
.form{
     padding:20px;
   background:rgb(250,250,250);  
}
</style>