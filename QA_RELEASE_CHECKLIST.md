# QA Implementation & Release Checklist

Use this checklist for website changes, redesigns, fixes, refactors, and release-readiness reviews. Mark items PASS, FAIL, BLOCKED, NOT APPLICABLE, or UNABLE TO VERIFY. Never mark PASS without supporting evidence.

## 1. Request and Scope
- [ ] Exact user-requested change is restated and understood.
- [ ] Elements that must remain unchanged are identified.
- [ ] Scope is limited to the smallest necessary files/components.
- [ ] Any requested screenshot/recording/reference is treated as target evidence.
- [ ] No unrelated redesign/refactor is bundled without authorization.

## 2. Source and Version Control
- [ ] Latest repository state was fetched before editing.
- [ ] Fresh blob/content SHA was fetched for every file changed.
- [ ] No parallel writes were made to the same file.
- [ ] Commit message clearly describes the change.
- [ ] Temporary workflows/helper files were removed when no longer needed.
- [ ] Changed files were re-fetched or commit-inspected after writing.

## 3. Targeted Change / Preservation
- [ ] Requested element changed exactly as requested.
- [ ] Parent/adjacent component was not accidentally removed.
- [ ] Existing working controls remain unless removal was requested.
- [ ] Navigation, links, and IDs remain valid.
- [ ] Removed sections no longer have dead navigation or references.
- [ ] User corrections from prior iterations were incorporated.

## 4. Functional Regression
- [ ] Main component renders.
- [ ] Primary interaction works.
- [ ] Secondary controls work.
- [ ] Error/empty/loading states remain sensible.
- [ ] Keyboard interaction works where applicable.
- [ ] Touch/swipe interaction works where applicable.
- [ ] No obvious new runtime/console errors are evidenced.
- [ ] No duplicate IDs or broken ARIA relationships were introduced.

## 5. Media / Carousel
- [ ] Media loads successfully.
- [ ] Native video controls are present when expected.
- [ ] Play/pause works.
- [ ] Seek/timeline works.
- [ ] Volume/mute/unmute works.
- [ ] Fullscreen works where supported.
- [ ] Autoplay is muted when required by browser policy.
- [ ] Manual pause does not trigger unexpected navigation.
- [ ] End-of-video auto-advance works only when intended.
- [ ] Portrait, landscape, and square media preserve intended composition.
- [ ] Inactive items use lightweight posters/thumbnails when scale requires it.
- [ ] Overlays do not block native controls.

## 6. Responsive / Mobile
- [ ] Large desktop reviewed when possible.
- [ ] Desktop/laptop reviewed when possible.
- [ ] Tablet landscape reviewed when possible.
- [ ] Tablet portrait reviewed when possible.
- [ ] Large mobile reviewed when possible.
- [ ] Standard/small mobile reviewed when possible.
- [ ] No unintended horizontal scrolling.
- [ ] No clipped controls or text.
- [ ] Tap targets are practical.
- [ ] Hover-only information has a touch equivalent.

## 7. Accessibility
- [ ] Skip navigation remains functional where present.
- [ ] Heading hierarchy remains logical.
- [ ] Focus indicators are visible.
- [ ] Keyboard order is usable.
- [ ] Controls have accessible names.
- [ ] Essential information is not color-only.
- [ ] Reduced-motion preference is respected.
- [ ] Autoplay/automatic transitions are reduced or disabled when appropriate.
- [ ] Media controls remain operable.
- [ ] Touch users can access information otherwise shown on hover.

## 8. Conversion / CTA
- [ ] Primary CTA is visually identifiable.
- [ ] CTA label matches its real action.
- [ ] CTA destination exists.
- [ ] User can complete the intended contact/booking/purchase/submission journey.
- [ ] No decorative dead-end CTA remains.
- [ ] No fake contact details were invented.
- [ ] No fake success message is shown without a real successful action.
- [ ] Success/failure state exists where submission is involved.

## 9. Content / Trust
- [ ] Copy is clear and current.
- [ ] No placeholder production copy remains.
- [ ] No unsupported client/testimonial/certification/metric claims were added.
- [ ] Proof statements are traceable to reliable source evidence.
- [ ] Removed/outdated content is not still referenced elsewhere.

## 10. SEO
- [ ] One logical H1 exists.
- [ ] Title/meta description remain appropriate.
- [ ] Canonical is correct for production.
- [ ] Heading hierarchy remains coherent.
- [ ] Social metadata remains valid.
- [ ] Social preview asset is suitable.
- [ ] robots.txt reviewed where applicable.
- [ ] sitemap.xml reviewed where applicable.
- [ ] Structured data remains factual and valid in scope.

## 11. Performance
- [ ] No unnecessary polling was introduced.
- [ ] Large inactive media is not eagerly loaded without need.
- [ ] Images/video are appropriately sized/compressed where practical.
- [ ] Third-party assets are limited to necessary dependencies.
- [ ] Removed components do not leave dead CSS/JS loaded.
- [ ] No obvious new layout-shift risk was introduced.
- [ ] Performance claims are not made without measurement.

## 12. Maintainability
- [ ] New CSS does not create avoidable override layers.
- [ ] Runtime-injected CSS is justified if used.
- [ ] Dead code was removed only after reference checks.
- [ ] No obsolete component data remains unintentionally.
- [ ] Third-party icon/media URLs were verified or have fallbacks.
- [ ] Exact brand assets are sourced appropriately when required.

## 13. Privacy / Security
- [ ] No secrets or sensitive configuration were exposed.
- [ ] HTTPS/mixed-content status reviewed when live evidence is available.
- [ ] New forms disclose data use where relevant.
- [ ] Cookie/consent UI is added only when actually required.
- [ ] Security/privacy claims are not made without evidence.

## 14. Deployment Truth
- [ ] SOURCE UPDATED status recorded.
- [ ] CI / BUILD VERIFIED status recorded if applicable.
- [ ] DEPLOYMENT OBSERVED status recorded if available.
- [ ] LIVE FUNCTION VERIFIED status recorded only after real live verification.
- [ ] Any unavailable verification is explicitly marked BLOCKED / UNABLE TO VERIFY.

## 15. Evidence Log
- [ ] Evidence source(s) recorded.
- [ ] Evidence type recorded: live_render, functional_interaction, page_source, HTTP_response, screenshot, screen_recording, repository_source, user_statement, third_party_measurement, or inference.
- [ ] Finding/change supported by evidence.
- [ ] Confidence recorded where meaningful.
- [ ] Limitations/unverified areas recorded.
- [ ] Commit SHA recorded for implementation work.
- [ ] Deployment status recorded separately from source status.

## 16. Release Gate
A change is RELEASE-READY only when:
- no unresolved P0/P1 issue remains within the changed scope unless explicitly accepted,
- critical user journey works or is clearly blocked and not falsely marked as working,
- requested behavior is preserved without adjacent regression,
- accessibility-critical controls remain usable,
- conversion-critical endpoints are real and functional,
- deployment state is truthfully reported,
- residual risks and blocked verification are documented.

Permitted final statuses:
- READY FOR RELEASE
- READY WITH MINOR FIXES
- CONDITIONAL RELEASE
- NOT READY FOR RELEASE
- UNABLE TO ASSESS / BLOCKED
