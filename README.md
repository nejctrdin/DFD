# DEXiFunctionDerivatives
This is an online application which enables the users to input a <a href="http://kt.ijs.si/MarkoBohanec/dexi.html">DEXi</a> type function, and produces the values of first partial derivatives in the function's defined points.

The functions is defined in three lines: the first line gives the integer output for the corresponding sorted input values. The inputs are sorted firstly by the first attribute, then second, etc. The second line of the function gives the names of the input attributes, delimited by a comma. The last line gives the sizes of the respective input's scales, which are also integral.

Any subsequent lines are interpreted as additional inputs to the constructed function, which can also be floats!

The application uses *flask* to serve the web pages and does the needed preprocessing of the inputs. The derivatives of the supplied functions are interpolated with splines, using *mathematica*, and the derivatives are also computed based on the interpolated function.

You can check the code and possibly contribute at <a href="https://github.com/nejctrdin/DEXiFunctionDerivatives">github</a>.

## Prerequisites
To run the server you need <a href="http://flask.pocoo.org/">flask</a> and <a href="http://www.wolfram.com/mathematica/">mathematica</a> installed (specifically, `math` must be in your path).

## Usage

```bash
python server.py [port|license]
```

Then go to `localhost:5000` and input the desired function, for which you require the derivatives.

## License

```
Copyright (C) 2015  Nejc Trdin

    This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with this program. If not, see <http://www.gnu.org/licenses/>.
```