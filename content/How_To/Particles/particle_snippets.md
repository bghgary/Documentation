## Snippet server
Starting with Babylon.js v4.2, you can save, load and edit sprite managers using the Inspector. These code snippets are saved on the Babylon.js snippet server. Make a note of the snippet Id shown in when you save it.

![Snippet](/img/how_to/Particles/snippet_screen.png)

When you have a snippet Id, you can easily load the manager using the following code:

```javascript
var sphere = BABYLON.MeshBuilder.CreateSphere("sphere", {diameter: 0.2, segments: 32}, scene);
BABYLON.ParticleHelper.CreateFromSnippetAsync("T54JV7", scene, false).then(system => {
    system.emitter = sphere;
});
```

live example https://www.babylonjs-playground.com/#76U9TK

You can also specify "_BLANK" for the snippet Id, in this case the system will create an empty one for you to work on:

```
BABYLON.SpriteManager.CreateFromSnippetAsync("_BLANK", scene);
```