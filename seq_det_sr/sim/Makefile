RTL  = ./../rtl/seq_det_sr.v
TB   = ./../tb/seq_det_sr_tb.v
TIME = ./../tb/timescale.v

run: compile simulate

compile:
	vcs -sverilog -debug_all $(TIME) $(RTL) $(TB) -l com.log

simulate:
	./simv +ntb_random_seed=$(SEED) -l sim.log

dve:
	dve -vpd vcdplus.vpd &

clean:
	rm -rf csrc* simv* *.tmp *.key *.vpd *.log DVEfiles coverage *.vdb *hdrs.v core.*
