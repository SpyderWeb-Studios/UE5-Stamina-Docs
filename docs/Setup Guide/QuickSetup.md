# Quick Setup

After installing, through the Epic Games Launcher or otherwise, let's walk through the steps to get started.

## Stamina Component

To get setup with the Component, simply add it to the Character you want to use it with. The Component will automatically add the required Attributes to the Character, and will automatically update the Character's Movement Speed based on the current Stamina.

However, you will need to set the character movement component that you want associated with this Stamina Component. This is done by calling the `SetCharacterMovementComponent` function on the Stamina Component. This is usually done in the Character's `BeginPlay` function or construction script.

When you have the Stamina Component added to your Character, you can now use the `Stamina` Category in the Component's Details panel to configure. You can set
the maximum Stamina, the rate at which Stamina regenerates, and the rate at which Stamina depletes. You can also set the sprinting and walk speed.

To actually use the Stamina Component, you will need to call the `ToggleSprint` or `Server_ToggleSprint` functions. These functions will automatically handle the Stamina and 
replication. The difference between the two functions is that `ToggleSprint` is a Server Only function, and `Server_ToggleSprint` is a Server RPC. If you are using the Stamina Component
in a multiplayer game, you will need to call the `Server_ToggleSprint` function if you are toggling from a client. If you are using the Stamina Component in a singleplayer game, you can call either function.

Don't worry about calling the `Server_ToggleSprint` function from a client in a singleplayer game, as standalone will pass the authority check and the function will be called appropriately.

## Stamina Widget

To get setup with the Widget, simply add it to the UI that you want to use it with. The Widget will automatically update the Stamina Bar based on the current Stamina, 
assuming that the Stamina Component is on the Character that the Player Controller is possessing. If you place it elsewhere, then you will need to update the 
Widget's `Stamina Component` variable to point to the Stamina Component that you want to use, by changing the Input for the `Set Stamina Component` function.
