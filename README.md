
# Silver Bullet plug for Mermaid diagrams
This plug adds basic [Mermaid](https://mermaid.js.org/) support to Silver Bullet.

**Note:** The Mermaid library itself is not bundled with this plug, it pulls the JavaScript from the JSDelivr CDN. This means _this plug will not work without an Internet connection_. The reason for this is primarily plug size (bundling the library would amount to 1.1MB). This way Mermaid is only loaded on pages with actual Mermaid diagrams rather than on every SB load.

## Installation
Run the {[Plugs: Add]} command and paste in: `github:silverbulletmd/silverbullet-mermaid/mermaid.plug.json`

That's all!

## Use

Put a mermaid block in your markdown:

    ```mermaid
    flowchart TD
        Start --> Stop
    ```

And move your cursor outside of the block to live preview it!

## Build
Assuming you have Deno and Silver Bullet installed, simply build using:

```shell
deno task build
```

Or to watch for changes and rebuild automatically

```shell
deno task watch
```

Then, load the locally built plug, add it to your `PLUGS` note with an absolute path, for instance:

```
- file:/Users/you/path/to/mermaid.plug.json
```

And run the `Plugs: Update` command in SilverBullet.