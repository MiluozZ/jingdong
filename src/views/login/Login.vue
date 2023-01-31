<template>
    <div class="wrapper">
        <img src="http://www.dell-lee.com/imgs/vue3/user.png" class="wrapper__img">
        <div class="wrapper__input">
            <input class="wrapper__input__value" placeholder="请输入手机号"/>
        </div>
        <div class="wrapper__input">
            <input class="wrapper__input__value" placeholder="请输入密码"/>
        </div>
        <div class="wrapper__login--button">登录</div>
        <div class="wrapper__footer">
            <span class="wrapper__footer__link--button">立即登录</span>
            <span>|</span>
            <span class="wrapper__footer__forget--button">忘记密码</span>
        </div>
    </div>
</template>

<script>
export default {
  name: 'LoginPage'
}
</script>

<style lang="scss" scoped>
.wrapper {
    position: absolute;
    top: 50%;
    left: 0;
    right: 0;
    transform: translateY(-50%);
    &__img {
        display: block;
        margin: 0 auto .24rem auto;
        height: .66rem;
        width: .66rem;
    }
    &__input {
        background: #F9F9F9;
        border: 1px solid rgba(0,0,0,0.10);
        border-radius: 6px;
        border-radius: 6px;
        width: 2.95rem;
        height: .48rem;
        margin: .16rem auto;
        &__value {
            border: none;
            outline: none;
            width: 80%;
            background: #F9F9F9;
            font-size: 16px;
            color: rgba(0,0,0,0.50);
            letter-spacing: 0;
            line-height: 24px;
            margin: .12rem .83rem .12rem .16rem;
            &::placeholder {
                color: rgba(0,0,0,0.50);
            }
        }
    }
    &__login--button {
        background: #0091FF;
        box-shadow: 0 4px 8px 0 rgba(0,145,255,0.32);
        border-radius: 4px;
        font-size: 16px;
        color: #FFFFFF;
        text-align: center;
        line-height: .48rem;
        width: 2.95rem;
        margin: .16rem auto;
    }
    &__footer {
        font-size: 14px;
        color: rgba(0,0,0,0.50);
        letter-spacing: 0;
        &__link--button {
            margin: 0 0.12rem 0 1.18rem;
        }
        &__forget--button {
            margin: 0 0 0 0.12rem;
        }
    }
}
</style>
