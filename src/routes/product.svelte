<script>
    import { onMount } from "svelte";
    import { gsap } from "gsap";
    
    let logo = document.querySelector(".logo");
    
    onMount(() => {
      gsap.fromTo(logo, {
        x: -100,
        duration: 2,
        easing: "bounce",
      }, {
        x: 0,
        duration: 1,
      });
    });
</script>
    
    <div class="container">
      <div class="logo">
        <img src="logo.png" alt="Logo" />
      </div>
    </div>
    