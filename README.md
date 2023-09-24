<div align="center">

# IsRendering Detection

[![Generic badge](https://img.shields.io/github/downloads/VRLabs/IsRendering-Detection/total?label=Downloads)](https://github.com/VRLabs/IsRendering-Detection/releases/latest)
[![Generic badge](https://img.shields.io/badge/License-MIT-informational.svg)](https://github.com/VRLabs/IsRendering-Detection/blob/main/LICENSE)
[![Generic badge](https://img.shields.io/badge/Unity-2019.4.31f1-lightblue.svg)](https://unity3d.com/unity/whats-new/2019.4.31)
[![Generic badge](https://img.shields.io/badge/SDK-AvatarSDK3-lightblue.svg)](https://vrchat.com/home/download)

[![Generic badge](https://img.shields.io/discord/706913824607043605?color=%237289da&label=DISCORD&logo=Discord&style=for-the-badge)](https://discord.vrlabs.dev/)
[![Generic badge](https://img.shields.io/endpoint.svg?url=https%3A%2F%2Fshieldsio-patreon.vercel.app%2Fapi%3Fusername%3Dvrlabs%26type%3Dpatrons&style=for-the-badge)](https://patreon.vrlabs.dev/)

Sets an "IsRendering" parameter to true when being looked at

![Alt text](https://raw.githubusercontent.com/VRLabs/IsRendering-Detection/main/Media/trollcull.gif)

### ⬇️ [Download latest Unitypackage](https://github.com/VRLabs/IsRendering-Detection/releases/latest)

<!-- 
### 📦 [Add to VRChat Creator Companion]() -->

</div>

---

## How it works

* The prefab contains a sub-animator, a sender, a receiver, and a renderer.  
* The sub-animator constantly animates the sender on, which is setting ``IsRendering`` to true.  
* When the renderer is not in view, the sub-animator stops running and will no longer animate the sender on.  
* The main-animator can then animate the sender off, which sets ``IsRendering`` to false.

## Install guide

* Merge the Animator Cdontroller ``IsRendering FX`` to your own FX Controller, using the [Avatars 3.0 Manager](https://github.com/VRLabs/Avatars-3.0-Manager) tool.
* Drag & Drop the ``IsRendering Detection`` prefab onto the avatar.
* Expand the prefab hierarchy and find ``Culling Animator`` -> ``Renderer``.
* Modify the bounds of the renderer to fit the view target such as your avatar.

## How to use

The ``IsRendering`` parameter is a bool. The value will be true when ``Renderer`` is in view, and false when outside of view.  
Under the prefab's hierarchy, the ``IsRendering Container`` is enabled when in view. ``IsNotRendering Container`` is enabled when not in view.

The containers have a cube and sphere for previewing and confirming that it works. Feel free to delete them.  
The FX layer ``Is Rendering`` is for the preview. It uses a 10 frames delay for [coyote time](https://en.wiktionary.org/wiki/coyote_time). Feel free to delete it.

## Performance stats

```c++
Contact Receivers:  1
Contact Senders:    1
FX Animator Layers: 1
Skinned Renderers:  1
Sub Animators:      1
```

## Hierarchy layout

```html
IsRendering Detection
|-IsRendering Container
|  |-Cube
|-NotRendering Container
|  |-Sphere
|-Culling Animator
|  |-Sender
|  |-Receiver
|  |-Renderer
```

## Contributors

* [hfcRed](https://github.com/hfcRed)  
* [Dreadrith](https://github.com/Dreadrith)

## License

IsRendering Detection is available as-is under MIT. For more information see [LICENSE](https://github.com/VRLabs/IsRendering-Detection/blob/main/LICENSE).

​

<div align="center">

[<img src="https://github.com/VRLabs/Resources/raw/main/Icons/VRLabs.png" width="50" height="50">](https://vrlabs.dev "VRLabs")
<img src="https://github.com/VRLabs/Resources/raw/main/Icons/Empty.png" width="10">
[<img src="https://github.com/VRLabs/Resources/raw/main/Icons/Discord.png" width="50" height="50">](https://discord.vrlabs.dev/ "VRLabs")
<img src="https://github.com/VRLabs/Resources/raw/main/Icons/Empty.png" width="10">
[<img src="https://github.com/VRLabs/Resources/raw/main/Icons/Patreon.png" width="50" height="50">](https://patreon.vrlabs.dev/ "VRLabs")
<img src="https://github.com/VRLabs/Resources/raw/main/Icons/Empty.png" width="10">
[<img src="https://github.com/VRLabs/Resources/raw/main/Icons/Twitter.png" width="50" height="50">](https://twitter.com/vrlabsdev "VRLabs")

</div>

---
