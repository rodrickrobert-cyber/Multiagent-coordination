# Multi-Agent Coordination

A collaborative environment for capturing human and AI teamwork as training data for multi-agent coordination.

## Overview

AI agents are becoming increasingly capable at completing tasks individually, but complex work often requires multiple agents and humans to coordinate effectively.

This project explores how teams divide work, delegate tasks, share information, manage dependencies, resolve conflicting information, verify each other's work, and recover from mistakes.

The platform allows the same coordination-dependent task to be completed by:

- Human-only teams
- Human + AI teams
- AI-agent-only teams

The goal is to capture the collaboration process as structured trajectories that can be used for training and evaluating multi-agent systems.

## How It Works

A task is divided across multiple participants with different roles, capabilities, and information.

No participant necessarily has everything required to solve the task alone.

Participants must communicate and coordinate to reach the final outcome.

During an experiment, the system records events such as:

- Messages
- Information requests
- Information sharing
- Task delegation
- Agent handoffs
- Tool usage
- Artifact changes
- Conflicts
- Reviews
- Corrections
- Human interventions
- Final outcomes

These events are combined into a structured coordination trajectory.

## Example

A financial analysis task might contain three participants:

**Financial Analyst**
Has access to financial statements.

**Market Analyst**
Has access to market and competitor research.

**Risk Analyst**
Has access to legal and risk information.

Some information may be incomplete or contradictory.

The participants must share information, identify conflicts, verify assumptions, and combine their findings to complete the task.

The same task can then be run with different team configurations to compare how humans and AI agents coordinate.

## Structured Trajectories

A simplified event might look like:

{
  "event_id": "evt_001",
  "experiment_id": "exp_001",
  "actor_type": "agent",
  "actor_role": "market_analyst",
  "event_type": "INFORMATION_REQUESTED",
  "recipient": "financial_analyst",
  "content": {
    "question": "Can you verify the reported revenue growth?"
  },
  "timestamp": "..."
}

Completed experiments can be replayed, annotated, compared, and exported as structured data.

## MVP

The initial MVP focuses on:

1. Creating coordination-dependent tasks
2. Assigning humans and AI agents different roles and private information
3. Providing a shared collaboration workspace
4. Recording collaboration as structured events
5. Replaying complete coordination trajectories
6. Annotating coordination successes and failures
7. Comparing human, human-agent, and agent-only teams
8. Exporting trajectories as JSON

## Hypothesis

Our core hypothesis is that expert human-team collaboration contains coordination signals that can improve multi-agent systems beyond what can be learned from individual demonstrations or synthetic agent interactions alone.

The MVP is designed to test that hypothesis.

## Status

Early-stage prototype under active development.
