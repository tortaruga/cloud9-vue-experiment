<template>
    <div class="marquee">
        <p>Due to unforeseeable adverse weather conditions we cannot guarantee you will land at your destination (or anywhere at all). By booking a flight you agree to take upon yourself all responsibility for what may or may not happen to you. Cloud9 will not refund you for missing limbs, scorched flesh, torn nails, broken ribs, suffocation and/or drowning. All our experiences are children-friendly! For legal information consult our contract.</p>
        <p>Due to unforeseeable adverse weather conditions we cannot guarantee you will land at your destination (or anywhere at all). By booking a flight you agree to take upon yourself all responsibility for what may or may not happen to you. Cloud9 will not refund you for missing limbs, scorched flesh, torn nails, broken ribs, suffocation and/or drowning. All our experiences are children-friendly! For legal information consult our contract.</p> 
    </div>
</template>

<script></script>

<style>

.marquee {
  width: 100%; 
  overflow: hidden;
  display: flex;
  flex-wrap: nowrap;
  margin-block: 5rem;
}

.marquee p {
  white-space: nowrap; 
  overflow: hidden;
  width: max-content;
  padding: .25rem;
  animation: marquee 20s infinite linear both;
  flex-shrink: 0;
  margin-right: 1rem;
  font-size: .8rem;
}

@keyframes marquee {
    to {
        transform: translateX(-100%);
    }
}

</style>