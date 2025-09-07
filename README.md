🚀 Enuygun.com Flight Search Load Testing Suite

📋 Overview
Professional JMeter test suite for load testing Enuygun.com's flight search functionality with Cloudflare bypass support and comprehensive reporting.
✨ Features

✅ Cloudflare Protection Bypass - Automated cookie handling
✅ Realistic User Simulation - Human-like behavior patterns
✅ Comprehensive Reporting - HTML, CSV, and Dashboard reports
✅ Parameterized Testing - Dynamic date and route selection
✅ Error Handling - Robust assertion and validation
✅ CI/CD Ready - Command-line execution support

🚦 Quick Start
Prerequisites
# Check Java installation (Required: Java 8+)
java -version

# Download and install JMeter
wget https://archive.apache.org/dist/jmeter/binaries/apache-jmeter-5.6.3.tgz
tar -xzf apache-jmeter-5.6.3.tgz
cd apache-jmeter-5.6.3

# Set environment variables
export JMETER_HOME=$(pwd)
export PATH=$PATH:$JMETER_HOME/bin


🏃‍♂️ Running Your First Test

# 1. Basic execution
jmeter -n -t enuygun-flight-search.jmx -l results.jtl

# 2. With HTML report generation
jmeter -n -t enuygun-flight-search.jmx -l results.jtl -e -o report/

# 3. With custom parameters
jmeter -n -t enuygun-flight-search.jmx \
-Jusers=10 \
-Jrampup=30 \
-Jloops=5 \
-l results.jtl \
-e -o report/

# Generate comprehensive HTML dashboard
jmeter -g results.jtl -o dashboard/

![img.png](img.png)