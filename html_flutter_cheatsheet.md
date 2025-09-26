# HTML to Flutter Cheat Sheet

| HTML Tag | Flutter Widget | Example | Notes |
|----------|----------------|---------|-------|
| `<h1>` - `<h6>` | `Text` | `Text('Heading', style: TextStyle(fontSize: 32))` | Adjust `fontSize` & `fontWeight`. |
| `<p>` | `Text` | `Text('Paragraph text')` | Add padding with `Padding` widget. |
| `<span>` | `Text` / `RichText` | `Text('Inline text')` | Use `TextSpan` for multiple styles inline. |
| `<strong>` / `<b>` | `Text` | `Text('Bold', style: TextStyle(fontWeight: FontWeight.bold))` | Bold text. |
| `<em>` / `<i>` | `Text` | `Text('Italic', style: TextStyle(fontStyle: FontStyle.italic))` | Italic text. |
| `<a>` | `InkWell` / `GestureDetector` | `InkWell(onTap: () {}, child: Text('Link'))` | Clickable link. |
| `<nav>` | `Drawer` / `BottomNavigationBar` | `Drawer(child: ListView(...))` | Page navigation. |
| `<input type="text">` | `TextField()` | `TextField(decoration: InputDecoration(labelText: 'Name'))` | Single-line text. |
| `<input type="password">` | `TextField(obscureText: true)` | `TextField(obscureText: true)` | Hide text input. |
| `<textarea>` | `TextField(maxLines: 5)` | Multi-line text. | `maxLines` controls height. |
| `<label>` | `Text` | `Column(children: [Text('Name'), TextField()])` | Place label above input. |
| `<button>` | `ElevatedButton` / `TextButton` | `ElevatedButton(onPressed: () {}, child: Text('Click'))` | Buttons with different styles. |
| `<select>` | `DropdownButton` | `DropdownButton(items: [...], onChanged: ...)` | Dropdown menu. |
| `<input type="checkbox">` | `Checkbox` | `Checkbox(value: true, onChanged: ...)` | Checkboxes. |
| `<input type="radio">` | `Radio` | `Radio(value: 1, groupValue: selected, onChanged: ...)` | Radio buttons. |
| `<form>` | `Form` | `Form(key: _formKey, child: Column(...))` | Wraps multiple inputs. |
| `<ul>` | `Column` + bullets | `Column(children: [Text('• Item1'), Text('• Item2')])` | Manual bullets. |
| `<ol>` | `Column` + numbers | `Column(children: [Text('1. Item1'), Text('2. Item2')])` | Manual numbering. |
| `<li>` | `Text` | Inside Column | Each list item is a child widget. |
| `<table>` | `Table` | `Table(children: [TableRow(children: [Text('A'), Text('B')])])` | Rows & cells. |
| `<tr>` | `TableRow` | Inside `Table` | Each row of the table. |
| `<td>` / `<th>` | Children of `TableRow` | `Text('Cell')` | `<th>` can use bold style. |
| `<thead>` / `<tbody>` | `DataTable` | `DataTable(columns: [...], rows: [...])` | With headers, sorting. |
| `<img>` | `Image.asset` / `Image.network` | `Image.network('url')` | Images. |
| `<video>` | `VideoPlayer` (package) | `VideoPlayerController.network('url')` | Needs plugin. |
| `<audio>` | `AudioPlayer` (package) | `AudioPlayer().setUrl('url')` | Needs plugin. |
| `<div>` | `Container` | `Container(padding: EdgeInsets.all(8), child: Text('Box'))` | Generic container. |
| `<section>` | `Container` / `Column` | Group widgets | Semantic. |
| `<article>` | `Card` / `Container` | `Card(child: Column(...))` | Article block. |
| `<header>` | `AppBar` / `Container` | `AppBar(title: Text('Header'))` | Page header. |
| `<footer>` | `BottomAppBar` / `Container` | `BottomAppBar(child: Text('Footer'))` | Page footer. |
| `<hr>` | `Divider()` | `Divider(thickness: 2)` | Horizontal line. |
| `<br>` | `SizedBox(height: 8)` | `SizedBox(height: 8)` | Line break / spacing. |
| `<iframe>` | `WebView` (plugin) | `WebView(initialUrl: 'https://...')` | Embedded web content. |
| `<div style="display:flex">` | `Row` / `Column` | `Row(children: [...])` | Flex layout. |
| `<div style="display:grid">` | `GridView` / `Wrap` | `GridView.count(crossAxisCount: 2, children: [...])` | Grid layout.
