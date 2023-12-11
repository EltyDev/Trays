<script setup lang="ts">
    import { appWindow } from "@tauri-apps/api/window"
</script>

<template>
    <div class="titlebar">
        <p id="title">Trays <small>#513a329-beta</small></p>
        <div class="titlebuttons">
            <svg id="minimize" width="27" height="4" viewBox="0 0 27 4" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M26.9807 2C26.9807 3.10625 26.0869 4 24.9807 4H2.98065C1.8744 4 0.980652 3.10625 0.980652 2C0.980652 0.89375 1.8744 0 2.98065 0H24.9807C26.0869 0 26.9807 0.89375 26.9807 2Z" fill="white"/>
            </svg>
            <svg id="maximize" width="21" height="20" viewBox="0 0 21 20" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M8.4844 -0.00500488H2.05262C1.45857 -0.00500488 0.980652 0.472913 0.980652 1.06696V7.49875C0.980652 7.932 1.23971 8.32505 1.6417 8.49031C2.04368 8.65557 2.50373 8.56624 2.81192 8.25805L4.59853 6.47145L8.12708 10L4.59853 13.5285L2.81192 11.7419C2.50373 11.4337 2.04368 11.3444 1.6417 11.5097C1.23971 11.6749 0.980652 12.068 0.980652 12.5012V18.933C0.980652 19.5271 1.45857 20.005 2.05262 20.005H8.4844C8.91765 20.005 9.31071 19.7459 9.47597 19.344C9.64123 18.942 9.5519 18.4819 9.24371 18.1737L7.4571 16.3871L10.9857 12.8586L14.5142 16.3871L12.7276 18.1737C12.4194 18.4819 12.3301 18.942 12.4953 19.344C12.6606 19.7459 13.0536 20.005 13.4869 20.005H19.9187C20.5127 20.005 20.9907 19.5271 20.9907 18.933V12.5012C20.9907 12.068 20.7316 11.6749 20.3296 11.5097C19.9276 11.3444 19.4676 11.4337 19.1594 11.7419L17.3728 13.5285L13.8442 10L17.3728 6.47145L19.1594 8.25805C19.4676 8.56624 19.9276 8.65557 20.3296 8.49031C20.7316 8.32505 20.9907 7.932 20.9907 7.49875V1.06696C20.9907 0.472913 20.5127 -0.00500488 19.9187 -0.00500488H13.4869C13.0536 -0.00500488 12.6606 0.254053 12.4953 0.65604C12.3301 1.05803 12.4194 1.51808 12.7276 1.82627L14.5142 3.61287L10.9857 7.14142L7.4571 3.61287L9.24371 1.82627C9.5519 1.51808 9.64123 1.05803 9.47597 0.65604C9.31071 0.254053 8.91765 -0.00500488 8.4844 -0.00500488Z" fill="white"/>
            </svg>
            <svg id="close" width="20" height="20" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M19.4079 3.4125C20.1891 2.63125 20.1891 1.3625 19.4079 0.581253C18.6266 -0.199997 17.3578 -0.199997 16.5766 0.581253L9.99535 7.16875L3.40785 0.587503C2.6266 -0.193747 1.35785 -0.193747 0.576599 0.587503C-0.204651 1.36875 -0.204651 2.6375 0.576599 3.41875L7.1641 10L0.582849 16.5875C-0.198401 17.3688 -0.198401 18.6375 0.582849 19.4188C1.3641 20.2 2.63285 20.2 3.4141 19.4188L9.99535 12.8313L16.5828 19.4125C17.3641 20.1938 18.6329 20.1938 19.4141 19.4125C20.1954 18.6313 20.1954 17.3625 19.4141 16.5813L12.8266 10L19.4079 3.4125Z" fill="white"/>
            </svg>
        </div> 
    </div>
</template>

<script lang="ts">
    document.getElementById("minimize")?.addEventListener("click", () => appWindow.minimize());
    document.getElementById("maximize")?.addEventListener("click", () => appWindow.maximize());
    document.getElementById("close")?.addEventListener("click", () => appWindow.close());
</script>


<style scoped>
    .titlebar {
        width: 100%;
        display: flex;
        align-items: center;
        flex-direction: row;
        justify-content: space-between;
        font-family: Inter;
        color: white;
        height: 2em;
        background-color: #242424;
        user-select: none;
    }

    .titlebar > * {
        padding: 0 0.75em 0 0.75em;
    }

    #title {
        font-weight: 400;
    }

    #title > small {
        color: #757575;
        font-weight: 300;
    } 

    .titlebuttons {
        display: flex;
        align-items: center;
        gap: 0.75em;
    }

    .titlebuttons > * {
        width: 1.2em;
        height: auto;
    }

</style>