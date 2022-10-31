<script>
  import Button from "./Button.svelte";

  import Card from "./Card.svelte";

</script>


<Card>
  <header>
    <h2>How do you rate our services?</h2>
  </header>
<form>
    <!--Rating Select-->
    <div class="input-group">
        <input type="text" placeholder="tell us something that keeps you coming back"/>
        <button>Send</button>
    </div>
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