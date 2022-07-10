<style>
    html,body{
    height:100%;
    margin:0;
    padding:0
    }
    body{
    display:flex;
    flex-direction:column;
    justify-content:center;
    align-items:center;
    }
    iframe{
    display:none;
    border:none;
    height:100%;
    width:100%;
</style>
<input type="url" placeholder="enter URL here" />
<iframe></iframe>
<script>
    const input = document.querySelector("input");
    const iframe = document.querySelector("iframe");
    input.addEventListener("keydown", (e) => {
        if (e.key === "Enter") {
            iframe.style.display = "flex";
            iframe.src = input.value;
            input.style.display = "none";
            document.documentElement.requestFullscreen();
        }
    });
</script>
