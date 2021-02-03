<template>
<div id="testimonials">
  <div v-for="(review, index) in reviews" :key='`review${index}`' class="review" :class='`review${index}`'
       :style="{gridTemplateColumns:`repeat(${review.reviews.length}, 1fr)`}">
    <div class="top" :style="{gridColumn:`span ${review.reviews.length}`}">
      <h3>{{ review.title }}</h3>
    </div>
    <div class="bot" v-for="(subReview, index) in review.reviews">
      <div class="testiHolder">
      <p>{{subReview.content}}</p>
        <p>{{subReview.author}}</p>
      </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: 'Testimonials',
  data(){
    return{
      reviews:[
        {
          title: 'Google Reviews',
          reviews:[
            {
              content:'"Everybody at Hoglund made a hard situation so much easier! From the moment I called, to meeting with an attorney to figure out my options, all the way to my discharge hearing this morning, Hoglund has been with me every step of the way. They kept in constant communication, kept me informed of all the steps, and answered my questions. I can\'t say enough about how excellent my experience was with Hoglund. I highly recommend them if you need an attorney."',
              author:'B.L.',
            },
            {
              content:'"I have been so impressed by this law firm from day one. I am so grateful for the help and support that I received. Hoglund Law has gone above and beyond and exceeded my expectations. I highly recommend them. If I could summarize in one word: kindness. They are going to do everything they can to answer your questions and make sure you are prepared and informed and complete the paperwork thoroughly. Hoglund Law has shown me that lawyers can be great counselors. I felt supported by them at every turn. I believe they challenge the lawyer stigma: the lawyers at Hoglund are great people."',
              author:'Matthew Hardy',
            },
            {
              content:'"Hoglund Law firm was very helpful and friendly staff at all times. In addition, to there professionalism Hoglund worked hard, answered all of my questions at anytime and stayed on top of things in regards to my case. It was a pleasure working with Hoglund law firm and it\'s there pleasure to work for you."',
              author:'Michelle Barnes Davenport',
            }
          ]
        },
        {
          title: 'Our Testimonials',
          reviews:[
            {
              content:'"They helped make a very difficult and overwhelming process easy. Staff is busy, but I have always been able to get someone on the phone the same day and many times right away. They were proactive in reaching out to me as needed and always were patient in answering my questions and concerns. I would highly recommend them to anyone if you are looking for an attorney\'s office who genuinely cares about their clients."',
              author:'Gonzalo Curiel',
            },
            {
              content:'"Love Hoglund law office. They took very good care of me. Always had time for my phone calls. If I had to leave a message they always got back with me in a timely manner. Awesome attorneys to work with. Highly recommend them!!!"',
              author:'Brenda Millsl',
            }
          ]
        },
        {
          title: 'Lawyers.com Reviews',
          reviews:[
            {
              content:'"After going through a divorce after a 23 year marriage, I sought assistance from the Hoglund Law office for my bankruptcy. Robert and his team were professional, prompt and assisted me with everything needed to regain hope."',
              author:'Past Client',
            },
            {
              content:'"Andrew did a wonderful job with my daughter case. Very professional and explained everything in detail. This was second time for her Jennifer was our first attorney she was less professional and not very prepared or we would have won back then."',
              author:'Past Client',
            }
          ]
        },
      ],
    }
  }
}
</script>

<style scoped lang="scss">
#testimonials{
  padding: 3rem 0 3rem 0;
  display: grid;
  grid-gap: 2rem;
}
.review{
  display: grid;
  @media (max-width: 1080px) {
    grid-template-columns: 1fr !important;
    .top{
      grid-column: span 1 !important;
    }
  }
  .bot{
    border-right: white 3px solid;
    padding: 0 1rem 0 0;
    margin: 0 2rem 0 0;
    &:last-child{
      border: none !important;
      margin: 0 !important;
      padding: 0 !important;
    }
    @media (max-width: 1080px) {
      padding: 0;
      margin: 0;
      border: none;
    }
  }

}
</style>
