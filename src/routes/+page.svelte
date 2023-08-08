<!-- <h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p> 
INTRODUCTORY START PAGE   -->

<script>
    let campaigns = [
      { 
        title: "BusBOX",
        description: "Aiming to reduce the hassle by half for intercity bus tracking. Always be on-time and never waste a minute standing and waiting in lines at bus stop.",
        currentAmount: 1000,
        goalAmount: 5000000,
        backers: 50
      },
      { 
        title: "Gear Fidget Bottle",
        description: "A sturdy and tactile bottle fidget which is sure to compliment your workout style.",
        currentAmount: 2500,
        goalAmount: 10000,
        backers: 100
      },
      { 
        title: "Dierect",
        description: "India's first dating app, that encourages you to decide on what you want, simplifying society with simple choices.",
        currentAmount: 1000,
        goalAmount: 2500000,
        backers: 75
      },
      // Add more campaign objects as needed
    ];
  </script>
  
  <style>
    .campaign {
      margin-bottom: 20px;
      padding: 20px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
    
    .title {
      font-size: 24px;
      font-weight: bold;
      margin-bottom: 10px;
    }
    
    .description {
      margin-bottom: 10px;
    }
    
    .amounts {
      display: flex;
      justify-content: space-between;
      margin-bottom: 10px;
    }
    
    .backers {
      font-style: italic;
    }
  </style>
  
  <div>
    {#each campaigns as campaign}
      <div class="campaign">
        <div class="title">{campaign.title}</div>
        <div class="description">{campaign.description}</div>
        <div class="amounts">
          <div>Current Amount: ${campaign.currentAmount}</div>
          <div>Goal Amount: ${campaign.goalAmount}</div>
        </div>
        <div class="backers">Backers: {campaign.backers}</div>
      </div>
    {/each}
  </div>