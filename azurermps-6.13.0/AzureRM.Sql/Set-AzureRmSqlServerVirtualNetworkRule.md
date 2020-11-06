---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: c71f8284cc3b1a2648e3523c77f0e9e2dd2d3876
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543348"
---
# <span data-ttu-id="b608a-101">Set-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b608a-101">Set-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="b608a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b608a-102">SYNOPSIS</span></span>
<span data-ttu-id="b608a-103">Modyfikuje konfigurację reguły sieci wirtualnej usługi Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b608a-103">Modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b608a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b608a-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b608a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b608a-105">DESCRIPTION</span></span>
<span data-ttu-id="b608a-106">To polecenie modyfikuje konfigurację reguły sieci wirtualnej usługi Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b608a-106">This command modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>
<span data-ttu-id="b608a-107">Aby sterować zestawem reguł sieci wirtualnej na serwerze, użyj polecenia "Add-AzureRmSqlServerVirtualNetworkRule" i "Remove-AzureRmSqlServerVirtualNetworkRule".</span><span class="sxs-lookup"><span data-stu-id="b608a-107">To control the set of virtual network rules in the server, use 'Add-AzureRmSqlServerVirtualNetworkRule' and 'Remove-AzureRmSqlServerVirtualNetworkRule' instead.</span></span>

## <span data-ttu-id="b608a-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b608a-108">EXAMPLES</span></span>

### <span data-ttu-id="b608a-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b608a-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Set-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="b608a-110">Modyfikuje istniejącą regułę sieci wirtualnej o identyfikator nowej podsieci sieci wirtualnej, który zawiera informacje o nowej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b608a-110">Modifies an existing virtual network rule with the new virtual network subnet id which contains information about the new virtual network</span></span>

## <span data-ttu-id="b608a-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b608a-111">PARAMETERS</span></span>

### <span data-ttu-id="b608a-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b608a-112">-AsJob</span></span>
<span data-ttu-id="b608a-113">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b608a-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b608a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b608a-114">-DefaultProfile</span></span>
<span data-ttu-id="b608a-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b608a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b608a-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="b608a-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="b608a-117">Tworzenie reguły zapory przed włączeniem punktu końcowego usługi VNET w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="b608a-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="b608a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b608a-118">-ResourceGroupName</span></span>
<span data-ttu-id="b608a-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b608a-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="b608a-120">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="b608a-120">-ServerName</span></span>
<span data-ttu-id="b608a-121">Nazwa programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b608a-121">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="b608a-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="b608a-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="b608a-123">Nazwa reguły sieci wirtualnej usługi Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b608a-123">The name of the Azure Sql Server Virtual Network Rule.</span></span>

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

### <span data-ttu-id="b608a-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="b608a-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="b608a-125">Identyfikator podsieci sieci wirtualnej dla reguły.</span><span class="sxs-lookup"><span data-stu-id="b608a-125">The Virtual Network Subnet Id for the rule.</span></span>

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

### <span data-ttu-id="b608a-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b608a-126">-Confirm</span></span>
<span data-ttu-id="b608a-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b608a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b608a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b608a-128">-WhatIf</span></span>
<span data-ttu-id="b608a-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b608a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b608a-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b608a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b608a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b608a-131">CommonParameters</span></span>
<span data-ttu-id="b608a-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b608a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b608a-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b608a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b608a-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b608a-134">INPUTS</span></span>

### <span data-ttu-id="b608a-135">System. String</span><span class="sxs-lookup"><span data-stu-id="b608a-135">System.String</span></span>

## <span data-ttu-id="b608a-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b608a-136">OUTPUTS</span></span>

### <span data-ttu-id="b608a-137">Microsoft. Azure. Commands. SQL. VirtualNetworkRule. model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="b608a-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="b608a-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b608a-138">NOTES</span></span>

## <span data-ttu-id="b608a-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b608a-139">RELATED LINKS</span></span>
