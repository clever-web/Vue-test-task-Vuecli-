<template>
    <div class="vue-footer">
        <p class="footer-title">Test Task, 2022</p>
        <div>
            <a href="tel:518-363-2171">518-363-2171</a>
            <p class="address">91 Park St. Fairhope, AL 36532</p>
        </div>
    </div>
</template>

<script>
    export default {
        name: "vue-footer",
    }
</script>

<style scoped>
 .vue-footer {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    padding: 31px 48px;
    gap: 10px;
    background: #292D32;
    box-shadow: 0px -4px 4px rgba(0, 0, 0, 0.25);
 }

 .footer-title {
    font-family: 'Roboto';
    font-style: normal;
    font-weight: 700;
    font-size: 18px;
    color: #FFFFFF;
 }
 .address {
    font-family: 'Roboto';
    font-style: normal;
    font-weight: 500;
    font-size: 14px;
    color: #FFFFFF;
 }

 a, a:hover {
    color: white;
 }
</style>