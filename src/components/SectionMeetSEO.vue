<template>
    <section>
        <div class="container">
            <InnerSectionTitle 
                h2-text="meet the new agency SEO template from the avada team"
                p-text="Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium."
            />
            <div class="features-container">
                <div v-for="(feature, index) in templateFeatures" :key="index" class="feature">
                    <i :class="feature.icon"></i>
                    <h3>{{ feature.title }}</h3>
                    <p>{{ feature.paragraph }}</p>
                </div>
            </div>

            <img src="../assets/images/agency-seo-desk-front.jpg" alt="Agency SEO desk front image">
        </div>
    </section>
</template>

<script>
import InnerSectionTitle from './InnerSectionTitle.vue';

export default {
    name: 'SectionMeetSEO',
    components: {
        InnerSectionTitle,
    },
    data: function() {
        return{
            templateFeatures: [
                {
                    icon: 'fas fa-road',
                    title: 'establish goals',
                    paragraph: 'Aliquam non elit lacus. Praesent aliquet, ipsum id scelirisque convallis, mi ligula euismod odio, cel dictum mi risus a mi.',
                },
                {
                    icon: 'fas fa-video',
                    title: 'work with a team',
                    paragraph: 'Cras semper auctor aliquam. Sed porta sed lacus sit amet consectetur. Lorem ipsum dolor sit amet, consecteur adipiscin.',
                },
                {
                    icon: 'fas fa-tint',
                    title: 'get results',
                    paragraph: 'Vestibulum scelirisque egestas lectus sit amet molestie. Donec consectetur cursus est sed blandit. Nunc sed risus lacus.',
                },
            ]
        }
    }
}
</script>

<style scoped lang="scss">
@import '../style/variables.scss';

    section{
        padding-top: 50px;
        background-color: $alabaster;
        color: black;
        text-align: center;
        .features-container{
            display: flex;
            flex-flow: row nowrap;
            justify-content: space-around;
            align-items: center;
            .feature{
                display: flex;
                flex-flow: column nowrap;
                justify-content: space-around;
                align-items: center;

                background-color: white;
                -webkit-box-shadow: -1px -1px 30px 1px rgba(0,0,0,0.1); 
                box-shadow: -1px -1px 30px 1px rgba(0,0,0,0.1);

                min-height: 250px;
                margin: 50px 10px;
                padding: 30px;
                i{
                    color: $yelloworange;
                    font-size: 30px;
                }
                h3{
                    margin-top: 30px;
                    margin-bottom: 15px;
                    text-transform: capitalize;
                }
                p{
                    font-size: 0.9rem;
                    font-weight: lighter;
                }
            }
        }
        img{
            width: 100%;
            margin-bottom: -5px;
        }
    }
</style>