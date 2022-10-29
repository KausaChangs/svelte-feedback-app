<script>
   import FeedbackList from "./components/FeedbackList.svelte";
   import FeedbackStats from "./components/FeedbackStats.svelte";
  


   let feedBack = [
    {
      id: 1,
      rating: 10,
      text: " Heres some random placeholder boilerplate text for my sample svelte.js feedback app"
    },
    {
      id: 2,
      rating: 7.5,
      text: " Heres some more random placeholder boilerplate text for my sample svelte.js feedback app"
    },
    {
      id: 3,
      rating: 8,
      text: " And lastly, suprise suprise! Heres some random placeholder boilerplate text for my sample svelte.js feedback app"
    },
   ]

   $: count = feedBack.length

   $: average = feedBack.reduce((a, {rating}) => a + rating, 0)/ feedBack.length

   const deleteFeedback = (e) =>{
       const itemId = e.detail

       feedBack = feedBack.filter((item)=> item.id != itemId)
   }
</script>

<main class = "container">

  <FeedbackStats {count} {average} />
  
  <FeedbackList  {feedBack}  on:delete-feedback = {deleteFeedback}/>

  
</main>

