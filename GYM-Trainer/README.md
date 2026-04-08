# Fitness Influencer Coaching Ecosystem - ER Diagram

## Overview
This ER diagram models an online coaching platform where trainers manage clients through programs, subscriptions, sessions, check-ins, and progress tracking.

It is not a gym management system. It is a digital coaching ecosystem.

## My Approach
I designed the schema in layers so the model stays clean and scalable:

1. Identity: users, trainer_profiles, client_profiles
2. Relationship: coach_client_links
3. Product: programs, program_components
4. Commerce: subscriptions, invoices, payments
5. Coaching Flow: sessions, check_ins, trainer_feedbacks
6. Progress: progress_entries, goal_milestones

## Key Design Decisions
- Separated trainer and client data from users for normalization.
- Kept sessions and check-ins separate because they represent different business activities.
- Added coach_client_links to track trainer-client lifecycle over time.
- Used invoices + payments for real billing flow.
- Used progress_entries (metric_code/value/unit) for flexible future metrics.

## Relationship Summary
- One trainer can manage many clients.
- One client can buy multiple programs over time.
- One program can have many client subscriptions.
- One subscription can have many sessions, check-ins, invoices, and payments.
- One check-in can have many progress entries and trainer feedback records.

## Files
- eraser.txt (Eraser schema source)
- Fitness Influencer Coaching Ecosystem.png (exported ER diagram)

## Conclusion
The goal was to keep the model practical, industry-oriented, and easy to extend as the coaching business grows.
