Module Name: Index Moderation State

Description
The "Index Moderation State" module enhances Drupal's content moderation capabilities by indexing and exposing the moderation state of the latest revision of entities. This allows developers and site builders to programmatically access and utilize the current moderation state of content entities, ensuring accurate representation and integration with external systems or custom functionality.

Features
Automatically indexes and exposes the moderation state of the latest revision of entities.
Provides API functions to retrieve and manage moderation state information programmatically.
Enhances content moderation workflows by ensuring accurate state representation across revisions.

Requirements
Drupal 8 or later
Content Moderation module enabled
Installation
Download and install the module in your Drupal modules directory (modules or modules/custom).
Enable the module through the Drupal administrative interface or using Drush:
drush en index_moderation_state_of_latest_revision -y

Configuration
No additional configuration is required. The module integrates seamlessly with Drupal's content moderation framework.
Usage
Once installed and enabled, the module automatically indexes the moderation state of the latest revision for entities that have content moderation enabled.
Developers can use the provided API functions to retrieve the moderation state programmatically and integrate it into custom modules or external systems.

Example Usage:
// Get the moderation state of a node's latest revision.
$node = \Drupal\node\Entity\Node::load($node_id);
$latest_revision_id = $node->get('vid')->value;
$latest_revision = \Drupal::entityTypeManager()->getStorage('node')->loadRevision($latest_revision_id);
$moderation_state = $latest_revision->moderation_state->value;

License
This module is licensed under the GNU General Public License, version 2 or later.

Maintainers
Mohammad

Support
For bug reports, feature requests, or general questions, please create an issue in the module's issue queue.

Notes:
**Replace placeholders (Module Name, Your Name, example.com, node_id, etc.) with actual values and URLs relevant to your module and project.
**Provide specific examples or additional usage scenarios based on your module’s functionality and intended audience.
**Include relevant links to documentation, issue queues, or project repositories for further information and support.