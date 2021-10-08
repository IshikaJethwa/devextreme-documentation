---
id: dxForm.Options.labelMode
acceptValues: 'static' | 'floating' | 'hidden' | 'default'
type: String
default: 'default'
---
---
##### shortDescription
Specifies a display mode for [item labels](/Documentation/ApiReference/UI_Components/dxForm/Item_Types/SimpleItem/label/).

---
#include texteditor-labelMode with {
    outside_mode: '
    <tr>
        <td><i>"outside"</i></td>
        <td>
            The label is displayed outside the editor, and its position depends on the following properties:
            <ul>
                <li><a href="/Documentation/ApiReference/UI_Components/dxForm/Configuration/#labelLocation">labelLocation</a></li>
                <li><a href="/Documentation/ApiReference/UI_Components/dxForm/Item_Types/SimpleItem/label/#location">items[].label.location</a></li>
                <li><a href="/Documentation/ApiReference/UI_Components/dxForm/Configuration/#alignItemLabels">alignItemLabels</a></li>
                <li><a href="/Documentation/ApiReference/UI_Components/dxForm/Configuration/#alignItemLabelsInAllGroups">alignItemLabelsInAllGroups</a></li>
                <li><a href="/Documentation/ApiReference/UI_Components/dxForm/Item_Types/SimpleItem/label/#alignment">items[].label.alignment</a></li>
            </ul>
        </td>
        <td><img src="/images/UiWidgets/texteditor-default-label.png" alt="DevExtreme {WidgetName}: Default label mode" /></td>
    </tr>'
}