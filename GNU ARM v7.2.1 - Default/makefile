################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include protocol/bluetooth/lib/EFR32BG13P/GCC/subdir.mk
-include platform/emlib/src/subdir.mk
-include platform/emdrv/sleep/src/subdir.mk
-include platform/Device/SiliconLabs/EFR32BG13P/Source/GCC/subdir.mk
-include platform/Device/SiliconLabs/EFR32BG13P/Source/subdir.mk
-include hardware/kit/common/drivers/subdir.mk
-include hardware/kit/common/bsp/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 

# All Target
all: MultibeaconBG13.axf

# Tool invocations
MultibeaconBG13.axf: $(OBJS) $(USER_OBJS)
	@echo 'Building target: $@'
	@echo 'Invoking: GNU ARM C Linker'
	arm-none-eabi-gcc -g -gdwarf-2 -mcpu=cortex-m4 -mthumb -T "/Users/clfilho/SimplicityStudio/BLE/MultibeaconBG13/efr32bg13p632f512gm48.ld" -Xlinker --gc-sections -Xlinker -Map="MultibeaconBG13.map" -mfpu=fpv4-sp-d16 -mfloat-abi=softfp --specs=nano.specs -o MultibeaconBG13.axf -Wl,--start-group "./Lab 3 - main.o" "./application_properties.o" "./gatt_db.o" "./init_app.o" "./init_board.o" "./init_mcu.o" "./pti.o" "./hardware/kit/common/bsp/bsp_stk.o" "./hardware/kit/common/drivers/mx25flash_spi.o" "./platform/Device/SiliconLabs/EFR32BG13P/Source/GCC/startup_efr32bg13p.o" "./platform/Device/SiliconLabs/EFR32BG13P/Source/system_efr32bg13p.o" "./platform/emdrv/sleep/src/sleep.o" "./platform/emlib/src/em_cmu.o" "./platform/emlib/src/em_core.o" "./platform/emlib/src/em_cryotimer.o" "./platform/emlib/src/em_crypto.o" "./platform/emlib/src/em_emu.o" "./platform/emlib/src/em_gpio.o" "./platform/emlib/src/em_i2c.o" "./platform/emlib/src/em_msc.o" "./platform/emlib/src/em_rmu.o" "./platform/emlib/src/em_rtcc.o" "./platform/emlib/src/em_system.o" "./platform/emlib/src/em_timer.o" "./platform/emlib/src/em_usart.o" "/Users/clfilho/SimplicityStudio/BLE/MultibeaconBG13/platform/radio/rail_lib/autogen/librail_release/librail_efr32xg13_gcc_release.a" "/Users/clfilho/SimplicityStudio/BLE/MultibeaconBG13/protocol/bluetooth/lib/EFR32BG13P/GCC/binapploader.o" "/Users/clfilho/SimplicityStudio/BLE/MultibeaconBG13/protocol/bluetooth/lib/EFR32BG13P/GCC/libpsstore.a" "/Users/clfilho/SimplicityStudio/BLE/MultibeaconBG13/protocol/bluetooth/lib/EFR32BG13P/GCC/libbluetooth.a" "/Users/clfilho/SimplicityStudio/BLE/MultibeaconBG13/protocol/bluetooth/lib/EFR32BG13P/GCC/libmbedtls.a" -lm -Wl,--end-group -Wl,--start-group -lgcc -lc -lnosys -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

	@echo 'Building hex file: MultibeaconBG13.hex'
	arm-none-eabi-objcopy -O ihex "MultibeaconBG13.axf" "MultibeaconBG13.hex"
	@echo ' '

	@echo 'Building bin file: MultibeaconBG13.bin'
	arm-none-eabi-objcopy -O binary "MultibeaconBG13.axf" "MultibeaconBG13.bin"
	@echo ' '

	@echo 'Building s37 file: MultibeaconBG13.s37'
	arm-none-eabi-objcopy -O srec "MultibeaconBG13.axf" "MultibeaconBG13.s37"
	@echo ' '

	@echo 'Running size tool'
	arm-none-eabi-size "MultibeaconBG13.axf"
	@echo ' '

# Other Targets
clean:
	-$(RM) $(EXECUTABLES)$(OBJS)$(C_DEPS) MultibeaconBG13.axf
	-@echo ' '

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
