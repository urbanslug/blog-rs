+++
title = "My first post"
date = 2019-11-27
[taxonomies]
tags = ["rust", "web"]
categories = ["programming"]
+++

This is my first blog post.

```js
function useLocalStorage(key, defaultValue='') {
  const [state, setState] = React.useState(
    () => window.localStorage.getItem(key) || defaultValue
  );

  React.useEffect(() => {
    window.localStorage.setItem(key, state);
  }, [state]);

  return [state, setState]
}

function MyComponent() {
  const [name, setName] = useLocalStorage('name', '');
  const handleChange = event => setName(event.target.value);
  
  return (
    <div>
      <form>
        <!-- htmlFor is like for in html for but JSX-->
        <label htmlFor="name""></label>
        <input id="name" onChange={handleChange}></input>
      </form>
      {name ? <strong>Helllo {name}</strong> : <span>Please type in name</span>}
    </div>
  )
}
```

Hello
