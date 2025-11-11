# Pricing Panel - Built from Memory

## What is this?

this is a responsive pricing panel I built following Colt Steele's Web Development Bootcamp 2025. the original design is by [Travis Williamson on CodePen](https://codepen.io/travisw) (open source), which Colt used as teaching material. but here's the thing: I didn't just copy the code. I rebuilt it from scratch, from memory, using only the concepts I learned.

## The Challenge

- Build the entire pricing panel without looking at reference code
- Use mobile-first approach (structure first, then details)
- Debug all issues myself
- Make it fully responsive (column on mobile, row on desktop)

## What I Learned

### The Big Concepts

**Mobile-First Workflow:**
1. Structure first (flexbox layout, containers)
2. Spacing (margins, padding)
3. Typography (fonts, sizes, weights)
4. Colors (backgrounds, borders, text)
5. Details (hover effects, transitions)

this approach changed everything. before this, I was trying to do colors and spacing at the same time and forgetting things. now I work in phases and nothing gets missed.

**Debugging Like a Pro:**
- Use `outline: 2px solid red;` to see container boundaries (doesn't affect layout like border does!)
- Add `background-color` to see where containers actually are
- Use DevTools responsive mode to test breakpoints
- When stuck, make things VISIBLE first, then fix them

### Specific Things I Figured Out

**The Border Bug:**
- On desktop (900px+), borders were extending outside the container
- Solution: Need to remove mobile borders AND add desktop borders in `@media` query
- Mobile uses `border-bottom` between cards
- Desktop uses `border-right` between cards

**The Button Alignment:**
- Buttons were sticking to bottom on mobile
- Fixed with `margin-bottom: 20px` on `.pricing-button`

**The Container Radius Bug:**
- Had a 1px border breaking the border-radius on last plan
- Used `outline: 2px solid red;` to diagnose
- Fixed with `.pricing-plan:last-child { border-right: none; }`

**width vs max-width:**
- `width: 100%` = "make me exactly 100% of parent width"
- `max-width: 100%` = "don't let me grow bigger than parent"
- Together = "fill container but never overflow it"
- This prevents images from breaking layouts!

## The Bugs I Debugged (All by myself!)

1. **Images weren't centered** → Added `text-align: center` to `.panel`
2. **Borders breaking on desktop** → Wrong borders in wrong places, fixed with proper `@media` rules
3. **One box smaller than others** → `padding: 15px 0px` was the culprit, changed to `margin: 50px 0 25px`
4. **Button sticking to bottom** → Added `margin-bottom: 20px`
5. **Border breaking border-radius** → Removed border on `:last-child`

## Tools I Used

- **CodePen** - Live preview made learning 10x faster than VS Code
- **Chrome DevTools** - Responsive mode to test mobile/desktop
- **Outline debugging** - `outline: 2px solid red;` to see container boundaries
- **Background colors** - Made invisible containers visible
- **Claude AI (Sonnet 4.5)** - My coding Assistant throughout this project. helped me understand concepts deeply, debug issues, and learn professional workflows instead of just giving me answers.

## What I'm Proud Of

- Wrote 150+ lines of CSS from memory
- Only looked at reference for hover/focus states
- Debugged ALL issues independently
- Used professional debugging techniques (outline, background-color)
- Understood WHY the code works, not just HOW

## The Stats

- **Time spent:** ~4-5 hours (including debugging)
- **Lines of code:** ~150 (without reset)
- **Bugs fixed:** 5+
- **Reference used:** ~5% (just hover states)
- **Understanding gained:** 💯

## Technologies

- HTML5
- CSS3
- Flexbox
- Media Queries
- Mobile-First Design

## Credits

- **Original Design:** [Travis Williamson](https://codepen.io/travisw) on CodePen
- **Course:** Colt Steele's Web Development Bootcamp 2025

## What's Next

Moving to Bootstrap section in Colt's course. But I'll come back and rebuild this again in a week to test my muscle memory.

## Notes to Future Me

- Always use mobile-first approach (column → row)
- Structure before details!
- Use outline for debugging (not border)
- Background colors make things visible
- Media queries need to override EVERYTHING that changes
- Padding/margin confusion is normal - it gets better with practice
- Keep building, keep debugging, keep learning

---

**Built on:** November 10, 2025  
**Course:** Colt Steele's Web Development Bootcamp 2025  
**Status:** ✅ Complete  
**Confidence Level:** 📈 Growing every day

52 days to 2026. Let's keep going! 🚀