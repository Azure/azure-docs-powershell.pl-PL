---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlSyncGroupSync.md
ms.openlocfilehash: d09f0032d44a0558c1052f1dcfc3a3c94a7dff00
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183275"
---
# <span data-ttu-id="53f66-101">Stop-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="53f66-101">Stop-AzSqlSyncGroupSync</span></span>

## <span data-ttu-id="53f66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53f66-102">SYNOPSIS</span></span>
<span data-ttu-id="53f66-103">Zatrzymuje synchronizację grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="53f66-103">Stops a sync group synchronization.</span></span>

## <span data-ttu-id="53f66-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="53f66-104">SYNTAX</span></span>

```
Stop-AzSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="53f66-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="53f66-105">DESCRIPTION</span></span>
<span data-ttu-id="53f66-106">Polecenie **cmdlet Stop-AzSqlSyncGroupSync** zatrzymuje synchronizację grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="53f66-106">The **Stop-AzSqlSyncGroupSync** cmdlet stops a sync group synchronization.</span></span>

## <span data-ttu-id="53f66-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="53f66-107">EXAMPLES</span></span>

### <span data-ttu-id="53f66-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="53f66-108">Example 1</span></span>
```
PS C:\> Stop-AzSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="53f66-109">To polecenie zatrzymuje synchronizację, która jest w toku dla mojej grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="53f66-109">This command stops the synchronization which is ongoing for the sync group mysg.</span></span>

## <span data-ttu-id="53f66-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53f66-110">PARAMETERS</span></span>

### <span data-ttu-id="53f66-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="53f66-111">-DatabaseName</span></span>
<span data-ttu-id="53f66-112">Nazwa usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="53f66-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="53f66-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53f66-113">-DefaultProfile</span></span>
<span data-ttu-id="53f66-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="53f66-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="53f66-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="53f66-115">-PassThru</span></span>
<span data-ttu-id="53f66-116">Definiuje, czy grupa synchronizacji ma być zwracana</span><span class="sxs-lookup"><span data-stu-id="53f66-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="53f66-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53f66-117">-ResourceGroupName</span></span>
<span data-ttu-id="53f66-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="53f66-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="53f66-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="53f66-119">-ServerName</span></span>
<span data-ttu-id="53f66-120">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="53f66-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="53f66-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="53f66-121">-SyncGroupName</span></span>
<span data-ttu-id="53f66-122">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="53f66-122">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53f66-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="53f66-123">-Confirm</span></span>
<span data-ttu-id="53f66-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="53f66-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53f66-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53f66-125">-WhatIf</span></span>
<span data-ttu-id="53f66-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53f66-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53f66-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="53f66-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53f66-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53f66-128">CommonParameters</span></span>
<span data-ttu-id="53f66-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53f66-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53f66-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53f66-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53f66-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="53f66-131">INPUTS</span></span>

### <span data-ttu-id="53f66-132">System.String</span><span class="sxs-lookup"><span data-stu-id="53f66-132">System.String</span></span>

## <span data-ttu-id="53f66-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="53f66-133">OUTPUTS</span></span>

### <span data-ttu-id="53f66-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="53f66-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="53f66-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="53f66-135">NOTES</span></span>

## <span data-ttu-id="53f66-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="53f66-136">RELATED LINKS</span></span>

[<span data-ttu-id="53f66-137">Start-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="53f66-137">Start-AzSqlSyncGroupSync</span></span>](./Start-AzSqlSyncGroupSync.md)

