# Kit List

The kit list is the checklist that is displayed on the left-side of the check out view, that reminds users who are checking out equipment to include all of the key components. This list is controlled by the `kit.json` file. This is a simple JSON file that is loaded on page load by the front end.

![](/assets/Kit-UIView.png)

## Format

```json
{
  "Section Title": [
    {
      "Name": "List Item Name",
      "Category": "Category ID"
    }
  ]
}
```

By modifying the `kit.json` file, you can change the section title, List Item names, and their corresponding categories. In regard to the Category, the name entered in the kit file, must match the category ID for the [category](/admin/categories.md). Other than that, the file follows standard JSON formatting.
