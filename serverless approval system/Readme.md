#Serverless Certification Approval System (AWS)

A serverless workflow that automates certification approval requests using AWS managed services. This project demonstrates secure, scalable, event‑driven architecture design.

##Architecture Overview

Amazon DynamoDB — Stores certification requests with unique request IDs.
AWS IAM — Role with permissions for DynamoDB, Step Functions, and CloudWatch.
AWS Lambda — Four Python functions handle request submission, manager notifications, approvals, and status checks.
AWS Step Functions — Orchestrates the approval workflow with human approval steps.
Amazon API Gateway — Exposes REST endpoints for external clients.
Amazon CloudWatch — Provides logging and monitoring for debugging and visibility.

##Features
Submit certification requests via API.
Notify managers with approval tokens.
Approve or reject requests securely.
Track request status in real time.
End‑to‑end logging and monitoring.

##API Endpoints
POST /request → SubmitRequestFunction
POST /approval → HandleApprovalFunction
GET /request/{requestId} → CheckStatusFunction

##Verification Workflow
Submit a request → DynamoDB entry created, Step Functions execution started.
Manager notified → Approval token logged in CloudWatch.
Approve/Reject → Decision recorded, workflow updated.
Check status → API returns current request state.

##Troubleshooting
Task Timed Out → Ensure State Machine is Standard, not Express (Express has 5‑minute limit).
