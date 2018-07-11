# cob-map

Web component for a Leaflet map and data from Esri. It accepts the configuration
block as an attribute or embedded `<script>` and generates a Leaflet map.

This component typechecks against the [JSON-Schema
files](https://cityofboston.github.io/vizwiz/#/jsonschema) from the vizwiz
repository. To update the types, run `npx gulp schema:vizwiz`. You may also have
to add to the list of URLs in the Gulpfile.

The map can operate in "modal" mode by setting the `modal` attribute. In this
mode, the map is hidden by default and, when shown, appears in a full-screen
modal dialog.

To show or hide the map, you can use the `show()`, `hide()`, `toggle()` methods.
The map will also listen to hash change events and, if its `id` comes up as the
hash, it will automatically appear.

## Slots

#### config

Alternate way to define the JSON configuration from the `config` attribute that
avoids the need to HTML escape and put in the “config” attribute. Include a
`<script slot="config" type="application/json">` element whose text contents are
the JSON configuration. 

<!-- Auto Generated Below -->


## Properties

#### config

string

A JSON string or equivalent object that defines the map and layers. The
schema for this config comes from VizWiz, so it won’t be documented here.

Any attributes prefixed with `map-` will be passed on to the generated
`<cob-map>` component. _E.g._ `map-id` or `map-style`.


#### id

string

ID of the HTML element. Used to automatically open the map modal.


#### modal

boolean

If true, the map starts hidden and, when shown, appears in a full-screen
modal dialog.

Note: On the server, this may be the empty string when true, so we need to
check against `!== false` to test it.


#### modalVisible

boolean

Change to true to make the modal appear.


#### openOverlay

boolean

Test attribute to make the overlay open automatically at mobile widths.
Only used so that we can take Percy screenshots of the overlay.


## Attributes

#### config

string

A JSON string or equivalent object that defines the map and layers. The
schema for this config comes from VizWiz, so it won’t be documented here.

Any attributes prefixed with `map-` will be passed on to the generated
`<cob-map>` component. _E.g._ `map-id` or `map-style`.


#### id

string

ID of the HTML element. Used to automatically open the map modal.


#### modal

boolean

If true, the map starts hidden and, when shown, appears in a full-screen
modal dialog.

Note: On the server, this may be the empty string when true, so we need to
check against `!== false` to test it.


#### modal-visible

boolean

Change to true to make the modal appear.


#### open-overlay

boolean

Test attribute to make the overlay open automatically at mobile widths.
Only used so that we can take Percy screenshots of the overlay.


## Methods

#### hide()

Hides the modal, if the map is in modal mode.


#### show()

Shows the modal, if the map is in modal mode.


#### toggle()

If the map is in modal mode, toggles whether or not it’s visible.



----------------------------------------------

*Built with [StencilJS](https://stenciljs.com/)*