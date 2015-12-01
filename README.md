
# "Dummy Switches" Plugin

Example config.json:

 ```
    "accessories": [
        {
          "accessory": "DummySwitch",
          "name": "My Switch 1"
        }   
    ]

```

With this plugin, you can create any number of fake switches that will do nothing when turned on (and will automatically turn off right afterward, simulating a stateless switch). This can be very useful for advanced automation with HomeKit scenes.

For instance, the Philips Hue app will automatically create HomeKit scenes for you based on Hue Scenes you create. But what if you want to create a scene that contains both Philips Hue actions and other actions (like turning on the coffee maker with a WeMo outlet)? You are forced to either modify the Hue-created scene (which can be a HUGE list of actions if you have lots of lights) or build your own HomeKit lighting scenes.

Instead, you can link scenes using these dummy switches. Let's say you have a Hue Scene called "Rise and Shine" that you want to activate in the morning. And you have also setup the system HomeKit scene "Good Morning" to turn on your coffee maker and disarm you security system. You can add a single dummy switch to your Good Morning scene, then create a Trigger based on the switching-on of the dummy switch that also activates Rise And Shine.