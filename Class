-- phpMyAdmin SQL Dump
-- version 4.7.0
-- https://www.phpmyadmin.net/
--
-- Servidor: 127.0.0.1
-- Tiempo de generación: 19-06-2020 a las 02:01:57
-- Versión del servidor: 10.1.26-MariaDB
-- Versión de PHP: 7.1.8

SET SQL_MODE = "NO_AUTO_VALUE_ON_ZERO";
SET AUTOCOMMIT = 0;
START TRANSACTION;
SET time_zone = "+00:00";


/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET @OLD_CHARACTER_SET_RESULTS=@@CHARACTER_SET_RESULTS */;
/*!40101 SET @OLD_COLLATION_CONNECTION=@@COLLATION_CONNECTION */;
/*!40101 SET NAMES utf8mb4 */;

--
-- Base de datos: `class`
--

-- --------------------------------------------------------

--
-- Estructura de tabla para la tabla `curse`
--

CREATE TABLE `curse` (
  `id` int(11) NOT NULL,
  `Curse` varchar(255) NOT NULL,
  `Duration_M` int(11) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

--
-- Volcado de datos para la tabla `curse`
--

INSERT INTO `curse` (`id`, `Curse`, `Duration_M`) VALUES
(1, 'Curso S', 17),
(2, 'Curso M', 17),
(3, 'Curso P', 17),
(4, 'Curso H', 20),
(5, 'Curso B', 15);

-- --------------------------------------------------------

--
-- Estructura de tabla para la tabla `estudent`
--

CREATE TABLE `estudent` (
  `id` int(11) NOT NULL,
  `Name` varchar(255) NOT NULL,
  `Telepone` int(11) NOT NULL,
  `Age` int(11) NOT NULL,
  `Curse_id` int(11) NOT NULL,
  `SeminaryE_id` int(11) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

--
-- Volcado de datos para la tabla `estudent`
--

INSERT INTO `estudent` (`id`, `Name`, `Telepone`, `Age`, `Curse_id`, `SeminaryE_id`) VALUES
(1, 'Albert Petrancovsk', 85764766, 21, 2, 1),
(2, 'Christin Peralta', 24154676, 26, 3, 2),
(3, 'Albert Monserrat', 5456242, 23, 1, 1),
(4, 'Zoren Herd', 6786662, 19, 1, 1),
(5, 'Cloud Phanin', 7577761, 28, 2, 1),
(6, 'Ciel Makinsen', 6767922, 25, 4, 3),
(7, 'Erwin Smith', 8096533, 30, 5, 3),
(8, 'Zack Hamilton', 4666121, 20, 3, 2),
(9, 'Trevor Salmont', 5766104, 23, 4, 3),
(10, 'Saipha Alpes', 1238932, 27, 5, 3),
(11, 'Cónrad Vhelor', 7961319, 29, 5, 3),
(12, 'Levi Ackerman', 7456000, 30, 1, 1),
(13, 'Mikasa Ackerman', 5796750, 18, 1, 1),
(14, 'Lucien De\'Latov', 5665765, 23, 3, 2),
(15, 'Vlad Montesco', 6748792, 27, 1, 1),
(16, 'Lucy Capuleto', 7859803, 24, 2, 1),
(17, 'Angeal Belior', 6547773, 22, 3, 2),
(18, 'Estehin Seraph', 7896968, 25, 5, 3),
(19, 'Raily Olsen', 5606105, 26, 4, 3),
(20, 'Keny Ackerman', 6765933, 27, 4, 3);

-- --------------------------------------------------------

--
-- Estructura de tabla para la tabla `seminary`
--

CREATE TABLE `seminary` (
  `id` int(11) NOT NULL,
  `Name` varchar(255) NOT NULL,
  `Duration_Me` int(11) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

--
-- Volcado de datos para la tabla `seminary`
--

INSERT INTO `seminary` (`id`, `Name`, `Duration_Me`) VALUES
(1, 'Seminary S and M', 5),
(2, 'Seminary P', 4),
(3, 'Seminary H And B', 6);

-- --------------------------------------------------------

--
-- Estructura de tabla para la tabla `teacher`
--

CREATE TABLE `teacher` (
  `id` int(11) NOT NULL,
  `Name` varchar(255) NOT NULL,
  `Direction` varchar(255) NOT NULL,
  `Telephon` int(11) NOT NULL,
  `Turn` varchar(255) NOT NULL,
  `CurseP_id` int(11) NOT NULL,
  `SeminaryP_id` int(11) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

--
-- Volcado de datos para la tabla `teacher`
--

INSERT INTO `teacher` (`id`, `Name`, `Direction`, `Telephon`, `Turn`, `CurseP_id`, `SeminaryP_id`) VALUES
(1, 'Jail Ross', 'Wall Maria', 1324243, 'AM', 1, 1),
(2, 'Shart Bol', 'Shiganshina', 9756487, 'PM', 1, 1),
(3, 'Historia Reis', 'Wall Maria', 2347645, 'AM', 2, 1),
(4, 'Tutankamon Sor', 'Egypt', 1367687, 'PM', 3, 2),
(5, 'Eren Jeaguer', 'Shiganshina', 8667586, 'AM', 4, 3),
(6, 'Shizuka Matsumoto', 'Wall Maria', 1325424, 'PM', 5, 3);

--
-- Índices para tablas volcadas
--

--
-- Indices de la tabla `curse`
--
ALTER TABLE `curse`
  ADD PRIMARY KEY (`id`);

--
-- Indices de la tabla `estudent`
--
ALTER TABLE `estudent`
  ADD PRIMARY KEY (`id`),
  ADD KEY `FOREIGN` (`Curse_id`),
  ADD KEY `FOREIGN_1` (`SeminaryE_id`);

--
-- Indices de la tabla `seminary`
--
ALTER TABLE `seminary`
  ADD PRIMARY KEY (`id`);

--
-- Indices de la tabla `teacher`
--
ALTER TABLE `teacher`
  ADD PRIMARY KEY (`id`),
  ADD KEY `FOREIGN` (`CurseP_id`) USING BTREE,
  ADD KEY `FOREIGN2` (`SeminaryP_id`);

--
-- AUTO_INCREMENT de las tablas volcadas
--

--
-- AUTO_INCREMENT de la tabla `curse`
--
ALTER TABLE `curse`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=6;
--
-- AUTO_INCREMENT de la tabla `estudent`
--
ALTER TABLE `estudent`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=21;
--
-- AUTO_INCREMENT de la tabla `seminary`
--
ALTER TABLE `seminary`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=4;
--
-- AUTO_INCREMENT de la tabla `teacher`
--
ALTER TABLE `teacher`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=7;
--
-- Restricciones para tablas volcadas
--

--
-- Filtros para la tabla `estudent`
--
ALTER TABLE `estudent`
  ADD CONSTRAINT `FOREIGN` FOREIGN KEY (`Curse_id`) REFERENCES `curse` (`id`),
  ADD CONSTRAINT `FOREIGN_1` FOREIGN KEY (`SeminaryE_id`) REFERENCES `seminary` (`id`);

--
-- Filtros para la tabla `teacher`
--
ALTER TABLE `teacher`
  ADD CONSTRAINT `FOREIGN1` FOREIGN KEY (`CurseP_id`) REFERENCES `curse` (`id`),
  ADD CONSTRAINT `FOREIGN2` FOREIGN KEY (`SeminaryP_id`) REFERENCES `seminary` (`id`);
COMMIT;

/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40101 SET CHARACTER_SET_RESULTS=@OLD_CHARACTER_SET_RESULTS */;
/*!40101 SET COLLATION_CONNECTION=@OLD_COLLATION_CONNECTION */;
