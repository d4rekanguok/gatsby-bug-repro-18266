# gatsby-remark-responsive-iframe bug repro

`gatsby-remark-responsive-iframe` creates `<undefined>` block around iframe

## Steps to reproduce

- Setup

```bash
git clone https://github.com/d4rekanguok/gatsby-bug-repro-18266.git
cd gatsby-bug-repro-18266
yarn && yarn develop
```

- Navigate to `localhost:8000/hello-world`
- Inspect the map
- See this markup:

```html
<undefined>
  <div class="gatsby-resp-iframe-wrapper" style="padding-bottom: 66.6667%; position: relative; height: 0px; overflow: hidden; margin-bottom: 1.0725rem;">
    <iframe id="inlineFrameExample" title="Inline Frame Example" src="https://www.openstreetmap.org/export/embed.html?bbox=-0.004017949104309083%2C51.47612752641776%2C0.00030577182769775396%2C51.478569861898606&amp;layer=mapnik" style="position: absolute; top: 0px; left: 0px; width: 100%; height: 100%;"></iframe>
  </div>
</undefined>
```