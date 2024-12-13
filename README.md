# Next.js 15 Async/Await Error Handling Bug

This repository demonstrates a common bug in Next.js 15 related to unhandled promise rejections within `getStaticProps` or `getServerSideProps` functions.  The bug involves the use of `async/await` with external API calls or database interactions.  Improper error handling can lead to unexpected application behavior or crashes.

## Bug Description

When using `async/await` within `getStaticProps` or `getServerSideProps`, neglecting proper error handling can cause unhandled promise rejections. These rejections may not be immediately apparent during development, leading to difficult-to-debug issues in production.

## Solution

The solution involves using `try...catch` blocks to handle potential errors during asynchronous operations.  This ensures that errors are caught, logged, and potentially gracefully handled, preventing application crashes or unexpected behavior.

## Reproduction

1. Clone this repository.
2. Install dependencies: `npm install`
3. Run the development server: `npm run dev`
4. Observe the console for errors (in the `bug.js` example).  The `bugSolution.js` example demonstrates the corrected code.
