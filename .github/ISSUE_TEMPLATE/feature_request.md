name: Feature request
description: Suggest a new checklist item, section, or scoring criterion
labels: [enhancement]
body:
  - type: textarea
    id: problem
    attributes:
      label: What evaluation gap does this address?
      description: Describe what aspect of browser agent evaluation is currently missing from the checklist.
    validations:
      required: true
  - type: textarea
    id: solution
    attributes:
      label: Proposed checklist item(s)
      description: Provide the concrete item(s) you'd add. Each should be observable and independently scorable.
    validations:
      required: true
  - type: dropdown
    id: section
    attributes:
      label: Which section?
      options:
        - Authentication
        - DOM complexity
        - Reliability
        - Final-state proof
        - Security
        - New section (describe below)
    validations:
      required: true
  - type: textarea
    id: additional
    attributes:
      label: Additional context
