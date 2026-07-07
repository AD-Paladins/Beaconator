# Rule examples

## Rule 1
id: review-too-old

condition:

    review_age > 72h

severity: medium

message:

    PR waiting for review

## Rule 2
id: epic-out-of-sync

condition:

    platforms_completed < platforms_expected

severity: high
