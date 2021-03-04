---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: f5dbea3701f7f0fdaf9c503e58e03fdcc9237530
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955194"
---
# <span data-ttu-id="57580-101">New-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="57580-101">New-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="57580-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57580-102">SYNOPSIS</span></span>
<span data-ttu-id="57580-103">Tworzy regułę wirtualnej sieci programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="57580-103">Creates an Azure SQL Server Virtual Network Rule.</span></span> 

## <span data-ttu-id="57580-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="57580-104">SYNTAX</span></span>

```
New-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57580-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="57580-105">DESCRIPTION</span></span>
<span data-ttu-id="57580-106">Tworzy regułę wirtualnej sieci programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="57580-106">Creates an Azure SQL Server Virtual Network Rule.</span></span> <span data-ttu-id="57580-107">Reguły sieci wirtualnej służą do łączenia programu Azure SQL Server z określoną siecią wirtualną w celu ograniczenia dostępu w usłudze Azure SQL Server tylko do sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="57580-107">Virtual Network Rules are used to connect the Azure SQL Server to a specific Virtual Network in order to restrict the access on the Azure SQL Server to only be available within the Virtual Network.</span></span> 

## <span data-ttu-id="57580-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="57580-108">EXAMPLES</span></span>

### <span data-ttu-id="57580-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="57580-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = New-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="57580-110">Tworzy regułę sieci wirtualnej programu Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="57580-110">Creates an Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="57580-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57580-111">PARAMETERS</span></span>

### <span data-ttu-id="57580-112">— AsJob</span><span class="sxs-lookup"><span data-stu-id="57580-112">-AsJob</span></span>
<span data-ttu-id="57580-113">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="57580-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="57580-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57580-114">-DefaultProfile</span></span>
<span data-ttu-id="57580-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="57580-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57580-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="57580-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="57580-117">Utwórz regułę zapory, zanim sieć wirtualna będzie włączona dla punktu końcowego usługi vnet.</span><span class="sxs-lookup"><span data-stu-id="57580-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="57580-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57580-118">-ResourceGroupName</span></span>
<span data-ttu-id="57580-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="57580-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="57580-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="57580-120">-ServerName</span></span>
<span data-ttu-id="57580-121">Nazwa programu Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="57580-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="57580-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="57580-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="57580-123">Nazwa reguły wirtualnej sieci programu Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="57580-123">Azure Sql Server Virtual Network Rule Name.</span></span>

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

### <span data-ttu-id="57580-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="57580-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="57580-125">Identyfikator podsieci wirtualnej sieci określający szczegóły witryny Microsoft.Network</span><span class="sxs-lookup"><span data-stu-id="57580-125">The Virtual Network Subnet Id that specifies the Microsoft.Network details</span></span>

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

### <span data-ttu-id="57580-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="57580-126">-Confirm</span></span>
<span data-ttu-id="57580-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="57580-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57580-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57580-128">-WhatIf</span></span>
<span data-ttu-id="57580-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57580-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57580-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="57580-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57580-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57580-131">CommonParameters</span></span>
<span data-ttu-id="57580-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57580-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57580-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57580-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57580-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57580-134">INPUTS</span></span>

### <span data-ttu-id="57580-135">System.String</span><span class="sxs-lookup"><span data-stu-id="57580-135">System.String</span></span>

## <span data-ttu-id="57580-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57580-136">OUTPUTS</span></span>

### <span data-ttu-id="57580-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="57580-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="57580-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="57580-138">NOTES</span></span>

## <span data-ttu-id="57580-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="57580-139">RELATED LINKS</span></span>
