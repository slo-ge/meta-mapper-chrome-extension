<script lang="ts">
    let count = 0;
    function sum() {
        chrome.tabs.executeScript({
            code: 'console.log(document.body)'
        });
        count++;
    }
</script>

<p>Counter: {count}</p>
<button on:click={sum}> + </button>

<style>
    body {
        background: red;
    }
</style>
