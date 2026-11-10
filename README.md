<!--
SPDX-FileCopyrightText: 2023 German Aerospace Center (DLR)
SPDX-License-Identifier: CC-BY-NC-ND-4.0
-->

[![experimental](http://badges.github.io/stability-badges/dist/experimental.svg)](http://github.com/badges/stability-badges)

> This tool is based on the paper [A Ros Adapter for RTLola](https://doi.org/10.1007/978-3-032-05435-7_6), which was published at [RV'25](https://rv25.isec.tugraz.at/).

> This work is ongoing, and I plan to add features in the future. Feel free to share any requests! You can reach me via sebastian dot schirmer at dlr dot de or open an issue.
# RTLola-Ros2-Monitor

ROS 2 adapter for CISPA's RTLola monitoring interpreter.
Minor fixes for usage in a ROS2 drone workspace have been applied.

# Usage
Start nodes that have to be monitored, e.g.:
```
ros2 bag play -l ./bags/rosbag_2026-08-28_16-56-25_hassan_box/
```
Write a minimal translator node that breaks important messages into single bool, int32, unit32 or float32 msgs that can be used for generation.
Navigate into repo directory, then:
```
cd monitor && cargo run
```
Once succesful set the ros2.toml to 
```
generate = False
```
Output of the monitoring is a bool for whether node transition conditions have been met under \RTLolaOutput

## Credits to
- Sebastian Schirmer
  
## License
Please see the file [LICENSE.md](LICENSE.md) for further information about how the content is licensed.
