<script>
    import { onNavigate } from '$app/navigation'

onNavigate ((navigation) => {
if (!document.startViewTransition) return

return new Promise(resolve => {
  document.startViewTransition(async () => {
      
      resolve()
      await navigation.complete()
  });
});
});
</script>
<link rel="stylesheet" href="/global.css">

<slot></slot>

<style>
    
    @keyframes fade-out {
        to {
            opacity: 0;
        }
    }

    @keyframes slide-from-right {
        from {
            transform: translateX(100%);
        }
    }

    :root::view-transition-old(root){
        animation: 500ms ease-out both fade-out;

    }

    :root::view-transition-new(root){
        animation: 500ms ease-out both slide-from-right;

    }
</style>