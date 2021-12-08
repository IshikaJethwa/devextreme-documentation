Default templates are based on data source fields. You can control appearance by adding or removing particular fields from data source objects. For example, the **List** widget has a [default template for items](/api-reference/10%20UI%20Widgets/dxList/5%20Default%20Item%20Template '/Documentation/ApiReference/UI_Widgets/dxList/Default_Item_Template/') that contains the **text**, **visible**, and **disabled** fields. If you assign the following array to the widget's **dataSource** option, the first item will be disabled, the second hidden, both of them will have text, and the third item will render a custom markup:

    <!--JavaScript-->
    function customMarkup() {
        var d = document.createElement("div");
        d.innerHTML = "<i>Oranges</i>";
        return d;
    }
    var fruits = [
        { text: "Apples", disabled: true },
        { text: "Lemons", visible: false },
        { template: customMarkup }
    ];

You can achieve the same in the markup using the [dxItem](/api-reference/10%20UI%20Widgets/Markup%20Components/dxItem '/Documentation/ApiReference/UI_Widgets/Markup_Components/dxItem/') component that supports default and [custom templates](/Documentation/Guide/Widgets/Common/Templates/#In_Collection_Widgets). Do not set the widget's **dataSource** option in this case. 

---
#####jQuery  

    <!--HTML-->
    <div id="list">
        <div data-options="dxItem: { text: 'Apples', disabled: true }"></div>
        <div data-options="dxItem: { text: 'Lemons', visible: false }"></div>
        <div data-options="dxItem: { }">
            <i>Oranges</i>
        </div>
    </div>

    <!--JavaScript-->
    $(function() {
        $("#list").dxList({/* ... */});
    });

#####Angular

    <!-- tab: app.component.html -->
    <dx-list>
        <dxi-item text="Apples" [disabled]="true"></dxi-item>
        <dxi-item text="Lemons" [visible]="false"></dxi-item>
        <dxi-item>
            <i>Oranges</i>
        </dxi-item>
    </dx-list>

    <!-- tab: app.module.ts -->
    import { DxListModule } from "devextreme-angular";
    // ...
    @NgModule({
        imports: [
            // ...
            DxListModule
        ],
        // ...
    })
    export class AppModule { }

#####AngularJS

    <!--HTML-->
    <div dx-list="{ }">
        <div data-options="dxItem: { text: 'Apples', disabled: true }"></div>
        <div data-options="dxItem: { text: 'Lemons', visible: false }"></div>
        <div data-options="dxItem: { }">
            <i>Oranges</i>
        </div>
    </div>

    <!--JavaScript-->
    angular.module('DemoApp', ['dx'])
        .controller('DemoController', function ($scope) {
            // ...
        });

#####Knockout

    <!--HTML-->
    <div data-bind="dxList: { ... }">
        <div data-options="dxItem: { text: 'Apples', disabled: true }"></div>
        <div data-options="dxItem: { text: 'Lemons', visible: false }"></div>
        <div data-options="dxItem: { }">
            <i>Oranges</i>
        </div>
    </div>

    <!--JavaScript-->
    var viewModel = {
        // ...
    };

    ko.applyBindings(viewModel);

#####React

    <!-- tab: DxComponent.js -->
    import React from 'react';
    import List, { Item } from 'devextreme-react/list';

    class DxComponent extends React.Component {
        render() {
            return (
                <List>
                    <Item text="Apples" disabled={true} />
                    <Item text="Oranges" visible={false} />
                    <Item>
                        <i>Oranges</i>
                    </Item>
                </List>
            );
        }
    }
    export default DxComponent;

---

Default templates and the fields available in them depend on the widget. For a list of default templates for a widget, search for "default template" in the left menu.