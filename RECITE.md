# Recite Writer patch

This branch carries one change that [Recite](https://github.com/plethu/recite)'s Writer needs, on top
of Copypasta 0.10.2 (`47f5501e3af68ba93e80cda02d94631aec795e63`): a Wayland clipboard constructor
that consumes a display owner, retains it across both clipboard handles, and stops the worker before
releasing the owner. The original raw constructor remains available.

Tests cover constructor errors, borrowed-owner rejection and native display lifetime; native tests
require an owned Wayland compositor. Drop this branch when equivalent upstream behaviour is available
and verified.

Alacritty's contribution policy excludes LLM-generated content. This change was written with LLM
assistance, so it is not proposed upstream in this form.
