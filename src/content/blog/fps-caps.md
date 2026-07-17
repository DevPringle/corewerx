---
title: "Why FPS Caps Still Matter"
date: "July 16, 2026"
description: "Looking at frame limits, fairness, and consistency."
---

FPS caps in FiveM racing servers were never implemented because higher frame rates looked worse or because players were expected to run weaker hardware. They existed because frame rate could influence vehicle behavior and create differences between drivers using different setups.

With Canary builds allowing servers to remove those restrictions, the original argument for FPS caps has changed. The obvious advantage of running higher FPS may no longer exist in the same way it once did, but that does not mean uncapped FPS automatically creates the best competitive racing environment.

The important distinction is that removing a direct advantage does not necessarily remove inconsistency.

In a competitive racing server, the goal is not only preventing one player from gaining an edge. It is creating a predictable environment where the vehicle behaves the same way every time a driver gets behind the wheel.

That is where a stable FPS cap still has value.

## GTA V Vehicle Handling Is More Than Static Numbers

A common argument after the removal of FPS restrictions is that the vehicle handling values have not changed, so the car should behave exactly the same.

On paper, that makes sense.

A vehicle's `handling.meta` values remain identical regardless of whether a player is running 60 FPS or 240 FPS. Parameters such as:

* `fInitialDriveForce`
* `fDriveInertia`
* `fInitialDriveMaxFlatVel`
* `fTractionCurveMax`
* `fTractionCurveMin`
* `fTractionCurveLateral`
* `fTractionLossMult`
* `fSuspensionForce`
* `fSuspensionCompDamp`
* `fSuspensionReboundDamp`
* `fAntiRollBarForce`
* `fRollCentreHeightFront`
* `fRollCentreHeightRear`
* `fDownforceModifier`

are still the same values being loaded by the game.

However, those values are not the vehicle itself. They are instructions used by the engine to calculate how the vehicle reacts.

The handling file defines the characteristics of the car, but the physics engine determines how those characteristics are applied during acceleration, braking, cornering, collisions, and suspension movement.

That distinction is important.

A car having the same settings does not necessarily guarantee that it will feel identical under different simulation conditions.

## Why Frame Rate Can Still Influence Vehicle Feel

Historically, GTA V has had a relationship between frame rate and vehicle simulation. The most well-known example was high FPS affecting vehicle speed, which was one of the primary reasons racing servers introduced FPS limitations.

While newer FiveM builds have worked to eliminate those direct advantages, the underlying relationship between frame timing and simulation behavior is still something worth considering.

Vehicle physics are not just about top speed or acceleration.

Every corner involves a constant series of calculations:

* Tire forces changing as grip is gained and lost.
* Suspension compressing and rebounding.
* Weight shifting between the front and rear axle.
* The chassis rolling under lateral load.
* Traction being transferred through driven wheels.

Variables like `fTractionCurveMax` and `fTractionCurveMin` determine the grip window of the vehicle, while `fTractionLossMult` affects how the vehicle behaves once that limit is exceeded.

Suspension variables such as `fSuspensionForce`, `fSuspensionCompDamp`, and `fSuspensionReboundDamp` determine how the vehicle reacts when those forces are applied.

The important part is that these are not isolated calculations. They are constantly interacting.

A change in how those calculations are processed can change how a vehicle feels, even when the actual handling values remain untouched.

## Why Racing Makes These Differences More Noticeable

In normal gameplay, these differences are almost irrelevant.

A player cruising around Los Santos is not going to notice if a vehicle settles slightly differently after hitting a bump or if the suspension reacts differently during a hard corner.

Competitive racing is the opposite.

Drivers build muscle memory around very specific vehicle behavior. They know how much curb they can take before losing stability. They know when they can apply throttle on corner exit. They know exactly how much steering correction is required when the rear begins to rotate.

The closer a driver gets to the limit of the car, the more important consistency becomes.

Small differences that are invisible during normal driving become obvious when repeating the same corner dozens of times.

An uncapped frame rate may not make the car objectively faster or slower, but if it changes how the car responds, the driver has to adapt to the vehicle instead of focusing purely on racing.

## Suspension, Curbs, and Weight Transfer

One of the biggest areas where this matters is vehicle stability.

GTA V racing is heavily influenced by how vehicles react to uneven surfaces. Curbs, bumps, elevation changes, and aggressive direction changes all rely on suspension behavior.

A vehicle with high `fSuspensionForce` and aggressive damping values may feel planted when it loads into a corner, but unsettled when it hits an unexpected surface. The interaction between compression, rebound, anti-roll forces, and tire grip determines whether the car stays composed or begins to rotate.

Similarly, `fRollCentreHeightFront` and `fRollCentreHeightRear` affect how the chassis transfers weight during cornering.

At the limit, a driver is relying on those reactions being predictable.

If the car feels slightly different from one setup to another, the problem is not that the car has become unusable. The problem is that the driver is no longer working with a completely consistent reference point.

For racing, that matters.

## Lower Input Delay Is Not The Only Goal

The strongest argument for uncapped FPS is responsiveness.

A higher frame rate can reduce input latency and make steering, throttle, and braking inputs appear smoother. That benefit is real.

However, racing is not only a reaction test.

A driver is not winning because they can move the steering wheel a few milliseconds faster. They are winning because they can consistently place the car in the correct position while managing grip, braking, and acceleration.

A slightly lower latency environment with inconsistent vehicle behavior can be less valuable than a slightly higher latency environment with predictable behavior.

Consistency creates confidence, and confidence creates faster laps.

## Why A Cap Can Still Be The Competitive Choice

Removing FPS restrictions solves the original problem of players gaining an unfair advantage from their frame rate.

It does not automatically mean unlimited FPS is the best environment for competitive racing.

A cap provides a controlled baseline. It reduces variables and ensures that vehicle behavior is experienced within a predictable range.

This is especially important for servers where vehicles are heavily tuned and balanced around close competition. When cars are separated by small performance margins, even minor differences in feel can influence driver performance.

The purpose of a cap is not to hold players back.

The purpose is to make the car more consistent.

## The Best Setup Is The One You Can Repeat

The highest FPS number is not always the best racing setup.

A stable frame rate provides a stable driving experience. Whether that means 60 FPS, 120 FPS, or another value depends on the player and hardware, but the principle remains the same.

A consistent car is more valuable than a theoretically smoother one.

Competitive racing is built around repeatability. Every lap, every corner, and every input depends on knowing exactly how the vehicle will respond.

Even after FPS restrictions are removed, keeping a cap remains a valid choice because the goal of racing is not simply maximum performance from the hardware.

The goal is maximum consistency from the vehicle.

## TL;DR

Canary builds remove the original reason FPS caps were introduced in FiveM racing: preventing direct frame rate advantages.

However, that does not mean uncapped FPS creates the most consistent driving experience.

GTA V vehicles still rely on complex interactions between `handling.meta` values, suspension calculations, traction behavior, and weight transfer.

A stable FPS cap reduces variables and provides a more predictable vehicle response.

In competitive racing, where small differences matter, consistency is often more valuable than additional frames.
