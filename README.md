UART #(
	.CLKFREQ(12000000)
	,.MASTER_BAUD(115200)
	,.SLAVE_BAUD(115200)
)uut_UART(
        //SYSTEM INTERFACE
			.clk(),
			.rst_n(),
        //MASTER INTERFACE
			.master_rx(),
			.master_tx(),
            //SEND DATA PORT
			.master_send(),
			.master_tx_data(),//8bits
			.master_ready(),
            //RECEIVE DATA PORT
			.master_valid(),
			.master_rx_data(),//8bits
			.master_cbe(),//check bit error   
			.master_sbe(),//stop bit error
        //SLAVE INTERFACE
			.slave_rx(),
			.slave_tx(),
            //SEND DATA PROT
			.slave_send(),
			.slave_tx_data(),
			.slave_ready(),
            //RECEIVE DATA PORT
			.slave_valid(),
			.slave_rx_data(),
			.slave_cbe(),//check bit error
			.slave_sbe()//stop bit error
);

This module can communicate with up to 2 independent device 
You can set baud individually to each one 
Check bit and Stop bit verification are supported , Initially with Odd verification and two stop bit
If one of the device is unused ,leave it unconnected
