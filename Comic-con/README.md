# Comic-Con India Parking System ERD

Production-style ER diagram for a multi-zone Comic-Con parking system.

## Scope
- Vehicle and vehicle category management
- Zone and level based parking layout
- Spot categories and reserved access handling
- Entry/exit session tracking with timestamps
- Ticket issuance per parking session
- Tariff and payment tracking
- Live occupancy support (currently parked vehicles)

## Main Entities
- vehicles
- vehicle_categories
- access_categories
- zones
- parking_spots
- spot_categories
- parking_sessions
- tickets
- tariffs
- payments

## Relationship Highlights
- One vehicle can have many parking sessions
- One parking spot can be reused across many sessions over time
- One zone contains many parking spots
- One session has one ticket and one payment record

## Files in This Folder
- `eraser.txt` - ERD source (Eraser format)
- `Comic-Con-Parking-Problem.png` - exported diagram image

## Notes
This design is normalized and suitable for production-style implementation and assignment evaluation.
