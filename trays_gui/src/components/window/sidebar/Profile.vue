<script setup lang="ts">
</script>

<template>
    <div id="profile">
        <img id="mchead" src="https://s3-alpha-sig.figma.com/img/5ca5/15fa/991323e7021ef3ec8db58fc797d1334b?Expires=1703462400&Signature=POJD17KH6RVbl1~0rXZRLx2NfM7PAU3hf60Zj-R-a6g7PX5Ecdz4rHNItZwim-Fq-XPjguvzYQLtMVOAVC5uHr1UkRhIE7lBqYq0NMVsNn0BYsc0HTRshfpv3LKMJJbBiwnIjrogCpYjSO6vUpwzc5BDatdnFF0PW1MXsgnUElr4N1kavEA67JyulJMEUqNNoB4dt-Smf7xQY8cVYv3r44qxem4Linqzmgm0eSjdHyWvvqRcJPK3psvRtNVv14ZWd8XKRQY~O~MPIMuJnSRWOtm6ajIAZqIBgXYDzykzkEn5UM94wdTqDroofdNriA1JxeG6RDqR7duSYEt~jrR-og__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4" alt="Profile Picture" />
        <div id="profile-info">
            <p id="username">MignonPetitXelow</p>
            <p id="switch-account">Switch Account</p>
        </div>
    </div>
</template>

<style scoped>
    #profile {
        display: flex;
        flex-direction: row;
        background-color: #323232;
        align-items: center;
        gap: 0.625em;
        border-radius: 0.938em;
        border-width: 100px;
        padding: 0.625em;
    }

    #profile-info {
        display: flex;
        flex-direction: column;
        gap: 0.3125em;
        justify-content:flex-end;
    }

    #profile-info > p {
        margin: 0;
    }

    #username {
        font-size: 1.563em;
        font-weight: 600;
    }

    #switch-account {
        font-size: 0.938em;
        color: #A5A5A5;
        font-weight: 300;
        cursor: pointer;
    }

    #mchead {
        width: 4.375em;
        height: 4.375em;
        image-rendering: pixelated;
        border-radius: 15%;
        box-shadow: 0px 4px 4px 0px rgba(0, 0, 0, 0.25); 
    }
</style>