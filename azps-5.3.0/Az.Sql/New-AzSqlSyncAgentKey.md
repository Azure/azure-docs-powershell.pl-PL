---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncagentkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgentKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgentKey.md
ms.openlocfilehash: e6ccf84d2de6c64000a6663de5a5b696d9033eae
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498309"
---
# <span data-ttu-id="0417c-101">New-AzSqlSyncAgentKey</span><span class="sxs-lookup"><span data-stu-id="0417c-101">New-AzSqlSyncAgentKey</span></span>

## <span data-ttu-id="0417c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0417c-102">SYNOPSIS</span></span>
<span data-ttu-id="0417c-103">Tworzy klucz agenta synchronizacji platformy Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="0417c-103">Creates an Azure SQL Sync Agent Key.</span></span>

## <span data-ttu-id="0417c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0417c-104">SYNTAX</span></span>

```
New-AzSqlSyncAgentKey [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0417c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0417c-105">DESCRIPTION</span></span>
<span data-ttu-id="0417c-106">Polecenie cmdlet **New-AzSqlSyncAgentKey** służy do tworzenia klucza agenta synchronizacji platformy Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="0417c-106">The **New-AzSqlSyncAgentKey** cmdlet creates an Azure SQL Sync Agent key.</span></span>

## <span data-ttu-id="0417c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0417c-107">EXAMPLES</span></span>

### <span data-ttu-id="0417c-108">Przykład 1. Utwórz klucz agenta synchronizacji dla agenta synchronizacji Azure SQL Sync.</span><span class="sxs-lookup"><span data-stu-id="0417c-108">Example 1: Create a sync agent key for an Azure SQL sync agent.</span></span>
```
PS C:\> New-AzSqlSyncAgentKey -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01"
SyncAgentKey                  : Key
```

<span data-ttu-id="0417c-109">To polecenie tworzy klucz agenta synchronizacji dla agenta synchronizacji Azure SQL Sync.</span><span class="sxs-lookup"><span data-stu-id="0417c-109">This command creates a sync agent key for an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="0417c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0417c-110">PARAMETERS</span></span>

### <span data-ttu-id="0417c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0417c-111">-DefaultProfile</span></span>
<span data-ttu-id="0417c-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="0417c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0417c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0417c-113">-ResourceGroupName</span></span>
<span data-ttu-id="0417c-114">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0417c-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="0417c-115">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="0417c-115">-ServerName</span></span>
<span data-ttu-id="0417c-116">Nazwa programu Azure SQL Server, w którym znajduje się Agent synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="0417c-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="0417c-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="0417c-117">-SyncAgentName</span></span>
<span data-ttu-id="0417c-118">Nazwa agenta synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="0417c-118">The sync agent name.</span></span>

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

### <span data-ttu-id="0417c-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0417c-119">-Confirm</span></span>
<span data-ttu-id="0417c-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0417c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0417c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0417c-121">-WhatIf</span></span>
<span data-ttu-id="0417c-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0417c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0417c-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0417c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0417c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0417c-124">CommonParameters</span></span>
<span data-ttu-id="0417c-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0417c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0417c-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0417c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0417c-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0417c-127">INPUTS</span></span>

### <span data-ttu-id="0417c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="0417c-128">System.String</span></span>

## <span data-ttu-id="0417c-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0417c-129">OUTPUTS</span></span>

### <span data-ttu-id="0417c-130">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncAgentKeyModel</span><span class="sxs-lookup"><span data-stu-id="0417c-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span></span>

## <span data-ttu-id="0417c-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0417c-131">NOTES</span></span>

## <span data-ttu-id="0417c-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0417c-132">RELATED LINKS</span></span>
