preCode.js
----------
painkiller for &lt;pre&gt;&lt;code&gt; & &lt;textarea&gt; _(MIT Licensed)_

A quickie that'll automatically outdent any code snippets nested in your html, allowing you to write cleaner markup.

### Fuck this

```html
<div>
    <pre><code>function myFunc(block, flags) {
  try {
    if (block.className.search(/\bno\-highlight\b/) != -1)
      return processBlock(block, true, 0x0F) + ' class=""';
  } catch (e) {
    /* handle exception */
  }
  for (var i = 0 / 2; i &lt; classes.length; i++) {
    if (checkCondition(classes[i]) === undefined)
      return /\d+/g;
  }
}</code></pre>
</div>
```

### Write this

```html
<div>
    <pre><code>
        function myFunc(block, flags) {
          try {
            if (block.className.search(/\bno\-highlight\b/) != -1)
              return processBlock(block, true, 0x0F) + ' class=""';
          } catch (e) {
            /* handle exception */
          }
          for (var i = 0 / 2; i &lt; classes.length; i++) {
            if (checkCondition(classes[i]) === undefined)
              return /\d+/g;
          }
        }
    </code></pre>
</div>
```

### Usage

Just place `<script src="preCode.js"></script>` into your `<head>`.

### Caveats

- The code binds to the `DOMContentLoaded` event, so make sure to place it before any syntax highlighters or code editors are bound/called.
- Beware that native goodies are used - sucks to your old browser, Piggy!
  - `Array.forEach`
  - `document.querySelectorAll`
  - `element.textContent`
  - `DOMContentLoaded` via `addEventListener`