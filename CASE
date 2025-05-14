# BD_CC

CASE

select nroa, capacidade,
case
	when capacidade <= 25 then 'pequeno'
    when capacidade > 25 and capacidade < 50 then 'medio'
    when capacidade >= 50 then 'grande'
    else 'valor incorreto'
end as tamanho
from clinica.ambulatorios;

-- clinica

-- 1

select status_pagamento,
	case 
    when status_pagamento = 'pago' then 'PG'
    when status_pagamento = 'pendente' then 'PD'
    when status_pagamento = 'cancelado' then 'C'
    else  'D'
end as status_descriçao
from eventos_db.inscricoes
join inscriçao as i on e.id = i.id_evento
join participantes as p on i.id_participantes = p.id;

-- 2

select data_inicio, data_fim,
	case
    when datediff(data_inicio, data_fim) then 'Evento de 1 dia'
	when datediff(data_inicio, data_fim) then 'Evento de curta duraçao'
    when datediff(data_inicio, data_fim) then 'Evento de longa duraçao'
end as classificacao_evento
from eventos_db.inscricoes,

-- 3

SELECT inscricao,
    CASE 
	WHEN YEAR(data_inscricao) < 2024 THEN 'Veterano'
	ELSE 'Novo'
    END AS tipo_participante
FROM eventos_db.participantes;

-- 4

select tarefas,
case
when tarefa = 'diretor' then 'Gestor principal'
when tarefa = 'Supervisor' then 'Coordenador' or 'Supervisor'
else 'Apoio'
end as funcao
from eventos_db.organizadores;

-- 5

select nome,
case
when telefone is not null then 'WhatsApp'
when telefone is null and email is not null then 'E-mail'
when telefone is null and email is null then 'Sem conatato disponivel'
end as prioridade_contato
from eventos_db.participantes;

-- 6

select nome_eventos,
case 
when tipo_de_evento = 'corrida' or 'Campeonato' or 'Torneio'
when tipo_de_evento = 'Oficina' or 'Curso' or 'Palestra'
else 'Outro'
end as classificacao_tipo
from eventos_db.eventos
