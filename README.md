# IsRendering Detection
  
[![Generic badge](https://img.shields.io/badge/Unity-2019.4.31f1-informational.svg)](https://unity3d.com/unity/whats-new/2019.4.31)
[![Generic badge](https://img.shields.io/badge/SDK-AvatarSDK3-informational.svg)](https://vrchat.com/home/download)
[![Generic badge](https://img.shields.io/badge/License-MIT-informational.svg)](https://github.com/VRLabs/Local-Mirror-Detection/blob/main/LICENSE)
[![Generic badge](https://img.shields.io/github/downloads/VRLabs/IsRendering-Detection/total?label=Downloads)](https://github.com/VRLabs/IsRendering-Detection/releases/latest)

Sets an "IsRendering" parameter to animate when being looked at.

![Alt text](https://raw.githubusercontent.com/VRLabs/IsRendering-Detection/main/Media/trollcull.gif)

## How it works

The prefab contains a sub-animator, a sender, a receiver, and a renderer.  
The sub-animator constantly animates the sender on, which with the receiver is setting 'IsRendering' to true.  
When the renderer is not in view, culling takes effect and the sub-animator stops enabling the sender.  
The main-animator then animates the sender off, which sets 'IsRendering' to false.  

## Install guide

Merge the FX controller 'IsRendering FX' to your own FX controller, using the [Avatars 3.0 Manager](https://github.com/VRLabs/Avatars-3.0-Manager) tool.  
Drag & Drop the 'IsRendering Detection' prefab onto the avatar.  
Expand the prefab hierarchy and find 'Culling Animator' -> 'Renderer'.  
Modify the bounds of the renderer to fit the view target such as your avatar.  
Done!

## How to use

The "IsRendering" parameter is a bool. The value will be true when the 'Renderer' is in view, and false outside of it.  
Under the prefab's hierarchy, the 'IsRendering Container' is enabled when in view. 'IsNotRendering Container' is enabled when not in view.  
The containers have a cube and sphere for previewing and confirming that it works. Feel free to delete them.  
The FX layer 'Is Rendering' is for the preview. It uses a 10 frames delay for [coyote time](https://en.wiktionary.org/wiki/coyote_time). Feel free to delete it.

## Credit

[hfcRed](https://github.com/hfcRed)  
[Dreadrith](https://github.com/Dreadrith)

## Downloads

You can grab the latest version of IsRendering Detection in [Releases](https://github.com/VRLabs/IsRendering-Detection/releases/latest).

## License

IsRendering Detection is available as-is under MIT. For more information see [LICENSE](https://github.com/VRLabs/IsRendering-Detection/blob/main/LICENSE).

## Contact us

If you need help, our support channel is on [Discord](https://discord.vrlabs.dev).
