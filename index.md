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
