# Privacy

## Introduction

Thank you for using FancyNpcs! We take your privacy seriously and are committed to protecting it. This
Privacy Policy explains what data is collected by our plugin, why it is collected, and how it is processed. We do not
collect any personally identifiable information (PII) or sensitive data from users.

## What Data is Collected

The plugin collects a limited set of **anonymous** metrics to help us improve the functionality and performance of the
plugin. The data collected is strictly related to the plugin's performance and usage and does not include any
information that can personally identify you, your server or your players.

The following data is collected:

- **Total number of NPCs**: The total number of NPCs created by the plugin on your server.
- **Update notifications enabled**: Whether update notifications are enabled or muted on your server.
- **Development build usage**: Whether your server is using a development build of the plugin.
- **Commit hash**: A shortened hash of the plugin build used to identify the specific development version.
- **Interaction cooldown**: Average interaction cooldown set for NPCs.
- **Number of NPCs with interaction cooldown greater than 5 minutes**.
- **Number of non-persistent NPCs**: NPCs that are not saved to file and therefore do not persist across server
  restarts.
- **Number of non-player NPCs**: NPCs that are not of the `PLAYER` type.
- **Number of NPCs with attributes**: NPCs that have npc attributes assigned.
- **Number of NPC actions**: The total number of actions assigned to all NPCs.
- **Language**: The language set for the plugin on your server.
- **Feature flags**: Whether specific plugin features (e.g., player-npcs feature flag) are enabled.
- **Plugin version**: When the plugin is updated, the new version is sent to track the adoption of new releases.

These metrics are essential for understanding how servers use the plugin and identifying any issues that may arise in
different environments.

## How Data is Collected

The data is collected via metrics and analytics systems integrated into the plugin. These systems collect the metrics
listed above and send them anonymously to our analytics platform. **No personal data, such as server IP addresses or
unique server identifiers, is collected**!

The plugin only sends data:

- When the plugin is enabled and used on your server.
- When the plugin version is updated.

## Why We Collect This Data

We collect this data to:

- Improve the performance, stability, and functionality of the plugin.
- Understand how servers use certain features.
- Provide better support for both development and release builds.
- Identify and resolve issues related to different configurations and environments.
- Track the adoption of new versions and features.

## Data Retention

The anonymous data we collect is used solely for internal purposes to enhance the plugin and its performance. We do not
share this data with third parties, and no identifiable information is ever stored.

## Opting Out of Data Collection

You can easily opt-out of sending any metrics data. To disable data collection:

1. Open the `FancyAnalytics/config.yml` file in your server’s plugin directory.
2. Set the following option:

```yaml
"send_metrics": false
```

Once this option is set to false, no data will be collected or sent from your server.

## Security

We are committed to ensuring that the data collected remains secure and is only used for the purposes outlined in this
Privacy Policy. The data is transmitted securely and is stored anonymously without any link to specific servers or
users.

## Contact Information

If you have any questions about this Privacy Policy or how the plugin handles data, please feel free to contact us at:

- **Email:** `support@fancyplugins.de`
- **Discord:** [https://discord.gg/ZUgYCEJUEx](https://discord.gg/ZUgYCEJUEx)
- **My personal discord:** `real_oliver`

We are happy to provide additional information about how the data is handled or address any concerns you may have.

## Changes to this Policy

We may update this Privacy Policy from time to time to reflect changes in our data collection practices or legal
obligations. Any updates will be documented in the plugin changelog, and we encourage users to review this policy
periodically.
