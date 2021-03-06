---
tags:
summary: 
---

# Responsive Table UI Pattern Reference
## Layout and Classes

![](<images/responsivetable-image-4.png>)


## CSS Selectors

| **Element** |  **CSS Class** |  **Description**  |
| ---|---|---
| .table-records-responsive |  .table-records-responsive.scrollable-row|  When the ResponsiveBehavior parameter is set to scrollable  |
| .table-records-responsive |  .table-records-responsive.expandable-row|  When the ResponsiveBehavior parameter is set to expandable  |
| table tbody tr |  .TableRecords_ExpandedRow |  When using the expandable-row option, identifies when the the row is expanded  |


## Advanced Use Case

### Change Responsive Behavior parameter according to device

1. Drag the ResponsiveTable Pattern into the page.

1.  Set the ResponsiveBehaviour parameter to `If(IsPhone(), Entities.ResponsiveTableRecords.ExpandableRows, Entities.ResponsiveTableRecords.ScrollabeRows)`. 

    We use the server action IsPhone as the condition to set the property for phone devices. You can also use the IsTablet action, or invert the False & True statements as required.

1. Publish and test.

### Change expandable-row's arrow color

To implement this, you can use either method described below.

1. Write the following CSS in the CSS editor and change `yourcolor` accordingly.

```css
.tablet.portrait .expandable-row .TableRecords tbody tr td:first-child:after, 
.phone .expandable-row .TableRecords tbody tr td:first-child:after {
    color: yourcolor;
}
```

2. Use CSS variables like `var(--color-yourcolor)`.

```css
.tablet.portrait .expandable-row .TableRecords tbody tr td:first-child:after, 
.phone .expandable-row .TableRecords tbody tr td:first-child:after {
    color: var(--color-yourcolor);
}
```


 ## See Also

* OutSystems UI Pattern Documentation: [Responsive Table](https://success.outsystems.com/Documentation/11/Developing_an_Application/Design_UI/Patterns/Using_Web_Patterns/Responsive/ResponsiveTable)

