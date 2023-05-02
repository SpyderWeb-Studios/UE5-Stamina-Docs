# Stamina Component

This is the main component that handles the system. It replicates the Stamina values to the clients and listen server.


These 2 functions are what you will be using in Blueprints to interact with the component on a 
basic level. 
```c++
/**
* @brief RPC to toggle stamina on the Server
 * @param bEnableStamina If the client is requesting the stamina to be enabled or disabled
 */
UFUNCTION(Server, Unreliable, BlueprintCallable, Category="Stamina|Toggle")
    void Server_ToggleStaminaActive(bool bEnableStamina);

/**
 * @brief Server Only Function to toggle stamina on the Server. Should be used over the RPC equivalent when possible.
 * @param bEnableStamina If the client is requesting the stamina to be enabled or disabled
 */
UFUNCTION(BlueprintAuthorityOnly, BlueprintCallable, Category="Stamina|Toggle")
    void ToggleStamina(bool bEnableStamina);
```

