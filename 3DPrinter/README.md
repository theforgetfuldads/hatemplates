- add following helpers (Settings > Devices & Services > Helpers > Create Helper > Toggle):

    name:   octo_controls
    type:   toggle 

    name:   octoprint_webcam
    type:   toggle 

    name:   octo_info
    type:   toggle 

- You will need a Octoprint instance with following plugins:
    - Slicer Thumbnails 
    - PrettyGCode (Not sure if needed)
- add a generic camera with the follwoing URL: http://<octourl>/plugin/prusaslicerthumbnails/thumbnail/{{states("sensor.octoprint_print_file") | replace("gcode","png",1) }}
- you will need HACS with following frontend integrations:
    - threedy
    - mushroom
    - layout card
    - stack-in-card
- Default HA Integration of Octoprint
Note: This guide assumes you’ve already configured MQTT with Octoprint. Lots of good guides out there if you haven’t yet.
- Will only work with gcode uploads NOT with bgcode 
