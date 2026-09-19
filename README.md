# MKM__JULIA__v1
Microkinetics modeling in JULIA, version 1, for research in heterogeneous catalysis

PARAMETERS
   these parameters override any similar parameters in the customization data file
   
   parameter               data type       description
   _______________________ _______________ _______________________________________________________________________________________________________________
   core_path               string          absolute path to the Microkinetics__Core.jl module used to perform the simulation
   datafile_path           string          absolute path to the customization data file (.xml)
   cl_dir                  string          absolute path to the directory from which the script was called
   runs_dir                string          relative path to the 'runs' subfolder - only used if the 'userunsubfolder' option is TRUE
   run_folder              string          relative path to the simulation run
   dbgprfx                 string          prefix string added to all logging
   partofset               boolean         must be FALSE
   setindex                integer         must be 0
   run_temperature_value   number/string   temperature at which to run the simulation; can be a comma-delimited string for multiple temperatures
   run_temperature_units   string          temperature units 
   run_timespan_value      double          timespan over which to run the simulation
   run_timespan_units      string          timespan units
   run_taskjobid           string          must be ''
   run_taskarrayid         string          must be '' 
   run_parallelworkers     integer         must be 0
   run_cache_method        string          must be '' 
   solv_sbs_extend         boolean         indicates whether to extend the timespan if stable state isn't detected 
   solv_sts_extend         boolean         indicates whether to extend the timespan if steady state isn't detected 
   solv_sps_extend         boolean         indicates whether to extend the timespan if single pathway state isn't detected 
   solv_scaling_tflag      boolean         indicates whether to use time scaling 
   solv_scaling_tfactor    double          time scaling factor
   solv_num_fmt            string          number format (Float64, Double64, BigFloat)
   solv_num_prec           integer         number precision which is meaningful only for BigFloat numbers
   drcs_analyze            boolean         indicates whether to perform sensitivity analysis
   calc_optss              boolean         must be FALSE
   
EXAMPLE SIMULATION - JULIA COMMANDS
   core_path             = "<path_to_core_module>"
   datafile_path         = "<path_to_data_file>"
   cl_dir                = "<path_to_cl_dir>"
   runs_dir              = "__Runs"
   run_folder            = "AcOH_Decomp_01"
   dbgprfx               = "" 
   partofset             = false
   setindex              = 0
   run_temperature_value = 300.0
   run_temperature_units = "K"
   run_timespan_value    = 1e15 
   run_timespan_units    = "sec"
   run_taskjobid         = "" 
   run_taskarrayid       = "" 
   run_parallelworkers   = 0 
   run_cache_method      = "" 
   solv_sbs_extend       = false
   solv_sts_extend       = false
   solv_sps_extend       = false
   solv_scaling_tflag    = true 
   solv_scaling_tfactor  = 1e10 
   solv_num_fmt          = "Double64"
   solv_num_prec         = 0
   drcs_analyze          = true 
   calc_optss            = false 
   include(core_path)
   Microkinetics__Core__Main(core_path, datafile_path, cl_dir, runs_dir, run_folder, dbgprfx, partofset, setindex, run_temperature_value, run_temperature_units, run_timespan_value, run_timespan_units, run_taskjobid, run_taskarrayid, run_parallelworkers, run_cache_method, solv_sbs_extend, solv_sts_extend, solv_sps_extend, solv_scaling_tflag, solv_scaling_tfactor, solv_num_fmt, solv_num_prec, drcs_analyze, calc_optss)
  
        
