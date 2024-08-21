<script>
    const card1 = {
        id: 1,
        recipient: '희성',
        date: '6월 18일',
        icon: 'diamond.svg',
        timeLeft: '79:33',
        daysLeft: '약 3일 남음',
        bgColor: '#DBE1FF',
        width: '130px',
        height: '224px',
        marginLeft: '16px',
        marginTop: '0px'
    };

    const card2 = {
        id: 2,
        recipient: '희성',
        date: '6월 18일',
        icon: '',
        timeLeft: '79:33',
        daysLeft: '약 3일 남음',
        bgColor: '#B4F6C8',
        width: '149px',
        height: '141px',
        marginLeft: '-6px',
        marginTop: '0px'
    };

    const card3 = {
        id: 3,
        recipient: '희성',
        date: '6월 18일',
        icon: 'gift.svg',
        timeLeft: '79:33',
        daysLeft: '약 3일 남음',
        bgColor: '#FFDBF5',
        width: '130px',
        height: '201px',
        marginLeft: '16px',
        marginTop: '0px'
    };

    const card4 = {
        id: 4,
        recipient: '희성',
        date: '6월 18일',
        icon: 'ribon.svg',
        timeLeft: '79:33',
        daysLeft: '약 3일 남음',
        bgColor: '#FFDFDB',
        width: '149px',
        height: '218px',
        marginLeft: '-6px',
        marginTop: '-80px'
    };

    const cards = [card1, card2, card3, card4];
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

    header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 10px;
    }

    h1 {
        color: #FF3E7A;
        font-size: 28px;
        font-weight: Extrabold;
        text-align: center;
        padding-left: 20px;
        width: calc(100% - 40px);
        margin-right: 140px;
        margin-bottom: 12px;
    }

    .icon-container {
        display: flex;
        align-items: center;
    }

    .icon-container img {
        width: 30px;
        height: 30px;
        margin-left: 20px;
    }

    p.subtitle {
        color: #732F4B;
        font-size: 20px;
        margin-bottom: 20px;
        margin-right: 148px;
        margin-top: 20px;
    }

    .card-grid {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 10px;
    }

    .card {
        border-radius: 16px;
        padding: 16px;
        color: #333;
        position: relative;
        background-color: #FFFFFF;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        margin-left: 0px; 
        margin-top: 0px; 
    }

    .card img {
        width: 74px;
        height: 74px;
        margin-bottom: 10px;
        margin-top: auto;  
        transform: translateY(-30%); 
    }

    .card h2 {
        color: #333;
        font-size: 24px;
        margin: 0;
    }

    .card p {
        font-size: 14px;
        color: #666;
        margin: 0;
    }
</style>

<div class="container">
    <header>
        <h1>타임머신</h1>
        <div class="icon-container">
            <img src="pencil.svg" alt="Edit">
            <img src="profile.svg" alt="Search">
        </div>
    </header>

    <p class="subtitle">조금 더 기다려야해요.</p>

    <div class="card-grid">
        {#each cards as card}
        <div class="card" style="background-color: {card.bgColor}; width: {card.width}; height: {card.height}; margin-left: {card.marginLeft}; margin-top: {card.marginTop};">
            {#if card.icon}
            <img src={card.icon} alt="Card Icon">
            {/if}
            <h2>{card.timeLeft}</h2>
            <p>{card.daysLeft}</p>
        </div>
        {/each}
    </div>
</div>
