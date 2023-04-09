<script lang="ts">
  // Change Event Items here!!
  let event_info_items = [
    {
      title: "Organizers Team",
      team_name: "Gold Team",
      color: "text-warning-500",
      content: "Gold team is responsible for the vision and execution of CyberStorm. Gold team also oversees all of the other teams and makes sure they are on schedule.",
      link: false
    },
    {
      title: "Scoring Team",
      team_name: "White Team",
      color: "",
      content: "White team is in charge of designing the event scenario, enacting and enforcing competition rules, outlining scoring guidelines and calculating final scores.",
      link: false
    },
    {
      title: "Logistics Team",
      team_name: "Pink Team",
      color: "text-tertiary-500",
      content: "Pink team coordinates all of the logistics of the event including registration, team matching, food, and other things that have to happen to make the event possible.",
      link: false
    },
    {
      title: "Infrastructure Team",
      team_name: "Black Team",
      color: "text-surface-500",
      content: "Black team is responsible for setting up infrastructure for the competition including programming custom solutions when applicable.",
      link: false
    },
    {
      title: "Inject Team",
      team_name: "Yellow Team",
      color: "text-warning-500",
      content: "In charge of creating and grading injects (business tasks) for the competition.",
      link: false
    },
    {
      title: "Support Team",
      team_name: "Green Team",
      color: "text-success-500",
      content: "Green team is available to help blue teams secure their networks and monitor their progress. Green team comprises highly technical and experienced individuals, several of which are on UVA's nationally accredited Cyber Defense team. They're here to help you! Ask them questions whenever you can!",
      link: false
    },
    {
      title: "Defense Teams", // Also could be competitor teams
      team_name: "Blue Teams",
      color: "text-secondary-500",
      content: "These are you all! Blue teams are competitors competing in the event, charged with defending their networks from the red team.",
      link: false
    },
    {
      title: "Adversary Emulation Team",
      team_name: "Red Team",
      color: "text-error-500",
      content: "The red team is comprised of hackers who are responsible for hacking blue teams networks.",
      link: false
    },
  ]
</script>

<div class="container h-full mx-auto flex justify-center mt-5">
	<div class="space-y-5">
		<h1 class="mt-10 text-center">
      What do all of the colors mean?
    </h1>
    <div class="card variant-ghost-secondary py-2 px-6 rounded-md">
      <ul>
        {#each event_info_items as item}
          <li class="my-3">
            <h3><span class="{item.color}">[{item.team_name}]</span> {item.title}</h3>
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
