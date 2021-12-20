# San Andreas Police Radio FiveM Script Documentation

This will be updated every release as needed. Deprecated events will be indicated, and eventually removed in the future. All events are client side, unless otherwise specified. Jump to [Server Events](#server)

## Client

### v1.1.3

#### Sent Events

-   `SAPR:PanicButton`: An emitted event when the panic button is triggered. _Both client and server events_. Values: None.
-   `SAPR:911Sent`: An emitted event when a 911 call is made. _Both client and server events_. Values: None.
-   `SAPR:311Sent`: An emitted event when a 311 call is made. _Both client and server events_. Values: None.

#### Received Events

-   `SAPR:IncidentReceived`: Parameters: None. Allows you to a CALL RECEIVED message to the APX8500 E3 head unit. (Will only display if the player is in the vehicle.)

### v1.2.0

#### Sent Events

No changes from previous versions.

#### Received Events

-   `SAPR:PlayTalkingAnim`: Parameters: boolean. Allows you to toggle the talking animation flag of an individual player. Parameter is to indicate if the talking animation should be played.

### v1.1.0

#### Sent Events

-   `RadioOn`: An emitted event when the radio state changes. _Both client and server events_. Values: true, false.
-   `RadioSignal`: An emitted event when the radio connection strength changes. _Both client and server events_. Values: [0-4]. 0 indicates no connection

#### Received Events

-   `SAPR:CloseNUI`: Parameters: None. Force closes the NUI. Typically used when displaying some other full screen NUI content. **Does not revoke NUI focus!**
-   `SAPR:HasRadio`: Parameters: bool. Allows you to indicate whether a player has a radio. Typically used with inventories. Parameter is to indicate if they have the radio on them.
-   `SAPR:ToggleRadio`: Parameters: bool. Allows you to turn a radio on/off from another script. Users can still override this with the UI. Parameter is to indicate the state to set the radio to.
-   `SAPR:911`: Parameters: bool. Allows you to trigger 911s, even if the setting is disabled for your community. Parameter is to indicate if the call is priority related.
-   `SAPR:311`: Parameters: None. Allows you to trigger 311s, even if the setting is disabled for your community.

## Server

### v1.3.0

#### Sent Events

None at this time.

#### Received Events

-   `SAPR:DisableRadioTowers`: Parameters: Player (No need to pass this if triggering from client). Allows you to disable radio towers for 15 minutes. Typically used with your own minigame. See separate documentation.

### v1.2.0

None at this time.
