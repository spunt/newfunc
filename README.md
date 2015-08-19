# barpatch
MATLAB tool to create bar graph with error bars using patch and line objects

This function will create a grouped bar graph with error bars without
using the standard plotting functions BAR and ERRORBAR. It uses PATCH to
create the bars and LINE to construct the error bars.

 USAGE: h = barpatch(data, varargin)

__________________________________________________________________________
 OUTPUT
    h: handles to graphic objects  

__________________________________________________________________________
 INPUTS
    data:       data matrix to plot; rows are cases, cols are variables  
    varargin:   each are "name, value" pairs
      figh        = parent figure for plot
      groupidx    = rows index columns of "data" to plot as a group
      groupname   = labels for different groups of bars
      barname     = labels for different bars within groups (in legend)
      grouptick   = flag to place tickmark between groups on x-axis
      t           = figure title
      xl          = x-axis label
      yl          = y-axis label
      fontsize    = base font size
      fontname    = name of font to use

__________________________________________________________________________
 USAGE EXAMPLE
    data        = randn(10, 8); 
    groupidx    = [1 2; 3 4; 5 6; 7 8]; 
    groupname   = {'Group A' 'Group B' 'Group C' 'Group D'};
    barname     = {'Level 1' 'Level 2'}; 
    xl          = 'X-Axis Label'; 
    yl          = 'Y-Axis Label';
    t           = 'The Figure Title';
  figh        = figure('color', 'white'); 
    h = barpatch(data, 'figh', figh, 'groupidx', groupidx, 'groupname', groupname, 'barname', barname, 'xl', xl, 'yl', yl, 't', t); 


---------------------- Copyright (C) 2014 Bob Spunt ----------------------
    Created:  2015-03-09
    Email:    spunt@caltech.edu

  This program is free software: you can redistribute it and/or modify
  it under the terms of the GNU General Public License as published by
  the Free Software Foundation, either version 3 of the License, or (at
  your option) any later version.
      This program is distributed in the hope that it will be useful, but
  WITHOUT ANY WARRANTY; without even the implied warranty of
  MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU
  General Public License for more details.
      You should have received a copy of the GNU General Public License
  along with this program.  If not, see: http://www.gnu.org/licenses/.
__________________________________________________________________________
