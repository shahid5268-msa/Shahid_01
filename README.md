---
- name: Setup Oracle environment
  hosts: all
  tasks:
    - name: Set ORACLE_HOME and LD_LIBRARY_PATH environment variables
      shell: |
        echo "ORACLE_HOME is set to $ORACLE_HOME"
        echo "LD_LIBRARY_PATH is set to $LD_LIBRARY_PATH"
      environment:
        ORACLE_HOME: /path/to/oracle/home
        LD_LIBRARY_PATH: /path/to/oracle/lib

    - name: Run Oracle-specific command
      shell: ./run_oracle_command.sh
      environment:
        ORACLE_HOME: /path/to/oracle/home
        LD_LIBRARY_PATH: /path/to/oracle/lib