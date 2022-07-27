<template>

  <div class="heading d-flex flex-column">
    <h2>{{ page.extend_title }}</h2>
    <div v-if="page.highlitedPosition == 'before'" class="subtitle">
      <h3 class="highlited-subtitle">{{ page.highlitedSubtitle }}</h3>
      <h3 class="non-highlited-subtitle"> {{ page.subtitle }}</h3>
    </div>
    <div v-else-if="page.highlitedPosition == 'none'" class="subtitle">
      <h3 class="bolder-h3">{{ page.subtitle }}</h3>
    </div>
    <div v-else class="subtitle">
      <h3 class="non-highlited-subtitle">{{ page.subtitle }}</h3>
      <h3 class="highlited-subtitle"> {{ page.highlitedSubtitle }}</h3>
    </div>
    <p>{{ page.description }}</p>
  </div>

</template>

<script>
export default {
  name: 'SectionHeading',
  props: {
    page: {
      type: Object,
      required: true,
    },
  },

}
</script>

<style lang="scss">
@import "../styles/variables.scss";

.container h2 {
  color: $sixth_color;
  font-size: 1rem;
}

.container h3 {
  font-weight: 900;
  font-size: 2.5rem;
  display: inline-block;
  padding-left: 0.5rem;
  padding-right: 0.5rem;
}

.container .highlited-subtitle {
  background-color: rgba($sixth_color, 0.4);
  border-radius: 3px;
}

.container p {
  color: $third_color;
  margin-left: 0;
}

div .subtitle {
  margin-left: -0.5rem;
}

section#about {
  .highlited-subtitle {
    color: $fourth_color;
  }

  .non-highlited-subtitle {
    color: $first_color;
  }
}

section#services {
  .highlited-subtitle {
    color: $second_color;
  }

  .non-highlited-subtitle {
    color: $second_color;
  }

}

section#process {
  .highlited-subtitle {
    color: $fourth_color;
  }

  .non-highlited-subtitle {
    color: $first_color;
  }
}

section#numbers {
  .highlited-subtitle {
    color: $second_color;
  }

  .non-highlited-subtitle {
    color: $second_color;
  }

}

section#testimonials {
  .highlited-subtitle {
    color: $second_color;
  }

  .non-highlited-subtitle {
    color: $second_color;
  }

}

h3.bolder-h3 {
  font-weight: 900;
  font-size: 5rem;
  text-transform: uppercase;
}
</style>