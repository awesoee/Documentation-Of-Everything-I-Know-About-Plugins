**This class is an extension of [IPublishPluginProps](/Documentation/PublishPlugin/BasePublishPlugin/IPublishPluginProps.md) and [IPublishPluginState.](/Documentation/PublishPlugin/BasePublishPlugin/IPublishPluginState.md)**

<br/>

_**Base class for React-powered publish plugins.**_
  
_**Note that this same setup structure could be used in a Vanilla JS component as well. The main requirements are as follows:**_

_**1) Assign a callback to FrayToolsCore.propsReceivedHandler to handle new props being passed to the plugin from the parent window.**_

_**2) Assign a callback to FrayToolsCore.forcePublishHandler to handle when the parent window requests a forced publish.**_

_**3) Assign a callback to FrayToolsCore.setupHandler that render a UI using the props passed to the function (check "props.configMode" to determine what view to render)**_

_**4) Use FrayToolsPluginCore.sendReady() after the above steps are completed and plugin DOM is ready.**_

_**To inform the parent window that it's time to publish, use FrayToolsPluginCore.sendPublish(). This will cause the parent UI to lock. When the publish logic is completed, send use FrayToolsPluginCore.sendPublishEnd(publishData) to pass the data back to FrayTools to export. To sync plugin configuration data that should persist between sessions to the filesystem, use FrayToolsPluginCore.configMetadataSync('PublishPlugin', yourConfigMetadata).**_

<br/>

| Function Name | Description |
| ----------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| componentDidMount() | Sets up **propsReceivedHandler** and **forcePublishRequestHandler**, then calls the **sendReady()** function to tell the window that the plugin has been mounted.  |
| componentWillUnmount() | Sets **propsReceivedHandler** and **forcePublishRequestHandler** to `null`. |
| onForcePublishRequest(): void | ![image](https://github.com/user-attachments/assets/ce944aa4-f7dc-4453-a4fd-18c226bdaa7a) |
| onPropsUpdated(props:**[IPublishPluginProps](/Documentation/PublishPlugin/BasePublishPlugin/IPublishPluginProps.md)**) | Override this with custom behavior |
