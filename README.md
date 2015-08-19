# newfunc
MATLAB tool to customize and create a formatted file for a new MATLAB function

### USAGE: newfunc(name, varargin)
          
Run `newfunc` with no args prints help and shows default VARARGINs

---

## NECESSARY ARGUMENT
- **name**
  + function name e.g. ['myfunc.m','myfunc',{'myfunc'}] if path is omitted, arg "outdir" is used (see below)

---

## VARARGIN (entered as name, value pairs)

|      NAME     |                   DESCRIPTION                   |
|---------------|-------------------------------------------------|
| descrip       | brief description to include at top of doc      |
| numargin      | number of necessary arguments                   |
| numvarargin   | number of optional arguments (name-value pairs) |
| numargout     | number of outputs                               |
| usage_example | flag to incl USAGE EXAMPLE section in doc       |
| credits       | flag to incl CREDITS section in doc             |
| authorname    | author name for Copyright seciton of doc        |
| authoremail   | author email for Copyright seciton of doc       |
| outdir        | path to save the new function file              |
| linewidth     | width (in chars) for doc and section dividers   |
| editafter     | flag to open created file in default editor     |

- run `newfunc` w/no arguments to see default values

---

## EXAMPLES

    newfunc

    newfunc('mynewfunc');

    newfunc('mynewfunc', ...
            'descrip',          'This is my new function', ...
            'numargin',         2, ...
            'numvarargin',      6, ...
            'numargout',        1, ...
            'usage_example',    true, ...
            'credits',          true  ...
            );         
