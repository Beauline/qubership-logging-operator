---
name: Bug report
description: Create a report to help us improve
title: "[BUG]"
labels: ["bug", "needs triage"]
assignees: ''
---
body:
  - type: markdown
    attributes:
      value: |
        Thank you for taking the time to report this issue. To help us address it efficiently, please ensure you complete all sections of this form with as much detail as possible. Providing comprehensive context will greatly assist our team in triaging and resolving your concern promptly.
        Before openning a bug report please make sure the issue is not in the list of [existing bugs](https://github.com/Netcracker/qubership-logging-operator/issues?q=is%3Aissue+is%3Aopen+sort%3Aupdated-desc+label%3Abug).
  - type: dropdown
    id: component
    attributes:
      label: Component(s)
      description: Which component(s) does your bug report concern?
      multiple: true
      options:
        - graylog
        - logging-operator
        - fluentbit
        - fluentd
        - events-reader
  - type: textarea
    attributes:
      label: Bug description
      description: Provide a clear and concise description of what the bug is.
      value: |
        ## Description

        ## Steps to Reproduce

        ## Expected Result

        ## Actual Result

    validations:
      required: true
  - type: input
    attributes:
      label: Logging operator version
      description: What version did you use? (e.g., `v0.4.0`, `1eb551b`, etc)
    validations:
      required: true
  - type: textarea
    attributes:
      label: Environment information
      description: Please provide any additional information about your installation.
      value: |
        ## Environment
        - OS: (e.g., "Ubuntu 24.04")
        - Cloud platform: K8S / OCP
  - type: textarea
    attributes:
      label: Log output
      description: |
        Please copy and paste any relevant log output.
      render: shell
  - type: textarea
    attributes:
      label: Additional context
      description: Add any other context about the problem here.
