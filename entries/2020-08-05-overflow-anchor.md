# Scroll anchoring and overflow-anchor property

[Scroll anchoring](https://www.w3.org/TR/css-scroll-anchoring/)
allows users visually stay on the same area on content changes.
It solves the content jumping around when some part of the page loads.

Modern browsers try to solve this content jumping by themselves, but
it can be slightly tweaked and controlled via `overflow-anchor` property.

`overflow-anchor` property can be either `auto` or `none`.
First tells the browser to handle anchoring automatically and the last to disable this element for anchoring.

Neat trick that can be done with `overflow-anchor` – auto chat scrolling on new messages.

We set `.messages` to be non-anchorable via `overflow-anchor: none;` and the last block to be
the anchor on the page so content changes will keep this part of the chat static.

```html
<div class="chat">
  <div class="mesasge"></div>
  <div class="mesasge"></div>
  ...
  <div class="mesasge"></div>

  <div class="anchor"></div>
</div>
```

```css
.message {
  overflow-anchor: none;
}

.anchor {
  overflow-anchor: auto;
  /* anchor nodes require non-zero area */
  height: 1px;
}
```

_2020-08-05 Wednesday_
