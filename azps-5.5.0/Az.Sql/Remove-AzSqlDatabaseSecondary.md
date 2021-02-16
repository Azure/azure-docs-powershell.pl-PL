---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 54E01B3B-FFA5-4E3C-BA5A-A281FF5C9F8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 4353a61efd0141947879ad6795c321f5ed43e1d3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196027"
---
# <span data-ttu-id="1508e-101">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="1508e-101">Remove-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="1508e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1508e-102">SYNOPSIS</span></span>
<span data-ttu-id="1508e-103">Kończy replikację danych między bazą danych SQL a określoną pomocniczą bazą danych.</span><span class="sxs-lookup"><span data-stu-id="1508e-103">Terminates data replication between a SQL Database and the specified secondary database.</span></span>

## <span data-ttu-id="1508e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1508e-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1508e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="1508e-105">DESCRIPTION</span></span>
<span data-ttu-id="1508e-106">Polecenie **cmdlet Remove-AzSqlDatabaseSecondary** wymusza zakończenie linku replikacji geograficznej.</span><span class="sxs-lookup"><span data-stu-id="1508e-106">The **Remove-AzSqlDatabaseSecondary** cmdlet forces termination of a geo-replication link.</span></span>
<span data-ttu-id="1508e-107">To polecenie cmdlet zastępuje Stop-AzSqlDatabaseCopy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1508e-107">This cmdlet replaces the Stop-AzSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="1508e-108">Przed zakończeniem nie ma synchronizacji replikacji.</span><span class="sxs-lookup"><span data-stu-id="1508e-108">There is no replication synchronization before termination.</span></span>

## <span data-ttu-id="1508e-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1508e-109">EXAMPLES</span></span>

## <span data-ttu-id="1508e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1508e-110">PARAMETERS</span></span>

### <span data-ttu-id="1508e-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1508e-111">-DatabaseName</span></span>
<span data-ttu-id="1508e-112">Określa nazwę podstawowej bazy danych Azure SQL Database z linkiem replikacji usuwanych przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1508e-112">Specifies the name of the primary Azure SQL Database that has the replication link that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1508e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1508e-113">-DefaultProfile</span></span>
<span data-ttu-id="1508e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="1508e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1508e-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1508e-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="1508e-116">Określa nazwę grupy zasobów partnerów.</span><span class="sxs-lookup"><span data-stu-id="1508e-116">Specifies the name of the partner  resource group.</span></span>

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

### <span data-ttu-id="1508e-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="1508e-117">-PartnerServerName</span></span>
<span data-ttu-id="1508e-118">Określa nazwę programu SQL Server partnera.</span><span class="sxs-lookup"><span data-stu-id="1508e-118">Specifies the name of the partner SQL Server.</span></span>

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

### <span data-ttu-id="1508e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1508e-119">-ResourceGroupName</span></span>
<span data-ttu-id="1508e-120">Określa nazwę grupy zasobów skojarzonej z linkiem replikacji do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="1508e-120">Specifies the name of the resource group that is associated with the replication link to remove.</span></span>

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

### <span data-ttu-id="1508e-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1508e-121">-ServerName</span></span>
<span data-ttu-id="1508e-122">Określa nazwę programu SQL Server z linkiem replikacji do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="1508e-122">Specifies the name of the SQL Server that has the replication link to remove.</span></span>

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

### <span data-ttu-id="1508e-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1508e-123">-Confirm</span></span>
<span data-ttu-id="1508e-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1508e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1508e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1508e-125">-WhatIf</span></span>
<span data-ttu-id="1508e-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1508e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1508e-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1508e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1508e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1508e-128">CommonParameters</span></span>
<span data-ttu-id="1508e-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1508e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1508e-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1508e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1508e-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1508e-131">INPUTS</span></span>

### <span data-ttu-id="1508e-132">System.String</span><span class="sxs-lookup"><span data-stu-id="1508e-132">System.String</span></span>

## <span data-ttu-id="1508e-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1508e-133">OUTPUTS</span></span>

### <span data-ttu-id="1508e-134">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="1508e-134">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="1508e-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1508e-135">NOTES</span></span>

## <span data-ttu-id="1508e-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1508e-136">RELATED LINKS</span></span>

[<span data-ttu-id="1508e-137">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="1508e-137">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="1508e-138">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="1508e-138">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="1508e-139">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="1508e-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
