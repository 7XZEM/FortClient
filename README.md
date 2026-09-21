# FortClient

FortClient is a client for Prison Life with various fun and quality of life features.
It is open source, and still a work in progress.

### INSTALLATION
You can take the release and import it into your executor, however this isn't recommended as it will not receive updates automatically.

You can also paste this into your executor, it will automatically get updated when I release a patch, new feature, or bugfix:

```lua
loadstring(game:HttpGet("https://raw.githubusercontent.com/7XZEM/FortClient/main/main"))()
```

DEPENDENCIES
You must copy the content of the Sounds folder and paste it into the Roblox content\sounds folder for the client to be able to use custom weapon sounds.

Once these steps are done you should be good to go.

CUSTOM MODULES
To create a module it is pretty simple, here is the template:

```lua
ClientFramework.Modules.Template = function()
    ClientFramework.ActiveUI.Template = ClientFramework.ActiveUI.Template or {}
    local TrackingRefs = ClientFramework.ActiveUI.Template

    for _, conn in ipairs(GlobalConnections) do
        table.insert(TrackingRefs, conn)
    end

    while true do
        ClientFramework.Heartbeats.Template = os.clock()
        task.wait(1)
    end
end
```

You can add your custom GUI or functionality inside of this function, but do not forget to attach your connections and instances to the tracking tables for them to be garbage collected and avoid memory leaks issues if the module crashes.



