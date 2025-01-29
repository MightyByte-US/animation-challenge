# Rive Animation Challenge: Dragon Breathing Animation

## Project Overview
Create a dragon character animation in Rive that shows natural breathing cycle with belly movement, controlled by drag gesture values.

## Design Assets
Figma reference: [Dragon Animation Design](https://www.figma.com/design/St55OhD31W5P0tlhtPDkLA/Rive-animation-challenge?node-id=0-1&p=f&t=VOrzWVqy1FLWwS8z-0)

The Figma file contains:
- Dragon character design
- Animation states reference
- Component structure

### Static State
- Default dragon illustration in resting position
- No animation
- Normal belly size

### Breath In (Left Drag)
- **Belly Animation:**
  * Gradual, organic expansion from center
  * Size increase proportional to drag distance
  * Smooth deformation without sharp edges

### Breath Out/Fire (Right Drag)
- **Belly Animation:**
  * Natural contraction back to original size
  * Smooth, elastic-like movement
  * Speed matches drag velocity
- **Fire Effect:**
  * Dynamic flame shape and movement
  * Intensity and size react to drag speed
  * Organic flame motion without sharp edges

### Secondary Movements
- Wing and tail movements should complement breathing actions
- All transitions should feel natural and weight-appropriate
- No mechanical or rigid movements

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

## Required Deliverables

### 1. .riv file including:
- Dragon character with separate belly layer
- Particle/fire effects
- Configured state machine with named inputs

### 2. Basic Documentation:
- Input parameters and their ranges
- Basic state machine structure

## Evaluation Criteria
- Naturalness of belly movement
- Quality of particle/fire effects
- Smoothness of state transitions  
- Response to input values

## Bonus Points: Detailed Developer Documentation

If you'd like to make the integration process smoother for our development team, you can provide detailed documentation in the following format:

```typescript
// State Machine Inputs
interface DragonAnimationInputs {
 breathInProgress: number;  // Range: 0-1, Controls belly expansion
 fireIntensity: number;    // Range: 0-1, Controls fire effect
}

// States
enum DragonStates {
 IDLE = 'idle',
 BREATHING_IN = 'breathingIn',
 BREATHING_FIRE = 'breathingFire'
}

// Example of expected behavior
interface StateMachineConfig {
 stateMachine: 'DragonControl';
 inputs: {
   breathInProgress: {
     type: 'number';
     range: [0, 1];
     description: 'Controls belly expansion and air particle effects';
     default: 0;
   };
   // Other inputs...
 };
}
```
## How to Submit

### Option 1: GitHub Repository (Preferred)
1. Create a private repository on GitHub
2. Include your .riv file and documentation
3. Share access with: **@mightybyte-yuliapi**
4. Send a notification email to: yulia@mightybyte.us
  Subject line: "Rive Animation Challenge - [Your Name]"

### Option 2: Direct Email
Send your submission to: yulia@mightybyte.us
Subject line: "Rive Animation Challenge - [Your Name]"

### Submission Package Should Include:
1. .riv file
2. README.md with:
  - Basic documentation
  - Any special instructions
  - (Bonus) Developer documentation
3. Your contact information

### Questions?
If you have any questions during the challenge, please email yulia@mightybyte.us with subject line "Rive Challenge Question - [Your Name]"


_Note: We will handle the React Native integration internally - focus on creating a well-structured Rive animation that responds to external input values._
