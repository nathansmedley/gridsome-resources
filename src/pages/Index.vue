<template>
  <Layout>
    <Nav mode="dark"></Nav>
    <NewsBlock></NewsBlock>
    <Footer mode="dark"></Footer>
  </Layout>
</template>

<page-query>
query Home ($page: Int) {
  allWordPressPost (page: $page, perPage: 10) @paginate {
    pageInfo {
      totalPages
      currentPage
    }
    edges {
      node {
        id
        title
        path
        excerpt
      }
    }
  }
}
</page-query>

<script>
import { Pager } from 'gridsome'
import Post from '~/components/Post.vue'

import Nav from "~/components/Nav.vue";
import Footer from "~/components/Footer.vue";
import NewsBlock from "~/componenents/NewsBlock.vue";

export default {
  components: {
    Pager,
    Post,
    Nav,
    Footer,
    NewsBlock
  },
  metaInfo: {
    title: 'Resources from Moneypenny'
  }
}
</script>
