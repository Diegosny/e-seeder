# E-seeder


Facil manipulação das seeds

Requirements
============

- Laravel >= 8.0
- PHP >= 8.0

Features
============

- Permite semear bancos de dados em diferentes ambientes com diferentes valores.
- Permite "versionar" sementes da mesma forma que o Laravel atualmente lida com migrações. A execução do ```php artisan seed``` só executará as sementes que ainda não foram executadas.
- Permite executar várias sementes do mesmo modelo/tabela
- Avisa se seu banco de dados está em produçã

Usage
============
Quando você instala o LaravelSeeder, vários comandos do artisan ficam disponiveis para se usar semelhante aos comandos da migrations

<tabela>
<tr><td>seed</td><td>Executa todas as sementes no diretório "seeders" que ainda não foram executadas.</td></tr>
<tr><td>seed:rollback</td><td>A reversão não desfaz a propagação (o que seria impossível com uma chave primária de incremento automático). Ele apenas permite que você execute novamente o último lote de sementes.</td></tr>
<tr><td>seed:reset</td><td>Reinicia todas as sementes.</td></tr>
<tr><td>seed:refresh</td><td>Reinicia e executa novamente todas as sementes.</td></tr>
<tr><td>seed:status</td><td>Obtém o status de cada propagador migrável.</td></tr>
<tr><td>seed:make</td><td>Cria uma nova classe seed no ambiente que você especificar.</td></tr>
<tr><td>seed:install</td><td>Você não precisa usar isso... ele será executado automaticamente quando você chamar "seed"</td></tr>
</table>

Ambiente Local
============

```
docker-compose up -d --build
```

```
docker-compose exec laravel-seeder test.sh
```

```
docker-compose exec laravel-seeder code-coverage.sh
```
