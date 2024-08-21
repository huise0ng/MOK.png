<script>
    let days = '';
    let title = '';
    let message = '';

    const handleSubmit = () => {
        console.log({ days, title, message });
        window.location.href = '/sent';
    };

    const handleSkip = () => {
        window.location.href = '/home';
    };
</script>

<style>
    .container {
        width: 375px;
        height: 960px;
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
        margin-top: 50px;
        text-align: left; 
        padding-left: 20px;
        width: calc(100% - 40px); 
    }

    label {
        display: block;
        color: #732F4B;
        font-size: 20px;
        margin-bottom: 8px; 
        padding-left: 20px; 
        width: calc(100% - 40px);
    }

    input[type="text"] {
        width: 248px;
        border: none;
        border-bottom: 2px solid #FF3E7A;
        padding: 8px 10px;
        font-size: 18px;
        margin-bottom: 30px; 
        box-sizing: border-box;
        background-color: transparent;
        outline: none;
        color: #FF3E7A;
        margin-right: 68px;
    }

    .white-box {
        width: 280px;
        height: 332px;
        background-color: #FFFFFF;
        border-radius: 8px;
        margin-top: 70px;
        position: relative;
        padding: 20px; 
    }

    .white-box-label {
        position: absolute;
        top: -40px;
        left: 0;
        width: 100%;
        text-align: left;
        padding-left: 10px;
        font-size: 20px;
        color: #732F4B;
        margin-left: -8px;
    }

    textarea {
        width: 100%;
        height: calc(100% - 20px); 
        border: none;
        resize: none;
        background-color: transparent;
        font-size: 18px;
        color: #FF3E7A;
        outline: none;
        padding: 10px;
        box-sizing: border-box;
        border-radius: 8px;
    }

    .button-container {
        display: flex;
        flex-direction: column;
        align-items: center;
        width: calc(100% - 40px); 
        margin-top: 50px; 
    }

    button {
        width: 310px;
        height: 50px;
        border: none;
        border-radius: 8px;
        color: #FFFFFF;
        font-size: 16pt;
        font-family: 'Pretendard', sans-serif;
        font-weight: 400;
        cursor: pointer;
        margin-bottom: 20px; 
        display: flex;
        align-items: center;
        justify-content: center;
    }

    button:first-of-type {
        background-color: #FF3E7A;
    }

    button:first-of-type:hover {
        background-color: #e03570;
    }

    .share-button {
        color: #FF3E7A;
        border: 2px solid #FF3E7A;
    }



</style>

<div class="container">
    <h1>너 또는 친구에게<br>전하고 싶은 말을 쓸 수 있어.</h1>
    
    <label for="days">몇일 후에 볼 수 있으면 좋겠어?</label>
    <input type="text" id="days" bind:value={days} placeholder="여기에 입력해줘." />

    <div class="white-box">
        <!-- svelte-ignore a11y-label-has-associated-control -->
        <label class="white-box-label">어떤 내용을 작성하고 싶어?</label>
        <textarea bind:value={message} placeholder="하고 싶은 이야기를 적어줘."></textarea>
    </div> 

    <div class="button-container">
        <button on:click={handleSubmit}>작성 완료</button>
        <button class="share-button" on:click={handleSubmit}>친구에게 공유하기</button> 
    </div>
</div>
