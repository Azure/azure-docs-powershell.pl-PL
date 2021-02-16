---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
ms.openlocfilehash: ca3ef83fab80e73d687fd11cde418c9ad43f499e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178362"
---
# <span data-ttu-id="a9fe8-101">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="a9fe8-101">Remove-AzSqlSyncAgent</span></span>

## <span data-ttu-id="a9fe8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9fe8-102">SYNOPSIS</span></span>
<span data-ttu-id="a9fe8-103">Usuwa agenta azure SQL Sync Agent.</span><span class="sxs-lookup"><span data-stu-id="a9fe8-103">Removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="a9fe8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a9fe8-104">SYNTAX</span></span>

```
Remove-AzSqlSyncAgent [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a9fe8-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a9fe8-105">DESCRIPTION</span></span>
<span data-ttu-id="a9fe8-106">Polecenie **cmdlet Remove-AzSqlSyncAgent** usuwa agenta azure SQL Sync Agent.</span><span class="sxs-lookup"><span data-stu-id="a9fe8-106">The **Remove-AzSqlSyncAgent** cmdlet removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="a9fe8-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a9fe8-107">EXAMPLES</span></span>

### <span data-ttu-id="a9fe8-108">Przykład 1. Usuwanie agenta synchronizacji</span><span class="sxs-lookup"><span data-stu-id="a9fe8-108">Example 1: Remove a sync agent</span></span>
```
PS C:\>Remove-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "syncAgent01"
```

<span data-ttu-id="a9fe8-109">To polecenie usuwa agenta synchronizacji języka Azure SQL o nazwie syncAgent01.</span><span class="sxs-lookup"><span data-stu-id="a9fe8-109">This command removes the Azure SQL Sync Agent named syncAgent01.</span></span>

## <span data-ttu-id="a9fe8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9fe8-110">PARAMETERS</span></span>

### <span data-ttu-id="a9fe8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9fe8-111">-DefaultProfile</span></span>
<span data-ttu-id="a9fe8-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="a9fe8-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9fe8-113">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="a9fe8-113">-Force</span></span>
<span data-ttu-id="a9fe8-114">Pomiń komunikat z potwierdzeniem wykonania akcji</span><span class="sxs-lookup"><span data-stu-id="a9fe8-114">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="a9fe8-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a9fe8-115">-Name</span></span>
<span data-ttu-id="a9fe8-116">Nazwa agenta synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="a9fe8-116">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9fe8-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a9fe8-117">-PassThru</span></span>
<span data-ttu-id="a9fe8-118">Definiuje, czy zwrócić usuniętego agenta synchronizacji</span><span class="sxs-lookup"><span data-stu-id="a9fe8-118">Defines Whether return the removed sync agent</span></span>

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

### <span data-ttu-id="a9fe8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9fe8-119">-ResourceGroupName</span></span>
<span data-ttu-id="a9fe8-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a9fe8-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="a9fe8-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a9fe8-121">-ServerName</span></span>
<span data-ttu-id="a9fe8-122">Nazwa serwera Azure SQL Server, w którym znajduje się agent synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="a9fe8-122">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="a9fe8-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a9fe8-123">-Confirm</span></span>
<span data-ttu-id="a9fe8-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a9fe8-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9fe8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9fe8-125">-WhatIf</span></span>
<span data-ttu-id="a9fe8-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9fe8-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9fe8-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a9fe8-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9fe8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9fe8-128">CommonParameters</span></span>
<span data-ttu-id="a9fe8-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9fe8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9fe8-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9fe8-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9fe8-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9fe8-131">INPUTS</span></span>

### <span data-ttu-id="a9fe8-132">System.String</span><span class="sxs-lookup"><span data-stu-id="a9fe8-132">System.String</span></span>

## <span data-ttu-id="a9fe8-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9fe8-133">OUTPUTS</span></span>

### <span data-ttu-id="a9fe8-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="a9fe8-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="a9fe8-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a9fe8-135">NOTES</span></span>

## <span data-ttu-id="a9fe8-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9fe8-136">RELATED LINKS</span></span>

[<span data-ttu-id="a9fe8-137">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="a9fe8-137">New-AzSqlSyncAgent</span></span>](./New-AzSqlSyncAgent.md)

[<span data-ttu-id="a9fe8-138">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="a9fe8-138">Get-AzSqlSyncAgent</span></span>](./Get-AzSqlSyncAgent.md)

