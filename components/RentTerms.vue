<template>
    <div :class="$style.Features" >
        <div>
            <div :class="$style.subtitle">Amet minim mollit non deserunt ullamco est sit aliqua dolor do amet sint.</div>
            <div :class="$style.subtitle">Amet minim mollit non deserunt ullamco est sit aliqua dolor do amet sint. Velit officia consequat duis enim velit mollit. Exercitation veniam consequat sunt nostrud amet.</div>
        </div>
        <div>

                <div :class="$style.FeaturesName">Additional conditions:</div>
                <ul :class="$style.container">
                    <li :class="$style.sub">Amet minim mollit non deserunt ullamco est sit aliqua dolor do amet sint. Velit officia consequat duis enim velit mollit. Exercitation veniam consequat sunt nostrud amet.</li>
                    <li :class="$style.sub">Amet minim mollit non deserunt ullamco est sit aliqua dolor do amet sint.</li>
                    <li :class="$style.sub">Amet minim mollit non deserunt ullamco est sit aliqua dolor do amet sint. Velit officia consequat duis enim velit mollit.</li>
                </ul>

        </div>
    </div>
</template>

<style module lang="css" scoped>
    .Features{
        margin-bottom: var(--base);
    }
  
    .FeaturesName{
        font-weight: bold;
        margin-bottom: 24px;
        margin-top: 24px;
    }

    .subtitle{
       font-size: 14px;
       color: #677B8F;
       margin-bottom: 16px;
    }
    .sub{
       font-size: 14px;
       color: #677B8F;
       margin-bottom: 16px;
    }
    .sub::before{
        content: "\2022";
        font-weight: bold;
        display: inline-block; 
        width: 1em;
        margin-left: -1em;
        color: #F84AB3;
       
    }
    .container{
        padding: 0;
        list-style: none;
    }

</style>