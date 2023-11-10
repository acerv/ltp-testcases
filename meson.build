# SPDX-License-Identifier: GPL-2.0-or-later
# Copyright (C) 2023 SUSE LLC Andrea Cervesato <andrea.cervesato@suse.com>

project(
    'ltp-testcases',
    'c',
    license : 'GPL-2.0+',
    version : '20230929',
    default_options : [
        'c_std=gnu99',
        'warning_level=2',
        'buildtype=debugoptimized',
        'prefix=/opt/ltp/testcases/bin',
    ],
    meson_version: '>=1.2.3'
)

compiler = meson.get_compiler('c')

libltp = compiler.find_library('ltp', required : true)

subdir('cve')
