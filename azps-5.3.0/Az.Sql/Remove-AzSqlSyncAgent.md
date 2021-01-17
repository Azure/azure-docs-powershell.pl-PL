---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
ms.openlocfilehash: ca3ef83fab80e73d687fd11cde418c9ad43f499e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489514"
---
# <span data-ttu-id="a1691-101">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="a1691-101">Remove-AzSqlSyncAgent</span></span>

## <span data-ttu-id="a1691-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a1691-102">SYNOPSIS</span></span>
<span data-ttu-id="a1691-103">Usuwa agenta synchronizacji usługi Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="a1691-103">Removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="a1691-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a1691-104">SYNTAX</span></span>

```
Remove-AzSqlSyncAgent [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a1691-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a1691-105">DESCRIPTION</span></span>
<span data-ttu-id="a1691-106">Polecenie cmdlet **Remove-AzSqlSyncAgent** usuwa agenta synchronizacji Azure SQL Sync.</span><span class="sxs-lookup"><span data-stu-id="a1691-106">The **Remove-AzSqlSyncAgent** cmdlet removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="a1691-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a1691-107">EXAMPLES</span></span>

### <span data-ttu-id="a1691-108">Przykład 1: usuwanie agenta synchronizacji</span><span class="sxs-lookup"><span data-stu-id="a1691-108">Example 1: Remove a sync agent</span></span>
```
PS C:\>Remove-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "syncAgent01"
```

<span data-ttu-id="a1691-109">To polecenie usuwa agenta synchronizacji SQL Azure o nazwie syncAgent01.</span><span class="sxs-lookup"><span data-stu-id="a1691-109">This command removes the Azure SQL Sync Agent named syncAgent01.</span></span>

## <span data-ttu-id="a1691-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a1691-110">PARAMETERS</span></span>

### <span data-ttu-id="a1691-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1691-111">-DefaultProfile</span></span>
<span data-ttu-id="a1691-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a1691-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a1691-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a1691-113">-Force</span></span>
<span data-ttu-id="a1691-114">Pomiń komunikat potwierdzający wykonanie akcji</span><span class="sxs-lookup"><span data-stu-id="a1691-114">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="a1691-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a1691-115">-Name</span></span>
<span data-ttu-id="a1691-116">Nazwa agenta synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="a1691-116">The sync agent name.</span></span>

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

### <span data-ttu-id="a1691-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a1691-117">-PassThru</span></span>
<span data-ttu-id="a1691-118">Określa, czy zwrócić usuniętego agenta synchronizacji</span><span class="sxs-lookup"><span data-stu-id="a1691-118">Defines Whether return the removed sync agent</span></span>

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

### <span data-ttu-id="a1691-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1691-119">-ResourceGroupName</span></span>
<span data-ttu-id="a1691-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a1691-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="a1691-121">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="a1691-121">-ServerName</span></span>
<span data-ttu-id="a1691-122">Nazwa programu Azure SQL Server, w którym znajduje się Agent synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="a1691-122">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="a1691-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a1691-123">-Confirm</span></span>
<span data-ttu-id="a1691-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1691-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1691-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1691-125">-WhatIf</span></span>
<span data-ttu-id="a1691-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1691-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1691-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a1691-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1691-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1691-128">CommonParameters</span></span>
<span data-ttu-id="a1691-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1691-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1691-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1691-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1691-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1691-131">INPUTS</span></span>

### <span data-ttu-id="a1691-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a1691-132">System.String</span></span>

## <span data-ttu-id="a1691-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a1691-133">OUTPUTS</span></span>

### <span data-ttu-id="a1691-134">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="a1691-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="a1691-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a1691-135">NOTES</span></span>

## <span data-ttu-id="a1691-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a1691-136">RELATED LINKS</span></span>

[<span data-ttu-id="a1691-137">Nowe — AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="a1691-137">New-AzSqlSyncAgent</span></span>](./New-AzSqlSyncAgent.md)

[<span data-ttu-id="a1691-138">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="a1691-138">Get-AzSqlSyncAgent</span></span>](./Get-AzSqlSyncAgent.md)

