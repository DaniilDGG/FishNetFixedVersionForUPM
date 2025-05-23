This demo shows how to use additive scenes per connection, both prewarming scenes on the server
as well hot-loading and unloading them on clients. AOI is separated by scenes and objects in
each scene, as well relative distance to the player.

Setup:
	* Place scenes in build settings, AdditiveScene_Start first, then the remainder scenes.
	* Start on AdditiveScene_Start for server and client.

On server:
	* Start/press play and start server.

On client:
	* Start/press play and start client.


Notes:
	* All scenes are loaded immediately on the server using ServerScenePrewarmer.
            When loaded they are marked to not automatically unload, and KeepUnused when unloading.
            See ServerScenePrewarmer and LeveLoader notes for more details.

	* The Player script is only used to move the player object on the server. It has no functionality
            on the scene management. Waypoint is only used to tell the player where to move.

	* Demo works as clientHost as well server or client only. Load multiple clients to see the
            Observer system work on moving objects across different scenes!

	* See NetworkManager > ObserverManager in AdditiveScene_Start to view ObserverConditions.