---
layout: kit
iid: spritekit
name: 'SpriteKit'
status:
type: kit
icon: /resources/images/kits/SpriteKit/spritekit-icon_2x.png
since: iOS7
detailedUpdates:
 - update:
     ios: iOS8
     brief: "The SpriteKit framework (SpriteKit.framework) adds many new features: see the content of the page."
prefixe: 'SK'
abstract: "provides a hardware-accelerated animation system optimized for creating 2D and 2.5D games."
kits:
 - SceneKit
 - GameController
links:
 - link:
     name: 'SpriteKit Programming Guide'
     url: https://developer.apple.com/library/ios/documentation/GraphicsAnimation/Conceptual/SpriteKit_PG/Introduction/Introduction.html
     description: ' - Apple Developer'
 - link:
     name: 'SpriteKit Framework Reference'
     url: https://developer.apple.com/library/ios/sprite_kit_framework_ref
     description: ' - Apple Developer'
---

The *SpriteKit* framework (`SpriteKit.framework`) provides a hardware-accelerated animation system for 2D and 2.5D games. SpriteKit provides the infrastructure that most games need, including:

* a graphics rendering and animation system, 
* sound playback support, 
* and a physics simulation engine. 

Using SpriteKit frees you from creating these things yourself and lets you focus on the design of your content and the high-level interactions for that content.



### iOS8

The *SpriteKit* framework adds new features to make it easier to create high-performance, battery-efficient 2D games. With support for custom OpenGL ES shaders and lighting, integration with SceneKit, and advanced new physics effects and animations, you can add force fields, detect collisions, and generate new lighting effects in your games. Xcode 6 also incorporates new shader and scene editors that save you time as you create your game. Create a scene’s contents, specifying which nodes appear in the scene and characteristics of those nodes, including physics effects. The scene is then serialized to a file that your game can easily load.

* An `SKShapeNode` object can specify textures to be used when the shape is either stroked or filled.
* The `SKSpriteNode`, `SKShapeNode`, `SKEmitterNode`, and `SKEffectNode` classes include support for custom rendering. Use the `SKShader` and `SKUniform` classes to compile an OpenGL ES 2.0-based fragment shader and provide input data to the shader.
* `SKSpriteNode` objects can provide lighting information so that SpriteKit automatically generates lighting effects and shadows. Add `SKLightNode` objects to the scene to specify the lights, and then customize the properties on these lights and any sprites to determine how the scene is lit.
* The `SKFieldNode` class provides physics special effects you can apply to a scene. For example, create magnetic fields, add drag effects, or even generate randomized motion. All effects are constrained to a specific region of the scene, and you can carefully tune both the effect’s strength and how quickly the effect is weakened by distance. Field nodes make it easy to drop in an effect without having to search the entire list of physics bodies and apply forces to them.
* A new `SK3DNode` class is used to integrate a SceneKit scene into your game as a sprite. Each time that SpriteKit renders your scene, it renders the 3D scene node first to generate a texture, then uses that texture to render a sprite in SpriteKit. Creating 3D sprites can help you avoid creating dozens of frames of animation to produce an effect.
* New actions have been added, including support for inverse kinematic animations.
* A new system of constraints has been added to scene processing. SpriteKit applies constraints after physics is simulated, and you use them to specify a set of rules for how a node is positioned and oriented. For example, you can use a constraint to specify that a particular node in the scene always points at another node in the scene. Constraints make it easier to implement rendering rules in your game without having to tweak the scene manually in your event loop.
* A scene can implement all of the run-loop stages in a delegate instead of subclassing the `SKScene` class. Using a delegate often means that you can avoid needing to subclass the `SKScene` class.
* The SKView class provides more debugging information. You can also provide more performance hints to the renderer.
* You can create normal map textures for use in lighting and physics calculations (or inside your own custom shaders). Use the new `SKMutableTexture` class when you need to create textures whose contents are dynamically updated.
* You can generate texture atlases dynamically at runtime from a collection of textures.

[Xcode6](/Xcode6) also incorporates many new SpriteKit editors. Create or edit the contents of scenes directly, specifying the nodes that appear in the scene as well as their physics bodies and other characteristics. The scene is serialized to a file and can be loaded directly by your game. The editors save you time because often you don’t need to implement your own custom editors to create your game’s assets.




### Design

* Content in a SpriteKit app is organized into **scenes** or `SKScene`. 
  * A scene can include textured **objects**, video, path-based shapes, Core Image **filters**, and other special effects, or `SKNode`
* SpriteKit takes those objects and determines the most efficient way to render them onscreen. 
* When it comes time to **animate** the content in your scenes, you can use SpriteKit to specify explicit **actions** you want to perform 
* or use the physics simulation engine to define physical behaviors (such as **gravity**, **attraction**, or **repulsion**) for your objects.

In addition to the SpriteKit framework, there are Xcode tools for creating particle emitter effects and texture atlases. You can use the Xcode tools to manage app assets and update SpriteKit scenes quickly.


### Sprite Kit vs. Unity

* Source: [Sprite Kit Swift Tutorial for Beginners](http://www.raywenderlich.com/84434/sprite-kit-swift-tutorial-beginners) - Ray Wenderlich

The most popular alternative to Sprite Kit at the moment is a game framework called Unity. Unity was originally developed as a 3D engine, but it recently got full built-in 2D support too.

So before you get started, I recommend you put some thought into whether Sprite Kit or Unity is the best choice for your game.

#### Advantages of Sprite Kit

* It’s built right into iOS. There is no need to download extra libraries or have external dependencies. You can also seamlessly use other iOS APIs like iAd, In-App Purchases, etc. without having to rely on extra plugins.
* It leverages your existing skills. If you already know Swift and iOS development, you can pick up Sprite Kit extremely quickly.
* It’s written by Apple. This gives you some confidence that it will be well supported moving forward on all of Apple’s new products.
* It’s free. Maybe one of the best reasons for small indies! You get all of Sprite Kit’s functionality at no cost. Unity does have a free version but does not have all of the features of the Pro version (you’ll need to upgrade if you want to avoid the Unity splash screen, for example).

#### Advantages of Unity

* Cross-platform. This is one of the big ones. If you use Sprite Kit, you’re locked into the iOS ecosystem. With Unity, you can easily port your games to Android, Windows, and more.
* Visual scene designer. Unity makes it extremely easy to lay out your levels and test your game in realtime with the click of a button. Sprite Kit does have a very basic scene editor in iOS 8, but it is very basic compared to what Unity offers.
* Asset store. Unity comes with a built-in asset store where you can buy various components for your game. Some of these components can save you a good bit of development time!
* More powerful. In general, Unity just has more features and functionality than the Sprite Kit / Scene Kit combination.



###&nbsp;Objects

* `UIViewController`
  * `SKScene`
    * `SKSpriteNode`
* Actions: `aNode.runAction(anAction)`
  * `SKAction.moveBy` (reversible: `anAction.reversedAction`) and `SKAction.moveTo`
  * `SKAction.removeFromParent`
  * `SKAction.sequence`
  * `SKAction.repeatActionForever`
* Collisions
  * **Physics world** is the simulation space for running physics calculations, one set up on the scene
  * **Physics body** a shape can be associated to each sprite for collision purposes, does not have to be the exact same shape that the sprite
  * A **Category** can be set on each sprite to use on collision management (ex: *Projectile* and *Target*)
  * The **Contact Delegate** is call when a collision occurs, and can use categories to ensure behavior.
