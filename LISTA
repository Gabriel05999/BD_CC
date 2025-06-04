-- 2
SELECT r.nome AS nome_responsavel,
COUNT(t.id) AS quantidade_tarefas
FROM responsaveis r
JOIN tarefas t ON r.id = t.id_responsavel_tarefa
GROUP BY r.id, r.nome
HAVING COUNT(t.id) >= 3
ORDER BY quantidade_tarefas DESC;

-- 5
SELECT p.id, p.nome as projeto, COUNT(t.id) as total_tarefas
from projetos p
left join tarefas t on p.id = t.id_projeto
group by p.id, p.nome
order by total_tarefas desc 
limit 5;

-- 6
select *
from responsaveis, projetos, tarefas;

select titulo, r.nome as responsaveis
from tarefas, responsaveis r;
