CREATE DATABASE uClases;
use uClases;
--
-- Base de datos: `uclases`
--
 
-- --------------------------------------------------------
 
--
-- Estructura de tabla para la tabla `area`
--
 
CREATE TABLE `area` (
  `areaid` int(11) NOT NULL,
  `nombre` varchar(80) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;
 
-- --------------------------------------------------------
 
--
-- Estructura de tabla para la tabla `cursos`
--
 
CREATE TABLE `cursos` (
  `cursoid` int(11) NOT NULL,
  `nombre` varchar(120) NOT NULL,
  `estado` char(1) NOT NULL DEFAULT '1',
  `areaid` int(11) NOT NULL,
  `instructorid` int(11) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;
 
-- --------------------------------------------------------
 
--
-- Estructura de tabla para la tabla `instructor`
--
 
CREATE TABLE `instructor` (
  `instructorid` int(11) NOT NULL,
  `nombrecompleto` varchar(200) NOT NULL,
  `especialidad` varchar(100) DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;
 
--
-- Índices para tablas volcadas
--
 
--
-- Indices de la tabla `area`
--
ALTER TABLE `area`
  ADD PRIMARY KEY (`areaid`);
 
--
-- Indices de la tabla `cursos`
--
ALTER TABLE `cursos`
  ADD PRIMARY KEY (`cursoid`),
  ADD KEY `areaid` (`areaid`),
  ADD KEY `instructorid` (`instructorid`);
 
--
-- Indices de la tabla `instructor`
--
ALTER TABLE `instructor`
  ADD PRIMARY KEY (`instructorid`);
 
--
-- AUTO_INCREMENT de las tablas volcadas
--
 
--
-- AUTO_INCREMENT de la tabla `area`
--
ALTER TABLE `area`
  MODIFY `areaid` int(11) NOT NULL AUTO_INCREMENT;
 
--
-- AUTO_INCREMENT de la tabla `cursos`
--
ALTER TABLE `cursos`
  MODIFY `cursoid` int(11) NOT NULL AUTO_INCREMENT;
 
--
-- AUTO_INCREMENT de la tabla `instructor`
--
ALTER TABLE `instructor`
  MODIFY `instructorid` int(11) NOT NULL AUTO_INCREMENT;
 
--
-- Restricciones para tablas volcadas
--
 
--
-- Filtros para la tabla `cursos`
--
ALTER TABLE `cursos`
  ADD CONSTRAINT `cursos_ibfk_1` FOREIGN KEY (`areaid`) REFERENCES `area` (`areaid`),
  ADD CONSTRAINT `cursos_ibfk_2` FOREIGN KEY (`instructorid`) REFERENCES `instructor` (`instructorid`);
COMMIT;
