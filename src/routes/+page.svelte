<script>
	import { Container, Row, Col } from 'sveltestrap';
	import { Button, Card, Modal } from 'sveltestrap';
	import { Badge, Form, FormGroup, Input, Label } from 'sveltestrap';
	import Navbar from '../components/+navbar.svelte';
	let email = '';

	let open = false;
	const toggle = () => {
    (open = !open);
    
  }
	
</script>

<main>
	<Navbar />
	<Container fluid>
		<Row>
			<Col class="p-5">
				<Card class="card p-5">
					<Row class="text-center">
						<h1>Welcome to best news ever</h1>
					</Row>
					<Row class="text-center">
            <p>Please watch all news articles under posts</p>
            <p>You can find them in the navbar</p>
          </Row>
          
					<Row class=" mt-5">
            <Col>
              <h2>Subscribe to our newsletter</h2>
							<Form>
                <br>
								<FormGroup floating label="Email">
									<Input bind:value={email} placeholder="Enter a value" />
								</FormGroup>
                <br>
								<Button disabled={email ? false : true}  on:click={toggle}>Subscribe</Button>
								<Modal body header="Subscribed" isOpen={open} on:close={() => email = ''} {toggle}>
									Successfully subscribed with email: <b>{email}</b>
								</Modal>
							</Form>
						</Col>
						<Col>
							<a href="https://unsplash.com/photos/_Zua2hyvTBk">
								<img style="max-width: 100%" src="/images/news.jpg" alt="" />
							</a>
						</Col>
					</Row>
				</Card>
			</Col>
		</Row>
	</Container>
</main>

<style>
	main {
		min-height: 100vh;
		background: lightgray;
	}

  :global(.carder){
    background: gray;
  }
</style>
