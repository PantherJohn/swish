# Copyright (C) 2015  Alexander Lamaison <swish@lammy.co.uk>
#
# This program is free software: you can redistribute it and/or modify it under
# the terms of the GNU General Public License as published by the Free Software
# Foundation, either version 3 of the License, or (at your option) any later
# version.
#
# This program is distributed in the hope that it will be useful, but WITHOUT
# ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS
# FOR A PARTICULAR PURPOSE.  See the GNU General Public License for more
# details.
#
# You should have received a copy of the GNU General Public License along with
# this program.  If not, see <http://www.gnu.org/licenses/>.

set(SOURCES
  # Need to get resources from shell_folder project:
  # http://stackoverflow.com/a/1631078/67013
  KbdInteractiveDialog_test.cpp)

swish_test_suite(
  SUBJECT shell_folder VARIANT dialogue
  SOURCES ${SOURCES}
  LIBRARIES ${CMAKE_BINARY_DIR}/swish/shell_folder/shell_folder.dir/${CMAKE_CFG_INTDIR}/shell_folder.res
  ${Boost_LIBRARIES}
  LABELS gui)
