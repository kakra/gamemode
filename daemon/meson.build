# Main daemon
daemon_sources = [
    'gamemoded.c',
    'gamemode-config.c',
    'gamemode-context.c',
    'gamemode-dbus.c',
    'gamemode-env.c',
    'gamemode-gpu.c',
    'gamemode-ioprio.c',
    'gamemode-proc.c',
    'gamemode-sched.c',
    'gamemode-tests.c',
    'gamemode-wine.c',
]

gamemoded_includes = libgamemode_includes
gamemoded_includes += config_h_dir

executable(
    'gamemoded',
    sources: daemon_sources,
    dependencies: [
        link_daemon_common,
        dep_threads,
        dep_systemd,
        inih_dependency,
        libdl,
    ],
    include_directories: [
        gamemoded_includes,
        include_daemon_common,
    ],
    install: true,
)
