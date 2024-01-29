<template>
    <div>{{ user }} Repositories</div>
</template>

<script>
export default {
    props: {
        user: {
            type: String,
            required: true,
        },
    },
    // eslint-disable-next-line no-unused-vars
    setup(_props, _ctx) {
        return {
            
        }
    },
    data() {
      return {
        repositories: [],
        filters: {},
        searchQuery: "",
      };
    },
    computed: {
      filteredRepositories() {
        return null;
      },
      repositoriesMatchingSearchQuery() {
        return null;
      }
    }
}
</script>