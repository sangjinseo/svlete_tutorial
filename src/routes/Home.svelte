<script>
    import Nested from "../components/Nested.svelte";

    let name = "서상진 서벌트 테스트";
    let htmlName = "<span style='color:green';>서상진 todo!! </span>";
    let src =
        "data:image/png;base64,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";
    let count = 0;
    function increaseCount() {
        count++;
    }

    $: if (count > 5) {
        alert("count: 5보다 클수없습니다");
        count = 5;
    }
    // watch vlaue
    $: sum = count * 2;
</script>

<style>
</style>

<button type="button" on:click={increaseCount}>Count</button>
<div>Count : {count}</div>
<div>Sum : {sum}</div>

<Nested name2={name} />

<h1>Hello {name}</h1>
<h1>
    Hello
    {@html htmlName}
</h1>
<img {src} />

<!-- npm run dev -->
