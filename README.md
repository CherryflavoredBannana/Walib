# WaLib

Walib (Fabric Dynamic Mod Adapter) is a compatibility layer that allows **Fabric-based Minecraft servers to run plugins that would normally only work on platforms like Bukkit or Spigot**. It bridges the gap between Fabric’s modding environment and plugin ecosystems that rely on non-Fabric server behavior.

Many existing plugins depend on internal server mechanics, packet handling, or platform-specific hooks that Fabric does not natively expose. WaLib handles this complexity internally, enabling these plugins to run without requiring extensive rewrites or unsafe manual patches.

---

## Features

* Run non-Fabric plugins on Fabric servers
* Provides a stable compatibility bridge for plugin-based APIs
* Reduces plugin conflicts caused by overlapping internal hooks
* Abstracts away obfuscated and version-specific Minecraft internals
* Designed for long-term maintainability across Minecraft versions

---

## Motivation

Fabric offers excellent performance and modding flexibility, but its ecosystem is largely separate from traditional plugin platforms. This forces server owners and developers to choose between Fabric mods and established plugins.

WaLib removes this limitation by adapting plugin expectations to Fabric’s runtime environment, making it possible to combine both approaches in a single server setup.

---

## How It Works

WaLib acts as an intermediary layer between Fabric and plugin logic. It translates platform-specific behavior into forms that Fabric can support, while preventing plugins from directly modifying fragile internal classes.

Instead of each plugin implementing its own hooks, WaLib centralizes this logic, improving stability and reducing the risk of crashes or hard-to-debug behavior.

---

## Compatibility

WaLib is built with compatibility as a primary goal. Internal server structures are resolved dynamically at runtime rather than hardcoded, allowing WaLib to remain resilient to obfuscation and internal changes between Minecraft versions.

Most updates require minimal maintenance, typically limited to bug fixes or feature improvements rather than breaking changes.

---

## Use Cases

* Running legacy or Bukkit/Spigot-style plugins on Fabric
* Migrating existing servers to Fabric without losing plugin functionality
* Combining Fabric mods with traditional plugin-based features
* Reducing maintenance overhead for cross-platform plugin support

---

## Limitations

* Not all plugins are guaranteed to be fully compatible
* Plugins that rely on deeply platform-specific behavior may require additional adaptation
* Performance may vary depending on plugin complexity

---

## Project Goals

* Maximize plugin compatibility on Fabric
* Provide a stable, centralized integration layer
* Minimize version-specific breakage
* Enable mixed mod + plugin server environments

---

## License

This project is licensed under the terms of its respective license. See the `LICENSE` file for details.
