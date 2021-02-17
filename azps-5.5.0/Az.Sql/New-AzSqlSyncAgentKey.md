---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncagentkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgentKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgentKey.md
ms.openlocfilehash: e6ccf84d2de6c64000a6663de5a5b696d9033eae
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243267"
---
# <span data-ttu-id="84131-101">New-AzSqlSyncAgentKey</span><span class="sxs-lookup"><span data-stu-id="84131-101">New-AzSqlSyncAgentKey</span></span>

## <span data-ttu-id="84131-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84131-102">SYNOPSIS</span></span>
<span data-ttu-id="84131-103">Tworzy klucz agenta synchronizacji sql platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="84131-103">Creates an Azure SQL Sync Agent Key.</span></span>

## <span data-ttu-id="84131-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="84131-104">SYNTAX</span></span>

```
New-AzSqlSyncAgentKey [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84131-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="84131-105">DESCRIPTION</span></span>
<span data-ttu-id="84131-106">Polecenie **cmdlet New-AzSqlSyncAgentKey** tworzy klucz agenta azure SQL Sync Agent.</span><span class="sxs-lookup"><span data-stu-id="84131-106">The **New-AzSqlSyncAgentKey** cmdlet creates an Azure SQL Sync Agent key.</span></span>

## <span data-ttu-id="84131-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="84131-107">EXAMPLES</span></span>

### <span data-ttu-id="84131-108">Przykład 1. Tworzenie klucza agenta synchronizacji dla agenta synchronizacji azure SQL.</span><span class="sxs-lookup"><span data-stu-id="84131-108">Example 1: Create a sync agent key for an Azure SQL sync agent.</span></span>
```
PS C:\> New-AzSqlSyncAgentKey -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01"
SyncAgentKey                  : Key
```

<span data-ttu-id="84131-109">To polecenie tworzy klucz agenta synchronizacji dla agenta azure SQL Sync Agent.</span><span class="sxs-lookup"><span data-stu-id="84131-109">This command creates a sync agent key for an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="84131-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84131-110">PARAMETERS</span></span>

### <span data-ttu-id="84131-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84131-111">-DefaultProfile</span></span>
<span data-ttu-id="84131-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="84131-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="84131-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84131-113">-ResourceGroupName</span></span>
<span data-ttu-id="84131-114">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="84131-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="84131-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="84131-115">-ServerName</span></span>
<span data-ttu-id="84131-116">Nazwa serwera Azure SQL Server, w którym znajduje się agent synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="84131-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="84131-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="84131-117">-SyncAgentName</span></span>
<span data-ttu-id="84131-118">Nazwa agenta synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="84131-118">The sync agent name.</span></span>

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

### <span data-ttu-id="84131-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="84131-119">-Confirm</span></span>
<span data-ttu-id="84131-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="84131-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84131-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84131-121">-WhatIf</span></span>
<span data-ttu-id="84131-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84131-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84131-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="84131-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84131-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84131-124">CommonParameters</span></span>
<span data-ttu-id="84131-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84131-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84131-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="84131-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84131-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84131-127">INPUTS</span></span>

### <span data-ttu-id="84131-128">System.String</span><span class="sxs-lookup"><span data-stu-id="84131-128">System.String</span></span>

## <span data-ttu-id="84131-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84131-129">OUTPUTS</span></span>

### <span data-ttu-id="84131-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span><span class="sxs-lookup"><span data-stu-id="84131-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span></span>

## <span data-ttu-id="84131-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="84131-131">NOTES</span></span>

## <span data-ttu-id="84131-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="84131-132">RELATED LINKS</span></span>
