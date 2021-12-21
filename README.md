
# Sonar Blob Background

This a modern animated background component that takes advantage of gradients to create an aesthetically pleasing look.


## Tech Stack

**Client:** HTML and CSS


## Accessibility

Individuals with **Vestibular Disorder** might react negatively to the movement of objects on the screen. Features such as animations and transitions of big objects on a web page will trigger dizzness and vertigo.

```bash 
Vestibular disorders can cause your vestibular system to struggle to make sense of what is happening, resulting in loss of balance and vertigo, migraines, nausea, and hearing loss. ``
```

**Solution**

I adopted the use of **Reduced Motion Media Query** to automatically serve animations and transitions to Individuals that require such effect.

```bash
@media (prefers-reduced-motion: reduce) {
  html:focus-within {
    scroll-behavior: auto;
  }
  *,
  *::before,
  *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
    scroll-behavior: auto !important;
  }
}
``` 

