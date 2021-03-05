---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 54E01B3B-FFA5-4E3C-BA5A-A281FF5C9F8B
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 566081ea78137c3816ecee58e76a4811c7f54f62
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961370"
---
# <span data-ttu-id="9154f-101">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="9154f-101">Remove-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="9154f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9154f-102">SYNOPSIS</span></span>
<span data-ttu-id="9154f-103">Kończy replikację danych między bazą danych SQL a określoną pomocniczą bazą danych.</span><span class="sxs-lookup"><span data-stu-id="9154f-103">Terminates data replication between a SQL Database and the specified secondary database.</span></span>

## <span data-ttu-id="9154f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9154f-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9154f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9154f-105">DESCRIPTION</span></span>
<span data-ttu-id="9154f-106">Polecenie **cmdlet Remove-AzSqlDatabaseSecondary** wymusza zakończenie linku replikacji geograficznej.</span><span class="sxs-lookup"><span data-stu-id="9154f-106">The **Remove-AzSqlDatabaseSecondary** cmdlet forces termination of a geo-replication link.</span></span>
<span data-ttu-id="9154f-107">To polecenie cmdlet zastępuje Stop-AzSqlDatabaseCopy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9154f-107">This cmdlet replaces the Stop-AzSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="9154f-108">Przed zakończeniem nie ma synchronizacji replikacji.</span><span class="sxs-lookup"><span data-stu-id="9154f-108">There is no replication synchronization before termination.</span></span>

## <span data-ttu-id="9154f-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9154f-109">EXAMPLES</span></span>

## <span data-ttu-id="9154f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9154f-110">PARAMETERS</span></span>

### <span data-ttu-id="9154f-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9154f-111">-DatabaseName</span></span>
<span data-ttu-id="9154f-112">Określa nazwę podstawowej bazy danych Azure SQL Database z linkiem replikacji usuwanych przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9154f-112">Specifies the name of the primary Azure SQL Database that has the replication link that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9154f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9154f-113">-DefaultProfile</span></span>
<span data-ttu-id="9154f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="9154f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9154f-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9154f-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="9154f-116">Określa nazwę grupy zasobów partnerów.</span><span class="sxs-lookup"><span data-stu-id="9154f-116">Specifies the name of the partner  resource group.</span></span>

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

### <span data-ttu-id="9154f-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="9154f-117">-PartnerServerName</span></span>
<span data-ttu-id="9154f-118">Określa nazwę programu SQL Server partnera.</span><span class="sxs-lookup"><span data-stu-id="9154f-118">Specifies the name of the partner SQL Server.</span></span>

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

### <span data-ttu-id="9154f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9154f-119">-ResourceGroupName</span></span>
<span data-ttu-id="9154f-120">Określa nazwę grupy zasobów skojarzonej z linkiem replikacji do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="9154f-120">Specifies the name of the resource group that is associated with the replication link to remove.</span></span>

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

### <span data-ttu-id="9154f-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9154f-121">-ServerName</span></span>
<span data-ttu-id="9154f-122">Określa nazwę programu SQL Server z linkiem replikacji do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="9154f-122">Specifies the name of the SQL Server that has the replication link to remove.</span></span>

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

### <span data-ttu-id="9154f-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9154f-123">-Confirm</span></span>
<span data-ttu-id="9154f-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9154f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9154f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9154f-125">-WhatIf</span></span>
<span data-ttu-id="9154f-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9154f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9154f-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9154f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9154f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9154f-128">CommonParameters</span></span>
<span data-ttu-id="9154f-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9154f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9154f-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9154f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9154f-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9154f-131">INPUTS</span></span>

### <span data-ttu-id="9154f-132">System.String</span><span class="sxs-lookup"><span data-stu-id="9154f-132">System.String</span></span>

## <span data-ttu-id="9154f-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9154f-133">OUTPUTS</span></span>

### <span data-ttu-id="9154f-134">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="9154f-134">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="9154f-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9154f-135">NOTES</span></span>

## <span data-ttu-id="9154f-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9154f-136">RELATED LINKS</span></span>

[<span data-ttu-id="9154f-137">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="9154f-137">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="9154f-138">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="9154f-138">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="9154f-139">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="9154f-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
