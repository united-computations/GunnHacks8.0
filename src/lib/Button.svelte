<button>
    <slot />
</button>

<style lang="scss">
  button {
    //$color: #EF4444;

    padding: 0.75rem 1rem;
    font-size: 0.9rem;
    border: 1px solid white;
    border-radius: 0.2rem;
    //box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
    cursor: pointer;
    text-decoration: none;
    background: none;
    //background-color: $color;
    transition: background-color 100ms ease-in-out;

    &:hover {
      //background-color: scale-color($color, $blackness: 8%);
      background-color: rgba(255, 255, 255, 0.2);
      box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
    }
  }
</style>
