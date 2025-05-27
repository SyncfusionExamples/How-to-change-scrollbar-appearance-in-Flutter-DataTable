# How to change scrollbar appearance in Flutter DataTable (SfDataGrid)?

In this article, we will show how to change scrollbar appearance in [Flutter DataTable](https://www.syncfusion.com/flutter-widgets/flutter-datagrid).

Initialize the [SfDataGrid](https://pub.dev/documentation/syncfusion_flutter_datagrid/latest/datagrid/SfDataGrid-class.html) widget with the necessary properties. Wrap the SfDataGrid with a [ScrollbarTheme](https://api.flutter.dev/flutter/material/ScrollbarTheme-class.html) widget to customize its scrollbar appearance. By using [ScrollbarThemeData](https://api.flutter.dev/flutter/material/ScrollbarThemeData-class.html), you can modify the scrollbar's appearance through the available properties.

```dart
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(title: const Text('Syncfusion Flutter DataGrid')),
      body: ScrollbarTheme(
        data: ScrollbarThemeData(
          // scrollbar color
          thumbColor: WidgetStatePropertyAll(Colors.red), 
        ),
        child: SfDataGrid(
          source: employeeDataSource,
          columnWidthMode: ColumnWidthMode.fill,
          columns: <GridColumn>[
            GridColumn(
              columnName: 'id',
              label: Container(
                padding: EdgeInsets.all(16.0),
                alignment: Alignment.center,
                child: Text('ID'),
              ),
            ),
            GridColumn(
              columnName: 'name',
              label: Container(
                padding: EdgeInsets.all(8.0),
                alignment: Alignment.center,
                child: Text('Name'),
              ),
            ),
            GridColumn(
              columnName: 'designation',
              label: Container(
                padding: EdgeInsets.all(8.0),
                alignment: Alignment.center,
                child: Text('Designation', overflow: TextOverflow.ellipsis),
              ),
            ),
            GridColumn(
              columnName: 'salary',
              label: Container(
                padding: EdgeInsets.all(8.0),
                alignment: Alignment.center,
                child: Text('Salary'),
              ),
            ),
          ],
        ),
      ),
    );
  }
```

You can download this example on [GitHub](https://github.com/SyncfusionExamples/How-to-change-scrollbar-appearance-in-Flutter-DataTable).