# UnBix Website Design

## Overview
- **Motion Style**: Cybernetic Fluidity with Kinetic Typography
- **Animation Intensity**: Ultra-Dynamic
- **Technology Stack**: WebGL (Three.js), GSAP (ScrollTrigger, Flip), CSS Houdini
- **Visual Theme**: "Controlled Chaos" – glitch-inspired transitions meeting smooth, liquid physics

## Brand Foundation
- **Colors**: 
  - Primary Body: #0e0e0e
  - Primary Text: #ffffff
  - Border: #292929, #1f1f1f
  - Accents: #ff4d4d (Red), #ff7b00 (Orange), #ffd700 (Yellow), #00ff00 (Green), #00ffff (Cyan)
- **Typography**: 
  - **Display:** "Clashgrotesk" (500/600)
  - **Body:** "Inter" (400/500)
  - **Accent:** "IBM Plex Mono" (400/500)
- **Core Message**: "AI-Powered Growth" communicated through a lens of high-tech precision.

## Global Motion System

### Animation Timing
- **Easing Library**: 
  - *Cyber-Snap*: `cubic-bezier(0.16, 1, 0.3, 1)` (Entrances)
  - *Data-Flow*: `cubic-bezier(0.65, 0, 0.35, 1)` (Transitions)
- **Duration Scale**: 
  - Micro: 200ms (Hover)
  - Macro: 800ms (Section transitions)
- **Stagger Patterns**: 0.05s per letter for text, 0.1s per grid item

### Continuous Effects
- **Living Textures**: Subtle "digital noise" grain overlay (opacity: 0.03) fixed over entire viewport.
- **Cursor System**: Custom "Data Lens" cursor – a ring that magnetically snaps to interactive elements, expanding into a "reticle" shape on hover.
- **Scroll Physics**: Momentum-based scrolling with velocity skew (content tilts slightly during fast scrolls).

## Section 1: Hero

### Layout
**"The Holographic Stage"**
A revolutionary 2.5D composition where the interface elements float in a layered 3D space. The traditional center alignment is exploded into depth.
- **Z-Layer 1 (Deep Background)**: WebGL "Neural Mesh" shader (dark wireframe on black).
- **Z-Layer 2 (Mid-Ground)**: Main Headline and CTA, floating with parallax.
- **Z-Layer 3 (Foreground)**: The Hero Image, detached from the grid, floating with mouse-reactive gyroscope effect.

### Content
- **Headline**: "UnBix AI Academy" (Split into two lines, massive scale)
- **Subtext**: "Master AI Automation & n8n Workflows"
- **CTA**: "Enroll Now"

### Images
**Hero Image (Main Illustration)**
- **Resolution:** Vector-based (scalable)
- **Aspect Ratio:** Flexible (approx 16:9)
- **Transparent Background:** Yes
- **Visual Style:** Flat vector illustration, minimalistic, clean lines
- **Subject:** Three young adults (two male, one female) standing together, smiling, friendly and welcoming mood.
- **Color Palette:** Bright blue (#4A90E2), yellow (#FFD700), orange (#FF7B00), red (#FF4D4D)
- **Generation Prompt:** "Flat vector illustration of three friendly young adults standing together, smiling. One woman with long dark hair, one man with beard and glasses, one man with short hair. Wearing casual colorful t-shirts (blue, yellow, orange, red). Clean white background. Minimalistic style with smooth curves, no outlines. Cheerful and welcoming mood. Modern and professional look."

### Motion Choreography

#### Entrance Sequence
| Element | Animation | Values | Duration | Delay | Easing |
|---------|-----------|--------|----------|-------|--------|
| Headline | 3D Text Reveal | RotateX(90deg) → 0, Y(50px) → 0 | 1.2s | 0.2s | Expo.out |
| Hero Image | Levitation Rise | Y(100%) → 0, Scale(0.8) → 1 | 1.4s | 0.4s | Elastic.out |
| Background | Shader Bloom | Brightness(0) → 1 | 2.0s | 0s | Linear |

#### Scroll Effects
- **Parallax Depth**: The Hero Image moves at 0.5x scroll speed, while text moves at 1x.
- **Blur Fade**: As user scrolls down, the hero section blurs `filter: blur(10px)` and scales down `transform: scale(0.95)`.

#### Interaction Effects
- **Magnetic Text**: The headline letters repel the cursor slightly (liquid effect).
- **Gyroscope Tilt**: On mobile/tablet, tilting the device shifts the perspective of the floating hero image.

### Advanced Effects
- **Shader Background**: A "Dark Energy" wireframe shader that undulates slowly. It reacts to scroll velocity (turbulence increases with speed).
- **Chromatic Aberration**: On rapid scroll, the edges of the Hero Image split into RGB channels.

## Section 2: Floating Stats

### Layout
**"The Data Stream"**
Breaking the grid completely. The stats are not in a row, but "floating" in a diagonal stream that crosses the viewport.
- **Composition**: Asymmetric scatter. Stat 1 (Top Left), Stat 2 (Center), Stat 3 (Bottom Right).
- **Connection**: A faint, pulsing SVG line connects the three stats, drawing itself as you scroll.

### Content
- **Stat 1**: "3000+ Students"
- **Stat 2**: "Active Community"
- **Stat 3**: "Live Support"

### Motion Choreography
- **Scroll Trigger**: The "Data Stream" pins for 500px of scroll, during which the numbers count up (0 -> 3000) with a "slot machine" rolling effect.
- **Hover**: Hovering a stat causes the number to "glitch" (random numbers flashing rapidly before settling back).

## Section 3: AI Interface (Orion)

### Layout
**"The Kinetic Terminal"**
A full-width immersive dark zone. Instead of a standard chat box, the interface is a "Command Line" aesthetic.
- **Structure**: Large, monospaced input field at the top.
- **Output**: Chat history reveals downwards, but with a "terminal print" effect (text appears character by character).

### Content
- **Title**: "Orion AI by UnBix"
- **Prompts**: Buttons for "What will I learn?", "Pricing?", "Support?"

### Images
**Orion AI Avatar**
- **Resolution:** Vector-based
- **Aspect Ratio:** 1:1 (circular)
- **Transparent Background:** Yes (inside circular frame)
- **Visual Style:** Flat vector illustration with gradient background
- **Subject:** Young man with short black hair, smiling, wearing red-orange shirt.
- **Color Palette:** Red-Orange (#FF6B35), Teal gradient background.
- **Generation Prompt:** "Flat vector illustration of a friendly young man with short black hair, smiling, wearing red-orange shirt. Circular frame with teal to light blue gradient background. Minimalistic modern style, no outlines, soft shadows. Cheerful and welcoming mood."

### Motion Choreography
- **Focus Mode**: When the user clicks the input field, the rest of the page dims (opacity 0.3), focusing entirely on the terminal.
- **Waveform**: While the AI "types", a dynamic soundwave-style animation pulses next to the avatar.

## Section 4: The Curriculum (Modules)

### Layout
**"The Hexagonal Grid"**
Abandoning the standard 3-column grid.
- **Structure**: A honeycomb-inspired layout where cards are offset in a masonry-style pattern.
- **Perspective**: The entire grid is tilted slightly on the X-axis (rotateX(5deg)) initially, straightening up as you scroll into view.

### Content
- 9 Module Cards (n8n Basics, AI Agents, RAG, etc.)

### Motion Choreography
- **Entrance**: Cards fly in from random Z-depths (some from far back, some from close) to assemble the grid.
- **Hover (The "Hologram" Effect)**: 
  - The hovered card scales up (1.05x).
  - The *border* of the card glows and traces around the edge.
  - The title of the card performs a "text-shadow cascade" (multiple colored shadows trailing behind the text).

## Section 5: Instructor & Testimonials

### Layout
**"The Split-Screen Reveal"**
- **Left (Instructor)**: A sticky column. The instructor's image is masked by a large typographic "R" (for Ronok) which expands to reveal the full portrait on scroll.
- **Right (Testimonials)**: A vertical scroll of testimonial cards that "stack" on top of each other like a deck of cards, rather than scrolling traditionally.

### Images
**Instructor Image (Ronok Sheikh)**
- **Resolution:** High-res portrait
- **Aspect Ratio:** 3:4
- **Transparent Background:** No (solid light gray)
- **Visual Style:** Clean professional studio portrait
- **Subject:** Young adult male, short dark hair, light beard, black shirt.
- **Generation Prompt:** "Professional studio portrait of a young adult man with short dark hair and light beard, wearing black shirt. Neutral friendly expression, slight smile. Solid light gray background. Soft even lighting, minimal shadows. Confident and approachable mood. Clean modern look."

### Motion Choreography
- **Card Stacking**: As a testimonial scrolls out of view, it doesn't just move up; it shrinks and fades, while the next one slides over it.
- **Instructor Interaction**: Hovering the instructor's name triggers a "glitch" effect on his image (RGB shift + displacement).

## Section 6: Pricing & Footer

### Layout
**"The Final Transaction"**
- **Pricing**: A "Glassmorphism" card that floats above a dark, immersive gradient.
- **Footer**: A "Curtain Reveal". The footer is fixed at the bottom (z-index -1). The Pricing section slides *up* to reveal the footer sitting underneath.

### Motion Choreography
- **Value Breakdown**: The pricing items (n8n Access, Program, etc.) slide in from the right, one by one, forming a list.
- **CTA Pulse**: The "Enroll Now" button has a perpetual, rhythmic "heartbeat" glow (soft red shadow pulsing).

## Technical Implementation Notes

### Required Libraries
- **Three.js**: For the Hero background shader and 3D text effects.
- **GSAP (GreenSock)**: Core animation engine (ScrollTrigger for timeline control).
- **Lenis**: For smooth, momentum-based scrolling (critical for the velocity effects).

### Critical Performance Rules
- **WebGL**: Use a single canvas context for the background to avoid memory leaks.
- **Will-Change**: Apply `will-change: transform` only to the active section elements.
- **Virtualization**: If testimonials exceed 10, use virtual scrolling.
- **Throttling**: Resize observers and scroll listeners must be throttled to 100ms.

### Browser Support
- **Fallbacks**: 
  - If WebGL fails, fallback to a static high-res image of the wireframe.
  - If `prefers-reduced-motion` is true, disable parallax and velocity skews; switch to simple fades.

---

## Output Path
`/mnt/okcomputer/output/design.md`
