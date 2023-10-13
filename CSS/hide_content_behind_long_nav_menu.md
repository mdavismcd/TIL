# Hide Content Behind a Long Navigation Menu Drop-down

I added the [Mapping module](https://omeka.org/s/modules/Mapping/) to an Omeka S page for a [campus building](https://digitalprojects.davidson.edu/omeka/s/encyclopedia/page/belk-katherine-and-tom-visual-arts-center). The map block was overlaying/hiding the navigation drop-down. Some simple CSS fixed the issue:

```
.mapping-block
{
position: relative;
z-index: 0;
```

Thanks to John Flatness from the Omeka S Team
[source](https://forum.omeka.org/t/mapping-module-hiding-navigation-menu-pages/14138)