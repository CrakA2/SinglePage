# Single Page Documentaion - README

A modern, minimalist documentation template perfect for teaching log analysis and technical documentation. Features clean green and white design with powerful syntax highlighting.

## 🚀 Features

- **Modern Minimalist Design**: Clean green and white color scheme
- **Syntax Highlighting**: Powered by Prism.js with support for 200+ languages
- **Bold Text Highlighting**: Special highlighting for important code segments
- **Responsive Design**: Works perfectly on desktop and mobile
- **Easy Content Management**: Simple markdown-based content editing
- **Author Section**: Professional documentation metadata
- **Multiple Alert Types**: Info, success, and warning callouts

## 📋 Quick Start

1. **Download the HTML file** to your computer
2. **Open in any modern web browser** (Chrome, Firefox, Safari, Edge)
3. **Edit the markdown content** in the JavaScript section
4. **Refresh the page** to see your changes

## 🛠️ How to Use

### Basic Setup

1. **Open the HTML file** in your preferred text editor
2. **Locate the markdown content** in the `<script>` section (around line 300)
3. **Replace the sample content** with your own documentation
4. **Save and refresh** in your browser

### Editing Content

The documentation content is stored in the `markdownContent` variable as a template string:

```javascript
const markdownContent = `
# Your Documentation Title

## Your Section
Your content here...
`;
```

### Syntax Highlighting

#### Supported Languages
- **Default**: JSON (when no language is specified)
- **Web**: HTML, CSS, JavaScript, TypeScript
- **Backend**: Python, PHP, Java, C++, C#
- **Database**: SQL, MongoDB
- **Config**: YAML, XML, Bash
- **And 200+ more languages**

#### Usage Examples

**Basic code block (defaults to JSON):**
```
\`\`\`
{
  "name": "example",
  "value": 123
}
\`\`\`
```

**Language-specific code block:**
```
\`\`\`python
def hello_world():
    print("Hello, World!")
\`\`\`
```

**Bold highlighting in code blocks:**
```
\`\`\`javascript
const apiKey = "**your-secret-key**";
console.log("API Key: " + **apiKey**);
\`\`\`
```

Text wrapped in `**text**` will appear with:
- ✅ **Red text color**
- ✅ **Bold font weight**
- ✅ **Yellow background**
- ✅ **Subtle border**

### Customizing Author Information

Update the author section in the HTML:

```html
<div class="author-section">
    <h3>Documentation Details</h3>
    <div class="author-info">
        <span><strong>Author:</strong> Your Name</span>
        <span><strong>Version:</strong> 2.0.0</span>
        <span><strong>Last Updated:</strong> June 2025</span>
    </div>
</div>
```

### Adding Alert Boxes

Use these HTML blocks within your markdown:

```html
<div class="alert alert-info">
<strong>Info:</strong> This is an informational message.
</div>

<div class="alert alert-success">
<strong>Success:</strong> This indicates a successful operation.
</div>

<div class="alert alert-warning">
<strong>Warning:</strong> This is a warning message.
</div>
```

### Creating Tables

Standard markdown tables are supported:

```markdown
| Column 1 | Column 2 | Column 3 |
|----------|----------|----------|
| Data 1   | Data 2   | Data 3   |
| Data 4   | Data 5   | Data 6   |
```

### Adding Images

```markdown
![Alt text](https://example.com/image.jpg)
```

## 🎨 Customization

### Changing Colors

The main color variables are defined in the CSS:

```css
/* Primary green colors */
#48bb78 - Main green
#38a169 - Darker green
#2f855a - Darkest green

/* Background colors */
#ffffff - White background
#f7fafc - Light gray background
```

### Modifying Typography

Font settings are in the body CSS:

```css
body {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
}
```

### Adjusting Layout

The main container width can be modified:

```css
.container {
    max-width: 1000px; /* Change this value */
}
```

## 📦 Bundling JavaScript (Optional)

### Should You Bundle?

**Pros of bundling:**
- ✅ Works offline
- ✅ Faster loading (no external requests)
- ✅ More reliable (no CDN downtime)
- ✅ Better for production use

**Cons of bundling:**
- ❌ Larger file size
- ❌ Manual updates required
- ❌ More complex setup

### How to Bundle

If you want to bundle the JavaScript libraries:

1. **Download the required files:**
   - `marked.min.js` from [marked CDN](https://cdnjs.cloudflare.com/ajax/libs/marked/9.1.2/marked.min.js)
   - `prism-core.min.js` from [Prism CDN](https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/components/prism-core.min.js)
   - `prism-autoloader.min.js` from [Prism CDN](https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/plugins/autoloader/prism-autoloader.min.js)

2. **Create a local folder structure:**
   ```
   your-project/
   ├── index.html
   ├── js/
   │   ├── marked.min.js
   │   ├── prism-core.min.js
   │   └── prism-autoloader.min.js
   └── css/
       └── prism.min.css
   ```

3. **Update the HTML script tags:**
   ```html
   <!-- Replace CDN links with local files -->
   <script src="js/marked.min.js"></script>
   <script src="js/prism-core.min.js"></script>
   <script src="js/prism-autoloader.min.js"></script>
   ```

4. **Update the CSS link:**
   ```html
   <link rel="stylesheet" href="css/prism.min.css">
   ```

5. **Update the autoloader path:**
   ```javascript
   Prism.plugins.autoloader.languages_path = 'js/';
   ```

## 📚 Perfect for Teaching

This template is specifically designed for educational purposes:

### Log Analysis Teaching
- **Bold highlighting** makes it easy to point out important log entries
- **Multiple language support** for different log formats
- **Clean layout** keeps students focused on content
- **Professional appearance** maintains credibility

### Code Documentation
- **Syntax highlighting** improves code readability
- **Responsive design** works on student devices
- **Easy navigation** with proper heading structure
- **Alert boxes** highlight important information

## 🔧 Troubleshooting

### Common Issues

**Bold highlighting not working:**
- Make sure you're using `**text**` format
- Check that JavaScript is enabled
- Refresh the page after making changes

**Syntax highlighting missing:**
- Verify internet connection for CDN resources
- Check browser console for errors
- Ensure language names are correct

**Content not updating:**
- Clear browser cache
- Check for JavaScript errors
- Verify markdown syntax

### Browser Compatibility

- ✅ Chrome 60+
- ✅ Firefox 55+
- ✅ Safari 12+
- ✅ Edge 79+

## 📝 Example Content Structure

```markdown
# Main Title

## Section 1
Introduction text here.

### Subsection 1.1
More detailed information.

\`\`\`python
# Sample code with **highlighted** parts
def process_logs():
    filename = "**access.log**"
    with open(filename, 'r') as file:
        for line in file:
            if "**ERROR**" in line:
                print(line)
\`\`\`

<div class="alert alert-warning">
<strong>Important:</strong> Always backup your log files before processing.
</div>
```

## 🤝 Contributing

To improve this template:

1. **Fork or copy** the HTML file
2. **Make your changes**
3. **Test thoroughly** in multiple browsers
4. **Share your improvements**

## 📄 License

This template is free to use for educational and commercial purposes.

### Attributions

- **Prism.js**: Syntax highlighting functionality and styles are powered by [Prism](https://github.com/PrismJS/prism), © 2012-2024 Lea Verou and contributors. Licensed under MIT.
- **Marked.js**: Markdown parsing provided by [Marked](https://github.com/markedjs/marked), © 2011-2024 Christopher Jeffrey. Licensed under MIT.

---

**Happy documenting!** 🎉

---

**Happy documenting!** 🎉