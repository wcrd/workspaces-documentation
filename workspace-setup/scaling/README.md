# Scaling

![Scale to fit, scale to workspace, fixed size, dynamic scaling - set your workspace scale preferences](<../../.gitbook/assets/image (47) (1).png>)

## Overview

Workspaces offers a number of scaling modes to suit any use case and screen. The core scaling modes are:

| Mode                      | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| ------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [Auto](./#auto-scaling)   | Tiles grow horizontally to fill screen width. No scaling of content. No vertical scaling.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [Fixed](./#fixed-scaling) | <p>All fixed scaling scales the tiles and content proportionally.</p><p><strong></strong></p><p><strong>Fixed (no scale)</strong></p><p>Workspace will not scale. It is always shown at design size. Workspace will be centered in view if screen is larger that workspace dimensions.</p><p></p><p><strong>Scale to Width</strong></p><p>Workspace will scale proportionally to fit the width of the screen. </p><p></p><p><strong>Scale to Screen</strong></p><p>Workspace will scale proportionally to a given size and aspect ratio.</p><p></p><p><strong>Full size scale</strong></p><p>Entire workspace will scale proportionally to fit within the screen. This is a special mode of the <em><strong>Scale to Screen</strong></em> mode.</p> |

{% hint style="success" %}
The scaling mode you are most familiar with will be the '**Scale to Screen**'. This will allow you to build a workspace and have it look the same on all screens.
{% endhint %}

Scaling modes are described in detail below. Information about how to set the scaling behaviour can be found [here](settings.md).&#x20;

## Auto Scaling

Auto scaling grows and shrinks the _**width**_ of the Tiles to fit the screen width. No vertical scaling occurs and no content scaling occurs, apart from auto redrawing of chart content (which happens by default). Font sizes will remain constant using this scaling method. The workspace will look slightly different on every screen it is shown on.

{% hint style="info" %}
Auto scaling works well when you want the content size to be fixed, but want the workspace to grow to fill the screen width.
{% endhint %}

{% hint style="warning" %}
Auto scaling causes tiles to reflow, and at screen size extremities may cause some overflow behavior.&#x20;
{% endhint %}

See the GIF below to see how 'auto' scaling works.

![](../../.gitbook/assets/scaling\_auto.webp)

Notice that the tile content is unchanged, but the width of each tile is changing as the width of the window changes.

{% hint style="info" %}
To set the workspace to Auto Scale, select the '**auto**' option in the Resolution settings for the workspace. See [here](./#undefined) for more information.
{% endhint %}

## Fixed Scaling

There are a number of fixed scaling modes to meet all display use cases. The term _**fixed**_ refers to the fact that these workspaces do not alter the layout of the tiles; that is workspace will always be laid out exactly as the User built it no matter the screen it is displayed on.&#x20;

All 'Fixed Scale' workspaces begin the same way.

{% hint style="info" %}
To set the workspace to a Fixed scaling mode, select a resolution (width) in the Resolution drop down settings for the workspace. The other fixed scaling options will appear once this is done. See [here ](./#undefined)for more information.
{% endhint %}

### Fixed (no scaling)

This is the most basic of the fixed scale modes. The User simply sets the canvas width they wish to build upon. (Note that all our canvases have infinite height - the User can keep adding tiles vertically as needed). The workspace will always be shown at this fixed width and will never scale.

Once completed, if the workspace is displayed on a screen that is too large, then the workspace will be centered. If it is displayed on a screen that is too small, it will overflow. This is displayed in the images below - notice that the workspace is always shown at its designed size.

![Fixed size workspace shown in window with same size](<../../.gitbook/assets/image (34).png>)

![Fixed size workspace shown in window that is much wider. Workspace is centered in the screen, but the workspace has not been scaled to fit.](<../../.gitbook/assets/image (36).png>)

![Fixed size workspace shown in window that is not wide enough. Workspace is cut-off, with a horizontal scroll bar appearing at the bottom of the screen. The workspace has not been scaled to fit.](<../../.gitbook/assets/image (47).png>)

{% hint style="info" %}
After selection a resolution (as per above), to set the workspace as **Fixed (no scale)** select the '**fixed**' option from the Scaling Mode drop-down.
{% endhint %}

### Scale to Width

The workspace will scale proportionally to fit the width of the screen. It only scales for screen width - screen height is ignored.

![The workspace scales so that the full width of the workspace is shown. It gives no consideration to the vertical space available. ](../../.gitbook/assets/scaling\_width.webp)

{% hint style="info" %}
After selection a resolution (as per above), to set the workspace as **Scale to Width** select the '**Scale to Width**' option from the Scaling Mode drop-down.
{% endhint %}

### Scale to Screen

{% hint style="info" %}
After selection a resolution (as per above), to set the workspace as **Scale to Screen** select the '**Scale to Screen**' option from the Scaling Mode drop-down, then set the canvas size that you want the screen to always see using the Aspect Ratio drop-down.
{% endhint %}

### Full Size Scale

## How to set the Workspace scaling mode
