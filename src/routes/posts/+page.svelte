<script>
// @ts-nocheck
  
  import { Container, Row, Col } from 'sveltestrap';
	import { Button, Card } from 'sveltestrap';
	import { Badge, Form, FormGroup, Input, Label } from 'sveltestrap';
  import Navbar from '../../components/+navbar.svelte'
  export let data;
  
</script>

<main>
  <Navbar/>
  <Container>
    <Card class="text-center mt-5 p-4">
      
        <h1>All posts 📰</h1>
      
      <Row class="mt-5 p-3">
        
        {#each data.posts as post}
        
        <Card class="card mb-4 p-5 text-center">
          <a class ="text-decoration-none" href="/posts/{post.id}/">
            <h2 class="text-black">{post.title}</h2>
          </a>
          <p>{post.body}</p>
          
        </Card>
        {/each}
      </Row>
    </Card>
    </Container>
</main>

<style>
  main{
  min-height: 100vh;
  background: lightgray;
}
  
</style>
