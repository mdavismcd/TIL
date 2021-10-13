# Today I Learned . . .

How to insert collapsable text, including `code`, in Markdown. While I promise myself not to go all out with this, I plan to use in longer files.

## How to structure

### A collapsible section with markdown
<details>
  <summary>Click to expand!</summary>
  
  ## Heading
  1. A numbered
  2. list
     * With some
     * Sub bullets
</details>

### A collapsible section containing code
<details>
  <summary>Click to expand!</summary>
  
  ```javascript
    function logSometing(something) {
      console.log(`Logging: ${something}`);
    }
  ```
</details>

___

[source: @pierrejoubert73](https://gist.github.com/pierrejoubert73/902cc94d79424356a8d20be2b382e1ab)