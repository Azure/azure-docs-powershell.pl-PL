---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 64fc7b3acdc497759b707f024a0fb14c7017c44c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196098"
---
# <span data-ttu-id="c5a5b-101">New-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c5a5b-101">New-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="c5a5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5a5b-102">SYNOPSIS</span></span>
<span data-ttu-id="c5a5b-103">Tworzy regułę wirtualnej sieci programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c5a5b-103">Creates an Azure SQL Server Virtual Network Rule.</span></span> 

## <span data-ttu-id="c5a5b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c5a5b-104">SYNTAX</span></span>

```
New-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5a5b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c5a5b-105">DESCRIPTION</span></span>
<span data-ttu-id="c5a5b-106">Tworzy regułę wirtualnej sieci programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c5a5b-106">Creates an Azure SQL Server Virtual Network Rule.</span></span> <span data-ttu-id="c5a5b-107">Reguły sieci wirtualnej służą do łączenia programu Azure SQL Server z określoną siecią wirtualną w celu ograniczenia dostępu w usłudze Azure SQL Server tylko do sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c5a5b-107">Virtual Network Rules are used to connect the Azure SQL Server to a specific Virtual Network in order to restrict the access on the Azure SQL Server to only be available within the Virtual Network.</span></span> 

## <span data-ttu-id="c5a5b-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c5a5b-108">EXAMPLES</span></span>

### <span data-ttu-id="c5a5b-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c5a5b-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = New-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="c5a5b-110">Tworzy regułę sieci wirtualnej programu Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="c5a5b-110">Creates an Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="c5a5b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5a5b-111">PARAMETERS</span></span>

### <span data-ttu-id="c5a5b-112">— AsJob</span><span class="sxs-lookup"><span data-stu-id="c5a5b-112">-AsJob</span></span>
<span data-ttu-id="c5a5b-113">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c5a5b-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c5a5b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5a5b-114">-DefaultProfile</span></span>
<span data-ttu-id="c5a5b-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="c5a5b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c5a5b-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="c5a5b-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="c5a5b-117">Utwórz regułę zapory, zanim sieć wirtualna będzie włączona dla punktu końcowego usługi vnet.</span><span class="sxs-lookup"><span data-stu-id="c5a5b-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="c5a5b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5a5b-118">-ResourceGroupName</span></span>
<span data-ttu-id="c5a5b-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c5a5b-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="c5a5b-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c5a5b-120">-ServerName</span></span>
<span data-ttu-id="c5a5b-121">Nazwa programu Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="c5a5b-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="c5a5b-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="c5a5b-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="c5a5b-123">Nazwa reguły wirtualnej sieci programu Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="c5a5b-123">Azure Sql Server Virtual Network Rule Name.</span></span>

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

### <span data-ttu-id="c5a5b-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="c5a5b-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="c5a5b-125">Identyfikator podsieci wirtualnej sieci określający szczegóły witryny Microsoft.Network</span><span class="sxs-lookup"><span data-stu-id="c5a5b-125">The Virtual Network Subnet Id that specifies the Microsoft.Network details</span></span>

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

### <span data-ttu-id="c5a5b-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c5a5b-126">-Confirm</span></span>
<span data-ttu-id="c5a5b-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c5a5b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5a5b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5a5b-128">-WhatIf</span></span>
<span data-ttu-id="c5a5b-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5a5b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5a5b-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c5a5b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5a5b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5a5b-131">CommonParameters</span></span>
<span data-ttu-id="c5a5b-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5a5b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5a5b-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c5a5b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5a5b-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c5a5b-134">INPUTS</span></span>

### <span data-ttu-id="c5a5b-135">System.String</span><span class="sxs-lookup"><span data-stu-id="c5a5b-135">System.String</span></span>

## <span data-ttu-id="c5a5b-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c5a5b-136">OUTPUTS</span></span>

### <span data-ttu-id="c5a5b-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="c5a5b-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="c5a5b-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c5a5b-138">NOTES</span></span>

## <span data-ttu-id="c5a5b-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c5a5b-139">RELATED LINKS</span></span>
