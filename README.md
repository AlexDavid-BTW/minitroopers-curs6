
# Maintenance Task Service – Requirements

## Overview
BMW Service Engineering wants a tiny internal service that manages **Maintenance Tasks**.  
Each task refers to work done on a car identified by its **VIN (Vehicle Identification Number)**.

For now, this service does not talk to a database — everything is stored **in memory** so we can move quickly.

Later, the team will replace the in‑memory storage with a **real H2 database**, without rewriting the entire application.  
The code should be structured so this swap is possible with minimal changes.

## MaintenanceTask Object
A `MaintenanceTask` must contain:

- `vin`
- `type` (`"OIL_CHANGE"`, `"BRAKE_INSPECTION"`)
- `status` (`"NEW"`, `"IN_PROGRESS"`, `"DONE"`)
- `notes` (optional string)

## Functional Requirements
The service must support:

### Create a task
Create a new maintenance task for a given VIN.

### Update a task’s status
Change the lifecycle state of a task.

### Add or update notes
Add or modify the notes field of a task.

### Get a task by ID
Return the details for a specific task.

### List all tasks
Return all recorded tasks.

### List tasks by VIN
Return tasks associated with a particular VIN.
