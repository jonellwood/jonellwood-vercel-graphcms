<script context="module">
  import { variables } from '../components/variables';
  import { gql, GraphQLClient } from 'graphql-request'

  export async function load() {
    const graphcms = new GraphQLClient(
      // import.meta.env.VITE_GRAPHCMS_URL,
      variables.VITE_GRAPHCMS_URL,
      {
        headers: {},
      }
    )

    const query = gql`
      query {
        posts {
          id
          title
          slug
          date
          excerpt
          coverImage{
            url
          }
        }
      }
    `

    const { posts } = await graphcms.request(query)

    return {
      props: {
        posts,
      },
    }
  }
</script>

<script>
  export let posts
</script>


<div class="post-list">
  {#each posts as post}
    <span>
      <a href="/post/{post.slug}">{post.title}</a>
      <img src={post.coverImage.url} alt="{post.title}" width=100px height=100px>
      <p class="post-excerpt">{post.excerpt}</p>
    </span>
  {/each}
</div>

<style>
  .post-list{
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr;
    padding: 5px;
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  }
  span{
    display: grid;
    grid-template-columns: 1fr 1fr;
    border: 2px solid #fcc600;
    border-radius: 7px;
    box-shadow: 2px 2px 5px 5px #4969e190;
    margin: 15px;
    padding: 15px;
    color: #2e2e2e;
    max-width: 300px;
  }
  span .post-excerpt{
    grid-column: 1/3;
  }
  span img{
    justify-items: right;
  }
  span:hover{
    box-shadow: 2px 2px 5px yellow;
    background: white;
    transform: scale(110%);
    transition: all 0.5s ease .5s;
  }
  a{
    text-decoration: none;
    list-style: none;
    padding: 15px;
    color: #2e2e2e;

  }
  @media (max-width: 1080px) {
    .post-list {
      grid-template-columns: 1fr 1fr;
      padding: 0 10px;
    }
    .post-excerpt{
      display: none;
    }
  }
  @media (max-width: 680px) {
    .post-list {
      grid-template-columns: 1fr;
      padding: 0 10px;
    }
    .post-excerpt{
      display: none;
    }
    img{
      justify-items: right;
      width: 50px;
      height: 50px;
    }
  }
</style>
