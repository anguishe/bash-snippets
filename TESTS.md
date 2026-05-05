# BashSnippets — Manual Test Checklist

## After Every Prompt — Open index.html in browser (file:// is fine)

### Canvas Test (after Prompt A)
- [ ] Dark hero background visible with moving green particles
- [ ] Particles look like characters, not dots
- [ ] Spiral wireframe vortex visible behind particles
- [ ] Moving mouse pulls particles slightly toward cursor
- [ ] Existing h1, badge, and CTA buttons are visible and clickable above canvas
- [ ] Nav still visible and functional
- [ ] No console errors (open DevTools → Console)

### Mobile Simulation Test (after Prompt A)
- [ ] Open DevTools → Toggle device toolbar → set to iPhone 12 (390px)
- [ ] Canvas still renders (particle count will be lower)
- [ ] No layout breakage
- [ ] CTA buttons still tappable

### Text Layer Test (after Prompt B)
- [ ] Hero text fades in on page load (not instant)
- [ ] Green word has glow pulse animation
- [ ] Badge animates in first
- [ ] h1, p, and CTAs stagger in sequence

### Cards Test (after Prompt C)
- [ ] Scroll down — cards animate in as they enter viewport
- [ ] Cards stagger (not all at once)
- [ ] Hover on card shows green left-border glow
- [ ] Hero canvas unaffected

### Performance Test (after Prompt D)
- [ ] Open DevTools → Performance tab → Record 5s → Stop
- [ ] No dropped frames (green bars in timeline)
- [ ] Tab away and back — canvas pauses/resumes (check via console.log if needed)
- [ ] Throttle CPU to 4x slowdown in DevTools — site still usable