<template>
    <div class="bottom">
        <!-- <PaiHang/> -->
        <!-- <QianDao/> -->
        <Rank/>
        <SignIn/>
        <!-- <Tongji/> -->
        <!-- <CuoTi/> -->
        <statistics/>
        <wrong/>
    </div>
</template>

<script>
    // import PaiHang from './PaiHang.vue'
    // import QianDao from './QianDao.vue'
    import Rank from './Rank.vue'
    import SignIn from './SignIn.vue'
    import Statistics from './statistics.vue'
    import wrong from './wrong.vue'
    // import Tongji from './TongJi.vue'
    // import CuoTi from './CuoTi.vue'


    export default {
        name: 'BottomLine',

        components: {
            // PaiHang,
            // QianDao,
            Rank,
            SignIn,
            // Tongji,
            // CuoTi
            Statistics,
            wrong
        }

    }
</script>

<style scoped>
    .bottom{
    height: 20vh;
    }
</style>
