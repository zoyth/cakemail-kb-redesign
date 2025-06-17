# Import Custom HTML Templates

## Overview

Importing custom HTML code gives you complete design control and allows you to use professionally coded templates or maintain existing design standards. This guide covers how to import, edit, and optimize HTML templates in Cakemail.

## When to Use Custom HTML

### Ideal Use Cases

**Existing Brand Templates:**
- You have professionally designed HTML templates
- Need to maintain specific design standards
- Require exact brand compliance
- Want to replicate existing marketing materials

**Advanced Design Requirements:**
- Complex layouts not available in standard templates
- Custom animations or interactive elements
- Specific coding standards or frameworks
- Integration with external design systems

**Developer-Created Content:**
- Templates built by your development team
- Third-party designed templates
- Responsive designs with custom breakpoints
- Advanced CSS styling and animations

### Benefits of HTML Import

**Complete Design Control:**
- Exact pixel-perfect designs
- Custom CSS styling capabilities
- Advanced layout possibilities
- Professional template integration

**Brand Consistency:**
- Maintain familiar designs across platforms
- Use existing approved templates
- Ensure regulatory compliance in design
- Preserve investment in custom development

**Advanced Features:**
- Custom responsive behavior
- Interactive elements and animations
- Advanced tracking and analytics integration
- Third-party service integrations

## HTML Import Process

### Step 1: Prepare Your HTML Code

**Code Requirements:**
- **Valid HTML structure** with proper opening/closing tags
- **Inline CSS styling** (external stylesheets may not work)
- **Email-safe CSS properties** (avoid unsupported features)
- **Responsive design** with mobile-friendly breakpoints

**Pre-Import Checklist:**
- ✓ Test HTML in email testing tools
- ✓ Validate code syntax and structure
- ✓ Optimize images and external resources
- ✓ Include fallback options for advanced features

### Step 2: Import Your Code

**Import Process:**
1. **Create a new campaign** in Cakemail
2. **Select "Start from scratch"** option
3. **Choose "Start with your own code"**
4. **Paste your HTML code** in the black code editor area
5. **Click "Upload and Edit"** to process the import

**What Happens During Import:**
- Cakemail processes your HTML structure
- Code is optimized for email client compatibility
- Content blocks are identified for editing
- Responsive elements are preserved

### Step 3: Edit and Customize

**Available Editing Options:**
- **HTML Editor**: Direct code editing for advanced users
- **Email Designer**: Visual editing of imported content
- **Hybrid approach**: Switch between code and visual editing

**Editing Capabilities:**
- Modify text content within HTML blocks
- Replace images with new uploads
- Adjust colors and styling
- Add or remove content sections

## HTML Template Best Practices

### Email-Safe HTML Structure

**Basic Template Structure:**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Email Title</title>
</head>
<body style="margin: 0; padding: 0;">
    <table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%">
        <!-- Email content here -->
    </table>
</body>
</html>
```

**Key HTML Principles:**
- **Table-based layouts**: Most reliable across email clients
- **Inline CSS**: Embedded styles for maximum compatibility
- **Absolute URLs**: Use full URLs for images and links
- **Alt text**: Include descriptive text for all images

### CSS Guidelines for Email

**Safe CSS Properties:**
- **Typography**: font-family, font-size, color, text-align
- **Spacing**: margin, padding, line-height
- **Background**: background-color, background-image
- **Borders**: border, border-radius (limited support)

**CSS to Avoid:**
- **External stylesheets**: Link to external CSS files
- **Advanced selectors**: Complex CSS selectors
- **Flexbox/Grid**: Modern layout methods
- **Media queries**: Limited and inconsistent support

**Inline Styling Example:**
```html
<td style="font-family: Arial, sans-serif; font-size: 16px; color: #333333; padding: 20px;">
    Your content here
</td>
```

### Responsive Design Considerations

**Mobile-First Approach:**
- Design for mobile screens first
- Use scalable layouts and flexible widths
- Ensure touch-friendly button sizes (minimum 44px)
- Test across different screen sizes

**Media Query Support:**
```html
<style type="text/css">
    @media only screen and (max-width: 600px) {
        .mobile-hide { display: none !important; }
        .mobile-stack { width: 100% !important; display: block !important; }
    }
</style>
```

**Responsive Techniques:**
- **Fluid tables**: Use percentage widths
- **Conditional content**: Hide/show elements on mobile
- **Scalable images**: Max-width: 100% for images
- **Stacked layouts**: Single column on mobile devices

## Working with the HTML Editor

### Interface Overview

**Code Editor Features:**
- **Syntax highlighting**: Makes code easier to read
- **Line numbering**: Navigate large templates easily
- **Auto-indentation**: Maintains clean code structure
- **Error detection**: Basic HTML validation

**Editing Workflow:**
1. **Import your template** using the custom code option
2. **Switch to HTML Editor** for direct code access
3. **Make necessary changes** to content and styling
4. **Preview frequently** to check rendering
5. **Test across email clients** before sending

### Common HTML Modifications

**Content Updates:**
- **Text changes**: Update headlines, body text, and CTAs
- **Image replacements**: Swap src attributes for new images
- **Link updates**: Modify href attributes for buttons and links
- **Color adjustments**: Change color values in style attributes

**Structural Changes:**
- **Add new sections**: Insert additional table rows/cells
- **Remove content blocks**: Delete unnecessary elements
- **Reorder elements**: Move sections within the template
- **Adjust spacing**: Modify padding and margin values

### Advanced HTML Features

**Custom Merge Tags:**
```html
<p>Hello [FirstName,Friend],</p>
<p>Your account expires on [ExpirationDate,Soon].</p>
```

**Conditional Content:**
```html
<!--[if gte mso 9]>
<table><tr><td>
<![endif]-->
    Content for Outlook
<!--[if gte mso 9]>
</td></tr></table>
<![endif]-->
```

**Tracking Integration:**
```html
<a href="https://example.com/track?utm_source=email&utm_campaign=newsletter">
    <img src="https://example.com/pixel.gif" width="1" height="1" alt="">
</a>
```

## Testing and Validation

### Pre-Send Testing

**Email Client Testing:**
- **Gmail**: Desktop and mobile apps
- **Outlook**: Various versions (2016, 2019, 365)
- **Apple Mail**: iOS and macOS versions
- **Yahoo/AOL**: Webmail interfaces

**Validation Tools:**
- **HTML validators**: Check for syntax errors
- **CSS validators**: Ensure compatible styling
- **Email testing services**: Litmus, Email on Acid
- **Spam checkers**: Test deliverability factors

### Common Issues and Solutions

**Rendering Problems:**
- **Broken layouts**: Check table structure and cell widths
- **Font issues**: Use web-safe font stacks with fallbacks
- **Image problems**: Verify image URLs and alt text
- **Color variations**: Test across different email clients

**Mobile Display Issues:**
- **Text too small**: Increase font sizes for mobile
- **Layout breaks**: Simplify complex table structures
- **Buttons too small**: Ensure minimum 44px touch targets
- **Content overflow**: Use responsive width techniques

**Deliverability Concerns:**
- **Spam filtering**: Balance images with text content
- **Code bloat**: Remove unnecessary CSS and HTML
- **Invalid markup**: Fix HTML validation errors
- **Missing alt text**: Add descriptive image alternatives

## Advanced Integration Techniques

### Dynamic Content Integration

**Merge Tag Implementation:**
- **Personalization fields**: [FirstName], [LastName], [Email]
- **Custom attributes**: [CompanyName], [PurchaseDate]
- **Fallback values**: [FirstName,Friend] for missing data
- **System fields**: [UnsubscribeLink], [Date], [Time]

**Conditional Display:**
```html
<div data-condition="segment:premium-members">
    <!-- Content only for premium members -->
</div>
```

### External Service Integration

**Analytics Tracking:**
- **UTM parameters**: Campaign tracking in URLs
- **Pixel tracking**: 1x1 transparent tracking images
- **Custom tracking**: Integration with analytics platforms
- **Conversion tracking**: Goal completion measurement

**Third-Party Integrations:**
- **Social media**: Share buttons and follow links
- **E-commerce**: Product catalogs and purchase buttons
- **CRM systems**: Lead tracking and customer data
- **Survey tools**: Embedded feedback forms

## Maintenance and Updates

### Template Management

**Version Control:**
- **Save working versions** before major changes
- **Document modifications** for team reference
- **Test updates thoroughly** before deployment
- **Maintain backup copies** of successful templates

**Performance Optimization:**
- **Minimize code size** by removing unnecessary elements
- **Optimize images** for web delivery
- **Clean up CSS** by removing unused styles
- **Reduce HTTP requests** by minimizing external resources

### Future-Proofing

**Stay Updated:**
- **Monitor email client updates** that affect rendering
- **Test new features** as they become available
- **Update deprecated code** to maintain compatibility
- **Follow email development best practices**

**Accessibility Compliance:**
- **Alt text for images** for screen reader users
- **Proper heading structure** for navigation
- **Sufficient color contrast** for readability
- **Semantic HTML markup** for better interpretation

Importing custom HTML templates provides maximum flexibility and control over your email designs. With proper preparation, testing, and maintenance, you can create sophisticated, professional emails that perfectly represent your brand while ensuring reliable delivery and display across all email clients.
