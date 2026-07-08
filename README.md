## VLA

Vision-Language-Action (VLA) is a multimodal policy framework that maps visual observations, language instructions, and robot state information to actions.

The vision encoder extracts spatial features from camera images, while the text encoder represents task instructions as language features.

These features are combined with robot state information to form a unified multimodal representation used by the policy network.

This structure enables the robot to interpret task context, identify relevant objects and targets, and generate actions according to natural-language commands.

## VLA - training result

### fetch ( Gymnasium, MuJoCo )
<div align="center">
<table>
  <tr>
    <td align="center">
      <img src="readme_assets/fet_01.gif" width="100%">
      <br>
      <em> Initial training </em>
    </td>
    <td align="center">
      <img src="readme_assets/fet_02.gif" width="100%">
      <br>
      <em> RL - Expert </em>
    </td>
    <td align="center">
      <strong>Under Implementation</strong>
      <br>
      <em> post training </em>
    </td>
  </tr>
</table>
</div>

## AIML

Adaptive Importance Metric Learning (AIML) is a trajectory-conditioned re-weighting module for reinforcement learning.

AIML learns dimension-wise importance weights from recent history and applies them to the current normalized input representation.

The input can be an observation, state, action-related feature, or any structured representation used by the policy or value or belief network.

## AIML - training result

### cart pole ( Gymnasium )
<div align="center">
<table>
  <tr>
    <td align="center">
      <img src="readme_assets/ctp_01.gif" width="100%">
      <br>
      <em> Initial training ( position 0 ~ 2 )</em>
    </td>
    <td align="center">
      <img src="readme_assets/ctp_02.gif" width="100%">
      <br>
      <em> post training ( position ≈ 0 ) </em>
    </td>
  </tr>
</table>
</div>

### inverted double pendulum ( Gymnasium, MuJoCo )
<div align="center">
<table>
  <tr>
    <td align="center">
      <img src="readme_assets/idp_01.gif" width="100%">
      <br>
      <em> Initial training ( position 0 ~ 2 )</em>
    </td>
    <td align="center">
      <img src="readme_assets/idp_02.gif" width="100%">
      <br>
      <em> post training ( position ≈ 0 ) </em>
    </td>
  </tr>
</table>
</div>

### half cheetah ( Gymnasium, MuJoCo )
<div align="center">
<table>
  <tr>
    <td align="center">
      <img src="readme_assets/hct_01.gif" width="100%">
      <br>
      <em> Initial training ( 0 m/s )</em>
    </td>
    <td align="center">
      <img src="readme_assets/hct_02.gif" width="100%">
      <br>
      <em> post training ( 6 ~ 7 m/s ) </em>
    </td>
  </tr>
</table>
</div> 

## Distributed Reinforcement Learning

Distributed Reinforcement Learning is a scalable reinforcement learning framework designed to accelerate data collection and policy optimization.

Multiple rollout workers interact with independent environment instances in parallel, while collected trajectories are aggregated and used to update the policy or value networks.

This approach improves sample efficiency, increases training throughput, and enables reinforcement learning agents to learn from diverse experiences at scale.

## Distributed Reinforcement Learning - concept
<div align="center">
  <img src="readme_assets/Concept.png" width="100%">
  <br>
  <em>Concept overview</em>
</div>
