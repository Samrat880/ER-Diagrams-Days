# LiftGrid Smart Elevator Problem

## Overview
This project models the database design for a smart elevator management system across one or more buildings. The ER diagram captures how elevators move, how requests are served, and how maintenance history is recorded.

## Core Scope
- Building structure: buildings and floors
- Elevator inventory per building
- Floor access mapping for each elevator (zoning)
- Live operational status for each elevator
- Passenger request lifecycle from call to drop-off
- Maintenance logs for service tracking

## Main Entities
- buildings
- floors
- elevators
- elevator_floor_access
- elevator_current_status
- floor_requests
- ride_logs
- maintenance_logs

## Relationship Summary
- One building has many floors and many elevators.
- Elevator-floor access defines which floors each elevator can serve.
- Each elevator has one current status record at a time.
- Floor requests are linked to source and destination floors.
- Ride logs connect requests with the elevator that served them.
- Maintenance logs track technical events per elevator.

## File
The ER source schema is available in Eraser.txt.
