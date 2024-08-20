<script>

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
      font-weight: 700px;
      margin-bottom: 1px;
      margin-right: 50px;
    }
  
    p {
      color: #732F4B;
      font-size: 18px;
      margin-bottom: 50px;
      margin-right: 100px;
      margin-top: 3px;
    }
  
    .image {
      margin-bottom: 2rem;
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
        display: flex;
        align-items: center;
        justify-content: center;
    }
  
    button:hover {
      background-color: #e03570;
    }
  </style>
  
  <div class="container">
    <h1>미래로 편지를 보냈어.</h1>
    <p>편지가 도착하면 알려줄게.</p>
    <img src="/sent.svg" alt="Sent" class="image" />
    <button on:click={() => window.location.href = '/home'}>홈으로</button>
  </div>
  