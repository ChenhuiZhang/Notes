# Busctl usage for dbus

[Man_CH](http://www.jinbuguo.com/systemd/busctl.html)

[Man_En](https://www.freedesktop.org/software/systemd/man/busctl.html)

* list all dbus service on system
```
root@axis-00408c07b902:~# busctl list
NAME                                                   PID PROCESS         USER             CONNECTION    UNIT                      SESSION    DESCRIPTION        
:1.0                                                     1 systemd         root             :1.0          init.scope                -          -                  
:1.100                                                1037 storage_manager storage          :1.100        storage-manager.service   -          -                  
:1.102                                                 776 wsd             root             :1.102        wsd.service               -          -                  
:1.108                                                1149 audio-service   audioapi         :1.108        audio-service.service     -          -                  
:1.118                                                 776 wsd             wsd              :1.118        wsd.service               -          -                  
:1.119                                                 776 wsd             wsd              :1.119        wsd.service               -          -                  
:1.12                                                  406 netd            root             :1.12         netd.service              -          -                  
:1.120                                                 776 wsd             wsd              :1.120        wsd.service               -          -                  
:1.121                                                1278 addonmanager    root             :1.121        addonmanager.service      -          -                  
:1.122                                                1279 acapmanager     root             :1.122        acapmanager.service       -          -                  
:1.123                                                1278 addonmanager    root             :1.123        addonmanager.service      -          -                  
:1.124                                                1279 acapmanager     root             :1.124        acapmanager.service       -          -                  
:1.13                                                  406 netd            root             :1.13         netd.service              -          -                  
:1.14                                                  406 netd            root             :1.14         netd.service              -          -                  
:1.15                                                  406 netd            root             :1.15         netd.service              -          -                  
:1.16                                                  467 ntpconfd        ntpconfd         :1.16         ntpconfd.service          -          -                  
:1.161                                                2160 com.axis.Captur capturemoded     :1.161        capturemoded.service      -          -                  
:1.162                                                2160 com.axis.Captur capturemoded     :1.162        capturemoded.service      -          -                  
:1.167                                                2116 video-scene-pro axis-video-scene :1.167        axis-video-scene-provi…ce -          -                  
:1.168                                                2116 video-scene-pro axis-video-scene :1.168        axis-video-scene-provi…ce -          -                  
:1.169                                                2264 video-scene-man video-scene-mana :1.169        video-scene-manager.se…ce -          -                  
:1.17                                                  467 ntpconfd        ntpconfd         :1.17         ntpconfd.service          -          -                  
:1.170                                                2264 video-scene-man video-scene-mana :1.170        video-scene-manager.se…ce -          -                  
:1.172                                                2327 bluetoothd      root             :1.172        bluetooth.service         -          -                  
:1.18                                                  467 ntpconfd        ntpconfd         :1.18         ntpconfd.service          -          -                  
:1.19                                                  460 event_switch    event            :1.19         event-switch.service      -          -                  
:1.20                                                  466 blinkenlights   led              :1.20         led-controller.service    -          -                  
:1.208                                                2859 bluetoothctl    root             :1.208        sshd@0-192.168.77.227:…ce -          -                  
:1.21                                                  528 vdo             vdo              :1.21         vdo.service               -          -                  
:1.233                                               13132 video-service-l video-service-le :1.233        video-service-legacy.s…ce -          -                  
:1.235                                               18551 busctl          root             :1.235        sshd@0-192.168.77.227:…ce -          -                  
:1.24                                                  547 policykit_cert  root             :1.24         policykit-cert.service    -          -                  
:1.25                                                  547 policykit_cert  root             :1.25         policykit-cert.service    -          -                  
:1.28                                                  586 axisns          axisns           :1.28         axisns.service            -          -                  
:1.32                                                  426 monolith        streamer         :1.32         monolith.service          -          -                  
:1.33                                                  405 image2d         imaged           :1.33         image2d.service           -          -                  
:1.34                                                  652 policykit_parha root             :1.34         policykit-parhand.service -          -                  
:1.35                                                  652 policykit_parha root             :1.35         policykit-parhand.service -          -                  
:1.36                                                  662 eventbridged    eventbridged     :1.36         event-bridge.service      -          -                  
:1.37                                                  662 eventbridged    eventbridged     :1.37         event-bridge.service      -          -                  
:1.38                                                  688 confcached      confcached       :1.38         confcache.service         -          -                  
:1.39                                                  426 monolith        streamer         :1.39         monolith.service          -          -                  
:1.41                                                  426 monolith        streamer         :1.41         monolith.service          -          -                  
:1.42                                                  426 monolith        streamer         :1.42         monolith.service          -          -                  
:1.43                                                  426 monolith        streamer         :1.43         monolith.service          -          -                  
:1.44                                                  426 monolith        streamer         :1.44         monolith.service          -          -                  
:1.45                                                  426 monolith        streamer         :1.45         monolith.service          -          -                  
:1.46                                                  426 monolith        streamer         :1.46         monolith.service          -          -                  
:1.49                                                  770 sensoryfeedback root             :1.49         sensoryfeedback.service   -          -                  
:1.5                                                   416 policykit_syste root             :1.5          policykit-system.service  -          -                  
:1.50                                                  779 confloggerd     confloggerd      :1.50         conflogger.service        -          -                  
:1.51                                                  780 virtualinputd   virtualinputd    :1.51         virtual-input.service     -          -                  
:1.52                                                  780 virtualinputd   virtualinputd    :1.52         virtual-input.service     -          -                  
:1.53                                                  768 depd            depd             :1.53         depd.service              -          -                  
:1.54                                                  768 depd            depd             :1.54         depd.service              -          -                  
:1.55                                                  768 depd            depd             :1.55         depd.service              -          -                  
:1.56                                                  769 httpwdd         httpwdd          :1.56         httpwdd.service           -          -                  
:1.6                                                   416 policykit_syste root             :1.6          policykit-system.service  -          -                  
:1.61                                                  797 stclient        stclient         :1.61         stclient.service          -          -                  
:1.62                                                  797 stclient        stclient         :1.62         stclient.service          -          -                  
:1.63                                                  784 scheduled       scheduled        :1.63         scheduled.service         -          -                  
:1.65                                                  752 actionengined   actionengined    :1.65         action-engine-system.s…ce -          -                  
:1.66                                                  688 confcached      confcached       :1.66         confcache.service         -          -                  
:1.67                                                  784 scheduled       scheduled        :1.67         scheduled.service         -          -                  
:1.68                                                  759 temperature_ctr environment      :1.68         temperature-controller…ce -          -                  
:1.7                                                   405 image2d         imaged           :1.7          image2d.service           -          -                  
:1.70                                                  759 temperature_ctr environment      :1.70         temperature-controller…ce -          -                  
:1.71                                                  764 indexer         storage          :1.71         recording-indexer.service -          -                  
:1.72                                                  764 indexer         storage          :1.72         recording-indexer.service -          -                  
:1.74                                                  758 motion          motion           :1.74         motion-detection.service  -          -                  
:1.75                                                  777 io2d            iod              :1.75         io2d.service              -          -                  
:1.78                                                  777 io2d            iod              :1.78         io2d.service              -          -                  
:1.79                                                  777 io2d            iod              :1.79         io2d.service              -          -                  
:1.8                                                   404 audiocontrol    audiocontrol     :1.8          audiocontrol.service      -          -                  
:1.80                                                  758 motion          motion           :1.80         motion-detection.service  -          -                  
:1.81                                                  995 actionengined   actionengined    :1.81         action-engine-user.ser…ce -          -                  
:1.83                                                  752 actionengined   actionengined    :1.83         action-engine-system.s…ce -          -                  
:1.84                                                  752 actionengined   actionengined    :1.84         action-engine-system.s…ce -          -                  
:1.85                                                  752 actionengined   actionengined    :1.85         action-engine-system.s…ce -          -                  
:1.86                                                  752 actionengined   actionengined    :1.86         action-engine-system.s…ce -          -                  
:1.87                                                  764 indexer         storage          :1.87         recording-indexer.service -          -                  
:1.88                                                  764 indexer         storage          :1.88         recording-indexer.service -          -                  
:1.89                                                  764 indexer         storage          :1.89         recording-indexer.service -          -                  
:1.90                                                  764 indexer         storage          :1.90         recording-indexer.service -          -                  
:1.91                                                  764 indexer         storage          :1.91         recording-indexer.service -          -                  
:1.93                                                  995 actionengined   actionengined    :1.93         action-engine-user.ser…ce -          -                  
:1.95                                                 1037 storage_manager storage          :1.95         storage-manager.service   -          -                  
:1.96                                                 1037 storage_manager storage          :1.96         storage-manager.service   -          -                  
:1.97                                                 1061 storage-stabili storage-stabilit :1.97         storage-stability-help…ce -          -                  
:1.98                                                 1062 todd            bodywornmanager  :1.98         todd.service              -          -                  
:1.99                                                 1037 storage_manager storage          :1.99         storage-manager.service   -          -                  
com.axis.AVHS                                          797 stclient        stclient         :1.62         stclient.service          -          -                  
com.axis.AcapManager1                                 1279 acapmanager     root             :1.124        acapmanager.service       -          -                  
com.axis.AddonDevMode1                                   - -               -                (activatable) -                         -         
com.axis.AddonExample1                                   - -               -                (activatable) -                         -         
com.axis.AddonManager                                 1278 addonmanager    root             :1.123        addonmanager.service      -          -                  
com.axis.Audio1                                       1149 audio-service   audioapi         :1.108        audio-service.service     -          -                  
com.axis.AudioControl                                  404 audiocontrol    audiocontrol     :1.8          audiocontrol.service      -          -                  
com.axis.AxisNS                                        586 axisns          axisns           :1.28         axisns.service            -          -                  
com.axis.BasicDeviceInfo1                                - -               -                (activatable) -                         -         
com.axis.CaptureMode1                                 2160 com.axis.Captur capturemoded     :1.162        capturemoded.service      -          -                  
com.axis.Configuration.Legacy.IOControl1.IOPort        777 io2d            iod              :1.75         io2d.service              -          -                  
com.axis.CustomFirmwareCertificates1                     - -               -                (activatable) -                         -         
com.axis.Emotion                                       758 motion          motion           :1.80         motion-detection.service  -          -                  
com.axis.Event.ActionEngine.System                     752 actionengined   actionengined    :1.65         action-engine-system.s…ce -          -                  
com.axis.Event.ActionEngine.User                       995 actionengined   actionengined    :1.81         action-engine-user.ser…ce -          -                  
com.axis.Event.DefaultProducer                         768 depd            depd             :1.54         depd.service              -          -                  
com.axis.Event.Scheduled                               784 scheduled       scheduled        :1.63         scheduled.service         -          -                  
com.axis.Event.Switch                                  460 event_switch    event            :1.19         event-switch.service      -          -                  
com.axis.EventConsumerd1                                 - -               -                (activatable) -                         -         
com.axis.EventProducerd1                                 - -               -                (activatable) -                         -         
com.axis.FirmwareManager1                                - -               -                (activatable) -                         -         
com.axis.GattServer                                      - -               -                (activatable) -                         -         
com.axis.HttpWatchDog                                  769 httpwdd         httpwdd          :1.56         httpwdd.service           -          -                  
com.axis.IOControl.State                               777 io2d            iod              :1.75         io2d.service              -          -                  
com.axis.IOD.Connector                                 777 io2d            iod              :1.75         io2d.service              -          -                  
com.axis.IOSupervised.Supervised                       777 io2d            iod              :1.75         io2d.service              -          -                  
com.axis.Image2d                                       405 image2d         imaged           :1.7          image2d.service           -          -                  
com.axis.ImageControl                                  405 image2d         imaged           :1.7          image2d.service           -          -                  
com.axis.Indexer                                       764 indexer         storage          :1.72         recording-indexer.service -          -                  
com.axis.LEDController                                 466 blinkenlights   led              :1.20         led-controller.service    -          -                  
com.axis.NTP.Legacy                                    467 ntpconfd        ntpconfd         :1.17         ntpconfd.service          -          -                  
com.axis.NTP1                                          467 ntpconfd        ntpconfd         :1.18         ntpconfd.service          -          -                  
com.axis.Net.Legacy                                    406 netd            root             :1.13         netd.service              -          -                  
com.axis.Net1                                          406 netd            root             :1.14         netd.service              -          -                  
com.axis.NetworkShare                                 1037 storage_manager storage          :1.95         storage-manager.service   -          -                  
com.axis.Onvif.Media                                   776 wsd             root             :1.102        wsd.service               -          -                  
com.axis.PackageManager.LicenseKey1                      - -               -                (activatable) -                         -         
com.axis.PackageManager.LicenseKeyConf1                  - -               -                (activatable) -                         -         
com.axis.PolicyKitCert                                 547 policykit_cert  root             :1.24         policykit-cert.service    -          -                  
com.axis.PolicyKitParhand                              652 policykit_parha root             :1.34         policykit-parhand.service -          -                  
com.axis.PolicyKitSystem                               416 policykit_syste root             :1.5          policykit-system.service  -          -                  
com.axis.PrioritizedTextOverlay                          - -               -                (activatable) -                         -         
com.axis.ProductInfo1                                    - -               -                (activatable) -                         -         
com.axis.RecordingFixer                                  - -               -                (activatable) -                         -         
com.axis.RuleEngine                                      - -               -                (activatable) -                         -         
com.axis.SensoryFeedback                               770 sensoryfeedback root             :1.49         sensoryfeedback.service   -          -                  
com.axis.Storage                                      1037 storage_manager storage          :1.95         storage-manager.service   -          -                  
com.axis.Streamer                                      426 monolith        streamer         :1.39         monolith.service          -          -                  
com.axis.TemperatureController                         759 temperature_ctr environment      :1.68         temperature-controller…ce -          -                  
com.axis.TriggerData                                     - -               -                (activatable) -                         -         
com.axis.UsageStatistics1                                - -               -                (activatable) -                         -         
com.axis.Vdo                                           528 vdo             vdo              :1.21         vdo.service               -          -                  
com.axis.Vdo.Channel                                   528 vdo             vdo              :1.21         vdo.service               -          -                  
com.axis.Vdo.Input                                     528 vdo             vdo              :1.21         vdo.service               -          -                  
com.axis.Vdo.Mask                                      528 vdo             vdo              :1.21         vdo.service               -          -                  
com.axis.Vdo.Stream                                    528 vdo             vdo              :1.21         vdo.service               -          -                  
com.axis.Vdo.System                                    528 vdo             vdo              :1.21         vdo.service               -          -                  
com.axis.Video0                                          - -               -                (activatable) -                         -         
com.axis.Video1                                          - -               -                (activatable) -                         -         
com.axis.VideoDisturbanceNotifier1                       - -               -                (activatable) -                         -         
com.axis.VideoLegacy1                                13132 video-service-l video-service-le :1.233        video-service-legacy.s…ce -          -                  
com.axis.VideoSceneManager1                           2264 video-scene-man video-scene-mana :1.170        video-scene-manager.se…ce -          -                  
com.axis.VirtualInput                                  780 virtualinputd   virtualinputd    :1.52         virtual-input.service     -          -                  
com.axis.VisionDevices1                                  - -               -                (activatable) -                         -         
com.axis.WLAN.Scan                                       - -               -                (activatable) -                         -         
com.axis.callbacks.axis_video_scene_provider          2116 video-scene-pro axis-video-scene :1.168        axis-video-scene-provi…ce -          -                  
com.axis.recording.RecordingControl                    764 indexer         storage          :1.72         recording-indexer.service -          -                  
com.axis.recording.RecordingManager1                   764 indexer         storage          :1.87         recording-indexer.service -          -                  
com.axis.storage.StorageManager1                      1037 storage_manager storage          :1.96         storage-manager.service   -          -                  
fi.epitest.hostap.WPASupplicant                          - -               -                (activatable) -                         -         
fi.w1.wpa_supplicant1                                    - -               -                (activatable) -                         -         
org.bluez                                             2327 bluetoothd      root             :1.172        bluetooth.service         -          -                  
org.freedesktop.DBus                                     1 systemd         root             -             init.scope                -          -                  
org.freedesktop.systemd1                                 1 systemd         root             :1.0          init.scope                -          -                  
root@axis-00408c07b902:~# 
```

* find the "bluetoothd" service
```
root@axis-00408c07b902:~# busctl list | grep bluetooth
:1.172                                                2327 bluetoothd      root             :1.172        bluetooth.service         -          -                  
:1.208                                                2859 bluetoothctl    root             :1.208        sshd@0-192.168.77.227:…ce -          -                  
org.bluez                                             2327 bluetoothd      root             :1.172        bluetooth.service         -          -                  
root@axis-00408c07b902:~# 
```

bluetoothd provide *org.bluez* (well-known name) while *:1.172* is the unique name on the bus.

* tree the inside of the service (object show)
```
root@axis-00408c07b902:~# busctl tree org.bluez
└─/org
  └─/org/bluez
    └─/org/bluez/hci0
      └─/org/bluez/hci0/dev_FF_FF_C2_13_E2_EC
root@axis-00408c07b902:~# 
```
* interospec the object in this service
```
root@axis-00408c07b902:~# busctl introspect org.bluez /org/bluez/hci0
NAME                                TYPE      SIGNATURE RESULT/VALUE                             FLAGS
org.bluez.Adapter1                  interface -         -                                        -
.RemoveDevice                       method    o         -                                        -
.SetDiscoveryFilter                 method    a{sv}     -                                        -
.StartDiscovery                     method    -         -                                        -
.StopDiscovery                      method    -         -                                        -
.Address                            property  s         "43:43:A1:12:1F:AC"                      emits-change
.Alias                              property  s         "BlueZ 5.46"                             emits-change writable
.Class                              property  u         0                                        emits-change
.Discoverable                       property  b         false                                    emits-change writable
.DiscoverableTimeout                property  u         180                                      emits-change writable
.Discovering                        property  b         false                                    emits-change
.Modalias                           property  s         "usb:v1D6Bp0246d052E"                    emits-change
.Name                               property  s         "BlueZ 5.46"                             emits-change
.Pairable                           property  b         true                                     emits-change writable
.PairableTimeout                    property  u         0                                        emits-change writable
.Powered                            property  b         false                                    emits-change writable
.UUIDs                              property  as        2 "00001801-0000-1000-8000-00805f9b34…b" emits-change
org.bluez.GattManager1              interface -         -                                        -
.RegisterApplication                method    oa{sv}    -                                        -
.UnregisterApplication              method    o         -                                        -
org.bluez.LEAdvertisingManager1     interface -         -                                        -
.RegisterAdvertisement              method    oa{sv}    -                                        -
.UnregisterAdvertisement            method    o         -                                        -
org.freedesktop.DBus.Introspectable interface -         -                                        -
.Introspect                         method    -         s                                        -
org.freedesktop.DBus.Properties     interface -         -                                        -
.Get                                method    ss        v                                        -
.GetAll                             method    s         a{sv}                                    -
.Set                                method    ssv       -                                        -
.PropertiesChanged                  signal    sa{sv}as  -                                        -
root@axis-00408c07b902:~# 

```
Here we could see interfaces, methods, propertys and signal elements in the object.

* Property operation
```
root@axis-00408c07b902:~# busctl get-property org.bluez /org/bluez/hci0 org.bluez.Adapter1 Powered
b false
root@axis-00408c07b902:~# busctl set-property org.bluez /org/bluez/hci0 org.bluez.Adapter1 Powered b true
root@axis-00408c07b902:~# busctl get-property org.bluez /org/bluez/hci0 org.bluez.Adapter1 Powered
b true
root@axis-00408c07b902:~# 
``` 
