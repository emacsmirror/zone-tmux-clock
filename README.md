<!--
SPDX-FileCopyrightText: 2023 Vasilij Schneidermann <mail@vasilij.de>

SPDX-License-Identifier: GPL-3.0-or-later
-->

![][image]

## About

A zone program displaying a textual clock, much like the `clock-mode`
command in tmux.

## Installation

Install manually for the time being.
<!-- Install via `package.el` from [MELPA] or [MELPA Stable]. -->

## Usage

Run `M-x zone-tmux-clock-preview` for a preview (yes, zone doesn't have a
preview command for checking out its programs).

To choose `zone-tmux-clock` as your only zone program, add the
following to your init file:

```elisp
(setq zone-programs [zone-tmux-clock])
```

Then either use `M-x zone` for instant gratification or `M-x
zone-when-idle` to run it after idling.

## Customization

Use `M-x customize-group RET zone-tmux-clock RET` to view the
available knobs. It's possible to change the rendering style and
to use the 12 hour format.

## FAQ

Q: I've found an error, but all Emacs says is that you were zoning out
when writing zone-tmux-clock...

A: I don't know why, but zone bypasses regular Emacs error handling
and displays an useless message instead. Use `M-x
toggle-debug-on-error`, switch to a buffer you don't mind losing, then
`M-: (zone-tmux-clock-progress (current-buffer))` and report a bug
with the backtrace and additional system information (your Emacs
build, operating system, origin and version of the package).

[image]: img/screencast.gif
[MELPA]: https://melpa.org/
[MELPA Stable]: https://stable.melpa.org
