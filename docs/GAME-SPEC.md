# Game specification

## Verified current behavior

Skyline Drop is a three-level, portrait-first isometric city puzzle for Android Chrome and desktop Chromium. The player positions a queued district, rotates it, may use an authored Road Remix where available, inspects the board, and drops it. Homes and shops must reach both the road entrance and underground utility hub. Terrain, trees, planning boundaries, and underground bedrock constrain placement.

Surface and underground are separate but aligned views. Roads may share cells where the district rules permit; underground conduits may overlap and merge their directional masks. Non-road surface overlap remains invalid. The always-visible information panel explains metrics and selected terrain, networks, districts, and conduits. The game supports pause, restart, fullscreen, touch controls, three level objectives, victory/loss, and persistent run upgrades.

The visual direction is supplied pixel-art terrain and modern districts presented through Pixi v8/WebGL. Audio is procedural. The game uses local bundled assets only, has no runtime external URLs, and has no documented online, account, or cloud-save requirement.

Accessibility and usability constraints currently evidenced are semantic keyboard/touch actions, portrait framing, clear invalid-placement feedback, layer toggle, and inspectable status information. No undocumented accessibility claims are made.

## Approved constraints and non-goals

This graduation preserves existing rules, balance, story, art direction, controls, level content, and scope. Unlimited Main Street shared-road reuse remains unchanged. No new gameplay systems, online functionality, redesign, or balance changes are approved here.

## Unresolved decisions

Fresh formal Samsung physical evidence is required for the newly generated canonical artifact. Any changes beyond source organization, verification, release automation, or clear build compatibility repair require separate approval.
