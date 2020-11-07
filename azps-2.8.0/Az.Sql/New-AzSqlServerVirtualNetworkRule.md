---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 8667de4551e9fc0c4baf623099f70f778ec8f0a3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887369"
---
# <span data-ttu-id="e007d-101">New-AzSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e007d-101">New-AzSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="e007d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e007d-102">SYNOPSIS</span></span>
<span data-ttu-id="e007d-103">Umożliwia utworzenie reguły sieci wirtualnej usługi Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e007d-103">Creates an Azure SQL Server Virtual Network Rule.</span></span> 

## <span data-ttu-id="e007d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e007d-104">SYNTAX</span></span>

```
New-AzSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e007d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e007d-105">DESCRIPTION</span></span>
<span data-ttu-id="e007d-106">Umożliwia utworzenie reguły sieci wirtualnej usługi Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e007d-106">Creates an Azure SQL Server Virtual Network Rule.</span></span> <span data-ttu-id="e007d-107">Reguły sieci wirtualnej są używane do nawiązywania połączenia z usługą Azure SQL Server z określoną siecią wirtualną w celu ograniczenia dostępu w usłudze Azure SQL Server tylko w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e007d-107">Virtual Network Rules are used to connect the Azure SQL Server to a specific Virtual Network in order to restrict the access on the Azure SQL Server to only be available within the Virtual Network.</span></span> 

## <span data-ttu-id="e007d-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e007d-108">EXAMPLES</span></span>

### <span data-ttu-id="e007d-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e007d-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = New-AzSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="e007d-110">Tworzenie reguły sieci wirtualnej usługi Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="e007d-110">Creates an Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="e007d-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e007d-111">PARAMETERS</span></span>

### <span data-ttu-id="e007d-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e007d-112">-AsJob</span></span>
<span data-ttu-id="e007d-113">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e007d-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e007d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e007d-114">-DefaultProfile</span></span>
<span data-ttu-id="e007d-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e007d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e007d-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="e007d-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="e007d-117">Tworzenie reguły zapory przed włączeniem punktu końcowego usługi VNET w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e007d-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="e007d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e007d-118">-ResourceGroupName</span></span>
<span data-ttu-id="e007d-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e007d-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="e007d-120">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="e007d-120">-ServerName</span></span>
<span data-ttu-id="e007d-121">Nazwa programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e007d-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="e007d-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="e007d-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="e007d-123">Nazwa reguły sieci wirtualnej platformy Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e007d-123">Azure Sql Server Virtual Network Rule Name.</span></span>

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

### <span data-ttu-id="e007d-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="e007d-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="e007d-125">Identyfikator podsieci sieci wirtualnej określający dane firmy Microsoft. Network</span><span class="sxs-lookup"><span data-stu-id="e007d-125">The Virtual Network Subnet Id that specifies the Microsoft.Network details</span></span>

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

### <span data-ttu-id="e007d-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e007d-126">-Confirm</span></span>
<span data-ttu-id="e007d-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e007d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e007d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e007d-128">-WhatIf</span></span>
<span data-ttu-id="e007d-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e007d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e007d-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e007d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e007d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e007d-131">CommonParameters</span></span>
<span data-ttu-id="e007d-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e007d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e007d-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e007d-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e007d-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e007d-134">INPUTS</span></span>

### <span data-ttu-id="e007d-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e007d-135">System.String</span></span>

## <span data-ttu-id="e007d-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e007d-136">OUTPUTS</span></span>

### <span data-ttu-id="e007d-137">Microsoft. Azure. Commands. SQL. VirtualNetworkRule. model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="e007d-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="e007d-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e007d-138">NOTES</span></span>

## <span data-ttu-id="e007d-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e007d-139">RELATED LINKS</span></span>
