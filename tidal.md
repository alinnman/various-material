# Tidal Forces and Weight Variations at Earth's Equator

## Overview

This document analyzes the gravitational and rotational effects that cause variations in apparent weight for a person standing at Earth's equator, focusing on the detailed geometry of solar tidal forces.

## Part 1: Rotation Vectors

### Three Rotational Motions

A person at Earth's equator participates in three rotational motions simultaneously:

| Rotation | Period | Angular Velocity (rad/s) | Direction |
|----------|--------|-------------------------|-----------|
| Earth's spin | 24 hours | $\omega_E = 7.27 \times 10^{-5}$ | North (Earth's axis, 23.5° tilt) |
| Earth around Sun | 1 year | $\omega_S = 1.99 \times 10^{-7}$ | North ecliptic pole |
| Sun around Galaxy | ~230 million years | $\omega_G = 8.6 \times 10^{-16}$ | North galactic pole |

### Vector Sum Result

Earth's rotation **dominates** by far:

- $\omega_E$ is ~365× larger than $\omega_S$
- $\omega_E$ is ~${10}^{11}$× larger than $\omega_G$

The resultant rotation vector is essentially just $\vec{\omega}_E$ with negligible corrections.

**Note on Galactic Effects:** Throughout the remainder of this analysis, galactic rotation and gravitational effects are omitted. They are approximately **10,000× smaller** than solar tidal effects and **$10^{11}$× smaller** than Earth's gravity, making them completely unmeasurable even with the most sensitive instruments. For all practical purposes, galactic contributions to weight variations are zero.

**Note on Earth-Moon Barycenter:** The Earth and Moon orbit their common center of mass (barycenter), located about 4,671 km from Earth's center. This creates a rotation with period 27.3 days and angular velocity $\omega_{EM} = 2.66 \times 10^{-6}$ rad/s (about 36× smaller than Earth's daily rotation, but 13× larger than Earth's yearly orbit around the Sun). The centrifugal acceleration from this motion ($\sim 3.3 \times 10^{-5}$ m/s²) is uniform across Earth and exactly balances the Moon's average gravitational pull at Earth's center. The lunar tidal forces discussed in this document already account for this barycenter motion - tidal effects arise from the *gradient* in the Moon's gravitational field, which is what remains after the uniform components (gravity at Earth's center and barycenter centrifugal force) cancel out.

## Part 2: Gravitational Fields

### Field Strengths at Earth's Surface

| Source | Gravitational Acceleration | Time Variation |
|--------|---------------------------|----------------|
| Earth | $g_E \approx 9.8$ m/s² | Essentially constant |
| Sun | $g_S \approx 5.9 \times 10^{-3}$ m/s² | 24-hour cycle |
| Galaxy | $g_G \approx 10^{-10}$ m/s² | Negligible |

## Part 3: Weight Variations

### Static Effects

**Earth's Rotation (Centrifugal Effect):**

- Reduction in apparent weight: $\Delta g = \omega_E^2 R_E \approx 0.034$ m/s²
- Percentage: ~0.3% of Earth's gravity
- For 70 kg person: ~240 grams lighter at equator vs poles

### Dynamic Effects (24-hour Cycle)

**Solar Tidal Effect:**

- Peak amplitude: ~$5 \times 10^{-7}$ m/s²
- Percentage: ~0.000005% of Earth's gravity
- For 70 kg person: ~0.035 grams variation

**Lunar Tidal Effect (larger than solar):**

- Peak amplitude: ~$1.1 \times 10^{-6}$ m/s²
- For 70 kg person: ~0.08 grams variation

## Part 4: Detailed Geometry of Solar Tidal Forces

### Coordinate System

- **Origin:** Earth's center
- **z-axis:** Earth's rotation axis (pointing North)
- **x-axis:** Toward vernal equinox
- **y-axis:** Completes right-handed system

### Position Vectors

**Person at equator (rotating with Earth):**
$$\vec{r}_{person} = R_E(\cos(\omega_E t), \sin(\omega_E t), 0)$$

where $R_E = 6.37 \times 10^6$ m and $t=0$ at local midnight.

**Sun's position (at equinox, for simplicity):**
$$\vec{r}_{Sun} \approx r_{AU}(1, 0, 0)$$

where $r_{AU} = 1.496 \times 10^{11}$ m.

### Tidal Field Derivation

The Sun's gravitational field varies across Earth's diameter. The tidal field (relative to Earth's center) is:

$$\vec{g}_{tidal} = -\frac{GM_{\odot}}{r_{AU}^3}[3(\vec{r}_{person} \cdot \hat{r}_{Sun})\hat{r}_{Sun} - \vec{r}_{person}]$$

Substituting the position vectors:

$$\vec{g}_{tidal} = -\frac{GM_{\odot} R_E}{r_{AU}^3}(2\cos(\omega_E t), -\sin(\omega_E t), 0)$$

### Local Vertical Component

The local vertical direction at the equator:
$$\hat{r}_{local} = (\cos(\omega_E t), \sin(\omega_E t), 0)$$

The component affecting weight (along local vertical):
$$g_{tidal,vertical} = \vec{g}_{tidal} \cdot \hat{r}_{local}$$

This gives:
$$g_{tidal,vertical} = -\frac{GM_{\odot} R_E}{r_{AU}^3}[3\cos^2(\omega_E t) - 1]$$

Using the double-angle formula:

$$\boxed{g_{tidal,vertical}(t) = -\frac{GM_{\odot} R_E}{r_{AU}^3}\left[\frac{3}{2}\cos(2\omega_E t) + \frac{1}{2}\right]}$$

### Numerical Result

With numerical values:

- Tidal gradient: $\frac{2GM_{\odot}}{r_{AU}^3} \approx 5.05 \times 10^{-14}$ s⁻²
- Amplitude: $A = \frac{2GM_{\odot} R_E}{r_{AU}^3} \approx 3.2 \times 10^{-7}$ m/s²

Therefore:
$$g_{tidal,vertical}(t) \approx -4.8 \times 10^{-7}\cos(2\omega_E t) - 1.6 \times 10^{-7} \text{ m/s}^2$$

## Part 5: Physical Interpretation

### Time of Day Variations

| Local Time | Phase | $\cos(2\omega_E t)$ | Tidal Effect | Interpretation |
|------------|-------|---------------------|--------------|----------------|
| Midnight | 0 | +1 | $-6.4 \times 10^{-7}$ m/s² | Slightly lighter |
| 6 AM | π/2 | -1 | $+3.2 \times 10^{-7}$ m/s² | Slightly heavier |
| Noon | π | +1 | $-6.4 \times 10^{-7}$ m/s² | Slightly lighter |
| 6 PM | 3π/2 | -1 | $+3.2 \times 10^{-7}$ m/s² | Slightly heavier |

### Key Features

1. **Twice-daily variation:** Weight oscillates **twice per day** (note the $2\omega_E$ frequency)
2. **Lightest at noon and midnight:** When Sun is directly overhead or underfoot
3. **Heaviest at sunrise and sunset:** When Sun is on the horizon
4. **Peak-to-peak variation:** ~$10^{-6}$ m/s² or 0.00001% of g

### Why Twice Daily?

The tidal force depends on the **gradient** of the gravitational field. The geometry is symmetric - whether the Sun is overhead or underfoot, you're at an extremum of the tidal field (stretched along the Sun-Earth line). At sunrise/sunset, you're compressed perpendicular to this line.

## Part 6: Measurement and Detection

### Detectability

These tiny variations are measurable with:

- **Gravimeters:** Precision instruments detecting $10^{-8}$ m/s² or better
- **Tidal gauges:** Ocean tides amplify these effects (water can flow)
- **Superconducting gravimeters:** Can resolve $10^{-11}$ m/s²

### Practical Considerations

For a 70 kg person:

- **Earth's rotation:** -240 g (always present at equator)
- **Solar tides:** ±0.035 g (twice daily)
- **Lunar tides:** ±0.08 g (twice daily, with 12.4 hour period)

A bathroom scale would need milligram precision to detect tidal effects.

## Part 7: Reference Frames Clarification

### Inertial Frame Perspective

- **Only real forces:** Gravity (from Earth, Sun, Moon)
- **Centripetal acceleration:** Provided by gravity for orbital motion
- **Net force on capsule in orbit:** Equals required centripetal force (not zero!)
- **Proper acceleration:** Zero (free-fall)

### Rotating Frame Perspective (Earth's surface)

- **Apparent forces:** Gravity + centrifugal force
- **Equilibrium:** Forces balance (from your perspective, you're stationary)
- **Centrifugal force:** Fictitious force arising from non-inertial frame
- **Proper acceleration:** Non-zero (ground pushes up on you)

### Key Distinction: Free-Fall vs. Supported

**In orbit (free-fall):**

- Accelerometer reads zero
- No normal force
- Gravity provides exactly the centripetal force needed

**On Earth's surface (supported):**

- Scale reads your apparent weight
- Normal force prevents free-fall
- Gravity provides more than needed for Earth's rotation; remainder is apparent weight

## Summary

A person at Earth's equator experiences:

1. **Dominant effect:** Earth's gravity (~9.8 m/s²)
2. **Static reduction:** Earth's rotation reduces apparent weight by ~0.3%
3. **Dynamic variations:**
   - Lunar tides: ~$10^{-6}$ m/s² (twice daily, 12.4 hour period)
   - Solar tides: ~$5 \times 10^{-7}$ m/s² (twice daily, 12 hour period)
4. **Galactic effects:** Completely negligible ( ~$10^{-10}$ m/s² )

The twice-daily variation in weight is real and measurable with precision instruments, though far too small to perceive directly. These same tidal forces create ocean tides, where the water's ability to flow amplifies the effect into the familiar rising and falling of sea level.

---

**Note:** This analysis assumes the equinox (Sun above equator) for geometric simplicity. At other times of year, the Sun's declination introduces additional complexity but doesn't change the fundamental twice-daily nature of the tidal variation.
