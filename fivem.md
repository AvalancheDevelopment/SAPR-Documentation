# San Andreas Police Radio FiveM Script Documentation

This will be updated every release as needed. Deprecated events will be indicated, and eventually removed in the future. All events are client side, unless otherwise specified.

### v1.1.0

#### Sent Events

-   `RadioOn`: An emitted event when the radio state changes. _Both client and server events_. Values: true, false.
-   `RadioSignal`: An emitted event when the radio connection strength changes. _Both client and server events_. Values: [0-4]. 0 indicates no connection

#### Received Events

-   `SAPR:CloseNUI`: No parameters. Force closes the NUI. Typically used when displaying some other full screen NUI content. **Does not revoke NUI focus!**
-   `SAPR:HasRadio`: Parameters: bool. Allows you to indicate whether a player has a radio. Typically used with inventories. Parameter is to indicate if they have the radio on them.
-   `SAPR:ToggleRadio`: Parameters: bool. Allows you to turn a radio on/off from another script. Users can still override this with the UI. Parameter is to indicate the state to set the radio to.
-   `SAPR:911`: Parameters: bool. Allows you to trigger 911s, even if the setting is disabled for your community. Parameter is to indicate if the call is priority related.
-   `SAPR:311`: No parameters. Allows you to trigger 311s, even if the setting is disabled for your community.

### v1.0.4 (Deprecated)

#### Sent Events

~~- `RadioOn`: An emitted event when the radio state changes. Values: true, false.~~

#### Received Events

##### Client

~~None at this time.~~
