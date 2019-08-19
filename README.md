# Annotated Notes plugin for Craft CMS 3.x

Field for multiple notes with automatic annotation

## Requirements

This plugin requires Craft CMS 3.0.0-beta.23 or later.

## Annotated Notes Overview

Annotated Notes is a varient of the [Table](https://docs.craftcms.com/v3/table-fields.html#settings) fieldtype, where the table has two columns:
 - **Note**, a text field (handle: `note`)
 - **Annotation** a non-editable text field whose content is generated by twig (handle: `annotation`)

## Configuring Annotated Notes

When you create an Annotated Notes field, you specify the twig code which will be parsed after the element is saved to generate the content for the annotations.

You can also (under Advanced) specify the user visible labels for the `note` and `annotation` columns (the handles are not changed).

## Using Annotated Notes

An Annotated Notes field behaves like a
[Table](https://docs.craftcms.com/v3/table-fields.html#settings) field.
It has two columns, `Note` and `Annotation`.
When you save an Element with an `Annotated Notes`
field, any rows which have a `Note` but no `Annotation`,
will have the `Annotation` set to the value of the
parsed twig. When you edit an Element with an `Annotated Notes`
field, the `Notes` can be modified, but the `Annotation`s
are not editable.

On the front end, the field behaves like any other
[Table](https://docs.craftcms.com/v3/table-fields.html#settings)
field. The handles for the columns are `note` and `annotation`.

Brought to you by [Marion Newlevant](http://marion.newlevant.com)
Many thanks to André Elvan, whose [Preparse Field](https://plugins.craftcms.com/preparse-field) was a major influence.
