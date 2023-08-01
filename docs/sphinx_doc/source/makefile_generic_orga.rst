Folder Organization use in Generic Makefile
===========================================

Project Folder Organization
---------------------------

Here is the folder organization of a HDL project:

.. Folder Organization
.. graphviz::
   
    digraph project_orga {
    "project_dir_name" [shape=folder];
    "scripts"          [shape=folder];
    "do_files"         [shape=folder];
    "run_files"        [shape=folder];
    "waves"            [shape=folder];
    "scenarios"        [shape=folder];
    "sources"          [shape=folder];
    "tb_sources"       [shape=folder];

    "sources_dir" [shape=plain label="HDL sources"];
    "scripts_dir" [shape=plain label="Makefile and specific scripts"]
    "scenarios_dir" [shape=plain label="Python scenarios"]
    "run_files_dir" [shape=plain label="Run files for each scenarios"]
    "waves_dir" [shape=plain label="Wave file for each scenarios"]
    "tb_sources_dir" [shape=plain label="Testbench sources"]
    
    "project_dir_name" -> "scripts"
    "project_dir_name" -> "do_files"
    "project_dir_name" -> "scenarios"
    "project_dir_name" -> "sources"
    "project_dir_name" -> "tb_sources"
    "do_files"         -> "run_files"
    "do_files"         -> "waves"


    "sources" -> "sources_dir"
    "scripts" -> "scripts_dir"
    "scenarios" -> "scenarios_dir"
    "run_files" -> "run_files_dir"
    "waves" -> "waves_dir"
    "tb_sources" -> "tb_sources_dir"
    }


Simulation Folder Organization
------------------------------

Here is the folder organization of the simulation of en HDL project :

.. graphviz::
       
    digraph simulation_folder {
    "HDL_SIMU_PATH"    [shape=folder];
    "PROJECT_NAME"     [shape=folder];
    "transcripts"      [shape=folder];
    "WLF"              [shape=folder];
    "scenarios"        [shape=folder];
    "LOGS"             [shape=folder];

    "transcripts_plain" [shape=plain label="Modelsim Transcript for each scenario"]

    "WLF_plain" [shape=plain label="Modelsim wavevorm in .wlf format"]
    "scenarios_plain" [shape=plain label="The scenarios in .txt format"]

    "LOGS_plain" [shape=plain label="The compilation logs"]

    "HDL_SIMU_PATH" -> "PROJECT_NAME"
    "PROJECT_NAME" -> "transcripts"
    "PROJECT_NAME" -> "WLF"
    "PROJECT_NAME" -> "scenarios"
    "PROJECT_NAME" -> "LOGS"

    "transcripts" -> "transcripts_plain"
    "WLF"         -> "WLF_plain"
    "scenarios"   -> "scenarios_plain"
    "LOGS"        -> "LOGS_plain"
    }



