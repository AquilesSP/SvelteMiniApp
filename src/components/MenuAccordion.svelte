<script>
  export let menu = [];

  // Usa un solo índice para controlar la sección abierta (una sola a la vez)
  let openIndex = null;

  function toggleSection(index) {
    openIndex = openIndex === index ? null : index;
  }
</script>

<style>
  .section {
    /* margin:0; */
    border-top: 1px solid #ddd;
  }

  .header {
    display: flex;
    justify-content: space-between;
    padding: 1rem;
    font-weight: bold;
    cursor: pointer;
    background: #eee;
  }

  .recipes {
    padding: 1rem;
    background: #fafafa;
  }

  .recipe {
    margin-bottom: 1rem;
  }

  .recipe img {
    width: 64px;
    height: 64px;
    object-fit: cover;
    border: 1px solid #ccc;
    /* margin-right: 1rem; */
    border-radius: 8px;
  }

  .price {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: #fff;
    /* border: 1px solid #ddd; */
    padding: 0.5rem;
    margin-top: 0.25rem;
    border-radius: 8px;
  }

  .price button {
    background: #EEA014;
    border: none;
    padding: 0.5rem 1rem;
    cursor: pointer;
    border-radius: 16px;
    font-weight: bold;
  }
</style>

{#each menu as section, index}
  <div class="section">
    <div class="header" on:click={() => toggleSection(index)}>
      <div></div>
      <div>{section.title}</div>
      <div>
        {#if openIndex === index}
          <i class="fa-solid fa-chevron-up"></i>
        {:else}
          <i class="fa-solid fa-chevron-down"></i>
        {/if}
      </div>
      
    </div>

    {#if openIndex === index}
      <div class="recipes">
        {#each section.recipes as recipe}
          <div class="recipe">
            <div style="display: flex; align-items: center;">
              <div>
                <div><strong>{recipe.recipe_title}</strong></div>
                <div>{recipe.ingredientes}</div>
              </div>
            </div>

            {#each recipe.precio as p}
              <div class="price">
                <div>
                  <div>{p.price_title} - ${p.price}</div>
                  <button>Pedir</button>
  
                </div>
                <img src={recipe.image} alt={recipe.recipe_title} />
              </div>
            {/each}
          </div>
        {/each}
      </div>
    {/if}
  </div>
{/each}
