# HomeAssistant - SamsungTV Tizen Component

***Key Chaining Patterns***
---------------

**Note:** If SmartThings API was enabled by setting `api_key` and `device_id`, then these codes are also supported: `ST_TV`, `ST_HDMI1`, `ST_HDMI2`, `ST_HDMI3`, etc. which will change the input source faster then key chaining patterns will

Key codes can be chained with the "+" symbol, delays can also be set in milliseconds between the "+" symbols.

This is a list of known and tested key chaining patterns. To see the complete list of known key codes, [check this list](./Key_codes.md)

*Switch to Live TV*
`KEY_EXIT+2000+KEY_TV+KEY_EXIT`

*Switch to first Source in List* (2019 TV)
`KEY_SOURCE+KEY_DOWN+KEY_UP+KEY_LEFT+KEY_LEFT+KEY_LEFT+KEY_ENTER`

*Switch to second Source in List* (2019 TV)
`KEY_SOURCE+KEY_DOWN+KEY_UP+KEY_LEFT+KEY_LEFT+KEY_LEFT+KEY_RIGHT+KEY_ENTER`

*Switch to third Source in List* (2019 TV)
`KEY_SOURCE+KEY_DOWN+KEY_UP+KEY_LEFT+KEY_LEFT+KEY_LEFT+KEY_RIGHT+KEY_RIGHT+KEY_ENTER`

*Switch to forth Source in List* (2019 TV)
`KEY_SOURCE+KEY_DOWN+KEY_UP+KEY_LEFT+KEY_LEFT+KEY_LEFT+KEY_RIGHT+KEY_RIGHT+KEY_RIGHT+KEY_ENTER`

*Switch to first Source in List* (2017 TV)
`KEY_SOURCE+KEY_LEFT+KEY_LEFT+KEY_LEFT+KEY_ENTER`

*Switch to second Source in List* (2017 TV)
`KEY_SOURCE+KEY_LEFT+KEY_LEFT+KEY_LEFT+KEY_RIGHT+KEY_ENTER`

*Switch to third Source in List* (2017 TV)
`KEY_SOURCE+KEY_LEFT+KEY_LEFT+KEY_LEFT+KEY_RIGHT+KEY_RIGHT+KEY_ENTER`

*Switch to forth Source in List* (2017 TV)
`KEY_SOURCE+KEY_LEFT+KEY_LEFT+KEY_LEFT+KEY_RIGHT+KEY_RIGHT+KEY_RIGHT+KEY_ENTER`

