# Setup
1. Add reference to the package: `dotnet add package QuickGridColumnResizer`
2. In `index.html` file (Blazor WebAssembly App) or `App.razor` file (Blazor Web App) add following lines:
```
<link rel="stylesheet" href="_content/QuickGridColumnResizer/style.css" />

<script src="_content/QuickGridColumnResizer/script.js"></script>
```

For example:
```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no" />
    <title>My Blazor Project</title>
    <base href="/" />
    <link rel="icon" type="image/png" href="favicon.png" />
    <link rel="stylesheet" href="css/bootstrap/bootstrap.min.css" />
    <link rel="stylesheet" href="css/bootstrap-icons/bootstrap-icons.min.css" />
    <link rel="stylesheet" href="_content/QuickGridColumnResizer/style.css" /> <!-- Add this line -->
    <link rel="stylesheet" href="css/app.css" />
    <link rel="stylesheet" href="MyBlazorProject.styles.css" />
</head>

<body>
    <div id="app">
        <svg class="loading-progress">
            <circle r="40%" cx="50%" cy="50%" />
            <circle r="40%" cx="50%" cy="50%" />
        </svg>
        <div class="loading-progress-text"></div>
    </div>

    <div id="blazor-error-ui">
        An unhandled error has occurred.
        <a href="" class="reload">Reload</a>
        <a class="dismiss">🗙</a>
    </div>
    <script src="_framework/blazor.webassembly.js"></script>
    <script src="_content/QuickGridColumnResizer/script.js"></script> <!-- Add this line -->
</body>

</html>
```

# Custom styling
You can override default styles.
1. If you use global style sheet:
```
table.quickgrid .column-resizer {
    cursor: ew-resize;
    border: none;
    background: transparent;
}
    table.quickgrid .column-resizer::before {
        content: "|";
    }
```
2. If you use isolated style sheet
```
::deep table.quickgrid .column-resizer {
    cursor: ew-resize;
    border: none;
    background: transparent;
}
    ::deep table.quickgrid .column-resizer::before {
        content: "|";
    }
```

## Package icon
[Resize Horizontal](https://icons8.com/icon/56327/resize-horizontal) icon by [Icons8](https://icons8.com)
