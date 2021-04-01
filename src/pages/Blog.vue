<template>
  <Layout>
    <div v-for="edge in $page.allPosts.edges" :key="edge.node.id">
      <h1 v-html="edge.node.title" />
      <div v-html="edge.node.body"></div>
    </div>
  </Layout>
</template>

<page-query>

  query {
  allPosts {
    edges {
      node {
        id
        title
        body
      }
    }
  }
}

</page-query>