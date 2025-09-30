### Các Section Chính

#### 1. **Header** (`.header`)

- Label "CV" với arrow decoration
- Caption text
- Name heading (H1)
- Job titles list

#### 2. **CV Tools** (`.cv-tool`)

- Print button (desktop only)
- Download button (mobile/tablet)
- Positioned absolute/fixed

#### 3. **Sidebar** (`.cv-info`)

- Avatar image với decorative border
- Contact information
- Skills
- Languages
- Software proficiency
- Other personal info sections

#### 4. **Main Content** (`.cv-main`)

- About Me
- Education
- Work Experience
- Hobbies
- Additional sections

## 🎯 Cấu Trúc SCSS Files

### File Import Order (app.scss)

### Vai Trò Từng File

#### `_variables.scss`

- **Colors**: Định nghĩa color palette
- **Breakpoints**: Responsive breakpoints (map)
- **Sizes**: aside-width, avatar-width (maps)
- **Z-index**: Layer management

#### `_mixins.scss`

- `flex-ct`: Flexbox center
- `flex-ct-c`: Flexbox center column
- `abs-ct`: Absolute center positioning
- `square($edge)`: Square dimensions
- `aside-w($size)`: Get aside width from map
- `avatar-w($size)`: Get avatar width from map
- `max-screen($breakpoint)`: Media query mixin

#### `_global.scss`

- CSS Reset (padding, margin, box-sizing)
- Base typography (font-size, font-family)
- Default element styles (ul, img, a, button)

#### `_layout.scss`

- `.wrapper`: Max-width container (1440px)
- `.container`: Content container (1024px)
- Responsive padding

#### `_header.scss`

- Header background image
- Name và job titles styling
- Label với arrow decoration (pseudo-elements)
- Responsive adjustments

#### `_aside.scss`

- Sidebar layout và colors
- Avatar với decorative effects
- Info sections styling
- Contact items layout
- Skills, languages, software lists
- Separator decorations

#### `_main-profile.scss`

- Main layout (flexbox 25%/75%)
- Responsive breakpoints:
    - Desktop: 25% sidebar
    - Tablet: 30% sidebar
    - Mobile: Full-width với toggle menu
- Mobile toggle functionality
- Hamburger animation
- Overlay effects

#### `_tools.scss`

- Print/Download buttons
- Hover effects
- Responsive visibility (show/hide based on screen size)

#### `_print.scss`

- `@page` settings (A4 size)
- Color adjustment for printing
- Unit conversions (px → mm)
- Hide interactive elements

## 📱 Responsive Breakpoints

### Behavior per Breakpoint

- **Desktop (> 1024px)**
    - Sidebar: 25% width
    - Tools: Fixed position với label
    - Print button visible

- **Tablet (650px - 1024px)**
    - Sidebar: 30% width
    - Tools: Fixed bottom-right
    - Download button only

- **Mobile (< 650px)**
    - Sidebar: Slide-in menu từ trái
    - Hamburger menu button
    - Full-width content
    - Overlay backdrop khi menu open