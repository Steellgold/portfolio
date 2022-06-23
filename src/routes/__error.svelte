<script context="module" lang="ts">
    
    import type { LoadEvent } from "@sveltejs/kit";
    
    export function load({ error, status }: LoadEvent) {
      return {
        props: {
          errorCode: status,
          message: error?.message,
        }
      };
    }

</script>
  
<script lang="ts">
    export let errorCode: number|null;
    export let message: string|null;
</script>

<title>{errorCode}</title>
<h1>{message}</h1>