CREATE DATABASE board_db;

USE board_db;

CREATE TABLE boards (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nome VARCHAR(255) NOT NULL
);

CREATE TABLE colunas (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nome VARCHAR(255) NOT NULL,
    tipo VARCHAR(50) NOT NULL,
    ordem INT NOT NULL,
    board_id INT,
    FOREIGN KEY (board_id) REFERENCES boards(id)
);

CREATE TABLE cards (
    id INT AUTO_INCREMENT PRIMARY KEY,
    titulo VARCHAR(255) NOT NULL,
    descricao TEXT,
    data_criacao DATETIME DEFAULT CURRENT_TIMESTAMP,
    bloqueado BOOLEAN DEFAULT FALSE,
    motivo_bloqueio TEXT,
    data_bloqueio DATETIME,
    data_desbloqueio DATETIME,
    coluna_id INT,
    data_movimento DATETIME DEFAULT CURRENT_TIMESTAMP,
    FOREIGN KEY (coluna_id) REFERENCES colunas(id)
);
