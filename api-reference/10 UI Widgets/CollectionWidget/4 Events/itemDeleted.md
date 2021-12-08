---
hidden: 
type: eventType
---
---
##### shortDescription
Raised after a collection item is deleted from the data source.

##### param(e): Object
Information about the event.

##### field(e.component): {WidgetName}
The widget's instance.

##### field(e.element): dxElement
The widget's container. It is an [HTML Element](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement) or a [jQuery Element](https://api.jquery.com/Types/#jQuery) when you use jQuery.

##### field(e.model): Object
The model data. Available only if you use Knockout.

##### field(e.itemData): Object
The removed item's data.

##### field(e.itemElement): dxElement
The item's container. It is an [HTML Element](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement) or a [jQuery Element](https://api.jquery.com/Types/#jQuery) when you use jQuery.

##### field(e.itemIndex): Number | Object
The removed item's index.

---
Main article: [onItemDeleted](/api-reference/10%20UI%20Widgets/CollectionWidget/1%20Configuration/onItemDeleted.md '{basewidgetpath}/Configuration/#onItemDeleted')

#####See Also#####
#include common-link-handleevents