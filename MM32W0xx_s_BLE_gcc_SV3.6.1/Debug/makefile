################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include USER/subdir.mk
-include SYSTEM/uart/subdir.mk
-include SYSTEM/sys/subdir.mk
-include SYSTEM/delay/subdir.mk
-include HARDWARE/SPI/subdir.mk
-include HARDWARE/RCC_MCU/subdir.mk
-include HARDWARE/LED_MESH/subdir.mk
-include HARDWARE/IWDG/subdir.mk
-include HARDWARE/IRQ/subdir.mk
-include HARDWARE/IIC/subdir.mk
-include HARDWARE/CALLBACK/subdir.mk
-include HARDWARE/AT_CMD/subdir.mk
-include HARDWARE/APP/subdir.mk
-include Device/MM32W0xx/Source/ARM/subdir.mk
-include Device/MM32W0xx/Source/subdir.mk
-include Device/MM32W0xx/HAL_lib/src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(ASM_DEPS)),)
-include $(ASM_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
SECONDARY_FLASH += \
MM32W0xx_s_BLE_gcc_SV3.6.1.hex \

SECONDARY_SIZE += \
MM32W0xx_s_BLE_gcc_SV3.6.1.siz \


# All Target
all: MM32W0xx_s_BLE_gcc_SV3.6.1.elf secondary-outputs

# Tool invocations
MM32W0xx_s_BLE_gcc_SV3.6.1.elf: $(OBJS) $(USER_OBJS)
	@echo 'Building target: $@'
	@echo 'Invoking: Cross ARM GNU C Linker'
	arm-none-eabi-gcc -mcpu=cortex-m0 -mthumb -O0 -fmessage-length=0 -fsigned-char -ffunction-sections -fdata-sections  -g3 -T "/home/neomissing/eclipse-workspace/MM32W0xx_s_BLE_gcc_SV3.6.1/Device/MM32W0xx/Source/mm32_flash.ld" -Xlinker --gc-sections -L"/home/neomissing/eclipse-workspace/MM32W0xx_s_BLE_gcc_SV3.6.1/SRC_LIB/lib" -Wl,-Map,"MM32W0xx_s_BLE_gcc_SV3.6.1.map" --specs=nosys.specs -o "MM32W0xx_s_BLE_gcc_SV3.6.1.elf" $(OBJS) $(USER_OBJS) $(LIBS)
	@echo 'Finished building target: $@'
	@echo ' '

MM32W0xx_s_BLE_gcc_SV3.6.1.hex: MM32W0xx_s_BLE_gcc_SV3.6.1.elf
	@echo 'Invoking: Cross ARM GNU Create Flash Image'
	arm-none-eabi-objcopy -O ihex "MM32W0xx_s_BLE_gcc_SV3.6.1.elf"  "MM32W0xx_s_BLE_gcc_SV3.6.1.hex"
	@echo 'Finished building: $@'
	@echo ' '

MM32W0xx_s_BLE_gcc_SV3.6.1.siz: MM32W0xx_s_BLE_gcc_SV3.6.1.elf
	@echo 'Invoking: Cross ARM GNU Print Size'
	arm-none-eabi-size --format=berkeley "MM32W0xx_s_BLE_gcc_SV3.6.1.elf"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) $(OBJS)$(SECONDARY_FLASH)$(SECONDARY_SIZE)$(ASM_DEPS)$(S_UPPER_DEPS)$(C_DEPS) MM32W0xx_s_BLE_gcc_SV3.6.1.elf
	-@echo ' '

secondary-outputs: $(SECONDARY_FLASH) $(SECONDARY_SIZE)

.PHONY: all clean dependents

-include ../makefile.targets
