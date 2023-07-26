# Sprint Component Interface

Unlike previous versions where the Stamina, Sprint and Character Movement components had to be on the same actor, we have updated the system to use an interface to be implemented on the owning actor of the Sprint Component. This is to allow it to successfully retrieve the relevant components, no matter where they are as long as the owning actor can reach them.  

If you choose not to implement this interface then the previous versions method will work, so this should be backwards compatible.

![](/assets/Examples/Interface/CharacterMovement.png)

![](/assets/Examples/Interface/SprintComponent.png)

![](/assets/Examples/Interface/StaminaComponent.png)