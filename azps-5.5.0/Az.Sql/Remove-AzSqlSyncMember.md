---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncMember.md
ms.openlocfilehash: c508dc9352bfcf70a9d3bad088f2b75de98db43d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195994"
---
# <span data-ttu-id="4cd4f-101">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="4cd4f-101">Remove-AzSqlSyncMember</span></span>

## <span data-ttu-id="4cd4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cd4f-102">SYNOPSIS</span></span>
<span data-ttu-id="4cd4f-103">Usuwa członka synchronizacji usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="4cd4f-103">Removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="4cd4f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4cd4f-104">SYNTAX</span></span>

```
Remove-AzSqlSyncMember -Name <String> [-Force] [-PassThru] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cd4f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4cd4f-105">DESCRIPTION</span></span>
<span data-ttu-id="4cd4f-106">Polecenie **cmdlet Remove-AzSqlSyncMember** usuwa członka synchronizacji usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="4cd4f-106">The **Remove-AzSqlSyncMember** cmdlet removes an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="4cd4f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4cd4f-107">EXAMPLES</span></span>

### <span data-ttu-id="4cd4f-108">Przykład 1. Usuwanie członka synchronizacji</span><span class="sxs-lookup"><span data-stu-id="4cd4f-108">Example 1: Remove a sync member</span></span>
```
PS C:\>Remove-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -Name "syncMember01"
```

<span data-ttu-id="4cd4f-109">To polecenie usuwa członka synchronizacji usługi Azure SQL Database o nazwie syncMember01.</span><span class="sxs-lookup"><span data-stu-id="4cd4f-109">This command removes the Azure SQL Database Sync Member named syncMember01.</span></span>

## <span data-ttu-id="4cd4f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4cd4f-110">PARAMETERS</span></span>

### <span data-ttu-id="4cd4f-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4cd4f-111">-DatabaseName</span></span>
<span data-ttu-id="4cd4f-112">Nazwa usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="4cd4f-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="4cd4f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cd4f-113">-DefaultProfile</span></span>
<span data-ttu-id="4cd4f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="4cd4f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4cd4f-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="4cd4f-115">-Force</span></span>
<span data-ttu-id="4cd4f-116">Pomiń komunikat z potwierdzeniem wykonania akcji</span><span class="sxs-lookup"><span data-stu-id="4cd4f-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="4cd4f-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4cd4f-117">-Name</span></span>
<span data-ttu-id="4cd4f-118">Nazwa członka synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="4cd4f-118">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cd4f-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4cd4f-119">-PassThru</span></span>
<span data-ttu-id="4cd4f-120">Definiuje, czy zwrócić usuniętego członka synchronizacji</span><span class="sxs-lookup"><span data-stu-id="4cd4f-120">Defines Whether return the removed sync member</span></span>

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

### <span data-ttu-id="4cd4f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cd4f-121">-ResourceGroupName</span></span>
<span data-ttu-id="4cd4f-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4cd4f-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="4cd4f-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4cd4f-123">-ServerName</span></span>
<span data-ttu-id="4cd4f-124">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4cd4f-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="4cd4f-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="4cd4f-125">-SyncGroupName</span></span>
<span data-ttu-id="4cd4f-126">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="4cd4f-126">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cd4f-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4cd4f-127">-Confirm</span></span>
<span data-ttu-id="4cd4f-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4cd4f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cd4f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cd4f-129">-WhatIf</span></span>
<span data-ttu-id="4cd4f-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cd4f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cd4f-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4cd4f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cd4f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cd4f-132">CommonParameters</span></span>
<span data-ttu-id="4cd4f-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cd4f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cd4f-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4cd4f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cd4f-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4cd4f-135">INPUTS</span></span>

### <span data-ttu-id="4cd4f-136">System.String</span><span class="sxs-lookup"><span data-stu-id="4cd4f-136">System.String</span></span>

## <span data-ttu-id="4cd4f-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4cd4f-137">OUTPUTS</span></span>

### <span data-ttu-id="4cd4f-138">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="4cd4f-138">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="4cd4f-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4cd4f-139">NOTES</span></span>

## <span data-ttu-id="4cd4f-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4cd4f-140">RELATED LINKS</span></span>

[<span data-ttu-id="4cd4f-141">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="4cd4f-141">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="4cd4f-142">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="4cd4f-142">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="4cd4f-143">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="4cd4f-143">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

