SKBlade
=======

Add a blade effect like fruit ninja to your Sprite Kit game.


USAGE

Create a new blade

    SKSpriteNode *spriteNode = [[SKBlade alloc] initWithPosition:(CGPoint)
                                                      TargetNode:(SKNode *)
                                                           Color:(UIColor *)];
    [self addChild:spriteNode];
    
    // Once a new blade is created you can apply your movement logic in touchesMoved or Update


(Optional) Add Physics Properties

    // a Blade must be created first 

    [blade enablePhysicsWithCategoryBitmask:(uint32_t)
                         ContactTestBitmask:(uint32_t)
                           CollisionBitmask:(uint32_t)];
                           
                           
                           
Implementation with Physics enabled e.g. 

    SKBlade *blade = [[SKBlade alloc] initWithPosition:touchLocation
                                   TargetNode:self
                                        Color:[UIColor whiteColor]];
    
    [blade enablePhysicsWithCategoryBitmask:PhysicsCategoryBlade
                         ContactTestBitmask:kNilOptions
                           CollisionBitmask:PhysicsCategoryDummyBox | PhysicsCategoryDummyObject];
    
    [self addChild:blade];


