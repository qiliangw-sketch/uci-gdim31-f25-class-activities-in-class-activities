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

W3 In-Class Activity

Activity 1

1. I will use string GetResponse(int friendshipLevel, bool knowsSecret). The method returns the character's text response as a string. Favorability is a number, and knowing the secret is a yes or no condition.

2. I would use void SetLightDimness(float sanityPercent). Floats let sanity levels contain values between integer percentages. The method changes the lights directly, so it does not return anything.

3. I will use bool DidPlayerHitBeat(float keyPressTime). Input is when the player presses the key. The method can compare it to the expected time and allowed timing window stored in the class, and return true for a hit or false for a miss.

Activity 2

A class is like a recipe, and a component is a dish made from a recipe and added to a game object. Member variables are settings for a specific dish, such as its portion size or spice level. Methods are operations described by a recipe. Two dishes can use the same ingredients but have different settings, just like two balls can use BallW3 but have different colors and speed multipliers.

Activity 3

Because each quick bounce of the ball multiplies the ball color by 1.5, and the code never limits the RGB value to 1. After a few bounces, these values will grow rapidly, and values above 1 will appear brighter than normal colors.

W4 In-Class Activity

1. I added a CapsuleCollider (oriented along the Z-axis) to the cat and a SphereCollider to the soccer ball, and attached a Rigidbody component to both. The "Is Trigger" option is left unchecked for these colliders, allowing the cat to kick the ball and ensuring both objects can interact with the ground. The goal uses a BoxCollider with "Is Trigger" enabled; it does not require a Rigidbody because it remains stationary—it only needs to detect when the soccer ball enters, and the ball should be able to pass through it. The existing force field in the scene also functions as a trigger; the BounceOffWall scripts attached to the cat and the soccer ball ensure that whenever they exit the force field, they are bounced back toward the center of the play area.

2. During setup, the Rigidbody field for CatW4 was initially unassigned; I linked the Rigidbody component once it was added. I also assigned the respective Rigidbody components to the BounceOffWall scripts. I also verified that the goal is tagged as "Goal," ensuring that points are awarded only when the soccer ball enters the goal, rather than when it interacts with the force field. In testing, the cat is able to kick the ball; scoring a goal triggers a confetti effect, updates the score, and resets the timer. If the ball remains inside the goal, it does not continuously accumulate points; however, if it leaves and then re-enters, it will award another point.

Components diagram: [CatW4 ground contact and jumping](W4-components.svg).


## Open-Source Assets
### W1
- Animals: https://assetstore.unity.com/packages/3d/characters/animals/animals-free-animated-low-poly-3d-models-260727 
- Low-poly environment: https://assetstore.unity.com/packages/3d/environments/landscapes/low-poly-simple-nature-pack-162153 
