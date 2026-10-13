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

1. I will use `string GetResponse(int friendshipLevel, bool knowsSecret)`. The method returns the character's text response as a string. Favorability is a number, and knowing the secret is a yes or no condition.

2. I would use `void SetLightDimness(float sanityPercent)`. Floats let sanity levels contain values between integer percentages. The method changes the lights directly, so it does not return anything.

3. I will use `bool DidPlayerHitBeat(float keyPressTime)`. Input is when the player presses the key. The method can compare it to the expected time and allowed timing window stored in the class, and return true for a hit or false for a miss.

#### Activity 2

A class is like a recipe, and a component is a dish made from a recipe and added to a game object. Member variables are settings for a specific dish, such as its portion size or spice level. Methods are operations described by a recipe. Two dishes can use the same ingredients but have different settings, just like two balls can use BallW3 but have different colors and speed multipliers.

#### Activity 3

Because each quick bounce of the ball multiplies the ball color by 1.5, and the code never limits the RGB value to 1. After a few bounces, these values will grow rapidly, and values above 1 will appear brighter than normal colors.

## Open-Source Assets
### W1
- Animals: https://assetstore.unity.com/packages/3d/characters/animals/animals-free-animated-low-poly-3d-models-260727 
- Low-poly environment: https://assetstore.unity.com/packages/3d/environments/landscapes/low-poly-simple-nature-pack-162153 
