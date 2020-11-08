---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 54E01B3B-FFA5-4E3C-BA5A-A281FF5C9F8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 4353a61efd0141947879ad6795c321f5ed43e1d3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052160"
---
# <span data-ttu-id="b665e-101">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b665e-101">Remove-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="b665e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b665e-102">SYNOPSIS</span></span>
<span data-ttu-id="b665e-103">Kończenie replikacji danych między bazą danych SQL a określoną pomocniczą bazą danych.</span><span class="sxs-lookup"><span data-stu-id="b665e-103">Terminates data replication between a SQL Database and the specified secondary database.</span></span>

## <span data-ttu-id="b665e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b665e-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b665e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b665e-105">DESCRIPTION</span></span>
<span data-ttu-id="b665e-106">Polecenie cmdlet **Remove-AzSqlDatabaseSecondary** wymusza zakończenie linku replikacji geograficznej.</span><span class="sxs-lookup"><span data-stu-id="b665e-106">The **Remove-AzSqlDatabaseSecondary** cmdlet forces termination of a geo-replication link.</span></span>
<span data-ttu-id="b665e-107">To polecenie cmdlet zastępuje Stop-AzSqlDatabaseCopy polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b665e-107">This cmdlet replaces the Stop-AzSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="b665e-108">Nie istnieje Synchronizacja replikacji przed zakończeniem.</span><span class="sxs-lookup"><span data-stu-id="b665e-108">There is no replication synchronization before termination.</span></span>

## <span data-ttu-id="b665e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b665e-109">EXAMPLES</span></span>

## <span data-ttu-id="b665e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b665e-110">PARAMETERS</span></span>

### <span data-ttu-id="b665e-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b665e-111">-DatabaseName</span></span>
<span data-ttu-id="b665e-112">Określa nazwę podstawowej bazy danych SQL Azure z linkiem replikacji usuwanym przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b665e-112">Specifies the name of the primary Azure SQL Database that has the replication link that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b665e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b665e-113">-DefaultProfile</span></span>
<span data-ttu-id="b665e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b665e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b665e-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b665e-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="b665e-116">Określa nazwę grupy zasobów partnera.</span><span class="sxs-lookup"><span data-stu-id="b665e-116">Specifies the name of the partner  resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b665e-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="b665e-117">-PartnerServerName</span></span>
<span data-ttu-id="b665e-118">Określa nazwę serwera SQL partnera.</span><span class="sxs-lookup"><span data-stu-id="b665e-118">Specifies the name of the partner SQL Server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b665e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b665e-119">-ResourceGroupName</span></span>
<span data-ttu-id="b665e-120">Określa nazwę grupy zasobów, która jest skojarzona z linkiem replikacji do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="b665e-120">Specifies the name of the resource group that is associated with the replication link to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b665e-121">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="b665e-121">-ServerName</span></span>
<span data-ttu-id="b665e-122">Określa nazwę serwera SQL z linkiem replikacji do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="b665e-122">Specifies the name of the SQL Server that has the replication link to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b665e-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b665e-123">-Confirm</span></span>
<span data-ttu-id="b665e-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b665e-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b665e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b665e-125">-WhatIf</span></span>
<span data-ttu-id="b665e-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b665e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b665e-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b665e-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b665e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b665e-128">CommonParameters</span></span>
<span data-ttu-id="b665e-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b665e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b665e-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b665e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b665e-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b665e-131">INPUTS</span></span>

### <span data-ttu-id="b665e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b665e-132">System.String</span></span>

## <span data-ttu-id="b665e-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b665e-133">OUTPUTS</span></span>

### <span data-ttu-id="b665e-134">Microsoft. Azure. Commands. SQL. Replication. model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="b665e-134">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="b665e-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b665e-135">NOTES</span></span>

## <span data-ttu-id="b665e-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b665e-136">RELATED LINKS</span></span>

[<span data-ttu-id="b665e-137">Nowe — AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b665e-137">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="b665e-138">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b665e-138">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="b665e-139">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="b665e-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
