<script>
   import FeedbackList from "./components/FeedbackList.svelte";


   let feedBack = [
    {
      id: 1,
      rating: 10,
      text: " Heres some random placeholder boilerplate text for my sample svelte.js feedback app"
    },
    {
      id: 2,
      rating: 9,
      text: " Heres some more random placeholder boilerplate text for my sample svelte.js feedback app"
    },
    {
      id: 3,
      rating: 8,
      text: " And lastly, suprise suprise! Heres some random placeholder boilerplate text for my sample svelte.js feedback app"
    },
   ]
</script>

<main class = "container">
  
  <FeedbackList  {feedBack}/>

  
</main>

