# Travel Department / Outbounder

## Consistent interfaces across a connected travel platform

My work on this team project spans shared React components and the applications that consume them: content websites, booking checkout, booking management, gift vouchers, and travel-agent login.

The challenge was to translate Outbounder designs into a consistent experience within an established platform serving multiple brands. A shared header, form control, or spacing change could affect several customer journeys.

### My contribution

I implemented and refined brand-specific typography, spacing, navigation, holiday cards, hotel information, and form controls. I also made application-level booking-interface refinements and coordinated shared-component updates across consuming repositories.

The stack includes React, Next.js, TypeScript, SCSS, Tailwind CSS, and a Strapi-backed content application. Shared UI is distributed through Git submodules.

### Decision: reuse structure, accommodate brand differences

The shared component layer supports brand-specific variants. My changes applied Outbounder styling while retaining the surrounding multi-brand structure. Form-control refinements included room for validation messages so longer feedback did not spill outside the field container.

Keeping shared changes and application updates aligned was part of delivery: updating the shared repository alone does not update the version consumed by each application.

### Example: a hero layout in a short mobile viewport

A reported in-app browser issue exposed a weakness in the homepage hero. Its viewport-based height could become smaller than the space needed by the fixed header, bottom-anchored content, slider controls, and search bar. The heading could overlap the header.

I added a minimum-height floor to the responsive hero rules while retaining viewport-based sizing where it provided enough space. Shorter viewports can scroll instead of forcing the content into an undersized container. Both the outer banner and image container use corresponding sizing rules.

The tradeoff is intentional: some screens show less of the following section initially, but the hero content has room to remain usable.

### Outcome and verification limits

The repository records the shared changes and their propagation across applications. I do not have a measured conversion uplift or complete device-test report to attribute to this change.

A regression check should exercise narrow and short viewports, long headings, the smallest mobile breakpoint, and other brands consuming these components. This is a proposed verification plan, not a claim that those checks were performed for this case study.

### What this demonstrates

- Translating detailed designs into reusable UI.
- Debugging viewport units, fixed headers, and content positioning.
- Delivering changes across shared-component dependencies.

This was a team project. This account describes my frontend contributions, not sole ownership of the platform.
