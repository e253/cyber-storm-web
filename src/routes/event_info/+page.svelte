<script lang="ts">
  // Change Event Items here!!
  let event_info_items = [
    {
      title: "Date and Time",
      content: "Sunday, April 23, 1-5 PM",
      link: false
    },
    {
      title: "Location",
      content: "Rice 130",
      link: false
    },
    {
      title: "Registration Form",
      content: "https://forms.gle/8wpJJvUvVcmi3FM1A",
      link: true
    },
    {
      title: "Team Size",
      content: "Up to 4",
      link: false
    },
    {
      title: "Who Can Participate",
      content: "Full time students at UVA",
      link: false
    },
    {
      title: "Food Provided?",
      content: "Hopefully... but we don't know yet",
      link: false
    },
    {
      title: "Discord Link",
      content: "https://discord.com/invite/dDmVrpqFwh",
      link: true
    },
    {
      title: "Who's Running It?",
      content: "Computer and Network Security club (CNS)",
      link: false
    }
  ]
</script>

<div class="container h-full mx-auto flex justify-center mt-5">
	<div class="space-y-5">
		<h1 class="mt-10 text-center">
      Event Info
    </h1>
    <div class="card variant-ghost-secondary py-2 px-6 rounded-md">
      <ul>
        {#each event_info_items as item}
          <li class="my-3">
            <h3>{item.title}</h3>
            {#if item.link}
              <a href={item.content}>
                <p class="ml-3">
                • {item.content}
              <a href={item.content}>
                </p>
              </a>
            {:else}
              <p class="ml-3">
              • {item.content}
              </p>
            {/if}
          </li>
        {/each}
      </ul>
    </div>
	</div>
</div>
