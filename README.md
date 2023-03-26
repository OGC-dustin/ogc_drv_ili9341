# OGC.Engineering
## ogc_drv_ili9341 - ILI9341 TFT Driver
Developer contact - dustin < at > ogc.engineering

---

* 16 bit RGB565 color format with 16 predefined VGA colors
* Structure provided to track display ( in the case multiple displays are used )
    - ID ( Unique ID to identify this display from others )
    - Resolution ( width, height )
    - Orientation ( landscape, portrait, landscape_flipped, portrait_flipped )
    - Pointer to interaction functions:
        - initialization
        - primitives
* Initialization function:
    TBD: default config options and overrides useful in deployment header
* Primative draw functions:
    - Dot
    - Rectangle
    - Line
    - Circle
    - Ellipse

---
Requirements:

---
- the HAL layer(folder) must define:
    - uint64_t hal_get_sys_tick( void );
        - a 64 bit unsigned monotonic clock must be avialable for calculating delays ( typically millisecond resolution )