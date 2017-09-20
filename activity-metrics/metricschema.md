# CHAOSS Metric Schema Document
## Version 0.00001

**Metrics Document: [required | one]**
```
Date Generated: [required | one]
Schema Version: [required | one]
Document License: [required | one]
Document Creator: [required | one]
Tool Creator: [required | many]
Reviewer: [required | many]
Date Reviewed: [required | one]
```

**Target Repository: [required | one]**
```
URL: [required | one]
Size: [required | one]
Owners: [required | one]
Parent URL counts: [required | many]
Dependency URL counts: [required | many]
Repository Age / Date of Creation: [required | one]
Package Source Name / Version: [required | one]
SHA-256 of Repository: [required | one]
```

**Metrics (Thought 1): [required | many]**
```
  Metric Category: [required | one]
  Metric Name: [required | one]
  Current Data: [required | many]
    Values/Key Value Pairs: [required | many]
      Key/Name: [required | one]
      Value: [required | one]
  Historical Data: [required | many]
    Date Range: [required | one]
      Values: [required | many]
      Key/Name: [required | one]
      Value: [required | one]
```

**Metrics (Thought 2): [required | many]**
```
  Metric Category:[required | one]
  Metric Name:[required | one]
  Format
    Displayable: [required | one]
    Display Name: [required | many]
    Date Range: [required | one]
    Values: [required | many]
      Key/Name: [required | one]
```
