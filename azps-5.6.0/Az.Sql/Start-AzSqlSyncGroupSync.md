---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/start-azsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlSyncGroupSync.md
ms.openlocfilehash: 13f58f454fb84a4bcd003afd84761197d41c16ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008490"
---
# <span data-ttu-id="e7e6e-101">Start-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="e7e6e-101">Start-AzSqlSyncGroupSync</span></span>

## <span data-ttu-id="e7e6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7e6e-102">SYNOPSIS</span></span>
<span data-ttu-id="e7e6e-103">Rozpoczyna synchronizację grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="e7e6e-103">Starts a sync group synchronization.</span></span>

## <span data-ttu-id="e7e6e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e7e6e-104">SYNTAX</span></span>

```
Start-AzSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e7e6e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e7e6e-105">DESCRIPTION</span></span>
<span data-ttu-id="e7e6e-106">Polecenie **cmdlet Start-AzSqlSyncGroupSync** uruchamia synchronizację grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="e7e6e-106">The **Start-AzSqlSyncGroupSync** cmdlet starts a sync group synchronization.</span></span>

## <span data-ttu-id="e7e6e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e7e6e-107">EXAMPLES</span></span>

### <span data-ttu-id="e7e6e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e7e6e-108">Example 1</span></span>
```
PS C:\> Start-AzSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="e7e6e-109">To polecenie rozpoczyna rundę synchronizacji grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="e7e6e-109">This command starts a round of synchronization for the sync group mysg.</span></span>

## <span data-ttu-id="e7e6e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7e6e-110">PARAMETERS</span></span>

### <span data-ttu-id="e7e6e-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e7e6e-111">-DatabaseName</span></span>
<span data-ttu-id="e7e6e-112">Nazwa usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="e7e6e-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="e7e6e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7e6e-113">-DefaultProfile</span></span>
<span data-ttu-id="e7e6e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="e7e6e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7e6e-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7e6e-115">-PassThru</span></span>
<span data-ttu-id="e7e6e-116">Definiuje, czy grupa synchronizacji ma być zwracana</span><span class="sxs-lookup"><span data-stu-id="e7e6e-116">Defines Whether return the sync group</span></span>

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

### <span data-ttu-id="e7e6e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7e6e-117">-ResourceGroupName</span></span>
<span data-ttu-id="e7e6e-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e7e6e-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="e7e6e-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e7e6e-119">-ServerName</span></span>
<span data-ttu-id="e7e6e-120">Nazwa serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e7e6e-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="e7e6e-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="e7e6e-121">-SyncGroupName</span></span>
<span data-ttu-id="e7e6e-122">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="e7e6e-122">The sync group name.</span></span>

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

### <span data-ttu-id="e7e6e-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e7e6e-123">-Confirm</span></span>
<span data-ttu-id="e7e6e-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e7e6e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7e6e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7e6e-125">-WhatIf</span></span>
<span data-ttu-id="e7e6e-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7e6e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7e6e-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e7e6e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7e6e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7e6e-128">CommonParameters</span></span>
<span data-ttu-id="e7e6e-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7e6e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7e6e-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7e6e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7e6e-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7e6e-131">INPUTS</span></span>

### <span data-ttu-id="e7e6e-132">System.String</span><span class="sxs-lookup"><span data-stu-id="e7e6e-132">System.String</span></span>

## <span data-ttu-id="e7e6e-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7e6e-133">OUTPUTS</span></span>

### <span data-ttu-id="e7e6e-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="e7e6e-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="e7e6e-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e7e6e-135">NOTES</span></span>

## <span data-ttu-id="e7e6e-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e7e6e-136">RELATED LINKS</span></span>

[<span data-ttu-id="e7e6e-137">Stop-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="e7e6e-137">Stop-AzSqlSyncGroupSync</span></span>](./Stop-AzSqlSyncGroupSync.md)

