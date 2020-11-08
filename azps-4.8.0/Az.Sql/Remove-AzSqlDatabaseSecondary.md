---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 54E01B3B-FFA5-4E3C-BA5A-A281FF5C9F8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 4353a61efd0141947879ad6795c321f5ed43e1d3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220290"
---
# <span data-ttu-id="898ab-101">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="898ab-101">Remove-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="898ab-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="898ab-102">SYNOPSIS</span></span>
<span data-ttu-id="898ab-103">Kończenie replikacji danych między bazą danych SQL a określoną pomocniczą bazą danych.</span><span class="sxs-lookup"><span data-stu-id="898ab-103">Terminates data replication between a SQL Database and the specified secondary database.</span></span>

## <span data-ttu-id="898ab-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="898ab-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="898ab-105">Opis</span><span class="sxs-lookup"><span data-stu-id="898ab-105">DESCRIPTION</span></span>
<span data-ttu-id="898ab-106">Polecenie cmdlet **Remove-AzSqlDatabaseSecondary** wymusza zakończenie linku replikacji geograficznej.</span><span class="sxs-lookup"><span data-stu-id="898ab-106">The **Remove-AzSqlDatabaseSecondary** cmdlet forces termination of a geo-replication link.</span></span>
<span data-ttu-id="898ab-107">To polecenie cmdlet zastępuje Stop-AzSqlDatabaseCopy polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="898ab-107">This cmdlet replaces the Stop-AzSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="898ab-108">Nie istnieje Synchronizacja replikacji przed zakończeniem.</span><span class="sxs-lookup"><span data-stu-id="898ab-108">There is no replication synchronization before termination.</span></span>

## <span data-ttu-id="898ab-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="898ab-109">EXAMPLES</span></span>

## <span data-ttu-id="898ab-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="898ab-110">PARAMETERS</span></span>

### <span data-ttu-id="898ab-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="898ab-111">-DatabaseName</span></span>
<span data-ttu-id="898ab-112">Określa nazwę podstawowej bazy danych SQL Azure z linkiem replikacji usuwanym przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="898ab-112">Specifies the name of the primary Azure SQL Database that has the replication link that this cmdlet removes.</span></span>

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

### <span data-ttu-id="898ab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="898ab-113">-DefaultProfile</span></span>
<span data-ttu-id="898ab-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="898ab-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="898ab-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="898ab-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="898ab-116">Określa nazwę grupy zasobów partnera.</span><span class="sxs-lookup"><span data-stu-id="898ab-116">Specifies the name of the partner  resource group.</span></span>

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

### <span data-ttu-id="898ab-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="898ab-117">-PartnerServerName</span></span>
<span data-ttu-id="898ab-118">Określa nazwę serwera SQL partnera.</span><span class="sxs-lookup"><span data-stu-id="898ab-118">Specifies the name of the partner SQL Server.</span></span>

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

### <span data-ttu-id="898ab-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="898ab-119">-ResourceGroupName</span></span>
<span data-ttu-id="898ab-120">Określa nazwę grupy zasobów, która jest skojarzona z linkiem replikacji do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="898ab-120">Specifies the name of the resource group that is associated with the replication link to remove.</span></span>

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

### <span data-ttu-id="898ab-121">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="898ab-121">-ServerName</span></span>
<span data-ttu-id="898ab-122">Określa nazwę serwera SQL z linkiem replikacji do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="898ab-122">Specifies the name of the SQL Server that has the replication link to remove.</span></span>

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

### <span data-ttu-id="898ab-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="898ab-123">-Confirm</span></span>
<span data-ttu-id="898ab-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="898ab-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="898ab-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="898ab-125">-WhatIf</span></span>
<span data-ttu-id="898ab-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="898ab-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="898ab-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="898ab-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="898ab-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="898ab-128">CommonParameters</span></span>
<span data-ttu-id="898ab-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="898ab-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="898ab-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="898ab-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="898ab-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="898ab-131">INPUTS</span></span>

### <span data-ttu-id="898ab-132">System. String</span><span class="sxs-lookup"><span data-stu-id="898ab-132">System.String</span></span>

## <span data-ttu-id="898ab-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="898ab-133">OUTPUTS</span></span>

### <span data-ttu-id="898ab-134">Microsoft. Azure. Commands. SQL. Replication. model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="898ab-134">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="898ab-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="898ab-135">NOTES</span></span>

## <span data-ttu-id="898ab-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="898ab-136">RELATED LINKS</span></span>

[<span data-ttu-id="898ab-137">Nowe — AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="898ab-137">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="898ab-138">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="898ab-138">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="898ab-139">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="898ab-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
