---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlsyncagentkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgentKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgentKey.md
ms.openlocfilehash: 35942c51aa383dbc7dcbe071083eee575228372a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957994"
---
# <span data-ttu-id="672bb-101">New-AzSqlSyncAgentKey</span><span class="sxs-lookup"><span data-stu-id="672bb-101">New-AzSqlSyncAgentKey</span></span>

## <span data-ttu-id="672bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="672bb-102">SYNOPSIS</span></span>
<span data-ttu-id="672bb-103">Tworzy klucz agenta synchronizacji sql platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="672bb-103">Creates an Azure SQL Sync Agent Key.</span></span>

## <span data-ttu-id="672bb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="672bb-104">SYNTAX</span></span>

```
New-AzSqlSyncAgentKey [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="672bb-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="672bb-105">DESCRIPTION</span></span>
<span data-ttu-id="672bb-106">Polecenie **cmdlet New-AzSqlSyncAgentKey** tworzy klucz programu Azure SQL Sync Agent.</span><span class="sxs-lookup"><span data-stu-id="672bb-106">The **New-AzSqlSyncAgentKey** cmdlet creates an Azure SQL Sync Agent key.</span></span>

## <span data-ttu-id="672bb-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="672bb-107">EXAMPLES</span></span>

### <span data-ttu-id="672bb-108">Przykład 1. Tworzenie klucza agenta synchronizacji dla agenta synchronizacji azure SQL.</span><span class="sxs-lookup"><span data-stu-id="672bb-108">Example 1: Create a sync agent key for an Azure SQL sync agent.</span></span>
```
PS C:\> New-AzSqlSyncAgentKey -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01"
SyncAgentKey                  : Key
```

<span data-ttu-id="672bb-109">To polecenie tworzy klucz agenta synchronizacji dla agenta azure SQL Sync Agent.</span><span class="sxs-lookup"><span data-stu-id="672bb-109">This command creates a sync agent key for an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="672bb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="672bb-110">PARAMETERS</span></span>

### <span data-ttu-id="672bb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="672bb-111">-DefaultProfile</span></span>
<span data-ttu-id="672bb-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="672bb-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="672bb-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="672bb-113">-ResourceGroupName</span></span>
<span data-ttu-id="672bb-114">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="672bb-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="672bb-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="672bb-115">-ServerName</span></span>
<span data-ttu-id="672bb-116">Nazwa serwera Azure SQL Server, w którym znajduje się agent synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="672bb-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="672bb-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="672bb-117">-SyncAgentName</span></span>
<span data-ttu-id="672bb-118">Nazwa agenta synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="672bb-118">The sync agent name.</span></span>

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

### <span data-ttu-id="672bb-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="672bb-119">-Confirm</span></span>
<span data-ttu-id="672bb-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="672bb-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="672bb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="672bb-121">-WhatIf</span></span>
<span data-ttu-id="672bb-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="672bb-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="672bb-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="672bb-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="672bb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="672bb-124">CommonParameters</span></span>
<span data-ttu-id="672bb-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="672bb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="672bb-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="672bb-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="672bb-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="672bb-127">INPUTS</span></span>

### <span data-ttu-id="672bb-128">System.String</span><span class="sxs-lookup"><span data-stu-id="672bb-128">System.String</span></span>

## <span data-ttu-id="672bb-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="672bb-129">OUTPUTS</span></span>

### <span data-ttu-id="672bb-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span><span class="sxs-lookup"><span data-stu-id="672bb-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span></span>

## <span data-ttu-id="672bb-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="672bb-131">NOTES</span></span>

## <span data-ttu-id="672bb-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="672bb-132">RELATED LINKS</span></span>
