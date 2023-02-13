**Getting help**
`xinput -h`
**List Available Devices and know device id**
`xinput list`
>`SynPS/2 Synaptics TouchPad id=13`

**Test a device**
`xinput test [device_id]`
`xinput watch-props [device_id]`
`xinput list-props [device_id]`
**Set Sensitivity**
`xinput --set-prop [device number] "Synaptics Finger" 10 10 10`