<template>
    <div>
        <!-- Headbar Part -->
        <div id="carouselExampleCaptions" class="carousel headbar" data-bs-ride="carousel">
            <div class="carousel-inner">
                <div class="carousel-item active head">
                    <img src="../../public/Headbar_Busan_1.png" class="d-block w-100" >
                    <div class="d-none d-md-block carousel_subtext">
                        <div class="subject" style="background-color:none;">
                            <p>로그인</p>
                            <p style="font-size: 30px;">Log IN</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- Content Part -->
        <div class="container" style="height:900px;">
            <header class="welcome-header">
                <h1 class="welcome-header__title">Busan For U 에 오신것을 환영합니다!</h1>
                <p class="welcome-header__text">사용자 계정이 있다면,</p>
                <p class="welcome-header__text2">ID와 Password를 입력하여 로그인 하세요.</p>
            </header>
            <form v-on:submit="submitForm" id="Login-form">
                <input v-model="username" type="text" id="users_id" name="users_id"  placeholder="ID" />
                <input v-model="password" type="password" id="users_pwd" name="users_pwd"  placeholder="Password"/>
                <input id = "button" type="submit" value="Log in" style="margin-top:40px;"/>
            </form>
            <router-link to="/signup">
                    <a href="" class="find">회원가입이 필요하십니까?</a>
            </router-link>          
        </div>
    </div>    
</template>

<script>
import axios from 'axios';
export default {
    data:function(){
        return{
            username:"",
            password:""
        }
    },
    methods: {       // 메서드 구현
        submitForm: function(){
            console.log(this.username, this.password);
            var url = 'https://jsonplaceholder.typicode.com/posts';   //이 url로 데이터를 보내고 받을 수 있음
            var data = {
                username: this.username,
                password: this.password
            }
            axios.post(url, data)
                .then(function(response){
                    console.log(response);
                })
                .catch(function(error){
                    console.log(error);
                })
        }
    }
}
</script>

<style>
        /* headbar Part */
        .head img{
            height: 450px;
            filter: brightness(90%);
        }
        .subject{
            vertical-align: middle;
            display:inline-block;  
            width:250px; 
            border-color: rgba(0, 0, 0, 0.5);
            text-align:left; 
            height: 350px;
            font-family: 'Gugi', cursive;
            font-size: 50px;
            color:white;
            margin-left: 20%;
            position: absolute;
            left: 0;
            bottom: 0;
        }
        .subject p:first-child{
            margin-bottom: 0px;
        }    
        /* content Part */
        .container{
            font-family: 'Noto Sans KR', sans-serif;
        }
        .welcome-header{
            margin:80px 0px;
            text-align: center;
            display:flex;
            flex-direction: column;
            align-items: center;
        }
        .welcome-header__title{
            margin-bottom: 35px;
            font-size: 30px;
            font-weight: bold;
        }
        .welcome-header__text,.welcome-header__text2{
            width : 70%;
            opacity: 0.7;
            font-weight: bold;
        }
        .welcome-header__text{
            margin-bottom: 5px;
        }
        #Login-form{
            display: flex;
            flex-direction: column;
            margin: 0px 100px;
        }
        #Login-form #button{
            margin-top: 17px;
            margin-bottom: 30px;
            padding: 13px;
            font-weight: bold;
            font-size: 15px;
            opacity: 0.7;
            color:rgba(255,255,255,0.9);
            border-radius: 8px;
            background-color: #007cc4;
            cursor: pointer;
        }

        #Login-form input{
            border: none;
            padding:17px 0px;
            font-size: 17px;
            margin-top: 15px;
        }
        
        #button:hover{
            background-color: rgb(111, 0, 255);
            transition: 0.5s ease-in-out;
        }

        .but{
            color:black;
            text-decoration:none;
            display:inline-block;
            width:1096px;
            height:45px;

        }
        #Login-form input::placeholder{
            color:rgba(0,0,0,0.3);
            font-weight: bold;
            font-size: 16px;
            text-align:center;
        }
        #Login-form input:not([type="submit"]){
            border-bottom:1.5px solid rgba(29,63,109,0.4);
            transition: border-color 0.8s ease-in-out;
        }
        #Login-form input:hover{
            border-color: rgb(111, 0, 255);
        }
        #Login-form input:focus{
            outline: 0;
            border-color: rgb(111, 0, 255);
        }
        .find{
            display: flex;
            justify-content: center;
            margin-top: 20px;
            font-size: 13px;
            color:rgba(0,0,0,0.6);
            font-weight: bold;
            text-decoration: none;
            cursor: pointer;
        }
</style>