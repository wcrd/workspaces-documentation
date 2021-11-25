# Scaling

{% hint style="danger" %}
This is being updated currently. This section will be completed once the changes are deployed.
{% endhint %}

![Scale to fit, scale to workspace, fixed size, dynamic scaling - set your workspace scale preferences](<../.gitbook/assets/image (47).png>)

## Overview

Workspaces offers a number of scaling modes to suit any use case and screen. The core scaling modes are:

| Mode  | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| ----- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Auto  | Tiles grow horizontally to fill screen width. No scaling of content. No vertical scaling.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Fixed | <p>All fixed scaling scales the tiles and content proportionally.</p><p><strong></strong></p><p><strong>Fixed no scale</strong></p><p>Workspace will not scale. Workspace will be centered in view if screen is larger that workspace dimensions.</p><p><strong></strong></p><p><strong>Full size scale</strong></p><p>Entire workspace will scale proportionally to fit within the screen.</p><p></p><p><strong>Width scale</strong></p><p>Workspace will scale proportionally to fit the width of the screen. </p><p></p><p><strong>Aspect ratio scale</strong></p><p>Workspace will scale proportionally to a given size and aspect ratio.</p> |

{% hint style="success" %}
The scaling mode you are most familiar with will be the '**Aspect ratio scale**'. This will allow you to build a workspace and have it look the same on all screens.
{% endhint %}

Scaling modes are described in detail below.



## Auto Scaling

Auto scaling grows and shrinks the width of the Tiles to fit the screen width. No vertical scaling occurs. No content scaling occurs, apart from auto redrawing of chart content (which happens by default). Font sizes will remain constant using this scaling method. The workspace will look slightly different on every screen it is shown on.

{% hint style="info" %}
Auto scaling works well when you want the content size to be fixed, but want the workspace to grow to fill the screen width.
{% endhint %}

{% hint style="warning" %}
Auto scaling causes tiles to reflow, and at screen size extremities may cause some overflow behavior.&#x20;
{% endhint %}

See the GIF below to see how 'auto' scaling works.

## Fixed Scaling
