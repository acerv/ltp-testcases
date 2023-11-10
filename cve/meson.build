# SPDX-License-Identifier: GPL-2.0-or-later
# Copyright (C) 2023 SUSE LLC Andrea Cervesato <andrea.cervesato@suse.com>

pthreads = dependency('threads')

executable(
    'cve-2014-0196',
    'cve-2014-0196.c',
    dependencies: [
        libltp,
        pthreads
    ],
    link_args : [
        '-lrt',
        build_machine.system() != 'android' ? '-lutil' : '',
    ],
)

executable(
    'cve-2015-3290',
    'cve-2015-3290.c',
    dependencies: [
        libltp,
        pthreads
    ],
    c_args : [
        '-D_GNU_SOURCE',
        '-fomit-frame-pointer'
    ],
)

keyutils = compiler.find_library('keyutils', required : false)

if keyutils.found()
    executable(
        'cve-2016-7042',
        'cve-2016-7042.c',
        dependencies: [
            libltp,
            keyutils
        ],
        c_args : [
            '-D_GNU_SOURCE',
        ],
    )
endif

executable(
    'cve-2016-7117',
    'cve-2016-7117.c',
    dependencies: [
        libltp,
        pthreads
    ],
    c_args : [
        '-D_GNU_SOURCE',
    ],
    link_args : [
        '-lrt',
    ],
)

executable(
    'cve-2016-10044',
    'cve-2016-10044.c',
    dependencies: [
        libltp,
    ],
)

executable(
    'cve-2017-2618',
    'cve-2017-2618.c',
    dependencies: [
        libltp,
    ],
)

executable(
    'cve-2017-2671',
    'cve-2017-2671.c',
    dependencies: [
        libltp,
        pthreads,
    ],
    link_args : [
        '-lrt',
    ]
)

executable(
    'cve-2017-16939',
    'cve-2017-16939.c',
    dependencies: [
        libltp,
    ],
)

executable(
    'cve-2017-17052',
    'cve-2017-17052.c',
    dependencies: [
        libltp,
        pthreads,
    ],
)

executable(
    'cve-2017-17053',
    'cve-2017-17053.c',
    dependencies: [
        libltp,
        pthreads,
    ],
)

executable(
    'cve-2022-4378',
    'cve-2022-4378.c',
    dependencies: [
        libltp,
    ],
)

executable(
    'icmp_rate_limit01',
    'icmp_rate_limit01.c',
    dependencies: [
        libltp,
    ],
)

cpu = build_machine.cpu()

executable(
    'meltdown',
    'meltdown.c',
    dependencies: [
        libltp,
    ],
    c_args : [
        '-D_GNU_SOURCE',
        cpu.startswith('x86_64') or cpu.startswith('x86') ? '-msse2' : ''
    ],
)

executable(
    'stack_clash',
    'stack_clash.c',
    dependencies: [
        libltp,
    ],
    c_args : [
        '-fno-optimize-sibling-calls',
        '-Wno-infinite-recursion'
    ],
)

executable(
    'tcindex01',
    'tcindex01.c',
    dependencies: [
        libltp,
    ],
)
