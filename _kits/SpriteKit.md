---
layout: kit
id: spritekit
name: 'SpriteKit'
status:
type: kit
icon: /resources/images/kits/SpriteKit/spritekit-icon_2x.png
since: iOS7
updates: iOS8
prefixe: 'SK'
abstract: "provides a hardware-accelerated animation system optimized for creating 2D and 2.5D games."
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
