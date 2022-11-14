<script>
  import Button from "./Button.svelte";
  import Card from "./Card.svelte";
  import RatingSelect from "./RatingSelect.svelte";

  let text = ""
  let rating = 10
  let btnDisabled = true
  let min = 12
  let ourMessage

  const handleInput = () =>{
    if(text.trim().length <= min){
      ourMessage = `text must be atleast ${min} characters`
      btnDisabled = true
    }else{
      ourMessage = null
      btnDisabled = false
    }
  }

</script>


<Card>
  <header>
    <h2>How do you rate our services?</h2>
  </header>
<form>
    <RatingSelect/>
    <div class="input-group">
        <input type="text" on:input={handleInput} bind:value = {text} placeholder="tell us something that keeps you coming back"/>

        <Button disabled ={btnDisabled} type="submit"> Send</Button>
    </div>
   {#if ourMessage}
   <div class="message">
    {ourMessage}
   </div>
   {/if}
</form>
</Card>
<style>
  header {
    max-width: 400px;
    margin: auto;
  }

  header h2 {
    font-size: 22px;
    font-weight: 600;
    text-align: center;
  }

  .input-group {
    display: flex;
    flex-direction: row;
    border: 1px solid #ccc;
    padding: 8px 10px;
    border-radius: 8px;
    margin-top: 15px;
  }

  input {
    flex-grow: 2;
    border: none;
    font-size: 16px;
  }

  input:focus {
    outline: none;
  }

  .message{
    padding-top: 10px;
    text-align: center;
    color: rebeccapurple;
  }
</style>