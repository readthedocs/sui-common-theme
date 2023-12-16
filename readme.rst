Read the Docs SUI common theme
==============================

This is a SemanticUI/FomanticUI theme that contains shared configuration and
styles between our website and our application. Common configuration, colors,
and styles all live here, and then both our application and website both load a
secondary theme in addition.

Using this theme
----------------

Since FUI 2.9.3, multiple inheritance of themes become difficult. For now, this
theme should be configured for each element/module/etc in theme.config:

    ...
    @button: "rtd-common";
    ...

The Webpack and the rest of the respective `theme.config` files will load this
theme as the primary theme, and use the `rtd-site` and `rtd-application` themes
via `siteFolder`. This is actually fairly correct usage, though the original
idea was to load multiple layers of themes.
