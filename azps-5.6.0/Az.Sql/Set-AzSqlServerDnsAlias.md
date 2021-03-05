---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDnsAlias.md
ms.openlocfilehash: bbc941c260579fb7fdb437f0b30002999635b8eb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970177"
---
# <span data-ttu-id="33ade-101">Set-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="33ade-101">Set-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="33ade-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33ade-102">SYNOPSIS</span></span>
<span data-ttu-id="33ade-103">Modyfikuje serwer, na który jest wskazują alias DNS programu Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="33ade-103">Modifies the server to which Azure SQL Server DNS Alias is pointing</span></span>

## <span data-ttu-id="33ade-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="33ade-104">SYNTAX</span></span>

```
Set-AzSqlServerDnsAlias -Name <String> -TargetServerName <String> [-ResourceGroupName] <String>
 -SourceServerName <String> -SourceServerResourceGroupName <String> -SourceServerSubscriptionId <Guid> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33ade-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="33ade-105">DESCRIPTION</span></span>
<span data-ttu-id="33ade-106">To polecenie aktualizuje serwer, na który jest wskazują alias.</span><span class="sxs-lookup"><span data-stu-id="33ade-106">This command is updating the server to which alias is pointing.</span></span> <span data-ttu-id="33ade-107">To polecenie musi zostać wydane po zalogowaniu się do subskrypcji, na którym znajduje się nowy serwer, do którego ma zostać wskażony alias.</span><span class="sxs-lookup"><span data-stu-id="33ade-107">This command needs to be issued while logged into subscription where new server to which alias is going to point is located.</span></span>

## <span data-ttu-id="33ade-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="33ade-108">EXAMPLES</span></span>

### <span data-ttu-id="33ade-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="33ade-109">Example 1</span></span>
```
PS C:\> Set-AzSqlServerDnsAlias -ResourceGroupName rg -DnsAliasName aliasName -TargetServerName newServer -SourceServerName oldServer -SourceServerResourceGroupName SourceServerRG -SourceServerSubscriptionId 0000-0000-0000-0000
```

<span data-ttu-id="33ade-110">To polecenie aktualizuje alias, który wcześniej wskaże stary serwer w celu wskazania nowego serwera serwera</span><span class="sxs-lookup"><span data-stu-id="33ade-110">This command is updating alias which was previously pointing to oldServer to point to server newServer</span></span>

## <span data-ttu-id="33ade-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33ade-111">PARAMETERS</span></span>

### <span data-ttu-id="33ade-112">— AsJob</span><span class="sxs-lookup"><span data-stu-id="33ade-112">-AsJob</span></span>
<span data-ttu-id="33ade-113">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="33ade-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="33ade-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33ade-114">-DefaultProfile</span></span>
<span data-ttu-id="33ade-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="33ade-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33ade-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="33ade-116">-Name</span></span>
<span data-ttu-id="33ade-117">Nazwa aliasu DNS programu Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="33ade-117">The Azure Sql Server Dns Alias name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33ade-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33ade-118">-ResourceGroupName</span></span>
<span data-ttu-id="33ade-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="33ade-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33ade-120">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="33ade-120">-SourceServerName</span></span>
<span data-ttu-id="33ade-121">Nazwa serwera Azure Sql Server, do którego obecnie wskazuje alias.</span><span class="sxs-lookup"><span data-stu-id="33ade-121">The name of Azure Sql Server to which alias is currently pointing.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33ade-122">-SourceServerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33ade-122">-SourceServerResourceGroupName</span></span>
<span data-ttu-id="33ade-123">Nazwa grupy zasobów serwera źródłowego.</span><span class="sxs-lookup"><span data-stu-id="33ade-123">The name of resource group of the source server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33ade-124">-SourceServerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="33ade-124">-SourceServerSubscriptionId</span></span>
<span data-ttu-id="33ade-125">Identyfikator subskrypcji serwera źródłowego</span><span class="sxs-lookup"><span data-stu-id="33ade-125">The subscription id of the source server</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33ade-126">-TargetServerName</span><span class="sxs-lookup"><span data-stu-id="33ade-126">-TargetServerName</span></span>
<span data-ttu-id="33ade-127">Nazwa serwera Azure Sql Server, do którego ma być wskaże alias.</span><span class="sxs-lookup"><span data-stu-id="33ade-127">The name of Azure Sql Server to which alias should point.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33ade-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="33ade-128">-Confirm</span></span>
<span data-ttu-id="33ade-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="33ade-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33ade-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33ade-130">-WhatIf</span></span>
<span data-ttu-id="33ade-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33ade-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33ade-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="33ade-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33ade-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33ade-133">CommonParameters</span></span>
<span data-ttu-id="33ade-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33ade-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33ade-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="33ade-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33ade-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="33ade-136">INPUTS</span></span>

### <span data-ttu-id="33ade-137">System.String</span><span class="sxs-lookup"><span data-stu-id="33ade-137">System.String</span></span>

## <span data-ttu-id="33ade-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="33ade-138">OUTPUTS</span></span>

### <span data-ttu-id="33ade-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="33ade-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="33ade-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="33ade-140">NOTES</span></span>

## <span data-ttu-id="33ade-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="33ade-141">RELATED LINKS</span></span>
