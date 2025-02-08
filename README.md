# PHP Header/Footer Implementation Guide

## Project Structure
```
your-project/
├── includes/
│   ├── header.php
│   ├── footer.php
│   └── settings.php
├── index.php
└── other-pages.php
```

## How to Include Header

1. First, ensure your header file (`header.php`) is in the `includes` directory

2. To include the header in any PHP page, add this line at the top of your file:
```php
<?php include 'includes/header.php'; ?>
```

### Example Implementation

```php
<?php

// Then include the header
include 'includes/header.php';
?>

<!-- Your page content goes here -->

<?php 
// Include footer at the bottom
include 'includes/footer.php'; 
?>
```

## Important Notes

- Make sure all file paths are correct relative to your root directory
- The header file contains the opening `<html>`, `<head>`, and `<body>` tags
- Keep consistent paths across all pages
- Use `require` instead of `include` if the file is absolutely necessary for the page to function

## Troubleshooting

If you encounter the "Failed to include file" error:
1. Check file permissions
2. Verify file paths are correct
3. Ensure PHP has read access to the includes directory

## Usage

1. Keep all common elements in the header/footer files
2. Maintain consistent naming conventions
3. Use relative paths for better portability
4. Consider using constants for base paths in settings.php