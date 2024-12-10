# MongoDB Aggregation Pipeline: $inc Operator Error
This repository demonstrates a common error when using the `$inc` operator within the `$project` stage of a MongoDB aggregation pipeline. The `$inc` operator is intended to increment a numeric field, but it's misused in the provided example.

## Problem
The original code incorrectly attempts to increment a field using `$inc` within the `$project` stage, applying it to an object, instead of a field name. This leads to unexpected behavior and incorrect results.

## Solution
The corrected code properly uses `$add` to increment the `count` field. The `$add` operator can work directly with existing fields and numerical values.

## How to reproduce
Clone this repository, create a MongoDB collection with sample documents, then run the 'bug.js' script.  Observe the unexpected output. Then, run 'bugSolution.js' to see the corrected aggregation.
