##
## This file is part of the libopencm3 project.
##
## Copyright (C) 2013 Frantisek Burian <BuFran@seznam.cz>
##
## This library is free software: you can redistribute it and/or modify
## it under the terms of the GNU Lesser General Public License as published by
## the Free Software Foundation, either version 3 of the License, or
## (at your option) any later version.
##
## This library is distributed in the hope that it will be useful,
## but WITHOUT ANY WARRANTY; without even the implied warranty of
## MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
## GNU Lesser General Public License for more details.
##
## You should have received a copy of the GNU Lesser General Public License
## along with this library.  If not, see <http://www.gnu.org/licenses/>.
##

LIBNAME		= libopencm3_stm32f0

PREFIX		?= arm-none-eabi
#PREFIX		?= arm-elf
CC		= $(PREFIX)-gcc
AR		= $(PREFIX)-ar
CFLAGS		= -Os -g \
		  -Wall -Wextra -Wimplicit-function-declaration \
		  -Wredundant-decls -Wmissing-prototypes -Wstrict-prototypes \
		  -Wundef -Wshadow \
		  -I../../../include -fno-common \
		  -mcpu=cortex-m0 $(FP_FLAGS) -mthumb -Wstrict-prototypes \
		  -ffunction-sections -fdata-sections -MD -DSTM32F0

ARFLAGS		= rcs

OBJS		= flash.o rcc.o usart.o dma.o rtc.o comparator.o crc.o \
                  dac.o i2c.o iwdg.o pwr.o gpio.o timer.o adc.o

OBJS            += gpio_common_all.o gpio_common_f0234.o crc_common_all.o \
                   pwr_common_all.o iwdg_common_all.o rtc_common_l1f024.o \
                   dma_common_l1f013.o exti_common_all.o spi_common_all.o \
		   spi_common_f03.o

VPATH += ../../usb:../:../../cm3:../common

include ../../Makefile.include

