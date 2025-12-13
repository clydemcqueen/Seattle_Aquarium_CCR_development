# ArduPilot Log Resource MCP Server

## The Problem

We have a lot of log data (e.g., BIN, tlog, CSV) from our dives. We use that data for research, but we also use that data to introspect and troubleshoot the ROV system. We use tools like [MAVExplorer.py](https://github.com/ArduPilot/MAVProxy/blob/master/MAVProxy/tools/MAVExplorer.py), [UAV Log Viewer](https://plot.ardupilot.org/#/) and [ardusub_log_tools](https://github.com/clydemcqueen/ardusub_log_tools) to open files and generate graphs from the data. Effective use of these tools requires a lot of knowledge of the data, and takes time. Deep analysis of some problem often requires the creation of a 1-off tool.

## The Proposed Solution

Create an ArduPilot log [resource MCP server](https://modelcontextprotocol.io/specification/2025-06-18/server/resources). This MCP server would support all ArduPilot log data, but it would focus on ArduSub and BlueOS data, including:
* Dataflash (BIN) files from ArduSub
* MAVLink telemetry (tlog) files from QGC and BlueOS MAVLink routers
* CSV files from BlueOS extensions
* BlueOS service logs

The logs and MCP server would run locally, but the LLM would typically run in the cloud. The MCP server should support connections to a variety of LLMs. In a future version we could add a local LLM option.

This MCP server could be used with Claude Desktop, Cline, Cursor, Antigravity and other local agents.

Example questions:
* Did this dive have problems with UGPS and DVL fusion? Why?
* There were 2 transects in this dive. Please identify the start and stop timestamps.
* How did SURFTRAK perform during the transects? Were the parameters correct? Can we improve them?
* Please identify BlueOS problems for this dive, and propose solutions.
* Please create a map showing the transects on this dive. Run an RTS smoother to smooth the EK3 outputs.

## Next Steps

It probably makes sense to start with a simple version that covers tlog files and focuses on a few questions. We can add support for other file types later and questions later.

## Caveats

Reconstruction of a dive timeline from multiple log files is tricky, see [timestamp notes](https://github.com/clydemcqueen/ardusub_log_tools/blob/main/timesync.md).