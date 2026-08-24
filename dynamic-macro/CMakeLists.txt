# Copyright (c) 2026 The ZMK Contributors
# SPDX-License-Identifier: MIT

# Dynamic macro events only exist on the central firmware.
if((NOT CONFIG_ZMK_SPLIT) OR CONFIG_ZMK_SPLIT_ROLE_CENTRAL)
  target_sources_ifdef(CONFIG_ZMK_BEHAVIOR_DYNAMIC_MACRO app PRIVATE src/behaviors/behavior_dynamic_macro.c)
endif()
target_include_directories(app PRIVATE include)
