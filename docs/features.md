---
title: List of HID++ 2.0 features
layout: page
---

# List of HID++ 2.0 features

## Feature status

See functions in `hidpp20.py` and `settings_templates.py`

Feature                                | ID       | Status             | Notes
---------------------------------------|----------|:------------------:|------
`ROOT`                                 | `0x0000` | Supported          | System
`FEATURE_SET`                          | `0x0001` | Supported          | System
`FEATURE_INFO`                         | `0x0002` | Supported          | System
`DEVICE_FW_VERSION`                    | `0x0003` | Supported          | `get_firmware`, read only
`DEVICE_UNIT_ID`                       | `0x0004` | Unsupported        |
`DEVICE_NAME`                          | `0x0005` | Supported          | `get_kind`, `get_name`, read only
`DEVICE_GROUPS`                        | `0x0006` | Unsupported        |
`DEVICE_FRIENDLY_NAME`                 | `0x0007` | Supported          | read only
`KEEP_ALIVE`                           | `0x0008` | Unsupported        |
`RESET`                                | `0x0020` | Unsupported        | aka “Config Change”
`CRYPTO_ID`                            | `0x0021` | Unsupported        |
`TARGET_SOFTWARE`                      | `0x0030` | Unsupported        |
`WIRELESS_SIGNAL_STRENGTH`             | `0x0080` | Unsupported        |
`DFUCONTROL_LEGACY`                    | `0x00C0` | Unsupported        |
`DFUCONTROL_UNSIGNED`                  | `0x00C1` | Unsupported        |
`DFUCONTROL_SIGNED`                    | `0x00C2` | Unsupported        |
`DFU`                                  | `0x00D0` | Unsupported        |
`BATTERY_STATUS`                       | `0x1000` | Supported          | `get_battery`, read only
`BATTERY_VOLTAGE`                      | `0x1001` | Supported          | `get_voltage`, read only
`CHARGING_CONTROL`                     | `0x1010` | Unsupported        |
`LED_CONTROL`                          | `0x1300` | Unsupported        |
`GENERIC_TEST`                         | `0x1800` | Unsupported        |
`DEVICE_RESET`                         | `0x1802` | Unsupported        |
`OOBSTATE`                             | `0x1805` | Unsupported        |
`CONFIG_DEVICE_PROPS`                  | `0x1806` | Unsupported        |
`CHANGE_HOST`                          | `0x1814` | Supported          |
`HOSTS_INFO`                           | `0x1815` | Partial Support    | `get_host_names`, partial listing only
`BACKLIGHT`                            | `0x1981` | Unsupported        |
`BACKLIGHT2`                           | `0x1982` | Supported          | `_feature_backlight2`
`BACKLIGHT3`                           | `0x1983` | Unsupported        |
`PRESENTER_CONTROL`                    | `0x1A00` | Unsupported        |
`SENSOR_3D`                            | `0x1A01` | Unsupported        |
`REPROG_CONTROLS`                      | `0x1B00` | Listing Only       | `get_keys`, only listing
`REPROG_CONTROLS_V2`                   | `0x1B01` | Unsupported        |
`REPROG_CONTROLS_V2_2`                 | `0x1B02` | Unsupported        |
`REPROG_CONTROLS_V3`                   | `0x1B03` | Unsupported        |
`REPROG_CONTROLS_V4`                   | `0x1B04` | Partial Support    | `get_keys`, _feature_reprogrammable_keys
`REPORT_HID_USAGE`                     | `0x1BC0` | Unsupported        |
`PERSISTENT_REMAPPABLE_ACTION`         | `0x1C00` | Unsupported        |
`WIRELESS_DEVICE_STATUS`               | `0x1D4B` | Read only          | status reporting from device
`REMAINING_PAIRING`                    | `0x1DF0` | Unsupported        |
`FIRMWARE_PROPERTIES`                  | `0x1F1F` | Unsupported        |
`ADC_MEASUREMENT`                      | `0x1F20` | Unsupported        |
`LEFT_RIGHT_SWAP`                      | `0x2001` | Unsupported        |
`SWAP_BUTTON_CANCEL`                   | `0x2005` | Unsupported        |
`POINTER_AXIS_ORIENTATION`             | `0x2006` | Unsupported        |
`VERTICAL_SCROLLING`                   | `0x2100` | Supported          | `get_vertical_scrolling_info`, read only
`SMART_SHIFT`                          | `0x2110` | Supported          | `_feature_smart_shift`
`HI_RES_SCROLLING`                     | `0x2120` | Supported          | `get_hi_res_scrolling_info`, `_feature_hi_res_scroll`
`HIRES_WHEEL`                          | `0x2121` | Supported          | `get_hires_wheel`, `_feature_hires_smooth_invert`, `_feature_hires_smooth_resolution`
`LOWRES_WHEEL`                         | `0x2130` | Supported          | `get_lowres_wheel_status`, `_feature_lowres_smooth_scroll`
`THUMB_WHEEL`                          | `0x2150` | Supported          | `_feature_thumb_mode`, `_feature_thumb_invert`
`MOUSE_POINTER`                        | `0x2200` | Supported          | `get_mouse_pointer_info`, read only
`ADJUSTABLE_DPI`                       | `0x2201` | Supported          | `_feature_adjustable_dpi`
`POINTER_SPEED`                        | `0x2205` | Supported          | `get_pointer_speed_info`, `_feature_pointer_speed`
`ANGLE_SNAPPING`                       | `0x2230` | Unsupported        |
`SURFACE_TUNING`                       | `0x2240` | Unsupported        |
`HYBRID_TRACKING`                      | `0x2400` | Unsupported        |
`FN_INVERSION`                         | `0x40A0` | Supported          | `_feature_fn_swap`
`NEW_FN_INVERSION`                     | `0x40A2` | Supported          | `get_new_fn_inversion`, `_feature_new_fn_swap`
`K375S_FN_INVERSION`                   | `0x40A3` | Supported          | `_feature_k375s_fn_swap`
`ENCRYPTION`                           | `0x4100` | Unsupported        |
`LOCK_KEY_STATE`                       | `0x4220` | Unsupported        |
`SOLAR_DASHBOARD`                      | `0x4301` | Unsupported        |
`KEYBOARD_LAYOUT`                      | `0x4520` | Unsupported        | read only
`KEYBOARD_DISABLE_KEYS`                | `0x4521` | Supported          | `_feature_disable_keyboard_keys`
`KEYBOARD_DISABLE_BY_USAGE`            | `0x4522` | Unsupported        |
`DUALPLATFORM`                         | `0x4530` | Supported          | `_feature_dualplatform`, untested
`MULTIPLATFORM`                        | `0x4531` | Supported          | `_feature_multiplatform`
`KEYBOARD_LAYOUT_2`                    | `0x4540` | Unsupported        | read only
`CROWN`                                | `0x4600` | Supported          |
`TOUCHPAD_FW_ITEMS`                    | `0x6010` | Unsupported        |
`TOUCHPAD_SW_ITEMS`                    | `0x6011` | Unsupported        |
`TOUCHPAD_WIN8_FW_ITEMS`               | `0x6012` | Unsupported        |
`TAP_ENABLE`                           | `0x6020` | Unsupported        |
`TAP_ENABLE_EXTENDED`                  | `0x6021` | Unsupported        |
`CURSOR_BALLISTIC`                     | `0x6030` | Unsupported        |
`TOUCHPAD_RESOLUTION`                  | `0x6040` | Unsupported        |
`TOUCHPAD_RAW_XY`                      | `0x6100` | Unsupported        |
`TOUCHMOUSE_RAW_POINTS`                | `0x6110` | Unsupported        |
`TOUCHMOUSE_6120`                      | `0x6120` | Unsupported        |
`GESTURE`                              | `0x6500` | Unsupported        |
`GESTURE_2`                            | `0x6501` | Partial Support    | `_feature_gesture2_gestures`, `_feature_gesture2_params`
`GKEY`                                 | `0x8010` | Partial Support    |
`MKEYS`                                | `0x8020` | Unsupported        |
`MR`                                   | `0x8030` | Unsupported        |
`BRIGHTNESS_CONTROL`                   | `0x8040` | Unsupported        |
`REPORT_RATE`                          | `0x8060` | Supported          |
`COLOR_LED_EFFECTS`                    | `0x8070` | Unsupported        |
`RGB_EFFECTS`                          | `0X8071` | Unsupported        |
`PER_KEY_LIGHTING`                     | `0x8080` | Unsupported        |
`PER_KEY_LIGHTING_V2`                  | `0x8081` | Unsupported        |
`MODE_STATUS`                          | `0x8090` | Unsupported        |
`ONBOARD_PROFILES`                     | `0x8100` | Unsupported        | in progress
`MOUSE_BUTTON_SPY`                     | `0x8110` | Unsupported        |
`LATENCY_MONITORING`                   | `0x8111` | Unsupported        |
`GAMING_ATTACHMENTS`                   | `0x8120` | Unsupported        |
`FORCE_FEEDBACK`                       | `0x8123` | Unsupported        |
`SIDETONE`                             | `0x8300` | Unsupported        |
`EQUALIZER`                            | `0x8310` | Unsupported        |
`HEADSET_OUT`                          | `0x8320` | Unsupported        |

A “read only” note means the feature is a read-only feature.

## Implementing a feature

Features are implemented as settable features in
lib/logitech_receiver/settings_templates.py
some features also have direct implementation in
lib/logitech_receiver/hidpp20.py

In most cases it should suffice to only implement the settable feature
interface for each setting in the feature.  That will add one or more
widgets in the Solaar main window to show and change the setting,
will permit storing and restoring changed settings, and
will output the feature settings in `solaar show`.

Adding a setting implementation involves several steps, described here and
illustrated by the pointer speed setting implementation.

First add a name, a label, and a description for the setting in the common strings section.
The name is used in the persistent settings structure to store and restore changed settings and
should be a valid Python identifier.  (Some older settings have dashes.)
The label is displayed in the Solaar main window and the description is used as a tooltip there.
The label and description should be specified as translatable strings.

```python
_POINTER_SPEED = ('pointer_speed',
		_("Sensitivity (Pointer Speed)"),
		_("How fast the pointer moves"))
```

Next implement an interface for the setting by creating
a reader/writer, a validator, and a setting instance for it.
Most settings use device features and thus need feature interfaces.
Some settings use device register and thus need register interfaces.
Only implement a register interface for the setting if you are very brave and
you have access to a device that has a register interface for the setting.
Register interfaces cannot be auto-discovered and need to be stated in descriptors.py
for each device with the register interface.

The reader/writer instance is responsible for reading raw values
from the device and writing values to it.
There are different classes for feature interfaces and register interfaces.
Pointer speed is a feature so the _FeatureRW reader/writer is used.
Reader/writers take the register or feature ID and the command numbers for reading and writing,
plus other arguments for complex interfaces.

The validator instance is responsible for turning read raw values into Python data
and Python data into raw values to be written and validating that the Python data is
acceptable for the setting.
There are several possible kinds of Python data for setting interfaces,
ranging from simple toggles, to ranges, to fixed lists, to
dynamic choices, to maps of dynamic choices.
Pointer speed is a setting whose values are integers in a range so a _RangeV validator is used.
The arguments to this class are the
the minimum and maximum values for the value
and the byte size of the value on the device.
Settings that are toggles or choices work similarly,
but their validators have different arguments.
Map settings have more complicated validators.

The setting instance keeps everything together and provides control.
It takes the strings for the setting, the reader/writer, the validator, and
which kinds of devices can have this setting.
(This last is no longer used because keyboards with integrated trackpads only
report that they are keyboards.)

```python
def _feature_pointer_speed():
    """Pointer Speed feature"""
    # min and max values taken from usb traces of Win software
    validator = _RangeV(0x002e, 0x01ff, 2)
    rw = _FeatureRW(_F.POINTER_SPEED)
    return _Setting(_POINTER_SPEED, rw, validator, device_kind=(_DK.mouse, _DK.trackball))
```

Settings where the acceptable values are determined from the device
need an auxiliary function to receive and decipher the permissible choices.
See `_feature_adjustable_dpi_choices` for an example.

Finally, add an element to _SETTINGS_TABLE with
the common strings for the setting,
the feature ID (if any),
the feature implementation (if any),
the register implementation (if any).
and
the identifier for the setting implementation if different from the setting name.
The identifier is used in descriptors.py to say that a device has the register or feature implementation.
This table is used to generate the data structures for describing devices in descriptors.py
and is also used to auto-discover feature implementations.

```python
_S( _POINTER_SPEED, _F.POINTER_SPEED, _feature_pointer_speed ),
```

The values to be used need to be determined from documentation of the
feature or from reverse-engineering behavior of Logitech software under
Windows or MacOS.
For more information on implementing feature settings
see the comments in lib/logitech_receiver/settings_templates.py.
