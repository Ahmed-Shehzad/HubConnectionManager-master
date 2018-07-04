Special Thanks To https://github.com/killnine for helping us at https://github.com/killnine/HubConnectionManager
I'll try to improve it more.

HubConnectionManager

Usage

Create an instance of HubConnectionManager through the static GetHubConnectionManager method, providing the url of your SignalR endpoint:

HubConnectionManager connectionManager = HubConnectionManager.GetHubConnectionManager("http://localhost:6789");

Create you IHubProxy via the CreateHubProxy method, passing in the name of your Hub:

IHubProxy clientProxy = connectionManager.CreateHubProxy("ClientHub");

Initialize the Manager via Initialize() method:

connectionManager.Initialize();

That's it! As long as you have a reference to the HubConnectionManager like you'd have a reference to your HubConnection in the past, it should work just the same.

Additional Functionality

I also expose many of the events and properties of HubConnection:

Events

Error
Received
Closed
Reconnecting
Reconnected
ConnectionSlow
StateChanged

Properties

State