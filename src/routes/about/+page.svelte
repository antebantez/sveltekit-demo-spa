<script>
	import { Container, Row, Col } from 'sveltestrap';
	import { Button, Card } from 'sveltestrap';
	import { Badge, Form, FormGroup, Input, Label } from 'sveltestrap';
  import Navbar from '../../components/+navbar.svelte'
  let name = "";
  let password = ""

  function submitForm() {
    console.log("name:", name)
    console.log("pass:", password)
    name = "";
    password ="";
  }


</script>

<main>
  <Navbar/>
  <Container fluid >
    <Card class="m-4 p-4">

      <Row class="text-center">
        <h1>About us</h1>
        <br>
        <h3>Contact</h3>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Molestiae, perspiciatis, ut a aliquid modi numquam vitae nemo hic quia, unde illum ratione dolorum? In, incidunt? Voluptas natus laboriosam modi ad.</p>
        <br>
        <h3>Our founder</h3>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Tenetur praesentium blanditiis sed? Cupiditate earum autem iure? Voluptas corporis facere doloribus delectus, exercitationem, tenetur a sunt molestiae magnam cumque ratione blanditiis quaerat dicta amet repellendus veniam sequi iure voluptatibus placeat omnis cum provident in assumenda dolore? Beatae dolor hic necessitatibus exercitationem.</p>
        <br>
        <h4>Open hours</h4>
        <p>Lorem, ipsum dolor.</p>
        <p>Lorem, ipsum dolor.</p>
        <p>Lorem, ipsum dolor.</p>

        
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
