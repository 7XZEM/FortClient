FortClient is a client for prison life with various fun and quality of life features.

it is open source, and still work in progress.

INSTALLATION:

You can take the release and import it into your executor, however this isn't recommended as it will not receive updates automatically.

You can also paste this into your executor, it will automatically get updated when i release a patch, new feature, or bugfix.

DEPENCIES:

you must copy the content of the Sounds folder and paste it into the roblox content\sounds folder for the client to be able to use custom weapon sounds.

Once these steps are done you should be good to go.

CUSTOM MODULES:

to create a module it is pretty simple, here is the template.

ClientFramework.Modules.Template = function()
	ClientFramework.ActiveUI.Template = ClientFramework.ActiveUI.Template or {}
	local TrackingRefs = ClientFramework.ActiveUI.Template

	for _, conn in ipairs(GlobalConnections) do
		table.insert(TrackingRefs, conn)
	end

	while true do
		ClientFramework.Heartbeats.AntiFling = os.clock()
		task.wait(1)
	end
end

You can add your custom gui, or functionallity inside of this function, but do not forget to attach your connections and instances to the tracking tables for them to be garbage collected and avoid memory leaks and issues if the module crashes.


