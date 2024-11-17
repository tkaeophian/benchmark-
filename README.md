## Benchmark Performance Tester

A simple Node.js script to measure and benchmark the performance of HTTP requests. This tool runs multiple iterations against a provided URL and calculates various performance metrics, including average latency, median latency, and percentiles.

### Features

- Request Performance Metrics:
  - Tracks duration, status, and timestamp for each request.
- Statistics Calculation:
  - Average, median, min, max latency.
    95th and 99th percentiles.
- Error Handling:
  - Logs failed requests for debugging.
- Dynamic Progress Indicator:
  - Provides real-time progress updates.

### Requirements

- Node.js: v16 or higher

### Installation

1. Clone this repository:

```shell
git clone git@github.com:tkaeophian/benchmark.git

```

2. Install dependencies:

```shell
npm install
```

### Usage

Run the script by providing the URL to benchmark and optionally the number of iterations (default: 300):

```shell
npm run benchmark <url>

```

### Examples

Benchmark with default iterations (300):

```shell
npm run benchmark https://example.com

```

Benchmark with custom iterations (e.g., 1000):

```shell
npm run benchmark https://example.com 1000

```

### Output

After running the script, you will see the following metrics:

- Total Requests: Number of successful requests.
- Failed Requests: Number of errors encountered.
- Average Latency: Average time taken for requests.
- Median Latency: Middle latency value.
- Min/Max Latency: Fastest and slowest requests.
- 95th and 99th Percentile: Tail latency metrics for high-load performance.

### Sample Output:

```shell
Starting benchmark for https://example.com
Running 300 iterations...
Progress: 100% (300/300)

Benchmark complete!

Results:
--------------------------------------------------
Total Requests: 290
Failed Requests: 10
Average Latency: 120.35ms
Median Latency: 115.00ms
Min Latency: 95.40ms
Max Latency: 210.80ms
95th Percentile: 200.45ms
99th Percentile: 210.00ms

Errors encountered:
Error 1: Network timeout
Error 2: 503 Service Unavailable

```