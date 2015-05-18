# swift-flappybird-clone
//first project


//
//  GameScene.swift
//  flappybird swift
//
//  Created by Michael Elbaz on 5/12/15.
//  Copyright (c) 2015 elboss-apps. All rights reserved.
//

import SpriteKit

class GameScene: SKScene {
    
    var bird = SKSpriteNode()
    
    override func didMoveToView(view: SKView) {
        /* Setup your scene here */
         //physics(makes it move down faster)
        self.physicsWorld.gravity = CGVectorMake(0.0, -5.0);
       
        //bird
        var BirdTexture = SKTexture(imageNamed:"bird")
        BirdTexture.filteringMode = SKTextureFilteringMode.Nearest
        
        bird = SKSpriteNode(texture: BirdTexture)
        bird.setscale (0.5)
        bird.position = CGPoint(x: self.frame.size.width, *0.35, y: self.frame.size.height, *0.6)            }
    
    
    bird.physicsBody = SkphysicsBody(circleOfRadis:bird.size.height/2.0)
    bird.physicsBody.dynamic = true
    bird.physicsbody.allowsRotation = faulse
    
        self.addChild(bird)
    //ground 
    
    var groundTexture = SKTexture(imageNamed:"ground")
    
    var sprite =SKSpriteNode(texture:groundTexture)
    sprite.setscale.(2.0)
    sprite.position = CGPointMake(self.size.width/2, sprite.size.height/2.0)
    self.addChild(sprite)
    
    var ground = SKNode()
    
    ground.position = CGPointMake(0, groundTexture.size().height)
    ground.physicsBody = SKPhysicsBody(rectangleOfSize: CGSizeMake(self.frame.size.width, groundTexture.size().Height = 2.0))
    
    
    
    
    
    
    
    
    
}

    override func touchesBegan(touches: Set<NSObject>, withEvent event: UIEvent) {
        /* Called when a touch begins */
        
        for touch in (touches as! Set<UITouch>) {
            
            
        }
    }
   
    override func update(currentTime: CFTimeInterval) {
        /* Called before each frame is rendered */
    }
}
