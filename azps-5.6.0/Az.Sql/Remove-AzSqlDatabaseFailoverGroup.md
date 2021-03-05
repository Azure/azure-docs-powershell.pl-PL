---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: adc3bc9c8d367da6f031f8847cee7ce48b3f9b43
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961386"
---
# <span data-ttu-id="27fce-101">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="27fce-101">Remove-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="27fce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27fce-102">SYNOPSIS</span></span>
<span data-ttu-id="27fce-103">Usuwa grupę trybu failover usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="27fce-103">Removes an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="27fce-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="27fce-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="27fce-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="27fce-105">DESCRIPTION</span></span>
<span data-ttu-id="27fce-106">To polecenie usuwa grupę trybu failover o określonej nazwie, pozostawiając wszystkie bazy danych i relacje replikacji bez zmian.</span><span class="sxs-lookup"><span data-stu-id="27fce-106">This command removes the Failover Group with the specified name, leaving all databases and replication relationships intact.</span></span> <span data-ttu-id="27fce-107">Punkt końcowy słuchacza nie zostanie wyrejestrowany z systemu DNS.</span><span class="sxs-lookup"><span data-stu-id="27fce-107">The listener endpoint will be unregistered from DNS.</span></span>
<span data-ttu-id="27fce-108">Do wykonania polecenia należy użyć serwera podstawowego grupy trybu failover.</span><span class="sxs-lookup"><span data-stu-id="27fce-108">The Failover Group's primary server should be used to execute the command.</span></span>

## <span data-ttu-id="27fce-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="27fce-109">EXAMPLES</span></span>

### <span data-ttu-id="27fce-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="27fce-110">Example 1</span></span>
```
PS C:\> Remove-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="27fce-111">Usuwanie grupy trybu failover.</span><span class="sxs-lookup"><span data-stu-id="27fce-111">Remove a Failover Group.</span></span>

## <span data-ttu-id="27fce-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27fce-112">PARAMETERS</span></span>

### <span data-ttu-id="27fce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27fce-113">-DefaultProfile</span></span>
<span data-ttu-id="27fce-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="27fce-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27fce-115">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="27fce-115">-FailoverGroupName</span></span>
<span data-ttu-id="27fce-116">Nazwa grupy trybu failover bazy danych Azure SQL Database do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="27fce-116">The name of the Azure SQL Database Failover Group to remove.</span></span>

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

### <span data-ttu-id="27fce-117">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="27fce-117">-Force</span></span>
<span data-ttu-id="27fce-118">Pomiń komunikat potwierdzenia wykonania akcji.</span><span class="sxs-lookup"><span data-stu-id="27fce-118">Skip confirmation message for performing the action.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27fce-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27fce-119">-ResourceGroupName</span></span>
<span data-ttu-id="27fce-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="27fce-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="27fce-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="27fce-121">-ServerName</span></span>
<span data-ttu-id="27fce-122">Nazwa podstawowego serwera usługi Azure SQL Database Server grupy trybu failover.</span><span class="sxs-lookup"><span data-stu-id="27fce-122">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="27fce-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="27fce-123">-Confirm</span></span>
<span data-ttu-id="27fce-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="27fce-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27fce-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27fce-125">-WhatIf</span></span>
<span data-ttu-id="27fce-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27fce-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27fce-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="27fce-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27fce-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27fce-128">CommonParameters</span></span>
<span data-ttu-id="27fce-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27fce-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27fce-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="27fce-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27fce-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="27fce-131">INPUTS</span></span>

### <span data-ttu-id="27fce-132">System.String</span><span class="sxs-lookup"><span data-stu-id="27fce-132">System.String</span></span>

## <span data-ttu-id="27fce-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="27fce-133">OUTPUTS</span></span>

### <span data-ttu-id="27fce-134">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="27fce-134">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="27fce-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="27fce-135">NOTES</span></span>

## <span data-ttu-id="27fce-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="27fce-136">RELATED LINKS</span></span>

[<span data-ttu-id="27fce-137">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="27fce-137">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="27fce-138">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="27fce-138">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="27fce-139">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="27fce-139">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="27fce-140">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="27fce-140">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="27fce-141">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="27fce-141">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="27fce-142">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="27fce-142">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="27fce-143">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="27fce-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
