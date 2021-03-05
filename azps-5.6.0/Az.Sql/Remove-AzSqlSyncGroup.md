---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
ms.openlocfilehash: ce69f6b087a7ed61f415e3d6a649f757bb10178f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995093"
---
# <span data-ttu-id="d0a5d-101">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="d0a5d-101">Remove-AzSqlSyncGroup</span></span>

## <span data-ttu-id="d0a5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0a5d-102">SYNOPSIS</span></span>
<span data-ttu-id="d0a5d-103">Usuwa grupę synchronizacji usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="d0a5d-103">Removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="d0a5d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d0a5d-104">SYNTAX</span></span>

```
Remove-AzSqlSyncGroup [-Name] <String> [-Force] [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d0a5d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d0a5d-105">DESCRIPTION</span></span>
<span data-ttu-id="d0a5d-106">Polecenie **cmdlet Remove-AzSqlSyncGroup** usuwa grupę synchronizacji usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="d0a5d-106">The **Remove-AzSqlSyncGroup** cmdlet removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="d0a5d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d0a5d-107">EXAMPLES</span></span>

### <span data-ttu-id="d0a5d-108">Przykład 1. Usuwanie grupy synchronizacji</span><span class="sxs-lookup"><span data-stu-id="d0a5d-108">Example 1: Remove a sync group</span></span>
```
PS C:\>Remove-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -Name "syncGroup01"
```

<span data-ttu-id="d0a5d-109">To polecenie usuwa grupę synchronizacji bazy danych Azure SQL o nazwie syncGroup01.</span><span class="sxs-lookup"><span data-stu-id="d0a5d-109">This command removes the Azure SQL Database Sync Group named syncGroup01.</span></span>

## <span data-ttu-id="d0a5d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0a5d-110">PARAMETERS</span></span>

### <span data-ttu-id="d0a5d-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d0a5d-111">-DatabaseName</span></span>
<span data-ttu-id="d0a5d-112">Nazwa usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="d0a5d-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="d0a5d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0a5d-113">-DefaultProfile</span></span>
<span data-ttu-id="d0a5d-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="d0a5d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d0a5d-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="d0a5d-115">-Force</span></span>
<span data-ttu-id="d0a5d-116">Pomiń komunikat potwierdzenia wykonania akcji</span><span class="sxs-lookup"><span data-stu-id="d0a5d-116">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0a5d-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d0a5d-117">-Name</span></span>
<span data-ttu-id="d0a5d-118">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="d0a5d-118">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0a5d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d0a5d-119">-PassThru</span></span>
<span data-ttu-id="d0a5d-120">Definiuje, czy przywrócić usuniętą grupę synchronizacji</span><span class="sxs-lookup"><span data-stu-id="d0a5d-120">Defines Whether return the removed sync group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0a5d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0a5d-121">-ResourceGroupName</span></span>
<span data-ttu-id="d0a5d-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d0a5d-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="d0a5d-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d0a5d-123">-ServerName</span></span>
<span data-ttu-id="d0a5d-124">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d0a5d-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="d0a5d-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d0a5d-125">-Confirm</span></span>
<span data-ttu-id="d0a5d-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d0a5d-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0a5d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0a5d-127">-WhatIf</span></span>
<span data-ttu-id="d0a5d-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0a5d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0a5d-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d0a5d-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0a5d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0a5d-130">CommonParameters</span></span>
<span data-ttu-id="d0a5d-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0a5d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0a5d-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d0a5d-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0a5d-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0a5d-133">INPUTS</span></span>

### <span data-ttu-id="d0a5d-134">System.String</span><span class="sxs-lookup"><span data-stu-id="d0a5d-134">System.String</span></span>

## <span data-ttu-id="d0a5d-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0a5d-135">OUTPUTS</span></span>

### <span data-ttu-id="d0a5d-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="d0a5d-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="d0a5d-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d0a5d-137">NOTES</span></span>

## <span data-ttu-id="d0a5d-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d0a5d-138">RELATED LINKS</span></span>

[<span data-ttu-id="d0a5d-139">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="d0a5d-139">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="d0a5d-140">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="d0a5d-140">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="d0a5d-141">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="d0a5d-141">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

