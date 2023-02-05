<script>
// @ts-nocheck
import { Container, Row, Col } from 'sveltestrap';
	import { Card } from 'sveltestrap';
  import Navbar from '../../../components/+navbar.svelte'
  export let data;
</script>

<main>
  <Navbar/>
  <Container>
    <Row class="mt-5 p-3">
      
      
      <Card class="mb-4 p-5">
        <Row>
          <h1>{data.post.title}</h1>
        </Row>
        <Row class="mt-5">
          <Col xs="12" sm="12" md="12" lg="6">
            <p>{data.post.body}</p>
          </Col>
          <Col>
            <img style="max-width: 100%" alt="news" src="https://source.unsplash.com/random/?{data.post.tags[0]}&1" >
          </Col>
        </Row>
        
        <footer class=" mt-5 text-center">
          <p>
            Published by Anton Olsson
          </p>
        </footer>
      </Card>
        
    </Row>
    
  </Container>
</main>

<style>
  main{
  min-height: 100vh;
  background: lightgray;
}
  
</style>
