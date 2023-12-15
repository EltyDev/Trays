<script setup lang="ts">
    import Profile from "./sidebar/Profile.vue"
    import Modpack from "./sidebar/Modpack.vue"

    let hide = false
</script>

<template>
    <div id="sidebar">
        <div class="sidebar-top">
            <Profile />
            <h2>Modpack</h2>
            <div id="modpacks">
                <Modpack name="Luminous" background="https://s3-alpha-sig.figma.com/img/3e7e/0488/37c72bbc38a89a26a66916248db7ea0c?Expires=1703462400&Signature=LHphgR0N2raA5Z-N21RsXWLBv1yBKfdbanvituCtN6VPTu~jhS-ujoLIo~hoDKn7GIv7oQhRIZ6RRLdHHQrwQB8zZsU32dp-P3ipPEcJV0aTKTr4~5RFSR6yjPNQNEehyU2wgfbgT3WUj~bqgEaLWMax-sEgM10kKuHAU0TEOaL7M8pK9IinPSUUzQlurgy3WnXy4dhU4x1fxdaE3Gm6PNC04CCr2zByjFGxDWO6kZyLtjm6a5oJv~eXPQHT9YFPAxxNJwRcpq93liPi4m20O3ZfScTKu1eQMMysnnQsD253yO4J0MFYw39fDm2x8lF-B~vPFZrmoEjWWOZFGKcH3w__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4" icon="https://s3-alpha-sig.figma.com/img/7987/9f16/e40d1f2dc2292e5c001e0d08911bec09?Expires=1703462400&Signature=eVFcx7rwj4SzpUxnc4me1oR9C7YPia9OZ0~VyqKeQFojNial~aH3DcWphB26DmRs~~p5k7fcHEujTDf-bbtx4uMQzp4EMryiNX01ATZDxpHk3vSPeuywS42goLo3ZBJSI4hewKYxJ~UtyWSjoAJw7ors1khLn8Thz~sj3xeXOgH7yqfzkx497k9W~ZsCe~lJPoJRQATXyoanLm3YIs9sv-PXyADBq3Az8gTRMN-xDp3mvUgyQQK03vygmJplRAmYgcHKRA1k-WaVnHX3LLpnEATgqXAZeV83nEQQPEoGC8q0VIb71yh7-z8tVTtd~yrdClLV~h0KT4TfE8lhXDrhZw__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4"/>
                <Modpack name="Brume" background="https://s3-alpha-sig.figma.com/img/864f/2ae9/62aec991266937f89d5855dcb612ef79?Expires=1703462400&Signature=ho8B~MNnUBstn5YiL2q02edPNu5RVYWyTmWLLMyB1Ymt8lWl81liWfoMaoT0g2rTUP7ipcg~f5ECXEjPKwP3Dhmczz533aIanrMGRKXPYGRBME-3CCIpgEyE9A9DI7fRcTVvMbX2gQMmFphSZvfQghrBZDb0HKNwP5Ypy5y1tSBwMbtxaGfhwRbEDSd3MR7fFJq6DAm6l0OCUrDFsYLrP43vsNoRa3eAhjRm8OUEGJnq-AYouNFxEh9fcQQUSlOOKlqxuHRZlAreX7HhBiB7NGUKJb4LXZDeMICDBCXG9gQ3Xm1v4~~NzJOACWSkRIcMV6MXdgYuU8o71oiiMogjqA__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4" icon="https://s3-alpha-sig.figma.com/img/267c/acc2/7fdb2d008190d60cf60000614be546d1?Expires=1703462400&Signature=N2Ar~W5mJO-htAdD68BMBJTvLkPAQ0C7PDzDNXI1HXdLdYxJQpW0kPEmpzAPp~v3t882QiFaJg7qWF7KaqDbINZUMURXxcYIPWUed6nJP80Eg5T8Kvvf75OxW1RwqUL~-0qTQxt4LvqxOxMboP-FsSrP2bl9YBE61DyjThn8Q6dZ9ZwHsr1mnDLMfDy9z0VSngEu14nT~tMHuYw1LqA5IERLByREQo57DzpHf~njYfv3Qyt5qpneTVbexHhD59ZyGv4RuU92dWrm3eIWRgWaOvsTYxi55JF2ATtH~axPoNICgbIbt-jSiYXdKh0fZnoHmluDJDP~WxEoNorMckG34Q__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4"/>
            </div>
        </div>
        <div class="sidebar-bottom">
            <div class="sidebar-button">
                <svg id="settings" width="47" height="50" viewBox="0 0 47 50" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <g filter="url(#filter0_d_31_30)">
                        <path d="M42.3947 13.9629C42.6466 14.6481 42.434 15.4121 41.8907 15.9004L38.4811 19.0035C38.5677 19.6572 38.6149 20.3267 38.6149 21.004C38.6149 21.6813 38.5677 22.3508 38.4811 23.0045L41.8907 26.1076C42.434 26.5959 42.6466 27.3599 42.3947 28.0451C42.0482 28.9823 41.6308 29.8802 41.1505 30.7465L40.7804 31.3845C40.2607 32.2509 39.678 33.07 39.0402 33.8418C38.5756 34.4089 37.8039 34.5979 37.1109 34.3774L32.7249 32.9833C31.6697 33.7945 30.5043 34.4719 29.2601 34.9838L28.2758 39.481C28.1183 40.1977 27.5671 40.7648 26.8427 40.8829C25.756 41.064 24.6379 41.1586 23.4961 41.1586C22.3543 41.1586 21.2361 41.064 20.1494 40.8829C19.425 40.7648 18.8738 40.1977 18.7163 39.481L17.732 34.9838C16.4878 34.4719 15.3224 33.7945 14.2672 32.9833L9.88907 34.3852C9.19612 34.6058 8.42443 34.4089 7.95984 33.8497C7.32201 33.0778 6.73931 32.2587 6.2196 31.3924L5.8495 30.7544C5.36916 29.8881 4.95181 28.9902 4.60534 28.053C4.35336 27.3678 4.56597 26.6038 5.1093 26.1155L8.51893 23.0124C8.43231 22.3508 8.38506 21.6813 8.38506 21.004C8.38506 20.3267 8.43231 19.6572 8.51893 19.0035L5.1093 15.9004C4.56597 15.4121 4.35336 14.6481 4.60534 13.9629C4.95181 13.0257 5.36916 12.1278 5.8495 11.2614L6.2196 10.6235C6.73931 9.75713 7.32201 8.93803 7.95984 8.16619C8.42443 7.59912 9.19612 7.4101 9.88907 7.63062L14.2751 9.02467C15.3303 8.21345 16.4957 7.53611 17.7399 7.02418L18.7242 2.52701C18.8817 1.81029 19.4329 1.24323 20.1573 1.12509C21.244 0.936064 22.3621 0.841553 23.5039 0.841553C24.6457 0.841553 25.7639 0.936064 26.8506 1.11721C27.575 1.23535 28.1262 1.80242 28.2837 2.51913L29.268 7.0163C30.5122 7.52824 31.6776 8.20557 32.7328 9.01679L37.1188 7.62275C37.8118 7.40222 38.5834 7.59912 39.048 8.15831C39.6859 8.93016 40.2686 9.74926 40.7883 10.6156L41.1584 11.2536C41.6387 12.1199 42.0561 13.0178 42.4025 13.955L42.3947 13.9629ZM23.5039 27.3048C25.1747 27.3048 26.777 26.6409 27.9584 25.4593C29.1398 24.2777 29.8035 22.6751 29.8035 21.004C29.8035 19.3329 29.1398 17.7303 27.9584 16.5487C26.777 15.3671 25.1747 14.7032 23.5039 14.7032C21.8332 14.7032 20.2309 15.3671 19.0495 16.5487C17.8681 17.7303 17.2044 19.3329 17.2044 21.004C17.2044 22.6751 17.8681 24.2777 19.0495 25.4593C20.2309 26.6409 21.8332 27.3048 23.5039 27.3048Z" fill="white"/>
                    </g>
                    <defs>
                        <filter id="filter0_d_31_30" x="0.5" y="0.841553" width="46" height="48.317" filterUnits="userSpaceOnUse" color-interpolation-filters="sRGB">
                        <feFlood flood-opacity="0" result="BackgroundImageFix"/>
                        <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha"/>
                        <feOffset dy="4"/>
                        <feGaussianBlur stdDeviation="2"/>
                        <feComposite in2="hardAlpha" operator="out"/>
                        <feColorMatrix type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0.25 0"/>
                        <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_31_30"/>
                        <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_31_30" result="shape"/>
                        </filter>
                    </defs>
                </svg>
            </div>
        </div> 
    </div>
</template>

<style scoped>
    #sidebar {
        width: 23.4375%;
        height: 100%;
        padding: 0.520833333333%;
        gap: 0.938em;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
    }

    .sidebar-top > h2 {
        font-weight: 600;
        font-size: 1.875em;
        margin: 0;
        margin-left: 0.25em;
        margin-bottom: 0.625em;
        margin-top: 0.512em;
    }

    #modpacks {
        display: flex;
        flex-direction: column;
        gap: 0.625em;
    }

    #settings {
        width: 4.750em;
        fill: white;
        cursor: pointer;
        filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.25)); 
    }

    .sidebar-button {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 4.688em;
        height: 4.688em;
        border-radius: 1.563em;
        background: #323232; 
    }
</style>