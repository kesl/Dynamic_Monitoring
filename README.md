# Dynamic monitoring framework for embedded virtualization system
  This monitoring framework have dependency of on k-hypervisor at arndaleboard (https://github.com/kesl/khypervisor)
 
 If you want to test this code please refer to k-hypervisor's repository.
 
 Debugging with GDB : <br>
 Start up monitoring guest and type "gdb" command, and The monitoring guest will be stopped.
 Next step, run gdb at other host machine, and type "target remote /dev/ttyUSB#".
  
 Related document :http://keslproject.iptime.org/mediawiki/images/4/43/%ED%94%84%EB%A1%9C%ED%8C%8C%EC%9D%BC%EB%A7%81_%EC%9E%84%EB%B2%A0%EB%94%94%EB%93%9C%EA%B3%B5%ED%95%99%ED%9A%8C.hwp
  
## Source Tree
    hypervisor - monitor.c
    			 vdev_hvc_monitor.c
                 vdev_monitor.c
                 vdev_monitor_utils.c
                 
    monitor_guest - gdb_stub.c
    				guest_monitor.c
                    monitor_cli.c
                    
    util - format.c
    	   print.c
           sscanf.c
           string.c
           
    include - arch_types.h
    		  asm_arm_inline.h
              format.h
              print.h
              serial_s5p.h
              sscanf.h
              string.h
              uart_print.h

	driver - serial_s5p.c
    	     uart.c
            
