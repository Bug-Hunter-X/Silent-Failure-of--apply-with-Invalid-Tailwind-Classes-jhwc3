# Silent Failure of @apply with Invalid Tailwind Classes

This repository demonstrates a subtle error that can occur when using Tailwind CSS's `@apply` directive with an invalid or misspelled utility class.  The issue is that Tailwind doesn't throw an error when an invalid class is used; instead, the class is simply ignored, leading to unexpected styling and difficult-to-debug issues.

## Problem

When you use `@apply` with a class that doesn't exist in your Tailwind configuration, the compiler won't report an error.  This can lead to situations where your CSS isn't applied as expected, and tracking down the source of the problem can be challenging.

## Solution

The solution involves carefully reviewing your class names to ensure they match the available Tailwind classes in your configuration.  Using a linter or IDE with Tailwind support can help prevent this issue by highlighting potential errors during development.  Furthermore, consistently using your IDE's auto-completion to avoid typos is highly recommended.

## Reproduction

1. Clone this repository.
2. Open `bug.html` in your browser.  Notice that the text is not blue, demonstrating that `text-not-found` is ignored.
3. Open `bugSolution.html` to see the corrected version.