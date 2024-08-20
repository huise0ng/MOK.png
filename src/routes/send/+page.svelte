<script>
    let days = '';
    let title = '';
    let message = '';

    const handleSubmit = () => {
        console.log({ days, title, message });
    };

    const handleSkip = () => {
        window.location.href = '/home';
    };
</script>

<style>
    .container {
        width: 375px;
        height: 931px;
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
        margin-top: -50px;
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
        width: 314px;
        height: 332px;
        background-color: #FFFFFF;
        border-radius: 8px;
        margin-top: 70px;
        position: relative;
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
        margin-left: -10px;
    }

    .button-container {
        display: flex;
        justify-content: center;
        width: calc(100% - 40px); 
        margin-top: 50px; 
    }

    button {
        width: 310px;
        height: 50px;
        background-color: #FF3E7A;
        border: none;
        border-radius: 8px;
        color: #FFFFFF;
        font-size: 18pt;
        font-family: 'Pretendard', sans-serif;
        font-weight: 400;
        cursor: pointer;
        position: absolute;
        bottom: 100px;
        left: 50%; 
        transform: translateX(-50%); 
        display: flex;
        align-items: center;
        justify-content: center;
    }

    button:hover {
        background-color: #e03570;
    }

    .skip-text {
        font-size: 16px;
        color: #FF3E7A;
        cursor: pointer;
        position: absolute;
        bottom: 60px; 
        left: 50%;
        transform: translateX(-50%);
        text-align: center;
    }

    .skip-text:hover {
        text-decoration: underline;
    }

</style>

<div class="container">
    <h1>미래의 너에게 <br>전하고 싶은 말을 쓸 수 있어.</h1>
    
    <label for="days">몇일 후의 너에게 전하고 싶어?</label>
    <input type="text" id="days" bind:value={days} placeholder="여기에 입력해줘." />

    <div class="white-box">
        <!-- svelte-ignore a11y-label-has-associated-control -->
        <label class="white-box-label">어떤 내용을 작성하고 싶어?</label>
    </div>

    <div class="button-container">
        <button on:click={handleSubmit}>작성했어</button>
    </div>

    <!-- svelte-ignore a11y-click-events-have-key-events -->
    <!-- svelte-ignore a11y-no-static-element-interactions -->
    <div class="skip-text" on:click={handleSkip}>건너뛰기</div>
</div>
