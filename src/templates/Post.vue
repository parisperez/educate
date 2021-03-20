<template>
  <Layout>
    <div class="post-title">
      <h1 class="post-title__text">
        {{ $page.post.title }}
      </h1>

      <PostMeta :post="$page.post" />

    </div>

    <div class="post content-box">
      <div class="post__header">
        <g-image alt="Cover image" v-if="$page.post.cover_image" :src="$page.post.cover_image" />
      </div>

      <div class="post__content" v-html="$page.post.content" />

      <div class="post__footer">
        <PostTags :post="$page.post" />
      </div>
    </div>

    <div class="post-comments">
      <!-- Add comment widgets here -->
    </div>

    <Author class="post-author" />
  </Layout>
</template>

<static-query>
query {
  metadata { 
        siteName 
        siteDescription 
        siteUrl 
        author 
    } 
  }
</static-query>

<script>
import PostMeta from '~/components/PostMeta'
import PostTags from '~/components/PostTags'
import Author from '~/components/Author.vue'



export default {
  components: {
    Author,
    PostMeta,
    PostTags
  },
  metaInfo () {
    return {
      title: this.$page.post.title,
      meta: [
        {
          name: 'description',
          content: this.$page.post.description
        },
        {
         name: 'keywords',
         content: this.$page.post.tags.title
        },
        // start open-graph
        {
          property: 'og:title',
          content: this.$page.post.title
        },
        {
          property: 'og:description',
          content: this.$page.post.description
        },
        {
          property: 'og:image',
          content: this.$static.metadata.siteUrl
        },
        {
          property: 'og:url',
          content: this.$static.metadata.siteUrl + this.$page.post.path
        },
        // end open-graph
      ],
       // start json-ld
      script: [
        {
          type: 'application/ld+json',
          json: {
            '@context': 'http://schema.org',
            '@type': 'BlogPosting',
            articleBody: this.$page.post.content,
            datePublished: this.$page.post.date,
            dateModified: this.$page.post.date,
            author: {
              '@type': 'Person',
              name: this.$static.metadata.siteUrl
            },
            publisher: {
              '@type': 'Organization',
              name: 'Listen Portland',
              logo: {
                '@type': 'ImageObject',
                url:  'this.$static.metadata.siteUrl',
              }
            },
            headline: this.$page.post.title,
            image: this.$static.metadata.siteUrl,
            mainEntityOfPage: {
              '@type': 'WebPage',
              '@id': this.$static.metadata.siteUrl + this.$page.post.path
            }
          }
        }
      ]
      // end json-ld
    }
  }
}
</script>

<page-query>
query Post ($id: ID!) {
  post: post (id: $id) {
    title
    path
    date (format: "D. MMMM YYYY")
    timeToRead
    tags {
      id
      title
      path
    }
    description
    content
  }
}
</page-query>

<style lang="scss">
.post-title {
  padding: calc(var(--space) / 2) 0 calc(var(--space) / 2);
  text-align: center;
}

.post {

  &__header {
    width: calc(100% + var(--space) * 2);
    margin-left: calc(var(--space) * -1);
    margin-top: calc(var(--space) * -1);
    margin-bottom: calc(var(--space) / 2);
    overflow: hidden;
    border-radius: var(--radius) var(--radius) 0 0;

    img {
      width: 100%;
    }

    &:empty {
      display: none;
    }
  }

  &__content {
    h2:first-child {
      margin-top: 0;
    }

    p:first-of-type {
      font-size: 1.2em;
      color: var(--title-color);
    }

    img {
      width: calc(100% + var(--space) * 2);
      margin-left: calc(var(--space) * -1);
      display: block;
      max-width: none;
    }
  }
}

.post-comments {
  padding: calc(var(--space) / 2);

  &:empty {
    display: none;
  }
}

.post-author {
  margin-top: calc(var(--space) / 2);
}

    // cover_image (width: 860, blur: 10)
</style>
