---
title: "Consultas básicas - Core EF"
author: rowanmiller
ms.author: divega
ms.date: 10/27/2016
ms.assetid: ab6e35f1-397f-41c0-9ef4-85aec5466377
ms.technology: entity-framework-core
uid: core/querying/basic
ms.openlocfilehash: 5070faf2aeeffad680e24e7de5a0ffa03a8f0064
ms.sourcegitcommit: 01a75cd483c1943ddd6f82af971f07abde20912e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2017
---
# <a name="basic-queries"></a>Consultas básicas

Saiba como carregar entidades do banco de dados usando linguagem integrar LINQ (consulta).

> [!TIP]  
> Você pode exibir este artigo [exemplo](https://github.com/aspnet/EntityFramework.Docs/tree/master/samples/core/Querying) no GitHub.

## <a name="101-linq-samples"></a>Exemplos do 101 LINQ

Esta página mostra alguns exemplos para realizar tarefas comuns com o Entity Framework Core. Para um amplo conjunto de exemplos que mostram o que é possível com o LINQ, consulte [exemplos do 101 LINQ](https://code.msdn.microsoft.com/101-LINQ-Samples-3fb9811b).

## <a name="loading-all-data"></a>Carregar todos os dados

<!-- [!code-csharp[Main](samples/core/Querying/Querying/Basics/Sample.cs)] -->
``` csharp
using (var context = new BloggingContext())
{
    var blogs = context.Blogs.ToList();
}
```

## <a name="loading-a-single-entity"></a>Carregar uma única entidade

<!-- [!code-csharp[Main](samples/core/Querying/Querying/Basics/Sample.cs)] -->
``` csharp
using (var context = new BloggingContext())
{
    var blog = context.Blogs
        .Single(b => b.BlogId == 1);
}
```

## <a name="filtering"></a>Filtragem

<!-- [!code-csharp[Main](samples/core/Querying/Querying/Basics/Sample.cs)] -->
``` csharp
using (var context = new BloggingContext())
{
    var blogs = context.Blogs
        .Where(b => b.Url.Contains("dotnet"))
        .ToList();
}
```
