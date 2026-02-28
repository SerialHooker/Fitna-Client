Fitna Client is a Minecraft Bedrock ghost client designed to be as configurable as possible

# Module Documentation

## Combat

### AimAssist
Automatically rotates the camera toward nearby entities.

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| yawSpeed | float | 20.0 | Horizontal rotation speed |
| pitchSpeed | float | 20.0 | Vertical rotation speed |
| fovThreshold | float | 60.0 | Maximum FOV angle to activate assist (degrees) |
| precision | float | 0.003 | Precision threshold (radians) to consider on-target |
| maxDistance | float | 6.0 | Maximum detection distance |
| minDistance | float | 0.5 | Minimum detection distance |
| acceleration | float | 0.5 | Exponential smoothing strength (0.0 = off, 1.0 = max) |
| prediction | bool | false | Entity movement prediction |
| pearlAimBot | bool | false | Pearl-specific aim assist |
| pearlRange | float | 5.0 | Pearl aimbot range |
| pearlSlot | int | 1 | Pearl hotbar slot |
| onlySlotA | bool | false | Only activate on a specific slot |
| slotA | int | 0 | Required slot (0-8) |
| entityNumber | int | 250 | Max entities to scan |
| backward | bool | true | Target entities behind the player |
| priority | enum | FOV | Targeting priority (Distance, FOV) |
| point | enum | ADAPTIVE | Aim point (HEAD, BODY, LEGS, FEET, ADAPTIVE) |

---

### AutoClicker
Automatic clicking with multiple modes.

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| avoidMenu | bool | true | Disable when a menu is open |
| breakBlocks | bool | true | Allow block breaking |
| reverseButton | bool | false | Use right click instead of left |
| uncappedMode | bool | false | Uncapped CPS mode |
| minC | int | 10 | Minimum CPS |
| maxC | int | 14 | Maximum CPS |
| rapidC | bool | false | Rapid burst mode |
| rapidMax | bool | false | Maximize burst |
| rapidValue | int | 20 | CPS during burst |
| rapidTime | int | 500 | Burst duration (ms) |

---

### Reach
Extends attack range.

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| minReach | float | 3.0 | Minimum reach |
| maxReach | float | 3.5 | Maximum reach |
| enableSharingan | bool | false | Adaptive reach (detects enemy reach) |
| onlySlot | bool | false | Only activate on a specific slot |
| slotChoice | int | 0 | Required slot (0-8) |
| onlyGround | bool | false | Only activate on ground |
| silentReach | float | 0.0 | Silent reach (server-side) |

---

### TriggerBot
Automatically clicks when crosshair is on an entity.

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| reaction | int | 100 | Reaction time (ms) |
| hitSelecting | bool | false | Hit selecting (alternate hits) |
| tradeDuration | int | 1000 | Trade duration (ms) |
| distanceT | bool | false | Enable distance filter |
| distanceTT | float | 3.0 | Maximum trigger distance |
| oneTap | bool | false | One-tap mode (single click per detection) |
| oneTapDistance | float | 4.0 | One-tap distance |
| oneTapDuration | int | 500 | One-tap duration (ms) |
| minCPS | int | 10 | Minimum CPS |
| maxCPS | int | 14 | Maximum CPS |
| fastOneTap | bool | false | Fast one-tap |
| fastOneTapBurstDuration | int | 100 | Fast one-tap burst duration (ms) |
| timeClickerEnabled | bool | false | Time clicker mode |
| timeClickerCPS | int | 20 | Time clicker CPS |
| timeClickerBurstDuration | int | 200 | Time clicker burst duration (ms) |

---

### KillAura
Automatically attacks entities within range.

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| mode | enum | Stable | Attack mode (Unstable, Stable) |
| maxRange | float | 3.2 | Maximum range |
| minRange | float | 0.2 | Minimum range |
| onlyPlayers | bool | true | Target players only |
| minAPS | int | 3 | Minimum attacks per second |
| maxAPS | int | 6 | Maximum attacks per second |
| fovCheck | bool | true | Enable FOV check |
| fovThreshold | float | 180.0 | FOV threshold (degrees) |
| rotateToTarget | bool | false | Rotate toward target |
| onlySlot | bool | true | Only activate on a specific slot |
| slot | int | 0 | Required slot (0-8) |
| criticals | bool | true | Enable critical hits |
| fallDistance | float | 0.1 | Fall distance for criticals |

---

### Criticals
Forces critical hits on every attack.

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| mode | enum | Sentinel | Mode (Timing, LowJump, Hybrid, Sentinel) |
| useVelocity | bool | true | Use velocity for criticals |
| positionChange | bool | true | Modify position to trigger crits |
| biggerPositionChange | bool | true | Larger position change |
| sendJumping | bool | true | Send jump flag |
| offSprint | bool | true | Disable sprint during crits |
| positionChangePercent | float | 1.5 | Position change percentage |
| lowJumpHeight | float | 0.15 | Low jump height |
| criticalChance | int | 70 | Critical chance (%) |
| checkInterval | int | 5 | Check interval (ticks) |
| cooldownAfterHit | int | 200 | Cooldown after hit (ms) |

---

### Hitbox
Modifies entity hitbox size.

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| horizontalHitbox | float | 0.6 | Horizontal hitbox size |
| verticalHitbox | float | 1.8 | Vertical hitbox size |
| silentHitbox | float | 0.0 | Silent hitbox (server-side) |
| onlySlot | bool | false | Only activate on a specific slot |
| slotChoice | int | 0 | Required slot (0-8) |

---


---

### ThrowPearl
Automatically throws an ender pearl.

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| keybind | int | 0 | Activation key (0 = disabled) |
| pearlId | int | 0x1c6 | Pearl item ID (454 decimal) |
| clickCount | int | 3 | Number of right clicks to simulate |
| clickDelay | int | 50 | Delay between clicks (ms) |

---

### ThrowPot
Automatically throws a potion.

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| keybind | int | 0 | Activation key (0 = disabled) |
| potionId | int | 0x258 | Potion item ID (600 decimal) |
| clickDelay | int | 50 | Delay after click (ms) |

---

### Regen
Automatically destroys redstone ore blocks (Hive Skywars regen).

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| range | float | 5.0 | Detection range |
| uncover | bool | true | Mine covering blocks above redstone first |
| rotate | bool | true | Rotate camera toward the block |
| hotbarOnly | bool | true | Only use hotbar items |
| swing | bool | false | Swing animation |
| delayBetweenBlocks | int | 350 | Delay between each block destruction (ms) |
| breakProgressPerTick | float | 0.0667 | Progress per tick (adjustable for haste) |
| maxMiningTicks | int | 15 | Max ticks before forcing destruction |
| ironPickAxeId | int | 0x148 | Iron pickaxe item ID |
| enableRedstoneOre | bool | true | Target redstone ore blocks |
| enableLitRedstoneOre | bool | true | Target lit redstone ore blocks |
| enableDeepslateRedstone | bool | false | Target deepslate redstone blocks |

---

### RegenAssist
Aim assist for redstone blocks (always targets the top face) (Hive Skywars regen).

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| range | float | 5.7 | Detection range |
| acceleration | float | 0.5 | Smoothing strength (0.0 = off, 1.0 = max) |
| maxAngle | float | 30.0 | Maximum angle to activate assist (degrees) |
| yawSpeed | float | 20.0 | Horizontal rotation speed |
| pitchSpeed | float | 20.0 | Vertical rotation speed |
| onlySlot | bool | true | Only activate on a specific slot |
| slot | int | 1 | Required slot (0-8) |
| enableRedstoneOre | bool | true | Target redstone ore blocks |
| enableLitRedstoneOre | bool | true | Target lit redstone ore blocks |
| enableDeepslateRedstone | bool | false | Target deepslate redstone blocks |

---

### Nuker
Destroys all blocks within a radius around the player.

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| radius | int | 1 | Destruction radius (1 = 3x3, 2 = 5x5, etc.) |
| delayPerBlock | int | 50 | Delay between each destruction (ms) |

---

## Movement

### Velocity
Reduces or cancels received knockback.

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| mode | enum | OomphSafe | Mode (Simple, GhostSim, MicroReduction, WTapCancel, GroundAbuse, OomphSafe) |
| horizontalReduction | float | 1.0 | Horizontal reduction (0 = no KB, 1 = normal) |
| verticalReduction | float | 1.0 | Vertical reduction |
| bypassAC | bool | true | Anti-cheat bypass |
| ghostSimEnabled | bool | true | Enable ghost simulation |
| microReductionFactor | float | 0.65 | Micro-reduction factor (per tick) |
| microReductionTicks | int | 6 | Number of reduction ticks |
| microPreserveY | bool | true | Preserve vertical KB |
| wTapDelay | int | 2 | Ticks before W-Tap |
| wTapSprintToggle | bool | true | Toggle sprint during W-Tap |
| groundAbortThreshold | float | 0.3 | Ground distance to abort |
| forceOnGround | bool | true | Force onGround flag |
| oomphSafeReduction | float | 0.5 | Oomph safe reduction (50%) |
| oomphEnableWTap | bool | true | Enable W-Tap in Oomph mode |
| oomphEnableGroundAbuse | bool | true | Enable ground abuse in Oomph mode |
| oomphMaxReductionTicks | int | 8 | Max reduction ticks for Oomph |
| onClickOnly | bool | false | Only activate while clicking |
| onGroundOnly | bool | false | Only activate on ground |
| onlyTargeting | bool | false | Only activate while targeting |
| reverseButton | bool | false | RMB instead of LMB |
| toggleThreadSleep | bool | false | Thread sleep |
| toggleThreadSleepValue | int | 10 | Sleep value (ms) |

---

### Timer
Modifies game tick speed.

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| onlyGround | bool | false | Only activate on ground |
| onlySlot | bool | false | Only activate on a specific slot |
| slotChoice | int | 0 | Required slot (0-8) |
| onlyClick | bool | false | Only activate while clicking |
| onlyHit | bool | false | Only activate while hitting |
| onlyTargeting | bool | false | Only activate while targeting |
| smartTimer | bool | false | Smart timer (adaptive) |
| smartTimerSelection | int | 0 | Smart mode selection |
| timerYDistance | float | 2.0 | Y distance for smart timer |
| timerIncrease | float | 5.0 | Timer increase value |
| bypassAC | bool | false | Anti-cheat bypass |
| recoverTimer | float | 18.0 | Recovery value |
| speedUpTimer | float | 22.0 | Speed-up value |
| useRandom | bool | false | Use random speed |
| speed | float | 1.0 | Fixed speed |
| minSpeed | float | 1.0 | Minimum speed (random mode) |
| maxSpeed | float | 1.0 | Maximum speed (random mode) |

---

### AutoJumpReset
Automatic combo reset via jumping.

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| onlyTargeting | bool | false | Only activate while targeting |
| ignoreFH | bool | false | Ignore fall height |
| mode | int | 0 | Mode (0 = Key Simulation, 1 = Internal) |
| jumpKey | int | VK_SPACE | Jump key |
| experimental | bool | false | Experimental mode |
| spamJump | bool | false | Spam jump |
| spamJumpDuration | int | 100 | Spam duration (ms) |
| milliseconds | float | 50.0 | Standard delay (ms) |
| fallingTime | float | 500.0 | Falling time (ms) |
| minTimer | float | 1.0 | Minimum timer |
| maxTimer | float | 1.0 | Maximum timer |
| notLegit | bool | false | Non-legit mode (velocity modifier) |
| chanceNLJR | int | 100 | Activation chance (%) |
| nljrMode | int | 0 | NLJR mode (0 = Velocity Change, 1 = Motion Change) |
| valueNLJR | float | 60.0 | Velocity percentage kept |
| toggleThreadSleep | bool | true | Thread sleep |
| toggleThreadSleepValue | int | 10 | Sleep value (ms) |

---

### Fly
Enables flight with multiple modes.

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| mode | enum | OomphSafe | Mode (Vanilla, Glide, Motion, Jetpack, Creative, OomphSafe) |
| flySpeed | float | 0.6 | Flight speed |
| verticalSpeed | float | 0.42 | Vertical speed |
| glideSpeed | float | 0.05 | Glide fall speed |
| useViewDirection | bool | true | Fly toward look direction |
| antiKick | bool | true | Limit height to avoid kick |
| glideFallSpeed | float | 0.02 | Fall speed in glide mode |
| glideBoostSpeed | float | 0.3 | Boost speed in glide mode |
| jetpackInterval | int | 8 | Jetpack interval (ticks) |
| jetpackBoost | float | 0.5 | Jetpack boost force |
| oomphMaxHeight | float | 3.0 | Max height above start (Oomph) |
| oomphPacketDelay | int | 350 | Latency spoof delay (Oomph) |
| oomphBlockCorrections | bool | true | Block server corrections (Oomph) |
| oomphSprintSpoof | bool | true | Spoof sprint (Oomph) |
| oomphGlideFlag | bool | true | Use START_GLIDING flag (Oomph) |
| spoofOnGround | bool | false | Spoof onGround flag |
| useLatencySpoof | bool | true | Enable latency spoof |
| latencySpoofValue | int | 350 | Latency spoof value (ms) |
| blockMotionPackets | bool | true | Block motion correction packets |

---

### AutoSTap
Automatic S-Tap (backward tap after hit for more KB).

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| horizontalDistance | float | 1.5 | Horizontal distance to trigger |
| verticalDistance | float | 0.0 | Vertical distance to trigger |
| adaptive | bool | false | Adaptive mode |
| backwardDelay | int | 75 | Backward tap duration (ms) |

---

### AutoWTap
Automatic W-Tap (releases forward after hit to reset sprint).

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| pressTime | int | 120 | Forward release duration (ms) |
| minActiveDistance | float | 0.0 | Minimum activation distance |
| maxActiveDistance | float | 6.0 | Maximum activation distance |

---

### InventoryWalk
Allows movement while inventory is open.

*No configurable parameters.*

---

## Visual

### Misplace
Manipulates entity positions (pull/push).

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| toggleThreadSleep | bool | false | Thread sleep |
| toggleThreadSleepValue | int | 10 | Sleep value (ms) |
| loopSleepTime | int | 2 | Loop delay (ms) |
| onClickOnly | bool | false | Only activate while clicking |
| reverseButton | bool | false | Right click instead of left |
| pullDistance | float | 1.0 | Pull distance |
| reachDistance | float | 20.0 | Misplace reach distance |
| reverseMode | bool | false | Push instead of pull |
| smoothingFactor | float | 0.35 | Smoothing factor (0.1 = smooth, 1.0 = instant) |

---

### BackTrack
Delays entity movement packets to hit them at a past position.

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| minimalInterval | float | 2000 | Minimum interval (ms) |
| maximalInterval | float | 5000 | Maximum interval (ms) |
| onlyEnemyInAir | bool | false | Only activate when enemy is airborne |
| yDiff | float | 1.5 | Y difference |
| onlyGround | bool | false | Only activate on ground |
| lagDelay | float | 100 | Lag delay (ms) |
| onlyOnClick | bool | false | Only activate while clicking |
| mode | enum | INTERNAL | Mode (INTERNAL, EXTERNAL) |

---

### Blink
Stores outgoing packets and releases them at once (teleportation).

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| manualMode | bool | true | Manual mode (hold key) |
| pulseMode | bool | false | Pulse mode (toggle on/off in loop) |
| pulseDelay | float | 500.0 | Pulse delay (ms) |
| onlyGround | bool | false | Only activate on ground |
| onlyClick | bool | false | Only activate while clicking |
| onlyMove | bool | false | Only activate while moving |

---

### FakeLag
Simulates artificial lag.

*No configurable parameters.*

---

### ESP
Renders players through walls (boxes, distance, lines).

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| showBoxes | bool | true | Show boxes |
| showDistance | bool | true | Show distance |
| showSnaplines | bool | false | Show snap lines |
| maxDistance | float | 120.0 | Maximum render distance |
| boxThickness | float | 1.5 | Box thickness |
| projectionFov | float | 90.0 | Projection FOV |
| colorR | float | 1.0 | Red color (0-1) |
| colorG | float | 0.30 | Green color (0-1) |
| colorB | float | 0.25 | Blue color (0-1) |
| colorA | float | 0.95 | Opacity (0-1) |

---

### Radar
Minimap showing nearby player positions.

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| range | float | 45.0 | Detection range |
| size | float | 170.0 | Radar size (pixels) |
| pointSize | float | 3.0 | Player dot size |
| margin | float | 24.0 | Margin from screen edge |
| showCross | bool | true | Show center cross |
| rotateWithCamera | bool | true | Rotate with camera |
| colorR | float | 0.20 | Red color (0-1) |
| colorG | float | 0.95 | Green color (0-1) |
| colorB | float | 0.35 | Blue color (0-1) |
| colorA | float | 0.95 | Opacity (0-1) |

---

## Miscellaneous

### Scaffold
Automatically places blocks under the player's feet.

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| onlySlot | bool | false | Only activate on a specific slot |
| slotChoice | int | 0 | Required slot (0-8) |
| placeDelay | int | 50 | Delay between placements (ms) |
| automaticallySwitchSlot | bool | false | Physically switch slot |
| spoofRotation | bool | true | Spoof rotation toward block |
| lockY | bool | false | Lock Y height |
| spoofSlot | bool | true | Spoof slot for server |

---

### AutoRefill
Automatically refills potions from inventory.

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| potionId | int | 0x258 | Potion item ID (600 decimal) |
| refillDelay | int | 10 | Delay between each move (ms) |
| keybind | int | 0x75 | Activation key (VK_F6 default) |
| autoDetect | bool | false | Auto-detect open inventory |

---

### InstantBreak
Speeds up block breaking.

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| breakSpeed | float | 1.0 | Break speed multiplier |

---

## Network

### FullLatencyDisabler
Adds artificial latency via WinDivert for anti-cheat bypass.

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| baseDelay | int | 50 | Base delay (ms) |
| minDelay | int | 40 | Minimum delay for randomization |
| maxDelay | int | 80 | Maximum delay for randomization |
| randomize | bool | false | Randomize delay each cycle |
| mode | int | 0 | Mode (0 = Constant, 1 = Pulse, 2 = OnAction) |
| pulseOnMs | float | 500.0 | Pulse ON duration (ms) |
| pulseOffMs | float | 200.0 | Pulse OFF duration (ms) |
| blockCorrections | bool | false | Block server correction packets |
| onlyOnClick | bool | false | Only activate while clicking |
| onlyOnGround | bool | false | Only activate on ground |
| onlyWithModules | bool | false | Only activate when combat/movement modules are active |
| autoAdjust | bool | false | Dynamically adjust delay |



## Discord server for support and help
https://discord.gg/zeyacheat
