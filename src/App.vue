<script setup>
const firstPerson = {
  gender: 'female',
  firstname: 'Emily',
  lastname: 'Parker',
  age: 24,
  job: 'Teacher',
  hobbies: ['read books', 'go hiking'],
  pet: {
    name: 'Whiskers',
    age: 2,
    species: 'ferret',
  },
}

const secondPerson = {
  gender: 'male',
  firstname: 'Marcus',
  lastname: 'Bennett',
  age: 38,
  job: 'Architect',
  hobbies: ['watch bird', 'play chess'],
  pet: {
    name: 'Nala',
    age: 6,
    species: 'dog',
  },
}

const thirdPerson = {
  gender: 'female',
  firstname: 'Sophia',
  lastname: 'Rodriguez',
  age: 31,
  job: 'Environmental scientist',
  hobbies: ['play guitar', 'bake cakes'],
  pet: {
    name: 'Paws',
    age: 3,
    species: 'cat',
  },
}

const fourthPerson = {
  gender: 'male',
  firstname: 'Oliver',
  lastname: 'Hughes',
  age: 56,
  job: 'Carpenter',
  hobbies: ['paint', 'ride horses'],
  pet: {
    name: 'Bubble',
    age: 4,
    species: 'snake',
  },
}
</script>

<template>
  <main>
    <h1>Description list</h1>
    <section class="container">
      <div class="card">
        <img src="./assets/img/emily-parker.jpg" alt="Photo de Emily Parker" />
        <h2>{{ firstPerson.firstname + ' ' + firstPerson.lastname }}</h2>
        <p>
          {{ firstPerson.gender === 'female' ? 'She' : 'He' }} is a {{ firstPerson.age }}-year-old
          {{ firstPerson.job.toLocaleLowerCase() }}.
        </p>
        <p>
          Outside of work, {{ firstPerson.firstname }} likes to
          {{ firstPerson.hobbies[0] + ' and ' + firstPerson.hobbies[1] }}.
        </p>
        <p>
          At home, {{ firstPerson.gender === 'female' ? 'her' : 'his' }} lively companion is
          {{
            firstPerson.pet.name +
            ' a ' +
            firstPerson.pet.age +
            '-years-old ' +
            firstPerson.pet.species
          }}.
        </p>
        <font-awesome-icon :icon="['fas', 'heart']" />
      </div>
      <div class="card">
        <img src="./assets/img/marcus-bennett.jpg" alt="Photo de Marcus Bennett" />
        <h2>{{ secondPerson.firstname + ' ' + secondPerson.lastname }}</h2>
        <p>
          {{ secondPerson.gender === 'female' ? 'She' : 'He' }} is a {{ secondPerson.age }}-year-old
          {{ secondPerson.job.toLocaleLowerCase() }}.
        </p>
        <p>
          Outside of work, {{ secondPerson.firstname }} likes to
          {{ secondPerson.hobbies[0] + ' and ' + secondPerson.hobbies[1] }}.
        </p>
        <p>
          At home, {{ secondPerson.gender === 'female' ? 'her' : 'his' }} lively companion is
          {{
            secondPerson.pet.name +
            ' a ' +
            secondPerson.pet.age +
            '-years-old ' +
            secondPerson.pet.species
          }}.
        </p>
        <font-awesome-icon :icon="['fas', 'heart']" />
      </div>
      <div class="card">
        <img src="./assets/img/sophia-rodriguez.jpg" alt="Photo de Sophia Rodriguez" />
        <h2>{{ thirdPerson.firstname + ' ' + thirdPerson.lastname }}</h2>
        <p>
          {{ thirdPerson.gender === 'female' ? 'She' : 'He' }} is a {{ thirdPerson.age }}-year-old
          {{ thirdPerson.job.toLocaleLowerCase() }}.
        </p>
        <p>
          Outside of work, {{ thirdPerson.firstname }} likes to
          {{ thirdPerson.hobbies[0] + ' and ' + thirdPerson.hobbies[1] }}.
        </p>
        <p>
          At home, {{ thirdPerson.gender === 'female' ? 'her' : 'his' }} lively companion is
          {{
            thirdPerson.pet.name +
            ' a ' +
            thirdPerson.pet.age +
            '-years-old ' +
            thirdPerson.pet.species
          }}.
        </p>
        <font-awesome-icon :icon="['fas', 'heart']" />
      </div>
      <div class="card">
        <img src="./assets/img/olivier-hughes.jpg" alt="Photo de Olivier Hughes" />
        <h2>{{ fourthPerson.firstname + ' ' + fourthPerson.lastname }}</h2>
        <p>
          {{ fourthPerson.gender === 'female' ? 'She' : 'He' }} is a {{ fourthPerson.age }}-year-old
          {{ fourthPerson.job.toLocaleLowerCase() }}.
        </p>
        <p>
          Outside of work, {{ fourthPerson.firstname }} likes to
          {{ fourthPerson.hobbies[0] + ' and ' + fourthPerson.hobbies[1] }}.
        </p>
        <p>
          At home, {{ fourthPerson.gender === 'female' ? 'her' : 'his' }} lively companion is
          {{
            fourthPerson.pet.name +
            ' a ' +
            fourthPerson.pet.age +
            '-years-old ' +
            fourthPerson.pet.species
          }}.
        </p>
        <font-awesome-icon :icon="['fas', 'heart']" />
      </div>
    </section>
  </main>
</template>

<style scoped>
main h1 {
  text-align: center;
  margin-bottom: 40px;
}

h1 {
  color: white;
  font-size: 70px;
  font-weight: bold;
}

section {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 25px;
  padding: 0 40px;
  align-items: stretch;
}

.card {
  width: calc((100% - 30px) / 4);
  background-color: #efeeee;
  padding: 10px;
  border-radius: 10px;
  box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.card img {
  width: 100%;
  aspect-ratio: 16/10;
  object-position: top;
  object-fit: cover;
  border-radius: 5px;
  margin-bottom: 10px;
}

.card h2 {
  font-weight: bold;
  font-size: 18px;
}

.job {
  text-transform: lowercase;
}

.card svg {
  font-size: 25px;
  color: #7f7f7f;
  align-self: flex-end;
}

@media (max-width: 1250px) {
  section {
    flex-wrap: wrap;
  }

  .card {
    width: 280px;
  }
}

@media (max-width: 550px) {
  main h1 {
    font-size: 45px;
  }
}
</style>
