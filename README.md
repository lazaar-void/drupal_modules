# Hello World Drupal Module

## Overview

This is a simple "Hello World" module for Drupal 10/11, created as a demonstration or starting point for custom module development. It provides a basic page and a configurable block.

## Features

*   **Hello World Page:**
    *   Access a simple "Hello, World!" message at the `/hello` path.
    *   Implemented via `Drupal\hello_world\Controller\HelloController`.

*   **Hello Block:**
    *   A custom block that displays a greeting: "Hello, [Name]!".
    *   The `[Name]` can be configured via the block's settings or defaults to 'Stranger' if not set.
    *   Implemented via `Drupal\hello_world\Plugin\Block\HelloBlock`.

## Installation

1.  **Place the module:**
    Place the `hello_world` folder in your Drupal installation's `web/modules/custom` directory.

    ```
    /path/to/your/drupal/root/web/modules/custom/hello_world
    ```

2.  **Enable the module:**
    Navigate to `Extend` (or `/admin/modules`) in your Drupal admin interface and enable the "Hello World" module. You can also enable it using Drush:

    ```bash
    drush en hello_world
    ```

## Usage

### Hello World Page

After enabling the module, you can visit `/hello` in your browser to see the "Hello, World!" message.

### Hello Block

1.  Navigate to `Structure` > `Block layout` (or `/admin/structure/block`).
2.  Click "Place block" in the desired region (e.g., "Sidebar First" or "Content").
3.  Search for "Hello block" and click "Place block".
4.  (Optional) Configure the block:
    *   You can set a custom title.
    *   The block might have a field to customize the name it greets.
5.  Save the block configuration.
6.  The "Hello, [Name]!" message will now appear in the chosen region on your site.

## Configuration

The "Hello block" can be configured via its block settings form in the Drupal administration.
The module can also pull a default name from `hello_world.settings.yml`. (which is my own name, Hamza Lazaar, in this case.)

