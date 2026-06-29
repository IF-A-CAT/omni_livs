# Time Synchronization

This document describes the time synchronization strategy used by the device
system.

## Overview

The system uses PTP synchronization for the main high-rate sensors. LiDAR,
cameras, and IMU data are synchronized with the host through PTP, using the
hardware clock of the host network interface as the PTP master clock.

The GNSS receiver uses its own satellite time reference. Its output time is
converted from GPS week and time-of-week seconds into UNIX time before being
used by the system.

## PTP-Based Synchronization

LiDAR, cameras, and IMU are synchronized through PTP. In this setup:

- The host network interface hardware clock acts as the PTP master.
- LiDAR timestamps are aligned to the PTP time domain.
- Camera timing is aligned to the same PTP time domain.
- IMU data associated with the LiDAR module follows the same synchronized time
  reference.

The expected PTP synchronization accuracy is in the sub-microsecond to
microsecond range under a properly configured wired network with hardware
timestamping support. The final measured accuracy should be verified on the
actual device using PTP offset logs and sensor timestamp comparison.

## Camera Triggering

The Hikvision cameras are synchronized through the camera internal action
trigger mechanism. After the cameras are aligned to the PTP time domain, an
internal action command is used to trigger the cameras together, so image frames
from the camera group can be captured with consistent timing.

## GNSS Time Conversion

The GNSS receiver outputs position data with GPS time. The GPS timestamp is
converted to UNIX time using:

- GPS week number
- Seconds within the GPS week

This conversion allows GNSS position data to be compared with host-side sensor
timestamps and logs.

## GNSS Latency Note

The host receives time through network time synchronization, while GNSS position
data is produced by the GNSS receiver and then transmitted to the host. Because
of this data path, the GNSS output position time can have millisecond-level
latency relative to the host's real time.

This latency should be considered when fusing GNSS data with LiDAR, camera, and
IMU data.
