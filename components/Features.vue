<template>
    <div :class="$style.Features">
        <div :class="$style.title">
            Features:
        </div>

            <div :class="$style.row">
                <div :class="$style.FeaturesImg">
                    <svg width="30" height="24" viewBox="0 0 30 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                      <path d="M16.3333 18.584V21.3333H23V24H7V21.3333H13.6667V18.584C11.0889 18.2589 8.71842 17.0044 7 15.0557C5.28158 13.107 4.33338 10.5981 4.33333 8V0H25.6667V8C25.6666 10.5981 24.7184 13.107 23 15.0557C21.2816 17.0044 18.9111 18.2589 16.3333 18.584ZM0.333332 2.66667H3V8H0.333332V2.66667ZM27 2.66667H29.6667V8H27V2.66667Z" fill="#677B8F"/>
                    </svg>

                </div>

                <div :class="$style.text">
                    <div :class="$style.FeaturesName">
                        A challenge for a true champion
                    </div>
                    <div :class="$style.FeaturesDesc">
                        Amet minim mollit non deserunt ullamco est sit aliqua dolor do amet sint. Velit officia consequat duis enim velit mollit.
                    </div>
                </div>
            </div>

            <div :class="$style.row">
                <div :class="$style.FeaturesImg">
                    <svg width="22" height="28" viewBox="0 0 22 28" fill="none" xmlns="http://www.w3.org/2000/svg">
                     <path d="M14.9413 18.752C18.4867 20.1627 21.096 23.4187 21.584 27.3333H0.416004C0.904004 23.4187 3.51334 20.1627 7.05867 18.752L11 24.6667L14.9413 18.752ZM19 0.666656V8.66666C19 13.0853 15.4187 16.6667 11 16.6667C6.58134 16.6667 3 13.0853 3 8.66666V0.666656H19ZM16.3333 8.66666H5.66667C5.66667 11.6133 8.05334 14 11 14C13.9467 14 16.3333 11.6133 16.3333 8.66666Z" fill="#677B8F"/>
                    </svg>

                </div>

                <div :class="$style.text">
                    <div :class="$style.FeaturesName">
                        Pilot's sweaty hands
                    </div>
                    <div :class="$style.FeaturesDesc">
                        Amet minim mollit non deserunt ullamco est sit aliqua dolor do amet sint. Velit officia consequat duis enim velit mollit.
                    </div>
                </div>
            </div>
    </div>    
</template>

<style module lang="css" scoped>
    .Features{
        margin-bottom: var(--base);
    }
    .title{
        font-size: 24px;
        font-weight: bold;
        margin-bottom: var(--base);
    }
    .FeaturesImg{
        display: flex;
        background: #F3F4F7;
        border-radius: 16px;
        min-width: 80px;
        max-width: 80px;
        height: 96px;
        justify-content: center;
        align-items: center;
        margin-bottom: 16px;
    }
    .FeaturesName{
        font-weight: bold;
        margin-bottom: 8px;
    }
    .FeaturesDesc{
        font-size: 14px;
        color: #677B8F;
    }
    .row{
        display: flex;
        align-items: center;
    }
    .text{
        margin-left: 24px;
    }
    @media (max-width: 1100px) {
        .Features{
            margin-bottom: 20px;
            margin-top: 20px;
        }
        .title{
            font-size: 20px;
        }
        .FeaturesImg{
            min-width:64px ;
            max-width: 64px;    
            height:80px;
            
        }
        .FeaturesName{
            margin-bottom: 4px;
            
        }
    }

</style>