<template>
  <b-container>
    <h3>
      <b class="roboto-fat text-purple text-title">FAQs</b>
    </h3>
    <div role="tablist" class="mt-3">
      <div class="card bg-barcamp">
        <ul class="list-group list-group-flush">
          <li
            v-for="faq in faqs"
            :key="faq.id"
            class="list-group-item text-purple"
          >
            <b-link v-b-toggle="`faq-${faq.id}`" class="faq-question">
              <h5>
                {{ faq.question }}
              </h5>
            </b-link>
            <b-collapse :id="`faq-${faq.id}`" visible accordion="my-accordion" role="tabpanel" class="mt-3">
              <b-card-text>{{ faq.answer }}</b-card-text>
            </b-collapse>
          </li>
        </ul>
      </div>
    </div>
  </b-container>
</template>

<script>
export default {
  data: () => {
    return {
      faqs: [
        {
          id: '1',
          question: 'What is the theme for Barcamp Cyberjaya 2020?',
          answer: 'The theme for Barcamp Cyberjaya 2020 will be based around: Technology, Healthcare and Entrepreneurship.'
        },
        {
          id: '2',
          question: 'How will the event be held?',
          answer: 'To ensure every participant\'s safety, our event will be held online. The platform we will be using is Google Meet, and the registered audience will receive our invitation to join the room. Speakers will then share knowledge with the audience after they join the room.'
        },
        {
          id: '3',
          question: 'How do I apply to become a speaker?',
          answer: 'You may register via this link: '
        },
        {
          id: '4',
          question: 'How can I participate in this event as an audience?',
          answer: 'You may register via this link: '
        },
        {
          id: '5',
          question: 'How do I sponsor this event?',
          answer: 'You can contact us a this email: '
        },
        {
          id: '6',
          question: 'How long is each session?',
          answer: 'Each session is about 45 minutes duration.'
        },
        {
          id: '7',
          question: 'Do I have to pay any registration fee?',
          answer: 'No, registration is free!'
        }
      ]
    }
  }
}
</script>

<style scoped>
  .faq-question {
    color:rgb(50,23,77);
  }

  .faq-question:hover {
    color:rgba(50,23,77,0.8);
    text-decoration: none;
  }
</style>
