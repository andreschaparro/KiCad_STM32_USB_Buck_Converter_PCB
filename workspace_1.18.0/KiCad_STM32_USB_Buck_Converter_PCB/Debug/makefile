################################################################################
# Automatically-generated file. Do not edit!
# Toolchain: GNU Tools for STM32 (13.3.rel1)
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include USB_DEVICE/Target/subdir.mk
-include USB_DEVICE/App/subdir.mk
-include Middlewares/ST/STM32_USB_Device_Library/Core/Src/subdir.mk
-include Middlewares/ST/STM32_USB_Device_Library/Class/CDC/Src/subdir.mk
-include Drivers/STM32F4xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(S_DEPS)),)
-include $(S_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

OPTIONAL_TOOL_DEPS := \
$(wildcard ../makefile.defs) \
$(wildcard ../makefile.init) \
$(wildcard ../makefile.targets) \


BUILD_ARTIFACT_NAME := KiCad_STM32_USB_Buck_Converter_PCB
BUILD_ARTIFACT_EXTENSION := elf
BUILD_ARTIFACT_PREFIX :=
BUILD_ARTIFACT := $(BUILD_ARTIFACT_PREFIX)$(BUILD_ARTIFACT_NAME)$(if $(BUILD_ARTIFACT_EXTENSION),.$(BUILD_ARTIFACT_EXTENSION),)

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
KiCad_STM32_USB_Buck_Converter_PCB.elf \

MAP_FILES += \
KiCad_STM32_USB_Buck_Converter_PCB.map \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
KiCad_STM32_USB_Buck_Converter_PCB.list \


# All Target
all: main-build

# Main-build Target
main-build: KiCad_STM32_USB_Buck_Converter_PCB.elf secondary-outputs

# Tool invocations
KiCad_STM32_USB_Buck_Converter_PCB.elf KiCad_STM32_USB_Buck_Converter_PCB.map: $(OBJS) $(USER_OBJS) E:\Proyectos\KiCad_STM32_USB_Buck_Converter_PCB\workspace_1.18.0\KiCad_STM32_USB_Buck_Converter_PCB\STM32F405RGTX_FLASH.ld makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-gcc -o "KiCad_STM32_USB_Buck_Converter_PCB.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"E:\Proyectos\KiCad_STM32_USB_Buck_Converter_PCB\workspace_1.18.0\KiCad_STM32_USB_Buck_Converter_PCB\STM32F405RGTX_FLASH.ld" --specs=nosys.specs -Wl,-Map="KiCad_STM32_USB_Buck_Converter_PCB.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

KiCad_STM32_USB_Buck_Converter_PCB.list: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "KiCad_STM32_USB_Buck_Converter_PCB.list"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) KiCad_STM32_USB_Buck_Converter_PCB.elf KiCad_STM32_USB_Buck_Converter_PCB.list KiCad_STM32_USB_Buck_Converter_PCB.map default.size.stdout
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST)

fail-specified-linker-script-missing:
	@echo 'Error: Cannot find the specified linker script. Check the linker settings in the build configuration.'
	@exit 2

warn-no-linker-script-specified:
	@echo 'Warning: No linker script specified. Check the linker settings in the build configuration.'

.PHONY: all clean dependents main-build fail-specified-linker-script-missing warn-no-linker-script-specified

-include ../makefile.targets
