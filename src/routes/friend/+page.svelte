<script>
    let friendName = '';

    const handleShare = () => {
        console.log({ friendName });
    };
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
        margin-top: -70px;
        text-align: left; 
        padding-left: 20px;
        width: calc(100% - 40px); 
    }

    p {
        display: block;
        color: #732F4B;
        font-size: 20px;
        margin-bottom: 8px; 
        padding-left: 20px; 
        width: calc(100% - 40px);
        margin-left: 10px;
    }

    label {
        display: block;
        color: #732F4B;
        font-size: 20px;
        margin-bottom: 8px; 
        padding-left: 20px; 
        width: calc(100% - 40px);
        margin-left: 10px;
    }

    .input-container {
        width: 100%;
        margin-bottom: 30px;
    }

    .input-container input {
        width: 248px;
        border: none;
        border-bottom: 2px solid #FF3E7A;
        padding: 8px 0;
        font-size: 18px;
        color: #FF3E7A;
        outline: none;
        background-color: transparent;
        margin-left: 30px;
    }


    .image-container {
        margin: 20px 0;
        display: flex;
        justify-content: center;
        width: 100%;
    }

    .image-container img {
        width: 180px;
        height: auto;
    }

    button {
        width: 310px;
        height: 50px;
        background-color: #FF3E7A;
        border: none;
        border-radius: 8px;
        color: #FFFFFF;
        font-size: 16pt;
        font-family: 'Pretendard', sans-serif;
        font-weight: 400;
        cursor: pointer;
        position: absolute;
        bottom: 100px;
        display: flex;
        align-items: center;
        justify-content: center;
    }


</style>

<div class="container">
    <h1>친구에게 공유하고 싶군아!</h1>

    <div class="input-container">
        <label for="friend-name">친구의 이름을 알려줘.</label>
        <input type="text" id="friend-name" bind:value={friendName} placeholder="ex)김우주" />
    </div>

    <p>이렇게 편지가 전달돼!</p>

    <div class="image-container">
        <img src="33b.svg" alt="Letter Envelope">
    </div>

    <button on:click={handleShare}>공유하기</button>
</div>
