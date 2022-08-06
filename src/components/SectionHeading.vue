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

div.heading{
  margin-bottom: 3rem;
}

.container h2 {
  color: $sixth_color;
  font-size: $title_fs;
  text-transform: uppercase;
  font-weight: $title_fw;

}

.container h3 {
  font-weight: $subtitle_fw;
  font-size: $subtitle_fs;
  display: inline-block;
  padding-left: 1rem;
  padding-right: 1rem;
}

.container .highlited-subtitle {
  background-color: rgba($sixth_color, 0.4);
  border-radius: .3rem;
}

.container p {
  margin-top: 2.25rem;
  color: $third_color;
  margin-left: 0;
  font-size: $description_fs;
  font-weight: $description_fw;
  color: $second_color;
}

div .subtitle {
  margin-left: -0.8rem;
}

section#about {
  .highlited-subtitle {
    color: $fourth_color;
  }
  .non-highlited-subtitle {
    color: $first_color;
  }
  p,div{
    color: rgba($third_color, 0.7);
  }
  div.vehicle-size{
    color: $first_color;
    font-size: 1.5rem;
    font-weight: 600;
  }
}

section#services {
  .highlited-subtitle {
    color: $second_color;
  }
  .non-highlited-subtitle {
    color: $second_color;
  }
    p,div{
    color: $fifth_color;
  }  

}

section#process {
  .highlited-subtitle {
    color: $fourth_color;
  }
  .non-highlited-subtitle {
    color: $first_color;
  }
      p,div{
    color: rgba($third_color, 0.7);
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
  p,div{
    color: $second_color;
    }

}
section#getintouch {
  .highlited-subtitle {
    color: $fourth_color;
  }

  .non-highlited-subtitle {
    color: $first_color;
  }
  p,div{
    color: $fifth_color;
    }

}

h3.bolder-h3 {
  font-weight: 900;
  font-size: 5rem;
  text-transform: uppercase;
}
</style>