# in-class-activities
## Devlogs
### W1
Write your W1 activity Devlog here.
https://qiliangw-sketch.itch.io/in-class-activity1
I would spot the cat appearing on the camera, shifting the view to a second-person perspective.
### W2
1. **Why are r, g, and b floats?** RGB channels use fractional values between 0.0 and 1.0, such as 0.1 and 0.3. Floats can store these values; ints store whole numbers, bools store true or false, and strings store text.

2. **Why is the bounce counter an int?** Each collision adds one whole bounce. An int represents this count directly; a float would allow unnecessary fractional counts, while bools and strings do not represent a numeric count appropriately.

3. **What does the Step 4 error tell us?** The original line `g -= 0.1f` is missing its terminating semicolon. The C# compiler reports CS1002, "; expected", indicating that the statement needs to end with `;`. The corrected line is `g -= 0.1f;`.

The W2 scene uses a circle sprite with initial RGB (0, 1, 0.3). Each collision increments the counter, changes the RGB channels with the required wrap conditions, and updates brightness using the average of the new RGB values. Completed Steps 1–9.

### W3 In-Class Activity

#### Activity 1

1. I would use `string GetResponse(int friendshipLevel, bool knowsSecret)`. "Friendship level" is a number, and "knowing the secret" is a yes/no condition. The method returns a string because the output is the character's text response.

2. I would use `void SetLightDimness(float sanityPercent)`. A `float` can represent sanity values between integer percentages. This method directly changes the light's brightness, so it doesn't need to return anything.

3. I would use `bool DidPlayerHitBeat(float keyPressTime)`. The input is the time the player pressed the key. The method compares this against the expected beat time and the allowed timing window stored in the class, then returns `true` for a hit or `false` for a miss.

#### Activity 2

I think of a class as the blueprint for an engine, while a Component is a specific engine built from that blueprint and installed in a car. Member variables describe the engine's state and settings—such as temperature and power—while methods represent actions it can perform, like starting up and accelerating. Two engines can share the same blueprint but have different settings, just as two balls might both use `BallW3` but have different colors and speed multipliers.

#### Activity 3

Because each rapid bounce of the ball multiplies its color value by 1.5—and the code doesn't cap RGB values at 1.0—the values grow rapidly after a few bounces; values exceeding 1.0 appear brighter than standard colors.

## Open-Source Assets
### W1
- Animals: https://assetstore.unity.com/packages/3d/characters/animals/animals-free-animated-low-poly-3d-models-260727 
- Low-poly environment: https://assetstore.unity.com/packages/3d/environments/landscapes/low-poly-simple-nature-pack-162153 
