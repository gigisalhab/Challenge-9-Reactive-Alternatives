<script>
	let posts = [];
  
	async function fetchPosts() {
	  const response = await fetch('https://jsonplaceholder.typicode.com/posts');
	  posts = await response.json();
	}
  
	fetchPosts();
  </script>
  
  <main>
	<h1>Posts</h1>
	{#each posts as post}
	  <div>
		<h2>{post.title}</h2>
		<p>{post.body}</p>
	  </div>
	{/each}
  </main>
  
  <style>
	main {
	  font-family: Arial, sans-serif;
	  padding: 20px;
	  background-color: #f9f9f9;
	  border-radius: 8px;
	  box-shadow: 0 2px 5px rgba(0,0,0,0.1);
	  max-width: 800px;
	  margin: 40px auto;
	}
  
	h1 {
	  color: #333;
	  text-align: center;
	}
  
	div {
	  margin-top: 20px;
	  padding: 15px;
	  background-color: white;
	  border-left: 5px solid #007BFF;
	  border-radius: 5px;
	}
  
	h2 {
	  margin: 0 0 10px 0;
	  color: #007BFF;
	}
  
	p {
	  margin: 0;
	  color: #666;
	  line-height: 1.5;
	}
  </style>
  