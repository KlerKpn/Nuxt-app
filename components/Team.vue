<template>
    <div :class="$style.main">
        <div>Amet minim mollit non deserunt ullamco est sit aliqua dolor do amet sint.</div>
        <div :class="$style.title">Qualified specialists</div>
        <div :class="$style.personContainer">
            <div>
                <div>
                    <img :class="$style.personImg" src="../static/img/img3.png" alt="">
                </div>
                <div :class="$style.personName">Marvin McKinney</div>
                <div :class="$style.personType">Pilot assistant</div>
            </div>
            <div>
                <div>
                    <img :class="$style.personImg" src="../static/img/img1.png" alt="">
                </div>
                <div :class="$style.personName">Savannah Nguyen</div>
                <div :class="$style.personType">Mechanic</div>
            </div>
            <div>
                <div>
                    <img :class="$style.personImg" src="../static/img/img2.png" alt="">
                </div>
                <div :class="$style.personName">Courtney Henry</div>
                <div :class="$style.personType">Stewardess</div>
            </div>
        </div>
        <div>
            Amet minim mollit non deserunt ullamco est sit aliqua dolor do amet sint. Velit officia consequat duis enim velit mollit. Exercitation veniam consequat sunt nostrud amet.
        </div>
    </div>
</template>

<style lang="css" module scoped>
    .personContainer{
        display: flex;
        justify-content: space-between;
        margin-bottom: var(--base);
    }
    .personImg{
        max-width:162px;
        height: auto;
    }
    .title{
        font-size: 24px;
        font-weight: bold;
        margin-top: var(--base);
        margin-bottom: var(--base);
    }
    .main{
        margin-bottom: var(--base);
    }
    .personName{
        font-weight: bold;
    }
    .personType{
        margin-top: 8px;
        font-size: 14px;
        color: #677B8F;
    }
</style>