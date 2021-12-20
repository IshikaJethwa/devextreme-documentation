---
id: dxTagBox.Options.onSelectionChanged
type: function(e)
default: null
---
---
##### shortDescription
A function that is executed when a list item is selected or selection is canceled.

##### param(e): Object
Information about the event.

##### field(e.addedItems): Array<String, Number, Object>
The data of the items that have been selected.

##### field(e.component): dxTagBox
The UI component's instance.

##### field(e.element): DxElement
#include common-ref-elementparam with { element: "UI component" }

##### field(e.model): any
Model data. Available only if Knockout is used.

##### field(e.removedItems): Array<String, Number, Object>
The data of the items whose selection has been canceled.

---

[note] When [applyValueMode](/api-reference/10%20UI%20Components/dxTagBox/1%20Configuration/applyValueMode.md '{basewidgetpath}/Configuration/#applyValueMode') is *"useButtons"*, the **onSelectionChanged** handler is executed only when users click the OK button.