# C based market data engine

### Core Requirements

This service should be responsible for acquiring, processing, and serving real-time market data with minimal latency.

**Data Acquisition:**
- Integrate with at least one financial data API (consider free options with rate limits)
- Implement a mechanism to fetch market data at regular intervals
- Design a strategy for handling API rate limits and connection failures
- Consider what granularity of data you need (tick data, minute bars, daily closes)

**Data Processing:**
- Implement technical indicators that traders use to analyze price action
- Calculate rolling statistics efficiently
- Store processed data in an appropriate format
- Consider what the memory footprint would be for storing historical data

**Data Serving:**
- Expose processed data through an API interface
- Design the API endpoints: what information should be queryable? (specific stocks, date ranges, indicators)
- Consider caching strategies for frequently requested data