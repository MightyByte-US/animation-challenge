markdownCopy# Rive Animation Challenge: Dragon Breathing Animation

## Project Overview
Create a dragon character animation in Rive that shows natural breathing cycle with belly movement, controlled by drag gesture values.

## Design Assets
Figma reference: [Dragon Animation Design](https://www.figma.com/design/St55OhD31W5P0tlhtPDkLA/Rive-animation-challenge?node-id=0-1&p=f&t=VOrzWVqy1FLWwS8z-0)

The Figma file contains:
- Dragon character design
- Animation states reference
- Component structure

## Animation Requirements

### Static State
- Default dragon illustration
- No animation
- Normal belly size

### Breath In (Left Drag)
- Belly gradually expands based on drag progress
- Air particles flowing into nose
- Subtle wing and tail movement
- All elements synchronized to drag progress (0-1)

### Breath Out/Fire (Right Drag)
- Belly gradually decreases to original size 
- Fire breathing effect from mouth
- Subtle wing and tail movement
- Effect intensity based on drag speed

## Technical Requirements

### State Machine Controls
- Input for breath in progress (0-1)
 * Controls belly expansion
 * Controls particle/air flow
- Input for breath out/fire intensity
 * Controls belly contraction
 * Controls fire effect
- Smooth transitions between states

### Animation Focus
- Natural belly expansion/contraction
- Fluid particle/fire effects  
- Synchronized secondary movements

## Deliverables

### 1. .riv file including:
- Dragon character with separate belly layer
- Particle/fire effects
- Configured state machine with named inputs

### 2. Brief documentation:
- Input parameters and their ranges
- Basic state machine structure

## Evaluation Criteria
- Naturalness of belly movement
- Quality of particle/fire effects
- Smoothness of state transitions  
- Response to input values

_Note: We will handle the React Native integration internally - focus on creating a well-structured Rive animation that responds to external input values._
