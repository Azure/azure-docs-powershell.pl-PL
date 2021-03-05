---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/stop-azsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlSyncGroupSync.md
ms.openlocfilehash: ea8390de90fff5fb1e228884b131551a5be86e48
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992363"
---
# <span data-ttu-id="a00d9-101">Stop-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="a00d9-101">Stop-AzSqlSyncGroupSync</span></span>

## <span data-ttu-id="a00d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a00d9-102">SYNOPSIS</span></span>
<span data-ttu-id="a00d9-103">Zatrzymuje synchronizację grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="a00d9-103">Stops a sync group synchronization.</span></span>

## <span data-ttu-id="a00d9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a00d9-104">SYNTAX</span></span>

```
Stop-AzSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a00d9-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a00d9-105">DESCRIPTION</span></span>
<span data-ttu-id="a00d9-106">Polecenie **cmdlet Stop-AzSqlSyncGroupSync** zatrzymuje synchronizację grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="a00d9-106">The **Stop-AzSqlSyncGroupSync** cmdlet stops a sync group synchronization.</span></span>

## <span data-ttu-id="a00d9-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a00d9-107">EXAMPLES</span></span>

### <span data-ttu-id="a00d9-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a00d9-108">Example 1</span></span>
```
PS C:\> Stop-AzSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="a00d9-109">To polecenie zatrzymuje synchronizację, która jest w toku dla mojej grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="a00d9-109">This command stops the synchronization which is ongoing for the sync group mysg.</span></span>

## <span data-ttu-id="a00d9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a00d9-110">PARAMETERS</span></span>

### <span data-ttu-id="a00d9-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a00d9-111">-DatabaseName</span></span>
<span data-ttu-id="a00d9-112">Nazwa usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="a00d9-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="a00d9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a00d9-113">-DefaultProfile</span></span>
<span data-ttu-id="a00d9-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="a00d9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a00d9-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a00d9-115">-PassThru</span></span>
<span data-ttu-id="a00d9-116">Definiuje, czy grupa synchronizacji ma być zwracana</span><span class="sxs-lookup"><span data-stu-id="a00d9-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="a00d9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a00d9-117">-ResourceGroupName</span></span>
<span data-ttu-id="a00d9-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a00d9-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="a00d9-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a00d9-119">-ServerName</span></span>
<span data-ttu-id="a00d9-120">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a00d9-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="a00d9-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="a00d9-121">-SyncGroupName</span></span>
<span data-ttu-id="a00d9-122">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="a00d9-122">The sync group name.</span></span>

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

### <span data-ttu-id="a00d9-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a00d9-123">-Confirm</span></span>
<span data-ttu-id="a00d9-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a00d9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a00d9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a00d9-125">-WhatIf</span></span>
<span data-ttu-id="a00d9-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a00d9-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a00d9-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a00d9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a00d9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a00d9-128">CommonParameters</span></span>
<span data-ttu-id="a00d9-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a00d9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a00d9-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a00d9-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a00d9-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a00d9-131">INPUTS</span></span>

### <span data-ttu-id="a00d9-132">System.String</span><span class="sxs-lookup"><span data-stu-id="a00d9-132">System.String</span></span>

## <span data-ttu-id="a00d9-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a00d9-133">OUTPUTS</span></span>

### <span data-ttu-id="a00d9-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="a00d9-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="a00d9-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a00d9-135">NOTES</span></span>

## <span data-ttu-id="a00d9-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a00d9-136">RELATED LINKS</span></span>

[<span data-ttu-id="a00d9-137">Start-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="a00d9-137">Start-AzSqlSyncGroupSync</span></span>](./Start-AzSqlSyncGroupSync.md)

