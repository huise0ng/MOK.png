<script>
    let userName = '희성';
    let userEmail = 'shinhuisoeng07@gmail.com';
</script>

<style>
    .container {
        width: 375px;
        height: 812px;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        position: relative;
        background-color: #FFF5FD;
        font-family: 'Pretendard', sans-serif;
        margin: 0 auto;
        overflow: hidden;
        border-radius: 32px;
        margin: 40px auto 0; 
    }

    h1 {
        color: #FF3E7A;
        font-size: 28px;
        font-weight: Extrabold; 
        margin-bottom: 50px; 
        margin-top: -460px;
        text-align: left; 
        padding-left: 20px;
        width: calc(100% - 40px); 
    }

    .profile-container {
        display: flex;
        align-items: center;
        width: 100%;
        padding-left: 20px;
        margin-left: 52px;
    }

    .profile-icon {
        width: 60px;
        height: 60px;
        background-color: #FF3E7A;
        border-radius: 50%;
        display: flex;
        align-items: center;
        justify-content: center;
        color: white;
        font-size: 28px;
        margin-right: 30px;
    }

    .user-info {
        display: flex;
        flex-direction: column;
    }

    .user-info .name {
        font-size: 20px;
        font-weight: bold;
        color: #000000;
        margin-bottom: 4px;
    }

    .user-info .email {
        font-size: 14px;
        font-weight: Regular;
        color: #000000;
    }
</style>

<div class="container">
    <h1>마이페이지</h1>

    <div class="profile-container">
        <div class="profile-icon">
            <img src="profile.svg" alt="Profile Icon" />
        </div>
        <div class="user-info">
            <div class="name">{userName}</div>
            <div class="email">{userEmail}</div>
        </div>
    </div>
</div>
