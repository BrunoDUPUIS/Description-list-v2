<script setup>
import FirstParagraph from './FirstParagraph.vue'
import Title from './Title.vue'
import SecondParagraph from './SecondParagraph.vue'
import ThirdParagraph from './ThirdParagraph.vue'

const props = defineProps({ personInfos: Object })
console.log(props.personInfos)
</script>

<template>
  <div class="card">
    <div>
      <img
        src="https://res.cloudinary.com/lereacteur-apollo/image/upload/v1704967000/RNCP31114/cours-vue/exo-sem-1/mystery-person_bueack.jpg"
        alt=""
      />
      <div>
        <Title
          :firstname="personInfos.firstname"
          :lastname="personInfos.lastname"
          :gender="personInfos.gender"
        />

        <FirstParagraph
          :age="personInfos.age"
          :job="personInfos.job"
          :gender="personInfos.gender"
        />
        <SecondParagraph
          :firstname="personInfos.firstname"
          :hobbies="personInfos.hobbies"
        />
        <ThirdParagraph :gender="personInfos.gender" :pet="personInfos.pet" />
      </div>
    </div>
    <font-awesome-icon :icon="['fas', 'heart']" />
  </div>
</template>

<style scoped>
img {
  width: 100%;
  border-radius: 5px;
  object-position: top;
  aspect-ratio: 16/10;
  margin-bottom: 20px;
  /* border: 2px solid yellow; */
}

svg {
  color: red;
  align-self: flex-end;
  /* border: 2px solid black; */
}

.card {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  gap: 30px;
}

.cards > div {
  width: calc((100% - 27px) / 4);
  padding: 10px;
  background-color: lightgrey;
  border-radius: 8px;
  box-shadow: 0 0 9px v-bind(personInfos.favoriteColor);

  /* border: 2px solid green; */
}

.cards > div > div {
  /* border: 1px solid green; */
}
</style>
