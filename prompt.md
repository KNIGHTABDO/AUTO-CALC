# 🧮 ULTIMATE AI-POWERED CALCULATOR WEB APPLICATION

## COMPREHENSIVE DEVELOPMENT PROMPT FOR GEMINI 3

---

# TABLE OF CONTENTS

1. [Project Overview](#project-overview)
2. [Design Philosophy](#design-philosophy)
3. [Visual Design System](#visual-design-system)
4.  [Layout Architecture](#layout-architecture)
5. [Drawing Canvas System](#drawing-canvas-system)
6.  [Calculator Modes & Features](#calculator-modes--features)
7. [AI & Intelligence Features](#ai--intelligence-features)
8. [Data Management](#data-management)
9. [Customization & Personalization](#customization--personalization)
10. [Accessibility Standards](#accessibility-standards)
11. [Performance Optimization](#performance-optimization)
12.  [Technical Architecture](#technical-architecture)
13. [Component Specifications](#component-specifications)
14. [Animation & Motion Design](#animation--motion-design)
15. [Error Handling & Edge Cases](#error-handling--edge-cases)
16. [Testing Requirements](#testing-requirements)
17. [Deployment & PWA](#deployment--pwa)
18.  [Future Extensibility](#future-extensibility)
19.  [Deliverables Checklist](#deliverables-checklist)

---

# PROJECT OVERVIEW

## Mission Statement

Create the most advanced, beautiful, and intelligent calculator web application ever built.  This is not just a calculator—it's a mathematical companion that combines the power of AI-driven handwriting recognition, stunning visual design, and comprehensive mathematical capabilities into a single, cohesive experience that delights users and makes mathematics accessible and enjoyable.

## Target Audience

- **Students**: From middle school to university level, needing a powerful tool for homework and exams
- **Professionals**: Engineers, scientists, financial analysts, and developers who need quick calculations
- **Educators**: Teachers who want to demonstrate mathematical concepts visually
- **Casual Users**: Anyone who appreciates beautiful design and wants more than a basic calculator
- **Power Users**: Those who need programmer modes, unit conversions, and advanced functions

## Core Value Propositions

1. **Draw to Calculate**: Revolutionary handwriting recognition that lets users draw mathematical expressions naturally
2. **Visual Excellence**: A design so beautiful it makes users want to do math
3. **Comprehensive Power**: Every mathematical function imaginable in one application
4. **Intelligent Assistance**: AI that understands context and helps users learn
5. **Seamless Experience**: Works offline, syncs across devices, adapts to user preferences

## Competitive Differentiation

Unlike existing calculators, this application offers:
- True handwriting recognition with support for complex mathematical notation
- Graph paper-style canvas for freeform mathematical exploration
- Real-time LaTeX rendering of recognized expressions
- Step-by-step solution explanations
- Voice input for hands-free calculation
- Collaborative features for sharing calculations
- Plugin architecture for extensibility

---

# DESIGN PHILOSOPHY

## Core Design Principles

### 1.  Elegant Simplicity
Despite the powerful features, the interface should feel simple and uncluttered. Advanced features reveal themselves progressively as users explore.  The default view should be approachable for anyone, while power features are discoverable through intuitive gestures and interactions.

### 2. Delightful Interactions
Every interaction should feel satisfying.  Buttons should respond with subtle animations that provide feedback. Results should appear with smooth, meaningful animations that reinforce the mathematical operation performed.  The application should feel alive and responsive.

### 3. Mathematical Beauty
The design should celebrate the beauty of mathematics. Use the golden ratio in layouts where appropriate. Display mathematical notation beautifully with proper typesetting. Show graphs and visualizations that are both accurate and aesthetically pleasing. 

### 4.  Contextual Intelligence
The interface should adapt to what the user is doing. When working with trigonometry, relevant functions should be more prominent. When drawing, the canvas should maximize.  When reviewing history, calculations should be easy to scan and search.

### 5. Error Prevention & Recovery
Prevent errors before they happen through intelligent input validation. When errors do occur, explain them clearly and offer solutions. Always provide an easy way to undo and recover from mistakes.

## Emotional Design Goals

- **Confidence**: Users should feel confident that their calculations are correct
- **Delight**: Small surprises and beautiful animations should make users smile
- **Flow**: The interface should never interrupt the user's mathematical thinking
- **Pride**: Users should feel proud to show the app to others

## Design Inspiration Sources

- Apple Calculator's simplicity and clarity
- Notion's beautiful typography and spacing
- Linear's smooth animations and attention to detail
- Figma's collaborative and responsive interface
- Desmos's powerful graphing capabilities
- GoodNotes's natural drawing experience

---

# VISUAL DESIGN SYSTEM

## Color System

### Primary Palette

```css
/* Primary Gradient - Used for main interactive elements */
--primary-gradient: linear-gradient(135deg, #6366F1 0%, #8B5CF6 50%, #3B82F6 100%);

/* Individual Primary Colors */
--primary-indigo: #6366F1;
--primary-violet: #8B5CF6;
--primary-blue: #3B82F6;

/* Primary Shades (for hover, active, disabled states) */
--primary-50: #EEF2FF;
--primary-100: #E0E7FF;
--primary-200: #C7D2FE;
--primary-300: #A5B4FC;
--primary-400: #818CF8;
--primary-500: #6366F1;
--primary-600: #4F46E5;
--primary-700: #4338CA;
--primary-800: #3730A3;
--primary-900: #312E81;
--primary-950: #1E1B4B;
```

### Secondary & Accent Colors

```css
/* Accent - For highlights, CTAs, and important actions */
--accent-coral: #F97316;
--accent-coral-light: #FB923C;
--accent-coral-dark: #EA580C;

/* Success States */
--success-50: #ECFDF5;
--success-400: #34D399;
--success-500: #10B981;
--success-600: #059669;

/* Warning States */
--warning-50: #FFFBEB;
--warning-400: #FBBF24;
--warning-500: #F59E0B;
--warning-600: #D97706;

/* Error States */
--error-50: #FEF2F2;
--error-400: #F87171;
--error-500: #EF4444;
--error-600: #DC2626;

/* Info States */
--info-50: #EFF6FF;
--info-400: #60A5FA;
--info-500: #3B82F6;
--info-600: #2563EB;
```

### Dark Theme (Default)

```css
/* Background Layers */
--bg-primary: #0F172A;      /* Main background */
--bg-secondary: #1E293B;    /* Card backgrounds */
--bg-tertiary: #334155;     /* Elevated elements */
--bg-elevated: #475569;     /* Highest elevation */

/* Surface Colors (for glassmorphism) */
--surface-glass: rgba(255, 255, 255, 0.03);
--surface-glass-hover: rgba(255, 255, 255, 0.06);
--surface-glass-active: rgba(255, 255, 255, 0.09);
--surface-glass-border: rgba(255, 255, 255, 0.08);

/* Text Colors */
--text-primary: #F8FAFC;
--text-secondary: #CBD5E1;
--text-tertiary: #94A3B8;
--text-muted: #64748B;
--text-disabled: #475569;

/* Border Colors */
--border-default: rgba(255, 255, 255, 0.06);
--border-hover: rgba(255, 255, 255, 0.12);
--border-focus: rgba(99, 102, 241, 0. 5);
```

### Light Theme

```css
/* Background Layers */
--bg-primary: #FFFFFF;
--bg-secondary: #F8FAFC;
--bg-tertiary: #F1F5F9;
--bg-elevated: #E2E8F0;

/* Surface Colors */
--surface-glass: rgba(0, 0, 0, 0. 02);
--surface-glass-hover: rgba(0, 0, 0, 0.04);
--surface-glass-active: rgba(0, 0, 0, 0. 06);
--surface-glass-border: rgba(0, 0, 0, 0.06);

/* Text Colors */
--text-primary: #0F172A;
--text-secondary: #334155;
--text-tertiary: #64748B;
--text-muted: #94A3B8;
--text-disabled: #CBD5E1;
```

### Special Effect Colors

```css
/* Glow Effects */
--glow-primary: rgba(99, 102, 241, 0. 4);
--glow-success: rgba(16, 185, 129, 0.4);
--glow-error: rgba(239, 68, 68, 0. 4);
--glow-accent: rgba(249, 115, 22, 0.4);

/* Canvas Colors */
--canvas-bg: #1A1A2E;
--canvas-grid: rgba(99, 102, 241, 0.1);
--canvas-grid-major: rgba(99, 102, 241, 0.2);

/* Ink Colors for Drawing */
--ink-white: #FFFFFF;
--ink-blue: #60A5FA;
--ink-green: #34D399;
--ink-yellow: #FBBF24;
--ink-red: #F87171;
--ink-purple: #A78BFA;
```

## Typography System

### Font Families

```css
/* Primary Font - UI and general text */
--font-primary: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;

/* Display Font - Large numbers and results */
--font-display: 'SF Pro Display', 'Inter', -apple-system, sans-serif;

/* Monospace Font - Calculations and code */
--font-mono: 'JetBrains Mono', 'SF Mono', 'Fira Code', 'Consolas', monospace;

/* Math Font - Mathematical expressions */
--font-math: 'STIX Two Math', 'Cambria Math', 'Latin Modern Math', serif;
```

### Type Scale

```css
/* Display Sizes - For main results */
--text-display-2xl: 4. 5rem;    /* 72px - Main calculation result */
--text-display-xl: 3. 75rem;    /* 60px - Secondary results */
--text-display-lg: 3rem;       /* 48px - Graph titles */
--text-display-md: 2.25rem;    /* 36px - Section headers */
--text-display-sm: 1.875rem;   /* 30px - Card titles */

/* Body Sizes - For interface elements */
--text-xl: 1.25rem;            /* 20px - Large buttons */
--text-lg: 1.125rem;           /* 18px - Button text */
--text-base: 1rem;             /* 16px - Default body */
--text-sm: 0.875rem;           /* 14px - Secondary text */
--text-xs: 0.75rem;            /* 12px - Captions, labels */
--text-2xs: 0. 625rem;          /* 10px - Tiny labels */

/* Line Heights */
--leading-none: 1;
--leading-tight: 1.25;
--leading-snug: 1. 375;
--leading-normal: 1.5;
--leading-relaxed: 1. 625;

/* Letter Spacing */
--tracking-tighter: -0.05em;
--tracking-tight: -0.025em;
--tracking-normal: 0;
--tracking-wide: 0.025em;
--tracking-wider: 0.05em;

/* Font Weights */
--font-light: 300;
--font-normal: 400;
--font-medium: 500;
--font-semibold: 600;
--font-bold: 700;
--font-extrabold: 800;
```

### Typography Patterns

```css
/* Result Display - Main answer */
. result-display {
  font-family: var(--font-mono);
  font-size: var(--text-display-2xl);
  font-weight: var(--font-semibold);
  letter-spacing: var(--tracking-tight);
  line-height: var(--leading-none);
  font-feature-settings: 'tnum' 1, 'kern' 1;
}

/* Expression Display - Current input */
.expression-display {
  font-family: var(--font-mono);
  font-size: var(--text-display-sm);
  font-weight: var(--font-normal);
  letter-spacing: var(--tracking-normal);
  color: var(--text-secondary);
}

/* Button Numbers */
.button-number {
  font-family: var(--font-display);
  font-size: var(--text-xl);
  font-weight: var(--font-medium);
}

/* Button Operators */
.button-operator {
  font-family: var(--font-mono);
  font-size: var(--text-lg);
  font-weight: var(--font-bold);
}

/* History Items */
.history-expression {
  font-family: var(--font-mono);
  font-size: var(--text-sm);
  color: var(--text-tertiary);
}

. history-result {
  font-family: var(--font-mono);
  font-size: var(--text-base);
  font-weight: var(--font-semibold);
  color: var(--text-primary);
}
```

## Spacing System

```css
/* Base spacing unit: 4px */
--space-0: 0;
--space-px: 1px;
--space-0. 5: 0. 125rem;   /* 2px */
--space-1: 0.25rem;      /* 4px */
--space-1.5: 0.375rem;   /* 6px */
--space-2: 0.5rem;       /* 8px */
--space-2.5: 0.625rem;   /* 10px */
--space-3: 0. 75rem;      /* 12px */
--space-3.5: 0.875rem;   /* 14px */
--space-4: 1rem;         /* 16px */
--space-5: 1. 25rem;      /* 20px */
--space-6: 1.5rem;       /* 24px */
--space-7: 1.75rem;      /* 28px */
--space-8: 2rem;         /* 32px */
--space-9: 2.25rem;      /* 36px */
--space-10: 2.5rem;      /* 40px */
--space-11: 2.75rem;     /* 44px */
--space-12: 3rem;        /* 48px */
--space-14: 3.5rem;      /* 56px */
--space-16: 4rem;        /* 64px */
--space-20: 5rem;        /* 80px */
--space-24: 6rem;        /* 96px */
--space-28: 7rem;        /* 112px */
--space-32: 8rem;        /* 128px */
```

## Border Radius System

```css
--radius-none: 0;
--radius-sm: 0.25rem;     /* 4px - Small elements */
--radius-default: 0.5rem; /* 8px - Buttons, inputs */
--radius-md: 0.75rem;     /* 12px - Cards */
--radius-lg: 1rem;        /* 16px - Large cards */
--radius-xl: 1. 25rem;     /* 20px - Modals */
--radius-2xl: 1. 5rem;     /* 24px - Large modals */
--radius-3xl: 2rem;       /* 32px - Feature cards */
--radius-full: 9999px;    /* Circular elements */
```

## Shadow System

```css
/* Elevation Shadows - Dark Theme */
--shadow-xs: 0 1px 2px 0 rgba(0, 0, 0, 0. 4);
--shadow-sm: 0 1px 3px 0 rgba(0, 0, 0, 0. 4), 0 1px 2px -1px rgba(0, 0, 0, 0. 4);
--shadow-md: 0 4px 6px -1px rgba(0, 0, 0, 0. 4), 0 2px 4px -2px rgba(0, 0, 0, 0. 4);
--shadow-lg: 0 10px 15px -3px rgba(0, 0, 0, 0. 4), 0 4px 6px -4px rgba(0, 0, 0, 0.4);
--shadow-xl: 0 20px 25px -5px rgba(0, 0, 0, 0.4), 0 8px 10px -6px rgba(0, 0, 0, 0.4);
--shadow-2xl: 0 25px 50px -12px rgba(0, 0, 0, 0. 5);

/* Glow Shadows - For interactive elements */
--shadow-glow-primary: 0 0 20px rgba(99, 102, 241, 0. 3), 0 0 40px rgba(99, 102, 241, 0. 1);
--shadow-glow-success: 0 0 20px rgba(16, 185, 129, 0. 3), 0 0 40px rgba(16, 185, 129, 0.1);
--shadow-glow-error: 0 0 20px rgba(239, 68, 68, 0. 3), 0 0 40px rgba(239, 68, 68, 0.1);
--shadow-glow-accent: 0 0 20px rgba(249, 115, 22, 0. 3), 0 0 40px rgba(249, 115, 22, 0.1);

/* Inset Shadows - For pressed states */
--shadow-inset-sm: inset 0 1px 2px 0 rgba(0, 0, 0, 0. 3);
--shadow-inset-md: inset 0 2px 4px 0 rgba(0, 0, 0, 0. 3);
--shadow-inset-lg: inset 0 4px 8px 0 rgba(0, 0, 0, 0.3);

/* Neomorphism Shadows */
--shadow-neo-raised: 8px 8px 16px rgba(0, 0, 0, 0.4), -8px -8px 16px rgba(255, 255, 255, 0. 02);
--shadow-neo-pressed: inset 4px 4px 8px rgba(0, 0, 0, 0.4), inset -4px -4px 8px rgba(255, 255, 255, 0.02);
```

## Glassmorphism Specifications

```css
/* Glass Panel Base */
.glass-panel {
  background: rgba(255, 255, 255, 0.03);
  backdrop-filter: blur(20px);
  -webkit-backdrop-filter: blur(20px);
  border: 1px solid rgba(255, 255, 255, 0.06);
  box-shadow: 
    0 8px 32px rgba(0, 0, 0, 0.3),
    inset 0 1px 0 rgba(255, 255, 255, 0.05);
}

/* Glass Panel Hover */
.glass-panel:hover {
  background: rgba(255, 255, 255, 0.05);
  border-color: rgba(255, 255, 255, 0. 1);
}

/* Glass Panel Active */
.glass-panel:active {
  background: rgba(255, 255, 255, 0.02);
  box-shadow: 
    0 4px 16px rgba(0, 0, 0, 0.3),
    inset 0 2px 4px rgba(0, 0, 0, 0. 2);
}

/* Frosted Glass (Higher blur) */
.glass-frosted {
  background: rgba(255, 255, 255, 0.05);
  backdrop-filter: blur(40px) saturate(180%);
  -webkit-backdrop-filter: blur(40px) saturate(180%);
  border: 1px solid rgba(255, 255, 255, 0.08);
}

/* Colored Glass Variants */
.glass-primary {
  background: linear-gradient(
    135deg,
    rgba(99, 102, 241, 0. 1) 0%,
    rgba(139, 92, 246, 0.05) 100%
  );
  border-color: rgba(99, 102, 241, 0. 2);
}

.glass-success {
  background: linear-gradient(
    135deg,
    rgba(16, 185, 129, 0.1) 0%,
    rgba(52, 211, 153, 0.05) 100%
  );
  border-color: rgba(16, 185, 129, 0.2);
}
```

---

# LAYOUT ARCHITECTURE

## Overall Application Structure

```
┌─────────────────────────────────────────────────────────────────────┐
│  HEADER BAR                                                          │
│  ┌─────────────────────────────────────────────────────────────────┐│
│  │ Logo    Mode Tabs    [Basic][Scientific][Graphing][Programmer]  ││
│  │                                            Settings  History    ││
│  └─────────────────────────────────────────────────────────────────┘│
├─────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  ┌──────────────────────────┐  ┌──────────────────────────────────┐ │
│  │                          │  │                                  │ │
│  │   CALCULATOR PANEL       │  │   DRAWING CANVAS                 │ │
│  │                          │  │                                  │ │
│  │   ┌──────────────────┐   │  │   ┌──────────────────────────┐   │ │
│  │   │ Expression       │   │  │   │                          │   │ │
│  │   │ Display Area     │   │  │   │   Handwriting Area       │   │ │
│  │   └──────────────────┘   │  │   │                          │   │ │
│  │   ┌──────────────────┐   │  │   │   Grid Background        │   │ │
│  │   │                  │   │  │   │                          │   │ │
│  │   │ Result Display   │   │  │   │   Recognition Preview    │   │ │
│  │   │                  │   │  │   │                          │   │ │
│  │   └──────────────────┘   │  │   └──────────────────────────┘   │ │
│  │                          │  │                                  │ │
│  │   ┌──────────────────┐   │  │   ┌──────────────────────────┐   │ │
│  │   │ ┌──┐ ┌──┐ ┌──┐   │   │  │   │ Pen │ Eraser │ Colors   │   │ │
│  │   │ │7 │ │8 │ │9 │÷  │   │  │   │ Size │ Clear │ Undo     │   │ │
│  │   │ └──┘ └──┘ └──┘   │   │  │   └──────────────────────────┘   │ │
│  │   │ ┌──┐ ┌──┐ ┌──┐   │   │  │                                  │ │
│  │   │ │4 │ │5 │ │6 │×  │   │  └──────────────────────────────────┘ │
│  │   │ └──┘ └──┘ └──┘   │   │                                       │
│  │   │ ┌──┐ ┌──┐ ┌──┐   │   │  ┌──────────────────────────────────┐ │
│  │   │ │1 │ │2 │ │3 │−  │   │  │ HISTORY SIDEBAR (Collapsible)   │ │
│  │   │ └──┘ └──┘ └──┘   │   │  │                                  │ │
│  │   │ ┌──┐ ┌──┐ ┌──┐   │   │  │ Search...                        │ │
│  │   │ │.  │ │0 │ │= │+  │   │  │ ─────────────────────────────── │ │
│  │   │ └──┘ └──┘ └──┘   │   │  │ 2 + 2 = 4           ⭐ 📋       │ │
│  │   └──────────────────┘   │  │ sin(45°) = 0.707    ⭐ 📋       │ │
│  │                          │  │ 15% of 200 = 30     ⭐ 📋       │ │
│  └──────────────────────────┘  └──────────────────────────────────┘ │
│                                                                      │
├─────────────────────────────────────────────────────────────────────┤
│  QUICK ACCESS BAR                                                    │
│  [π] [e] [√] [^] [! ] [%] [log] [ln] [sin] [cos] [tan] [( )]        │
└─────────────────────────────────────────────────────────────────────┘
```

## Responsive Layouts

### Desktop Layout (≥1280px)

```
┌────────────────────────────────────────────────────────────────────────────┐
│ HEADER                                                                      │
├───────────────────────────┬───────────────────────────┬────────────────────┤
│                           │                           │                    │
│   CALCULATOR (40%)        │   CANVAS (40%)            │   HISTORY (20%)    │
│                           │                           │                    │
│   All features visible    │   Full drawing area       │   Searchable       │
│   Scientific row shown    │   Tool palette visible    │   Filterable       │
│                           │                           │                    │
└───────────────────────────┴───────────────────────────┴────────────────────┘
```

### Large Tablet Layout (1024px - 1279px)

```
┌────────────────────────────────────────────────────────────────────┐
│ HEADER                                                              │
├────────────────────────────────┬───────────────────────────────────┤
│                                │                                   │
│   CALCULATOR (50%)             │   CANVAS (50%)                    │
│                                │                                   │
│   Compact scientific row       │   Full drawing area               │
│                                │                                   │
├────────────────────────────────┴───────────────────────────────────┤
│ HISTORY (Collapsible drawer from right)                            │
└────────────────────────────────────────────────────────────────────┘
```

### Tablet Layout (768px - 1023px)

```
┌────────────────────────────────────────────────────────────────────┐
│ HEADER with Tab Navigation                                          │
├────────────────────────────────────────────────────────────────────┤
│                                                                     │
│  [Calculator Tab] | [Canvas Tab] | [History Tab]                   │
│                                                                     │
│  ┌─────────────────────────────────────────────────────────────┐   │
│  │                                                             │   │
│  │   ACTIVE TAB CONTENT                                        │   │
│  │                                                             │   │
│  │   Full width, optimized for touch                          │   │
│  │                                                             │   │
│  └─────────────────────────────────────────────────────────────┘   │
│                                                                     │
└────────────────────────────────────────────────────────────────────┘
```

### Mobile Layout (<768px)

```
┌──────────────────────────────────────┐
│ HEADER (Minimal)              ☰     │
├──────────────────────────────────────┤
│                                      │
│  ┌──────────────────────────────┐   │
│  │ Expression                    │   │
│  │ Result Display (Large)        │   │
│  └──────────────────────────────┘   │
│                                      │
│  ┌──────────────────────────────┐   │
│  │  ┌────┐ ┌────┐ ┌────┐ ┌────┐ │   │
│  │  │ C  │ │ ⌫  │ │ %  │ │ ÷  │ │   │
│  │  └────┘ └────┘ └────┘ └────┘ │   │
│  │  ┌────┐ ┌────┐ ┌────┐ ┌────┐ │   │
│  │  │ 7  │ │ 8  │ │ 9  │ │ ×  │ │   │
│  │  └────┘ └────┘ └────┘ └────┘ │   │
│  │  ┌────┐ ┌────┐ ┌────┐ ┌────┐ │   │
│  │  │ 4  │ │ 5  │ │ 6  │ │ −  │ │   │
│  │  └────┘ └────┘ └────┘ └────┘ │   │
│  │  ┌────┐ ┌────┐ ┌────┐ ┌────┐ │   │
│  │  │ 1  │ │ 2  │ │ 3  │ │ +  │ │   │
│  │  └────┘ └────┘ └────┘ └────┘ │   │
│  │  ┌────┐ ┌──────────┐ ┌────┐  │   │
│  │  │ .   │ │    0     │ │ =  │  │   │
│  │  └────┘ └──────────┘ └────┘  │   │
│  └──────────────────────────────┘   │
│                                      │
│  ← Swipe for Canvas | History →     │
└──────────────────────────────────────┘
```

## Panel System Specifications

### Calculator Panel

- **Minimum width**: 320px
- **Maximum width**: 600px
- **Aspect ratio**: Flexible, maintains button proportions
- **Padding**: 16px (mobile), 24px (tablet), 32px (desktop)
- **Background**: Glass panel with subtle gradient

### Canvas Panel

- **Minimum width**: 400px
- **Preferred aspect ratio**: 4:3 or 16:9
- **Touch target size**: Minimum 44px × 44px for tools
- **Canvas resolution**: 2x device pixel ratio for crisp lines
- **Background**: Darker shade with optional grid

### History Sidebar

- **Default width**: 280px (collapsible)
- **Minimum width**: 240px
- **Maximum width**: 400px
- **Virtualized list**: For smooth scrolling with many items
- **Group by**: Date, with collapsible sections

---

# DRAWING CANVAS SYSTEM

## Canvas Technical Specifications

### Canvas Properties

```javascript
const canvasConfig = {
  // Resolution
  baseWidth: 1920,
  baseHeight: 1080,
  pixelRatio: window.devicePixelRatio || 2,
  
  // Drawing
  defaultStrokeWidth: 3,
  minStrokeWidth: 1,
  maxStrokeWidth: 30,
  smoothingFactor: 0. 3,
  
  // Recognition
  recognitionDelay: 800, // ms after last stroke
  minimumStrokeLength: 10, // pixels
  
  // Performance
  maxUndoSteps: 100,
  chunkSize: 50, // strokes per chunk for optimization
};
```

### Stroke Data Structure

```typescript
interface Point {
  x: number;
  y: number;
  pressure: number;
  timestamp: number;
  tiltX?: number;
  tiltY?: number;
}

interface Stroke {
  id: string;
  points: Point[];
  color: string;
  width: number;
  opacity: number;
  tool: 'pen' | 'highlighter' | 'eraser';
  timestamp: number;
  boundingBox: {
    minX: number;
    minY: number;
    maxX: number;
    maxY: number;
  };
}

interface CanvasState {
  strokes: Stroke[];
  currentStroke: Stroke | null;
  recognizedExpression: string;
  recognizedConfidence: number;
  gridEnabled: boolean;
  gridSize: number;
}
```

## Drawing Tools

### Pen Tool

```typescript
interface PenToolConfig {
  name: 'pen';
  icon: 'PenIcon';
  
  // Appearance
  defaultColor: '#FFFFFF';
  defaultWidth: 3;
  
  // Behavior
  pressureSensitive: true;
  minPressure: 0. 1;
  maxPressure: 1. 0;
  pressureWidthMultiplier: 2.5;
  
  // Smoothing
  smoothingEnabled: true;
  smoothingIterations: 3;
  
  // Line end caps
  lineCap: 'round';
  lineJoin: 'round';
}
```

### Highlighter Tool

```typescript
interface HighlighterToolConfig {
  name: 'highlighter';
  icon: 'HighlighterIcon';
  
  // Appearance
  defaultColor: '#FBBF24';
  defaultWidth: 20;
  opacity: 0.4;
  
  // Behavior
  pressureSensitive: false;
  blendMode: 'multiply';
  
  // Line end caps
  lineCap: 'square';
  lineJoin: 'round';
}
```

### Eraser Tool

```typescript
interface EraserToolConfig {
  name: 'eraser';
  icon: 'EraserIcon';
  
  // Modes
  mode: 'stroke' | 'point';
  
  // Stroke mode: removes entire strokes on touch
  strokeModeThreshold: 20; // pixels
  
  // Point mode: removes points within radius
  pointModeRadius: 10;
  
  // Appearance
  cursorSize: 20;
  showCursor: true;
}
```

### Lasso Select Tool

```typescript
interface LassoToolConfig {
  name: 'lasso';
  icon: 'LassoIcon';
  
  // Selection
  selectionColor: 'rgba(99, 102, 241, 0. 3)';
  selectionBorder: 'rgba(99, 102, 241, 0.8)';
  
  // Actions on selection
  actions: ['delete', 'copy', 'move', 'recognize'];
}
```

## Color Palette

```typescript
const inkColors = [
  { name: 'White', value: '#FFFFFF', category: 'basic' },
  { name: 'Light Gray', value: '#CBD5E1', category: 'basic' },
  { name: 'Blue', value: '#60A5FA', category: 'primary' },
  { name: 'Indigo', value: '#818CF8', category: 'primary' },
  { name: 'Purple', value: '#A78BFA', category: 'primary' },
  { name: 'Green', value: '#34D399', category: 'accent' },
  { name: 'Yellow', value: '#FBBF24', category: 'accent' },
  { name: 'Orange', value: '#FB923C', category: 'accent' },
  { name: 'Red', value: '#F87171', category: 'accent' },
  { name: 'Pink', value: '#F472B6', category: 'accent' },
];

// Custom color picker for advanced users
interface CustomColorPicker {
  recentColors: string[]; // Last 8 used custom colors
  favoriteColors: string[]; // User-saved colors
  colorSpace: 'hex' | 'rgb' | 'hsl';
}
```

## Grid System

```typescript
interface GridConfig {
  enabled: boolean;
  type: 'lines' | 'dots' | 'graph';
  
  // Sizing
  cellSize: 20; // pixels
  majorLineEvery: 5; // cells
  
  // Appearance
  minorLineColor: 'rgba(99, 102, 241, 0. 08)';
  majorLineColor: 'rgba(99, 102, 241, 0.15)';
  minorLineWidth: 0.5;
  majorLineWidth: 1;
  
  // Behavior
  snapToGrid: false;
  snapThreshold: 8; // pixels
  showAxisLabels: false;
}
```

## Handwriting Recognition Engine

### Recognition Pipeline

```typescript
interface RecognitionPipeline {
  // Step 1: Preprocessing
  preprocessing: {
    normalizeSize: true;
    targetSize: { width: 256, height: 256 };
    centerStrokes: true;
    removeNoise: true;
    noiseThreshold: 5; // pixels
  };
  
  // Step 2: Feature Extraction
  featureExtraction: {
    method: 'stroke-based' | 'image-based' | 'hybrid';
    strokeFeatures: [
      'direction',
      'curvature', 
      'length',
      'aspectRatio',
      'crossings'
    ];
  };
  
  // Step 3: Recognition
  recognition: {
    engine: 'tensorflow' | 'myscript' | 'custom';
    model: 'math-expression-v2';
    confidenceThreshold: 0.7;
  };
  
  // Step 4: Post-processing
  postProcessing: {
    applyGrammar: true;
    balanceParentheses: true;
    suggestCorrections: true;
  };
}
```

### Supported Mathematical Symbols

```typescript
const supportedSymbols = {
  // Digits
  digits: ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9'],
  
  // Basic Operators
  basicOperators: ['+', '-', '×', '÷', '=', '≠'],
  
  // Advanced Operators
  advancedOperators: ['^', '√', '∛', '! ', '%', '±'],
  
  // Comparison
  comparison: ['<', '>', '≤', '≥', '≈', '≡'],
  
  // Grouping
  grouping: ['(', ')', '[', ']', '{', '}', '|'],
  
  // Fractions (detected by spatial relationship)
  fractionLine: '—', // horizontal line separating numerator/denominator
  
  // Greek Letters
  greekLetters: {
    lowercase: ['α', 'β', 'γ', 'δ', 'ε', 'θ', 'λ', 'μ', 'π', 'σ', 'φ', 'ω'],
    uppercase: ['Δ', 'Γ', 'Λ', 'Π', 'Σ', 'Φ', 'Ω'],
  },
  
  // Functions (recognized as text)
  functions: [
    'sin', 'cos', 'tan', 'cot', 'sec', 'csc',
    'arcsin', 'arccos', 'arctan',
    'sinh', 'cosh', 'tanh',
    'log', 'ln', 'lg',
    'exp', 'abs', 'sqrt',
    'lim', 'sum', 'prod', 'int'
  ],
  
  // Calculus (spatial recognition)
  calculus: ['∫', '∬', '∮', 'Σ', '∏', 'lim', '∂', '∇', 'd/dx'],
  
  // Special Constants
  constants: ['π', 'e', 'i', '∞', 'φ'],
  
  // Set Theory
  setTheory: ['∈', '∉', '⊂', '⊃', '∪', '∩', '∅'],
  
  // Arrows (for limits, implications)
  arrows: ['→', '←', '↔', '⇒', '⇐', '⇔'],
};
```

### Recognition Confidence Display

```typescript
interface RecognitionResult {
  expression: string;
  latex: string;
  confidence: number; // 0-1
  alternatives: Array<{
    expression: string;
    confidence: number;
  }>;
  segments: Array<{
    strokes: string[]; // stroke IDs
    symbol: string;
    confidence: number;
    boundingBox: BoundingBox;
  }>;
}

// Visual feedback based on confidence
const confidenceStyles = {
  high: { // confidence >= 0.9
    color: 'var(--success-500)',
    background: 'rgba(16, 185, 129, 0. 1)',
  },
  medium: { // confidence >= 0.7
    color: 'var(--warning-500)',
    background: 'rgba(245, 158, 11, 0.1)',
  },
  low: { // confidence < 0. 7
    color: 'var(--error-500)',
    background: 'rgba(239, 68, 68, 0. 1)',
    showAlternatives: true,
  },
};
```

## Canvas Gestures

```typescript
const canvasGestures = {
  // Drawing
  singleFinger: 'draw',
  
  // Navigation
  twoFingerPan: 'pan',
  twoFingerPinch: 'zoom',
  twoFingerRotate: 'rotate', // optional
  
  // Actions
  twoFingerTap: 'undo',
  threeFingerTap: 'redo',
  longPress: 'contextMenu',
  doubleTap: 'zoomToFit',
  
  // Selection (with lasso tool)
  circleGesture: 'selectArea',
  scratchOut: 'delete',
};
```

## Canvas Actions & Shortcuts

```typescript
const canvasShortcuts = {
  // Tools
  'p': 'selectPenTool',
  'h': 'selectHighlighterTool',
  'e': 'selectEraserTool',
  'l': 'selectLassoTool',
  
  // Actions
  'Ctrl/Cmd + Z': 'undo',
  'Ctrl/Cmd + Shift + Z': 'redo',
  'Ctrl/Cmd + Y': 'redo',
  'Delete/Backspace': 'deleteSelected',
  'Ctrl/Cmd + A': 'selectAll',
  'Ctrl/Cmd + C': 'copy',
  'Ctrl/Cmd + V': 'paste',
  'Escape': 'deselectAll',
  
  // View
  'Ctrl/Cmd + 0': 'zoomToFit',
  'Ctrl/Cmd + +': 'zoomIn',
  'Ctrl/Cmd + -': 'zoomOut',
  'g': 'toggleGrid',
  
  // Canvas
  'Ctrl/Cmd + Enter': 'calculate',
  'c': 'clearCanvas',
};
```

---

# CALCULATOR MODES & FEATURES

## Mode System Overview

```typescript
type CalculatorMode = 
  | 'basic'
  | 'scientific'
  | 'programmer'
  | 'graphing'
  | 'matrix'
  | 'equations'
  | 'converter';

interface ModeConfig {
  id: CalculatorMode;
  name: string;
  icon: string;
  description: string;
  keypadLayout: KeypadLayout;
  additionalPanels?: Panel[];
  shortcuts: Shortcut[];
}
```

## Basic Mode

### Keypad Layout

```
┌─────────────────────────────────────────────────┐
│  Expression: 125 × 4                            │
│  Result: 500                                    │
├─────────────────────────────────────────────────┤
│  ┌─────┐ ┌─────┐ ┌─────┐ ┌─────┐               │
│  │  C  │ │ +/- │ │  %  │ │  ÷  │               │
│  └─────┘ └─────┘ └─────┘ └─────┘               │
│  ┌─────┐ ┌─────┐ ┌─────┐ ┌─────┐               │
│  │  7  │ │  8  │ │  9  │ │  ×  │               │
│  └─────┘ └─────┘ └─────┘ └─────┘               │
│  ┌─────┐ ┌─────┐ ┌─────┐ ┌─────┐               │
│  │  4  │ │  5  │ │  6  │ │  −  │               │
│  └─────┘ └─────┘ └─────┘ └─────┘               │
│  ┌─────┐ ┌─────┐ ┌─────┐ ┌─────┐               │
│  │  1  │ │  2  │ │  3  │ │  +  │               │
│  └─────┘ └─────┘ └─────┘ └─────┘               │
│  ┌───────────┐ ┌─────┐ ┌─────────┐             │
│  │     0     │ │  .   │ │    =    │             │
│  └───────────┘ └─────┘ └─────────┘             │
└─────────────────────────────────────────────────┘
```

### Basic Mode Features

```typescript
interface BasicModeFeatures {
  // Core Operations
  operations: [
    { symbol: '+', name: 'add', precedence: 1 },
    { symbol: '-', name: 'subtract', precedence: 1 },
    { symbol: '×', name: 'multiply', precedence: 2 },
    { symbol: '÷', name: 'divide', precedence: 2 },
    { symbol: '%', name: 'percentage', precedence: 3 },
  ];
  
  // Memory Functions
  memory: {
    MC: 'memoryClear',
    MR: 'memoryRecall',
    'M+': 'memoryAdd',
    'M-': 'memorySubtract',
    MS: 'memoryStore',
  };
  
  // Input Controls
  controls: {
    C: 'clearAll',
    CE: 'clearEntry',
    '⌫': 'backspace',
    '±': 'negate',
  };
  
  // Display Options
  display: {
    maxDigits: 15,
    decimalPlaces: 'auto', // or fixed number
    thousandsSeparator: true,
    scientificNotationThreshold: 1e12,
  };
}
```

## Scientific Mode

### Extended Keypad Layout

```
┌────────────────────────────────────────────────────────────────────┐
│  Expression: sin(45°) + √(16)                                       │
│  Result: 4.7071067811865475                                         │
├────────────────────────────────────────────────────────────────────┤
│  [2nd] [Rad/Deg: DEG]                                               │
├────────────────────────────────────────────────────────────────────┤
│  ┌────┐ ┌────┐ ┌────┐ ┌────┐ ┌────┐ ┌────┐ ┌────┐ ┌────┐          │
│  │ x² │ │ x³ │ │ xʸ │ │ eˣ │ │10ˣ │ │ 1/x│ │ √  │ │ ³√ │          │
│  └────┘ └────┘ └────┘ └────┘ └────┘ └────┘ └────┘ └────┘          │
│  ┌────┐ ┌────┐ ┌────┐ ┌────┐ ┌────┐ ┌────┐ ┌────┐ ┌────┐          │
│  │sin │ │cos │ │tan │ │sinh│ │cosh│ │tanh│ │ (  │ │ )  │          │
│  └────┘ └────┘ └────┘ └────┘ └────┘ └────┘ └────┘ └────┘          │
│  ┌────┐ ┌────┐ ┌────┐ ┌────┐ ┌────┐ ┌────┐ ┌────┐ ┌────┐          │
│  │ ln │ │log │ │log₂│ │ n!  │ │ π  │ │ e  │ │EE  │ │Rand│          │
│  └────┘ └────┘ └────┘ └────┘ └────┘ └────┘ └────┘ └────┘          │
├────────────────────────────────────────────────────────────────────┤
│  ┌────┐ ┌────┐ ┌────┐ ┌────┐                                       │
│  │ C  │ │ ⌫  │ │ %  │ │ ÷  │                                       │
│  └────┘ └────┘ └────┘ └────┘                                       │
│  ┌────┐ ┌────┐ ┌────┐ ┌────┐                                       │
│  │ 7  │ │ 8  │ │ 9  │ │ ×  │                                       │
│  └────┘ └────┘ └────┘ └────┘                                       │
│  ┌────┐ ┌────┐ ┌────┐ ┌────┐                                       │
│  │ 4  │ │ 5  │ │ 6  │ │ −  │                                       │
│  └────┘ └────┘ └────┘ └────┘                                       │
│  ┌────┐ ┌────┐ ┌────┐ ┌────┐                                       │
│  │ 1  │ │ 2  │ │ 3  │ │ +  │                                       │
│  └────┘ └────┘ └────┘ └────┘                                       │
│  ┌──────────┐ ┌────┐ ┌──────────┐                                  │
│  │    0     │ │ .  │ │    =     │                                  │
│  └──────────┘ └────┘ └──────────┘                                  │
└────────────────────────────────────────────────────────────────────┘
```

### Scientific Functions

```typescript
interface ScientificFunctions {
  // Trigonometric (in both degrees and radians)
  trigonometric: {
    primary: ['sin', 'cos', 'tan', 'cot', 'sec', 'csc'],
    inverse: ['arcsin', 'arccos', 'arctan', 'arccot', 'arcsec', 'arccsc'],
    hyperbolic: ['sinh', 'cosh', 'tanh', 'coth', 'sech', 'csch'],
    inverseHyperbolic: ['arcsinh', 'arccosh', 'arctanh'],
  };
  
  // Exponential & Logarithmic
  exponential: {
    functions: ['exp', 'exp2', 'exp10', 'expm1'],
    logarithms: ['ln', 'log', 'log2', 'log10', 'log1p'],
    custom: 'logₙ(x)', // log with custom base
  };
  
  // Powers & Roots
  powers: {
    squares: ['x²', 'x³', 'xⁿ'],
    roots: ['√x', '³√x', 'ⁿ√x'],
    reciprocal: '1/x',
  };
  
  // Factorial & Combinatorics
  combinatorics: {
    factorial: 'n! ',
    doubleFactorial: 'n!!',
    permutation: 'nPr',
    combination: 'nCr',
    gamma: 'Γ(x)',
  };
  
  // Constants
  constants: {
    pi: { symbol: 'π', value: Math.PI },
    e: { symbol: 'e', value: Math.E },
    phi: { symbol: 'φ', value: 1.618033988749895 },
    sqrt2: { symbol: '√2', value: Math.SQRT2 },
    sqrt3: { symbol: '√3', value: 1.7320508075688772
