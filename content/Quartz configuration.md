---
created: 2025-02-11
modified: 2026-02-17
---
The site [docs.louisnel.co.nz](https://docs.louisnel.co.nz) is built on [Quartz]() v4. The source code is available [here]().

# Configuration
Most configuration of this site is done through the standard `quartz.layout.ts` and `quartz.config.ts` files using existing components from the upstream repository.

## `quartz.config.ts`

``` typescript
//Selected changes to the default configuration
typography: {
	header: "Open sans",
	body: "Open sans",
	code: "Source Code Pro",
}
	
```

## `quartz.layout.ts`

```typescript
Footer: Component.Footer({
	links: {
		Archive: "https://louisnel.co.nz",
		"View on GitHub": "https://github.com/eighteeneightythree/docs",
}

left: [
Component.DesktopOnly(
	Component.RecentNotes({
		showTags: false,
		limit: 3
	}),
),
Component.LeftFooter({
	links: {
		"Tag Index": "/tags",
		//Archive: "https://louisnel.co.nz/archive",
	},
}),
]
```

# Content

The entire ZK Vault is provided to Quartz through a [[ln --help|symlink]]. This is done to allow Obsidian to use iCloud to keep my devices in sync. It also means the content can be edited from both devices and potentially directly from GitHub though I haven't tested how this behaves with [[Quartz sync command|quartz sync]].


# Links:

---
#quartz 