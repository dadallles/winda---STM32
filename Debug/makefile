################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Startup/subdir.mk
-include Src/subdir.mk
-include Drivers/STM32F4xx_HAL_Driver/Src/subdir.mk
-include Drivers/BSP/STM32F429I-Discovery/subdir.mk
-include Drivers/BSP/Components/wm8994/subdir.mk
-include Drivers/BSP/Components/ts3510/subdir.mk
-include Drivers/BSP/Components/stmpe811/subdir.mk
-include Drivers/BSP/Components/stmpe1600/subdir.mk
-include Drivers/BSP/Components/st7789h2/subdir.mk
-include Drivers/BSP/Components/st7735/subdir.mk
-include Drivers/BSP/Components/s5k5cag/subdir.mk
-include Drivers/BSP/Components/ov2640/subdir.mk
-include Drivers/BSP/Components/otm8009a/subdir.mk
-include Drivers/BSP/Components/mfxstm32l152/subdir.mk
-include Drivers/BSP/Components/lsm303dlhc/subdir.mk
-include Drivers/BSP/Components/ls016b8uy/subdir.mk
-include Drivers/BSP/Components/lis3dsh/subdir.mk
-include Drivers/BSP/Components/lis302dl/subdir.mk
-include Drivers/BSP/Components/l3gd20/subdir.mk
-include Drivers/BSP/Components/ili9341/subdir.mk
-include Drivers/BSP/Components/ili9325/subdir.mk
-include Drivers/BSP/Components/ft6x06/subdir.mk
-include Drivers/BSP/Components/exc7200/subdir.mk
-include Drivers/BSP/Components/cs43l22/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
lab2a.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
lab2a.list \

OBJCOPY_HEX += \
lab2a.hex \

OBJCOPY_BIN += \
lab2a.bin \


# All Target
all: lab2a.elf secondary-outputs

# Tool invocations
lab2a.elf: $(OBJS) $(USER_OBJS) C:\Users\Student_lab507\Documents\lab0004\projekt\STM32F429ZITX_FLASH.ld
	arm-none-eabi-gcc -o "lab2a.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"C:\Users\Student_lab507\Documents\lab0004\projekt\STM32F429ZITX_FLASH.ld" --specs=nosys.specs -Wl,-Map="lab2a.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -u _printf_float -u _scanf_float -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

lab2a.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "lab2a.list"
	@echo 'Finished building: $@'
	@echo ' '

lab2a.hex: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "lab2a.hex"
	@echo 'Finished building: $@'
	@echo ' '

lab2a.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "lab2a.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_HEX) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
