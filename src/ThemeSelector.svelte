<script>
    import { createEventDispatcher } from 'svelte';
    const dispatch = createEventDispatcher();
  
    let themes = [
      { value: 'light', label: 'Thème clair' },
      { value: 'dark', label: 'Thème sombre' }
    ];
  
    let selectedTheme = themes[0];
  
    function selectTheme(theme) {
      selectedTheme = theme;
      dispatch('themeChange', theme.value);
    }
  </script>
  
  <div class="dropdown">
    {#each themes as theme}
      <!-- svelte-ignore a11y-click-events-have-key-events -->
      <!-- svelte-ignore a11y-no-static-element-interactions -->
      <div 
        class="option {theme.value === selectedTheme.value ? 'selected' : ''}" 
        on:click={() => selectTheme(theme)}>
        {theme.label}
      </div>
    {/each}
  </div>
  
  <style>
    .dropdown {
      border: 1px solid #ccc;
      width: 150px;
    }
  
    .option {
      padding: 8px;
      cursor: pointer;
    }
  
    .option:hover {
      background-color: #f5f5f5;
    }
  </style>
  
