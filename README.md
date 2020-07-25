# Responsive Portfolio
BootCampSpot Web Development - Week 2 Homework

![Preview](https://github.com/BCS-WebDev/Week2-Homework/blob/master/Assets/Portfolio.gif)

## Notes on Bootstrap
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Bootstrap is an open source toolkit for developing
with HTML, CSS, and JavaScript. We will be utilizing its front-end component library
to build a responsive, mobile-friendly website for a portfolio.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Bootstrap's CSS & JS files are available on the
Bootstrap website and have documentation explaining their pre-defined classes and 
features. Most notably for this project, we will be using the grid system which
facilitates the organization of different HTML elements into rows and columns, navbars
that allow different styles and colors for its lists, and spacing syntax to truncate code
used for margins, borders, and paddings, amongst others.

## Motive & Action
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Since this is a project geared towards familiarizing
ourselves with Bootstrap, we will be recreating a layout using only Bootstrap classes
while minimizing the use of custom classes and media queries for different viewports.
The media query will be necessary, however, for static widths due to Bootstrap's
inclination towards responsive widths and also for positioning when the layout shifts.
As the project developed, it was necessary to utilize a media query for the xs viewport
which is categorized as widths less than 576px, but media queries for the sm or md
viewports were not necessary. But even though this was the case, the media query for the
xs viewport was used extremely minimally.

* Design Choices:
    - Header
        - Placed outside & above main container
        - Variable width (fluid-xs) box used for Name
            - Hover Name for spaz animation
        - Variable width (fluid-xs) navbar class used to contain list-group for links
    
    - Main container
        - Container-fluid class limited to max width: 768px (md viewport)
        - No margins or padding, adjusts position via media query at xs viewport
        - Contains Main canvas with margins
            - Main canvas contains row for page header
            - Main canvas contains content section which uses row & columns for respective layouts
                - Needed for text-wrap and image placements
                - Variable width (fluid-xs) for figures & repective images
                - Portfolio content uses columns
                - Contact uses forms in rows

    - Sticky Footer
        - 'Sticky' is different from 'Fixed'
            - 'Fixed' will always show at the bottom of the page regardless of whether
              or not there is more content to be shown and has a higher z-index than the body.
            - 'Sticky' will show at the bottom of the page only if there is no more content
              to be shown. If there is more content to be shown, the content will push the
              footer down to the end of the bottom of the page, not appear on top of the content.
        - To achieve:
            - Html element needs
                - Relative position
                - Minimum height: 100%
            - Body element needs
                - Bottom margin wider than footer height
            - Footer element needs
                - Absolute position
                - Bottom: 0
