# Hamburger at the top

To move the hamburger toggle button from the bottom of the screen to the top — and have it slide along with the sidebar as it opens and closes, while maintaining responsive behavior — insert the following snippet into the `<head>...</head>` section of your `index.html`:

```html
<style>
    /* Move hamburger to the top, following the sidebar's edge (responsive) */
    .sidebar-toggle {
        position: fixed;
        top: 10px;
        left: 300px;
        bottom: unset;
        transition: left 0.3s ease;
        z-index: 9999; /* Ensure it always stays in front of the content.*/
    }

    body.close .sidebar-toggle {
        left: 10px;
    }

    @media screen and (max-width: 768px) {
        .sidebar-toggle {
            top: -11px;
            left: 10px;
        }
        body.close .sidebar-toggle {
            top: 10px;
            left: 300px;
        }
    }
</style>
```

By Daniel Dias Rodrigues<br>
`mon 21 jul 2025 16:36:53 -0300`