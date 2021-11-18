<template>
  <main>
        <Banner />
        <section>
            <Card 
                src="https://a0.muscache.com/im/pictures/eb9c7c6a-ee33-414a-b1ba-14e8860d59b3.jpg?im_w=720"
                title="Expériences en ligne"
                description="Des activités uniques que nous pouvons faire ensemble, animées par un monde d'hôtes."
            />
            <Card
                src="https://a0.muscache.com/im/pictures/15159c9c-9cf1-400e-b809-4e13f286fa38.jpg?im_w=720"
                title="Des séjours uniques"
                description="Des espaces qui sont plus qu'un simple endroit pour dormir."
            />
            <Card
                src="https://a0.muscache.com/im/pictures/fdb46962-10c1-45fc-a228-d0b055411448.jpg?im_w=720"
                title="Des maisons entières"
                description="Des lieux privés confortables, avec de la place pour les amis ou la famille."
            />
        </section>
        <section>
            <Card
                src="https://media.nomadicmatt.com/2019/airbnb_breakup3.jpg"
                title="Appartement de 3 chambres à Deauville"
                description="Appartement avec une vue imprenable sur la plage"
                price="130€/nuit"
            />
            <Card
                src="https://thespaces.com/wp-content/uploads/2017/08/Courtesy-of-Airbnb.jpg"
                title="Penthouse à Paris"
                description="Profitez des vues incroyables de Paris avec ce magnifique penthouse"
                price="350€/nuit"
            />
            <Card
                src="https://media.nomadicmatt.com/2018/apartment.jpg"
                title="Appartement 1 chambre"
                description="Appartement avec de superbes équipements"
                price="70€/nuit"
            />
        </section>
  </main>

</template>

<script>
import Banner from '../components/Banner.vue'
import Card from '../components/Card.vue'
export default {
    name: 'Home',
    components: {
        Banner,
        Card
    }
}
</script>

<style scoped lang='scss'>
section {
    display: flex;
    padding: 30px;
}
</style>