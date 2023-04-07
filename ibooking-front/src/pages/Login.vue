<template>
    <div class="background">
        <div class="main">
            <div class="login">
                <div class="language">
                    <span>Language:</span>
                    <select>
                        <option>简体中文</option>
                        <option>English</option>
                    </select>
                </div>

                <div class="login-input">
                    <div class="title">
                        <img src="@/assets/cas_logo.png" />
                        <h2>统一身份认证</h2>
                    </div>
                    <div class="warn" style="margin-top: 8px; margin-bottom: 6px;">您将登录的是：网上办事服务大厅</div>
                    <input class="input" placeholder="用户名（本人学工号）" />
                    <input class="input" />
                    <div class="warn">
                        <img src="@/assets/cas_prompt.png" />
                        <span> 请输入值</span>
                    </div>
                </div>

                <div class="login-submit">
                    <input class="btn" value="登录" type="button" />
                    <a class="help" href="https://myform.fudan.edu.cn/eservice/find_password">找回密码</a>
                </div>

            </div>

            <div class="notice">
                <div class="title">
                    <img src="@/assets/cas_prefix_ico.png" />
                    <span>&nbsp;&nbsp;通知公告</span>
                </div>
                <div class="line"></div>
                <ul>
                    <li>
                        <div class="arrow"></div>
                        <a href="http://www.xxb.fudan.edu.cn/29/7f/c2240a76159/page.htm">复旦大学邮箱封禁列表</a>
                        <span>[2017-10-11]</span>
                    </li>
                </ul>
            </div>

            <div class="warn">
                友情提示：失效时间为2小时
            </div>
        </div>


        <div class="footer">
            <div class="link">
                <span>友情链接： </span>
                <a href="http://ehall.fudan.edu.cn">eHall | </a>
                <a href="https://xxb.fudan.edu.cn/">Ecampus | </a>
                <a href="https://mail.fudan.edu.cn/">Email | </a>
                <a href="https://cloud.fudan.edu.cn/">Cloud@Fudan</a>
            </div>
            <div>Copyright © 复旦大学版权所有，&nbsp;联系我们： urp@fudan.edu.cn (86)021-65643207</div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Login',
}
</script>
<style scoped>
.background {
    height: 100%;
    background-image: url("~@/assets/cas_bg.png");
}
.main {
    height: 425px;
    display: flex;
    position: absolute;
    box-sizing: border-box;
    top: 50%;
    left: calc(50% + 8px);
    transform: translate(-50%, -50%);
}

.main>.warn {
    position: absolute;
    color: #bbbbbb;
    left: 34px;
    bottom: -10px;
    transform: translateY(100%);
}

.login,
.notice {
    height: 100%;
    display: inline-block;
    background-color: #fff;
    box-shadow: 0 3px 4px #bbb;
    position: relative;
}

.login {
    width: 360px;
    display: flex;
    flex-direction: column;
}

.login-input {
    margin: 12px 36px 16px 36px;
}

.login-submit {
    margin-right: 28px;
    align-self: self-end;
    display: flex;
    flex-direction: column;
    align-items: end;
}

.notice {
    width: 446px;
    margin-left: 16px;
}

.language {
    font-size: 14px;
    align-self: self-end;
    margin-top: 18px;
    margin-right: 15px;
}

.language select {
    font-size: 12px;
    margin-left: 16px;
    padding: 3px 3px 3px 3px;
}

.login-input .title {
    display: flex;
}

.login-input .title img {
    margin-right: 16px;
}

.login-input .title h2 {
    color: #0e419c;
    font-size: 24px;
}

.login-input .warn {
    color: #f3a771;
}

.login-input .input {
    line-height: 34px;
    height: 34px;
    width: 280px;
    padding-left: 4px;
    margin-bottom: 20px;
}

.login-submit .btn {
    background-color: #0e419c;
    color: #fff;
    font-size: 16px;
    line-height: 35px;
    border: 0px;
    width: 98px;
    height: 38px;
}

.login-submit .help {
    color: #666666;
    text-decoration: blink;
    margin-top: 8px;
}

.notice .title {
    margin: 30px 20px;
    margin-bottom: 0px;
    font-size: 18px;
    font-weight: 600;
    color: #666666;
}

.notice .title span {
    font-size: 14px;
}

.notice .line {
    margin: 16px 24px;
    margin-bottom: 0px;
    background-color: #EEEEEE;
    width: 382px;
    height: 1px;
}

.notice .arrow {
    border-left: 6px solid #DDDDDD;
    border-right: 6px solid transparent;
    border-bottom: 6px solid transparent;
    border-top: 6px solid transparent;
    margin-right: 4px;
    margin-top: 4px;
}

.notice ul {
    margin-left: 38px;
    padding: 0;
    list-style-type: none;
}

.notice li a,
.notice li div,
.notice li span {
    display: inline-block;
    text-decoration: none;
    color: #666666;
}

.notice li a {
    width: 247px;
    margin-right: 8px;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
    vertical-align: top;
}

.footer {
    background-color: #e3e8f0;
    text-align: center;
    width: 100%;
    padding: 6px 0;
    color: #666666;
    line-height: 32px;
    position: absolute;
    bottom: 0px;
}

.link a {
    color: #666666;
    text-decoration: blink;
}
</style>