---
title: "Novidades no EF Core 1.1 – EF Core"
author: divega
ms.author: divega
ms.date: 10/27/2016
ms.assetid: C7FE8C85-445A-4F0C-97EC-CC3F7F1D6F5E
ms.technology: entity-framework-core
uid: core/what-is-new/ef-core-1.1
ms.openlocfilehash: 74c1033cab2704bdbb9fa4d3ce111df1f1c29418
ms.sourcegitcommit: 01a75cd483c1943ddd6f82af971f07abde20912e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2017
---
# <a name="new-features-in-ef-core-11"></a>Novos recursos no EF Core 1.1

## <a name="modelling"></a>Modelagem
### <a name="field-mapping"></a>Mapeamento de campo
Permite que você configure um campo de suporte para uma propriedade. Isso pode ser útil para propriedades somente leitura, ou para dados que tenham os métodos Get/Set em vez de uma propriedade.
### <a name="mapping-to-memory-optimized-tables-in-sql-server"></a>Mapeamento de tabelas com otimização de memória no SQL Server
Você pode especificar que a tabela para a qual uma entidade está mapeada tem otimização de memória. Ao usar o EF Core para criar e manter um banco de dados com base em seu modelo (com migrações ou `Database.EnsureCreated()`), uma tabela com otimização de memória será criada para essas entidades.

## <a name="change-tracking"></a>Change tracking
### <a name="additional-change-tracking-apis-from-ef6"></a>APIs de controle de alterações adicionais do EF6
Como `Reload`, `GetModifiedProperties`, `GetDatabaseValues` etc.

## <a name="query"></a>Consulta
### <a name="explicit-loading"></a>Carregamento explícito
Permite que você dispare o preenchimento de uma propriedade de navegação em uma entidade que carregada previamente do banco de dados.
### <a name="dbsetfind"></a>DbSet.Find
Fornece uma maneira fácil de obter uma entidade com base em seu valor de chave primária.

## <a name="other"></a>Outros
### <a name="connection-resiliency"></a>Resiliência da conexão
Automaticamente repete comandos de banco de dados com falha. Isso é especialmente útil ao se conectar com o SQL Azure, em que falhas transitórias são comuns.
### <a name="simplified-service-replacement"></a>Substituição de serviço simplificada
Facilita a substituição dos serviços internos usados pelo EF.
