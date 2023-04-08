# Svelte Interactive Tutorial

* ## Welcome to Svelte

  + ### Referencing A Variable In Markup
    - You can reference JS variables and write JS code inside of markup by using `{}`

        ```
        <script>
            let name = 'Mateo';
        </script>
        
        <h1> Hello, my name is {name} </h1>
        
        ------------------------------------------------
        Output:
        
        Hello, my name is Mateo
        
        ```
        ```
        <script>
            let name = 'Mateo';
        </script>
        
        <h1> Hello, my name is {name.toUpperCase()}! </h1>
        
        ------------------------------------------------
        Output:
        
        Hello, my name is MATEO!
        
        ```
  + ### Dynamic Attributes
    - The following


 