## Installing Hadoop

**Prerequisites:**

* Operating System: Linux (Recommended) - While alternatives like Windows with Cygwin exist, Linux provides a more straightforward installation process.
* Java Development Kit (JDK): Ensure you have a compatible Java version installed. Check the official Hadoop documentation for supported versions.

**Installation Steps:**

1. **Download Hadoop:**

   * Visit the Apache Software Foundation's Hadoop download page: [https://hadoop.apache.org/releases.html](https://hadoop.apache.org/releases.html)
   * Download a recent stable release of the pre-built binary package for your chosen Linux distribution.

2. **Extract the Archive:**

   * Open a terminal window and navigate to the directory where you downloaded the Hadoop archive.
   * Use an appropriate command based on the archive format (e.g., tar or zip) to extract the files.
   * Common commands:
     * `tar -xvf hadoop-<version>.tar.gz`
     * `unzip hadoop-<version>.zip`

3. **Configure Environment Variables:**

   * Edit your shell configuration file (e.g., `.bashrc` for Bash).
   * Add the following lines, replacing `<hadoop_installation_directory>` with the actual path where you extracted Hadoop:

   ```bash
   export JAVA_HOME=/usr/lib/jvm/java-X.X  # Replace X.X with your Java version
   export HADOOP_INSTALL=/path/to/hadoop-<version>
   export PATH=$PATH:$HADOOP_INSTALL/bin:$HADOOP_INSTALL/sbin
   export HADOOP_MAPRED_HOME=$HADOOP_INSTALL
   export HADOOP_COMMON_HOME=$HADOOP_INSTALL
   export HADOOP_HDFS_HOME=$HADOOP_INSTALL
   export YARN_HOME=$HADOOP_INSTALL
   ```

   * Save and source the configuration file to apply changes:

   ```bash
   source ~/.bashrc
   ```

4. **Verify Installation:**

   * Open a new terminal window to ensure environment variables are loaded correctly.
   * Check Java installation:

   ```bash
   java -version
   ```

   * Verify Hadoop installation:

   ```bash
   hadoop version
   ```


