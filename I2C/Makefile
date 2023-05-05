TARGET          = i2c_master
IVERILOG        = iverilog

SRC             = \
     $(TARGET)_top.v i2c_master_bit_ctrl.v i2c_master_byte_ctrl.v  

SIM_SRC = $(TARGET)_TB.v    wb_master_model.v \
                            i2c_slave_model.v

iversim: 
	$(IVERILOG) -gno-io-range-error -o $(TARGET)_TB.vvp $(VINCDIR) $(SRC) $(SIM_SRC) -s $(TARGET)_TB
	vvp $(TARGET)_TB.vvp; 
	gtkwave $(TARGET)_TB.vcd&


