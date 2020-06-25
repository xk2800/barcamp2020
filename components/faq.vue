<template>
  <b-container>
    <h3>
      <b class="roboto-fat text-purple" style="font-size:1.5em; letter-spacing:2px;">FAQs</b>
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
          question: 'Question 1',
          answer: 'Answer 1'
        },
        {
          id: '2',
          question: 'Question 2',
          answer: 'Answer 2'
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
