LLM Collaboration Guide for Galaxy Grapple

Version: 1.0
🚀 Introduction

This document provides a guide and a set of prompt templates for collaborating with a Large Language Model (LLM) like Gemini to improve, debug, and expand the "Galaxy Grapple" game. The key to successful collaboration is providing clear, specific, and context-rich prompts.
🧠 Core Concepts for Prompting

When asking for code changes, always remember these key principles:

    Provide Full Context: The LLM needs the complete, most recent version of the game's code to work effectively. Always ensure the latest version is available to it.

    Be Specific: Vague requests like "make it better" are less effective than specific instructions like "increase the player's boost duration after releasing a grapple."

    Describe the "Why": Explain why you want a change. Instead of "the flight is wrong," say "the flight time feels too short after a good swing, it should feel more rewarding." This helps the LLM understand the goal and make better adjustments.

    Reference Specific Code: If you can, mention the variable or function name you think is related to your request (e.g., "I think the BOOST_DURATION constant needs to be increased").

✨ Prompts for Improving Features

Use these templates to request new features or modify existing ones.
Adding a New Power-Up

Prompt:

    "I want to add a new power-up to the game. Let's call it a 'Score Multiplier.' When the player collects it, their score should be doubled for the next 10 seconds.

        Create a new collectible type called score_multiplier.

        It should look like a spinning, purple star.

        When collected, play a distinct sound effect.

        For 10 seconds after collection, any points earned from ascending should be doubled. Add a visual indicator on the screen to show that the multiplier is active."

Changing an Existing Hazard

Prompt:

    "Let's change how the 'moving' planets work. Instead of moving side-to-side, I want them to move in a figure-eight pattern. Please update the update function within the Anchor class for the 'moving' type to implement this new movement logic."

🐞 Prompts for Fixing Bugs

Use these templates when you encounter a problem or something feels wrong.
Fixing Physics & Game Feel

Prompt:

    "The flight time after releasing a grapple feels too short and not very powerful. It doesn't feel like my momentum is carrying me far enough.

    Please review the physics constants, specifically GRAVITY and BOOST_DURATION, and adjust them to make the post-release flight last significantly longer and feel more rewarding."

Correcting Visual Glitches

Prompt:

    "I've noticed a visual bug. When the player is swinging, the dynamic rope sometimes draws from the wrong location for a split second, making it jump across the screen.

    Please review the drawRope function in the Player class and the Rope class itself to ensure the rope's start and end points are always correctly anchored to the player and the planet."

Fixing Gameplay Errors

Prompt:

    "I've found a bug where sometimes the game doesn't end when I fall off the bottom of the screen. Review the game over condition in the main gameLoop to ensure gameState is correctly set to 'gameOver' when player.y exceeds the bottom boundary of the screen."

🎨 Prompts for Art & Aesthetics

Use these templates to request changes to the game's visual style.
Changing an Object's Appearance

Prompt:

    "I want to change the art for the player's rocket. Please update the draw function in the Player class to give the rocket a sleeker, more futuristic design. Make the body a darker metallic color, add two side fins, and make the cockpit window glow more brightly."

Modifying the UI

Prompt:

    "Let's polish the UI. The score display at the top is a bit plain. Please modify the drawScore function to draw a semi-transparent, rounded rectangle behind the score and high score text to make it stand out more."
