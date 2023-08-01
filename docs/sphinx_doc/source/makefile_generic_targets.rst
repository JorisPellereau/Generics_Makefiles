Targets of Generic Makefile
===========================

List of the targets
-------------------

+---------------------------+--------------------------------------------------------------------------------------+
| Targets                   | Description                                                                          |
+===========================+======================================================================================+
| create_dir                | Create project directories from the $(ROOT) path                                     |
+---------------------------+--------------------------------------------------------------------------------------+
| create_temp_project       | Create the simulation folder named $(PROJECT_NAME) in $(HDL_SIMU_PATH)               |
+---------------------------+--------------------------------------------------------------------------------------+
| create_temp_dir           | Create sub-folder in $(PROJECT_NAME)/$(HDL_SIMU_PATH) path                           |
+---------------------------+--------------------------------------------------------------------------------------+
| create_work               | Create Modelsim work directory in $(PROJECT_NAME)/$(HDL_SIMU_PATH) path              |
+---------------------------+--------------------------------------------------------------------------------------+
| create_simulation_dir     | This target performed : create_temp_project create_temp_dir create_work              |
+---------------------------+--------------------------------------------------------------------------------------+
| clean_work                | Clean the work directory                                                             |
+---------------------------+--------------------------------------------------------------------------------------+
| clean_transcripts         | Clean the transcript directory                                                       |
+---------------------------+--------------------------------------------------------------------------------------+
| clean_wlf                 | Clean the WLF directory                                                              |
+---------------------------+--------------------------------------------------------------------------------------+
| clean_logs                | Clean the logs directory                                                             |
+---------------------------+--------------------------------------------------------------------------------------+
| clean_all                 | Remove all folder in $(HDL_SIMU_PATH)/$(PROJECT_NAME) path                           |
+---------------------------+--------------------------------------------------------------------------------------+
| prepare_libs              | Create Modelsim Library folder with vlib command                                     |
|                           | in $(HDL_SIMU_PATH)/$(PROJECT_NAME) path and from the LIB_LIST                       |
+---------------------------+--------------------------------------------------------------------------------------+
| create_libs               | Mapped Modelsim Library folder with vmap command                                     |
|                           | in $(HDL_SIMU_PATH)/$(PROJECT_NAME) path and from the LIB_LIST                       |
+---------------------------+--------------------------------------------------------------------------------------+
| libs                      | prepare_libs create_libs                                                             |
+---------------------------+--------------------------------------------------------------------------------------+
| compile_tb_vhd_files      | Compile Testench VHDL files                                                          |
+---------------------------+--------------------------------------------------------------------------------------+
| compile_tb_v_files        | Compile Testench Verilog/SystemVerilog files                                         |
+---------------------------+--------------------------------------------------------------------------------------+
| compile_design_vhd_files  | Compile Design VHDL files                                                            |
+---------------------------+--------------------------------------------------------------------------------------+
| compile_design_v_files    | Compile Design Verilog/SystemVerilog files                                           |
+---------------------------+--------------------------------------------------------------------------------------+
| compile_all               | TBD   Compile Design Verilog/SystemVerilog files                                     |
+---------------------------+--------------------------------------------------------------------------------------+
| generate_scn              | Run the $(TEST).py python scenario in and generates its text format in               |
|                           | $(HDL_SIMU_PATH)/$(PROJECT_NAME)/scenarios path                                      |
+---------------------------+--------------------------------------------------------------------------------------+
| generate_all_scn          | Generates text scenarii from the SCN_LIST in                                         |
|                           | $(HDL_SIMU_PATH)/$(PROJECT_NAME)/scenarios path                                      |
+---------------------------+--------------------------------------------------------------------------------------+
| run_test                  | Run the test from $(TEST). Check the scenario at the end                             |
+---------------------------+--------------------------------------------------------------------------------------+
| run_multiple_test         | Run Multiple test                                                                    |
+---------------------------+--------------------------------------------------------------------------------------+
| check_one_tests           | Check if the test is succesful and display the result in the prompt                  |
+---------------------------+--------------------------------------------------------------------------------------+
| check_multiple_tests      | Check if multiple test are succesful and display the result in the prompt            |
+---------------------------+--------------------------------------------------------------------------------------+
| create_run_do_files       | Create a run do file from a $(TEST)                                                  |
+---------------------------+--------------------------------------------------------------------------------------+
| create_wave_do_files      | Create a wave do file from a $(TEST)                                                 |
+---------------------------+--------------------------------------------------------------------------------------+
| print_compile_logs_file   | Get compilation log and print color in console                                       |
+---------------------------+--------------------------------------------------------------------------------------+


.. code-block:: 

   Run a test :
   make run_test TEST=UART_000
