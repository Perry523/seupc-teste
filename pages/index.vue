<template>
  <div>
    <div class="text-center mb-4 h5">
      <b>Usuários: 85</b>      
    </div>
    <div class="d-flex flex-wrap">
      <div v-for="(client, i) in clients" :key="i" class="col-12 col-md-6 col-lg-4">
        <client-suggestions-card :client="client"></client-suggestions-card>
      </div>
    </div>
  </div>
</template>

<script>
import ClientSuggestionsCard from '@/components/ClientSuggestionsCard.vue'
export default {
  name: 'IndexPage',
  components: {
    ClientSuggestionsCard,
  },
  data() {
    return {
      clients: [
        {
          name: 'Lucas',
          phone: '31 9 1234-5678',
          email: 'lucas@gmail.com',
          tags: ['tag 1', 'tag 2', 'tag 3'],
          suggestions: [
            'Gostaria que desse pra buscar um notebook',
            'Não estou conseguindo entrar na página do notebook',
          ],
        },
        {
          name: 'Vitor',
          phone: '31 9 5678-1234',
          email: 'lucas@gmail.com',
          tags: ['tag 1', 'tag 2', 'tag 3'],
          suggestions: [
            'Gostaria que desse pra buscar um notebook',
            'Não estou conseguindo entrar na página do notebook',
            'Queria ver vídeos reviews do notebook',
            'Não estou conseguindo logar',
          ],
        },
        {
          name: 'Lucas',
          phone: '31 9 1234-5678',
          email: 'lucas@gmail.com',
          tags: ['tag 1', 'tag 2', 'tag 3'],
          suggestions: [],
        },
      ],
    }
  },
}
</script>
<style>
@media (max-width: 768px) {
  .no-border-on-mobile {
    border-top: none;
    border-left: none;
    border-right: none;
  }
}
@media (min-width: 768px) {
  .shadow-on-desktop {
    box-shadow: 0 0.5rem 1rem rgb(0 0 0 / 15%);
  }
}
</style>
