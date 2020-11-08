---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
ms.openlocfilehash: ca3ef83fab80e73d687fd11cde418c9ad43f499e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052132"
---
# <span data-ttu-id="1ba4e-101">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="1ba4e-101">Remove-AzSqlSyncAgent</span></span>

## <span data-ttu-id="1ba4e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1ba4e-102">SYNOPSIS</span></span>
<span data-ttu-id="1ba4e-103">Usuwa agenta synchronizacji usługi Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="1ba4e-103">Removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="1ba4e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1ba4e-104">SYNTAX</span></span>

```
Remove-AzSqlSyncAgent [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1ba4e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1ba4e-105">DESCRIPTION</span></span>
<span data-ttu-id="1ba4e-106">Polecenie cmdlet **Remove-AzSqlSyncAgent** usuwa agenta synchronizacji Azure SQL Sync.</span><span class="sxs-lookup"><span data-stu-id="1ba4e-106">The **Remove-AzSqlSyncAgent** cmdlet removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="1ba4e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1ba4e-107">EXAMPLES</span></span>

### <span data-ttu-id="1ba4e-108">Przykład 1: usuwanie agenta synchronizacji</span><span class="sxs-lookup"><span data-stu-id="1ba4e-108">Example 1: Remove a sync agent</span></span>
```
PS C:\>Remove-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "syncAgent01"
```

<span data-ttu-id="1ba4e-109">To polecenie usuwa agenta synchronizacji SQL Azure o nazwie syncAgent01.</span><span class="sxs-lookup"><span data-stu-id="1ba4e-109">This command removes the Azure SQL Sync Agent named syncAgent01.</span></span>

## <span data-ttu-id="1ba4e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1ba4e-110">PARAMETERS</span></span>

### <span data-ttu-id="1ba4e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ba4e-111">-DefaultProfile</span></span>
<span data-ttu-id="1ba4e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1ba4e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1ba4e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="1ba4e-113">-Force</span></span>
<span data-ttu-id="1ba4e-114">Pomiń komunikat potwierdzający wykonanie akcji</span><span class="sxs-lookup"><span data-stu-id="1ba4e-114">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="1ba4e-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1ba4e-115">-Name</span></span>
<span data-ttu-id="1ba4e-116">Nazwa agenta synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="1ba4e-116">The sync agent name.</span></span>

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

### <span data-ttu-id="1ba4e-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1ba4e-117">-PassThru</span></span>
<span data-ttu-id="1ba4e-118">Określa, czy zwrócić usuniętego agenta synchronizacji</span><span class="sxs-lookup"><span data-stu-id="1ba4e-118">Defines Whether return the removed sync agent</span></span>

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

### <span data-ttu-id="1ba4e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ba4e-119">-ResourceGroupName</span></span>
<span data-ttu-id="1ba4e-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1ba4e-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="1ba4e-121">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="1ba4e-121">-ServerName</span></span>
<span data-ttu-id="1ba4e-122">Nazwa programu Azure SQL Server, w którym znajduje się Agent synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="1ba4e-122">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="1ba4e-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1ba4e-123">-Confirm</span></span>
<span data-ttu-id="1ba4e-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ba4e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ba4e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ba4e-125">-WhatIf</span></span>
<span data-ttu-id="1ba4e-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ba4e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ba4e-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1ba4e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ba4e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ba4e-128">CommonParameters</span></span>
<span data-ttu-id="1ba4e-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ba4e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ba4e-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ba4e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ba4e-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1ba4e-131">INPUTS</span></span>

### <span data-ttu-id="1ba4e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1ba4e-132">System.String</span></span>

## <span data-ttu-id="1ba4e-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1ba4e-133">OUTPUTS</span></span>

### <span data-ttu-id="1ba4e-134">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="1ba4e-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="1ba4e-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1ba4e-135">NOTES</span></span>

## <span data-ttu-id="1ba4e-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1ba4e-136">RELATED LINKS</span></span>

[<span data-ttu-id="1ba4e-137">Nowe — AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="1ba4e-137">New-AzSqlSyncAgent</span></span>](./New-AzSqlSyncAgent.md)

[<span data-ttu-id="1ba4e-138">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="1ba4e-138">Get-AzSqlSyncAgent</span></span>](./Get-AzSqlSyncAgent.md)

