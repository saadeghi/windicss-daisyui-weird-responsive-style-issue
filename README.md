## Windi CSS issue on generating responsive style from plugins  
<details>
<summary>
Source: 
</summary>

```json
{
  "@media (min-width:1024px)": [
  {
    ".drawer-mobile": {
      "gridAutoColumns": [
        "-webkit-max-content auto",
        "max-content auto"
      ]
    },
    ".drawer-mobile>.drawer-toggle~.drawer-content": {
      "height": "auto"
    },
    "@media (min-width:1024px)": [
      {
        ".drawer-mobile>.drawer-toggle~.drawer-content": {
          "gridColumnStart": "2"
        }
      },
      {
        ".drawer-mobile>.drawer-toggle~.drawer-side>.drawer-overlay": {
          "visibility": "visible"
        }
      },
      {
        ".drawer-mobile>.drawer-toggle~.drawer-side>.drawer-overlay+*": {
          "-TwTranslateX": "0px"
        }
      },
      {
        ".drawer-mobile.drawer-end>.drawer-toggle~.drawer-content": {
          "gridColumnStart": "1"
        }
      },
      {
        ".drawer-mobile.drawer-end>.drawer-toggle~.drawer-side": {
          "gridColumnStart": "2"
        }
      },
      {
        ".drawer-mobile.drawer-end>.drawer-toggle~.drawer-side>.drawer-overlay": {
          "visibility": "visible"
        }
      },
      {
        ".drawer-mobile.drawer-end>.drawer-toggle~.drawer-side>.drawer-overlay+*": {
          "-TwTranslateX": "0px"
        }
      }
    ],
    ".drawer-mobile>.drawer-toggle~.drawer-side": {
      "overflowY": "auto"
    },
    ".drawer-mobile.drawer-end": {
      "gridAutoColumns": [
        "auto -webkit-max-content",
        "auto max-content"
      ]
    },
    ".drawer-mobile.drawer-end>.drawer-toggle~.drawer-content": {
      "height": "auto"
    },
    ".drawer-mobile.drawer-end>.drawer-toggle~.drawer-side": {
      "overflowY": "auto"
    }
  },
  {
    ".drawer-mobile>.drawer-toggle:checked~.drawer-content": {
      "-TwTranslateX": "0px"
    }
  }
]
}
```

</details>

<details>
<summary>
Expected CSS: 
</summary>

```css
@media (min-width: 1024px) {
  .drawer-mobile {
    grid-auto-columns: -webkit-max-content auto;
    grid-auto-columns: max-content auto;
  }
  .drawer-mobile > .drawer-toggle ~ .drawer-content {
    height: auto;
  }
  @media (min-width: 1024px) {
    .drawer-mobile > .drawer-toggle ~ .drawer-content {
      grid-column-start: 2;
    }
  }
  .drawer-mobile > .drawer-toggle ~ .drawer-side {
    overflow-y: auto;
  }
  @media (min-width: 1024px) {
    .drawer-mobile > .drawer-toggle ~ .drawer-side > .drawer-overlay {
      visibility: visible;
    }
  }
  @media (min-width: 1024px) {
    .drawer-mobile > .drawer-toggle ~ .drawer-side > .drawer-overlay + * {
      --tw-translate-x: 0px;
    }
  }
  .drawer-mobile.drawer-end {
    grid-auto-columns: auto -webkit-max-content;
    grid-auto-columns: auto max-content;
  }
  .drawer-mobile.drawer-end > .drawer-toggle ~ .drawer-content {
    height: auto;
  }
  @media (min-width: 1024px) {
    .drawer-mobile.drawer-end > .drawer-toggle ~ .drawer-content {
      grid-column-start: 1;
    }
  }
  .drawer-mobile.drawer-end > .drawer-toggle ~ .drawer-side {
    overflow-y: auto;
  }
  @media (min-width: 1024px) {
    .drawer-mobile.drawer-end > .drawer-toggle ~ .drawer-side {
      grid-column-start: 2;
    }
  }
  @media (min-width: 1024px) {
    .drawer-mobile.drawer-end > .drawer-toggle ~ .drawer-side > .drawer-overlay {
      visibility: visible;
    }
  }
  @media (min-width: 1024px) {
    .drawer-mobile.drawer-end > .drawer-toggle ~ .drawer-side > .drawer-overlay + * {
      --tw-translate-x: 0px;
    }
  }
}

```

</details>

<details>
<summary>
Windi CSS output: 
</summary>

```css
@media (min-width:1024px) {
  0 {
    @media (min-width:1024px): [object Object];
  }
  0 .drawer-mobile {
    grid-auto-columns: -webkit-max-content auto;
    grid-auto-columns: max-content auto;
  }
  0 .drawer-mobile>.drawer-toggle~.drawer-content {
    height: auto;
  }
  0 .drawer-mobile>.drawer-toggle~.drawer-side {
    overflow-y: auto;
  }
  0 .drawer-mobile.drawer-end {
    grid-auto-columns: auto -webkit-max-content;
    grid-auto-columns: auto max-content;
  }
  0 .drawer-mobile.drawer-end>.drawer-toggle~.drawer-content {
    height: auto;
  }
  0 .drawer-mobile.drawer-end>.drawer-toggle~.drawer-side {
    overflow-y: auto;
  }
  1 .drawer-mobile>.drawer-toggle:checked~.drawer-content {
    --tw-translate-x: 0px;
  }
}
```

</details>
