<template>
  <div class="home">
    <h1 class="app-title">YaymoY</h1>
    <TourCardView>
      <TourCard
        v-for="tour in mockingTour"
        :key="tour.id"
        :id="tour.id"
        :title="tour.title"
        :shortDescription="tour.shortDescription"
        :description="tour.description"
        :image="tour.image"
        :categoryName="tour.category"
        :schedules="tour.schedules"
      >
      </TourCard>
    </TourCardView>
  </div>
</template>

<script>
// @ is an alias to /src
import TourCard from '@/components/TourCard'
import TourCardView from '@/components/TourCardView'
export default {
  name: 'home',
  data () {
    return {
      mockingTour: [
        {
          id: '1029310832122098',
          category: 'SAIL BOAT',
          image: 'https://images.pexels.com/photos/457878/pexels-photo-457878.jpeg',
          title: 'Phi Phi/Khai /YaoYai Island by Speed Boat',
          shortDescription: 'Phi Phi Island is the most popular programs available by combiningvisits to three islands.',
          description: 'hi Phi Island is the most popular programs available by combiningvisits to three islands. Phi Phi Island , Khai island and Kho Yao Yai Islands by speed boat all in one day.You will be having a great time exploring YaoYai where there are wonderful beaches and the best of times to be had on this breathtaking Island.',
          schedules: [
            {
              time: '10.00',
              description: 'จริงอั้นแหนะ Lorem ipsum dolor sit amet, consectetur adipiscing elit. Mauris nunc elit, volutpat faucibus auctor ut, faucibus at dui. Duis vehicula.'
            },
            {
              time: '12.00 - 13.00',
              description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis sodales massa mi, sit amet aliquet diam malesuada id. Class aptent'
            },
            {
              time: '13.30 - 15.00',
              description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque aliquam urna non velit rhoncus dictum. Mauris at justo sodales tellus.'
            },
            {
              time: '17.00-19.00',
              description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque nec placerat odio. Ut in ultrices dui. Lorem ipsum dolor sit.'
            },
            {
              time: '19.30',
              description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque nec placerat odio. Ut in ultrices dui. Lorem ipsum dolor sit.'
            }
          ]
        },
        {
          id: '123123123',
          category: 'HOLIDAY',
          image: 'https://images.pexels.com/photos/40976/beach-beautiful-blue-coast-40976.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940',
          title: 'James Bond & Canoe & Nang She by VIP Cruise',
          shortDescription: 'If you have been wide-eyed about JAMES BOND ISLAND',
          description: 'If you have been wide-eyed about JAMES BOND ISLAND. Then our special experience excursion adventure tour to UNSEEN PHANG-NGA will really and truly leave you extraordinarily wide eyed. We with pleasure present to you on intinerary for the specially amazing Unseen of Phang nga daily tour.',
          schedules: [
            {
              time: '10.00',
              description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Mauris nunc elit, volutpat faucibus auctor ut, faucibus at dui. Duis vehicula.'
            },
            {
              time: '12.00 - 13.00',
              description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis sodales massa mi, sit amet aliquet diam malesuada id. Class aptent'
            },
            {
              time: '13.30 - 15.00',
              description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque aliquam urna non velit rhoncus dictum. Mauris at justo sodales tellus.'
            },
            {
              time: '17.00',
              description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque nec placerat odio. Ut in ultrices dui. Lorem ipsum dolor sit.'
            }
          ]
        },
        {
          id: 'alskdjflasj',
          category: 'RESORT',
          image: 'https://images.pexels.com/photos/69787/sea-ocean-water-palms-69787.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940',
          title: 'Jakkapan Report And spain Hair Spa Hair Tookleaw',
          shortDescription: 'Jakkapan is the most handsome man in PHUKETTTTTT.',
          description: 'If you have been wide-eyed about JAMES BOND ISLAND. Then our special experience excursion adventure tour to UNSEEN PHANG-NGA will really and truly leave you extraordinarily wide eyed. We with pleasure present to you on intinerary for the specially amazing Unseen of Phang nga daily tour.',
          schedules: [
            {
              time: '10.00',
              description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Mauris nunc elit, volutpat faucibus auctor ut, faucibus at dui. Duis vehicula.'
            },
            {
              time: '12.00 - 13.00',
              description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis sodales massa mi, sit amet aliquet diam malesuada id. Class aptent'
            },
            {
              time: '13.30 - 15.00',
              description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque aliquam urna non velit rhoncus dictum. Mauris at justo sodales tellus.'
            },
            {
              time: '17.00',
              description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque nec placerat odio. Ut in ultrices dui. Lorem ipsum dolor sit.'
            }
          ]
        }
      ]
    }
  },
  components: {
    TourCard,
    TourCardView
  }
}
</script>

<style>
.home {
  padding: 8px;
}
.app-title {
  text-align: left;
  font-family: "Pacifico";
  font-size: 1.7rem;
  font-weight: 3;
}
</style>
