<template>
  <section class="bg-base-foreground">
    <div class="container mx-auto p-4 sm:pb-10 relative box-border">
      <div class="prose !container dark:prose-invert">
        <h2>Authors</h2>
        <ul class="my-4">
          <li
            v-for="item in AUTHORS"
            :key="item.person"
          >
            <span class="block"
              ><span class="font-bold">{{ item.person }}</span> -
              {{ item.position }}</span
            >
            <span>{{ item.location }}</span>
          </li>
        </ul>

        <div>
          <h2>Contributing Collections</h2>
          <ul>
            <li
              v-for="item in CONTRIBUTORS"
              :key="item.person"
            >
              <span class="font-bold">{{ item.person }}</span> -
              {{ item.location }}
            </li>
          </ul>
        </div>
        <div class="my-4">

          <ul>
            <li
              v-for="item in ASSISTANT_EDITORS"
              :key="item.person"
            >
              <span class="font-bold">{{ item.person }}</span> -
              {{ item.location }}
            </li>
          </ul>
          <h2>Developers</h2>
          <ul>
            <li
              v-for="item in DEVELOPERS"
              :key="item.person"
            >
              <span class="font-bold">{{ item.person }}</span> -
              {{ item.location }}
            </li>
          </ul>
          </div>
      </div>
      <OSFLogo
        class="hidden xl:block opacity-10 w-[40rem] text-primary-color absolute right-0 bottom-56 dark:text-base-content"
      />
    </div>
         </section>
</template>

<script setup>

const AUTHORS = [
  {
    person: 'Sangmi Lee',
    position: 'Author',
    location:
      'ASU Biocollections, Biodiversity Knowledge Integration Center, Arizona State University, USA'
  },
  {
    person: 'K. Samanta Orellana',
    position: 'Author',
    location:
      'Biodiversity Institute and Natural History Museum, University of Kansas, USA'
  }
]

const CONTRIBUTORS = [
   {
    person: 'ASUCOB-',
    location: 'OBrien Collection, Arizona State University, USA (Sangmi Lee)'
  },
   {
    person: 'ASUHIC-',
    location: 'Hasbrouck Insect Collection, Arizona State University, USA (Sangmi Lee)'
  }
]

const DEVELOPERS = [
   {
    person: 'TaxonPages',
    location: 'TaxonPages Working Group'
  }
]
</script>
