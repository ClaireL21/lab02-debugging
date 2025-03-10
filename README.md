# lab06-debugging - Claire Lu & Dineth Meegoda

bug1: on line 97, vec2 was written as vec
There was compile error preventing it from being run so we were able to quickly see where the bug was.

bug2: on line 100, we were passing in uv to raycast instead of uv2 in the main method.
we started by looking at main and then parsed through the code sequentially. We realized that uv2 was being initialized but not used. 

bug3: in raycast, the height was calculated by dividing by x resolution over x resolution instead of x over y. We found it by realizing that the height of the image was warped/cut off.

bu4: in the march function we changed the iterations from 64 to 200. There was warping on the sides on the spheres and the background wasnt shown as much as it was in the example render. By increasing the iterations the ray was able to cast further.

bug5: in the sdf3D funftion, we fixed the reflection by reflecting over dir instead of eye. We realized that eye was a position vector and not a directional vector so we couldnt accurately reflect the direction from the camera across the normal of the intersection surface.

[Shadertoy solution link](https://www.shadertoy.com/view/cdcczj)
# Setup 

Create a [Shadertoy account](https://www.shadertoy.com/). Either fork this shadertoy, or create a new shadertoy and copy the code from the [Debugging Puzzle](https://www.shadertoy.com/view/flGfRc).

Let's practice debugging! We have a broken shader. It should produce output that looks like this:
[Unbelievably beautiful shader](https://user-images.githubusercontent.com/1758825/200729570-8e10a37a-345d-4aff-8eff-6baf54a32a40.webm)

It don't do that. Correct THREE of the FIVE bugs that are messing up the output. You are STRONGLY ENCOURAGED to work with a partner and pair program to force you to talk about your debugging thought process out loud.

Extra credit if you can find all FIVE bugs.

# Submission
- Create a pull request to this repository
- In the README, include the names of both your team members
- In the README, create a link to your shader toy solution with the bugs corrected
- In the README, describe each bug you found and include a sentence about HOW you found it.
- Make sure all three of your shadertoys are set to UNLISTED or PUBLIC (so we can see them!)
