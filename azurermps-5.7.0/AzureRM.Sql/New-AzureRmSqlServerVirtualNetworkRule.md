---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 2955834fdb5c902b7495fe212cb9e697b0cee940
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717298"
---
# <span data-ttu-id="4494e-101">New-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4494e-101">New-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="4494e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4494e-102">SYNOPSIS</span></span>
<span data-ttu-id="4494e-103">Umożliwia utworzenie reguły sieci wirtualnej usługi Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4494e-103">Creates an Azure SQL Server Virtual Network Rule.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4494e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4494e-104">SYNTAX</span></span>

```
New-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4494e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4494e-105">DESCRIPTION</span></span>
<span data-ttu-id="4494e-106">Umożliwia utworzenie reguły sieci wirtualnej usługi Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4494e-106">Creates an Azure SQL Server Virtual Network Rule.</span></span> <span data-ttu-id="4494e-107">Reguły sieci wirtualnej są używane do nawiązywania połączenia z usługą Azure SQL Server z określoną siecią wirtualną w celu ograniczenia dostępu w usłudze Azure SQL Server tylko w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4494e-107">Virtual Network Rules are used to connect the Azure SQL Server to a specific Virtual Network in order to restrict the access on the Azure SQL Server to only be available within the Virtual Network.</span></span> 

## <span data-ttu-id="4494e-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4494e-108">EXAMPLES</span></span>

### <span data-ttu-id="4494e-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4494e-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = New-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="4494e-110">Tworzenie reguły sieci wirtualnej usługi Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="4494e-110">Creates an Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="4494e-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4494e-111">PARAMETERS</span></span>

### <span data-ttu-id="4494e-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4494e-112">-AsJob</span></span>
<span data-ttu-id="4494e-113">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="4494e-113">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4494e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4494e-114">-DefaultProfile</span></span>
<span data-ttu-id="4494e-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="4494e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4494e-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="4494e-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="4494e-117">Tworzenie reguły zapory przed włączeniem punktu końcowego usługi VNET w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4494e-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4494e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4494e-118">-ResourceGroupName</span></span>
<span data-ttu-id="4494e-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4494e-119">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4494e-120">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="4494e-120">-ServerName</span></span>
<span data-ttu-id="4494e-121">Nazwa programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4494e-121">The Azure Sql Server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4494e-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="4494e-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="4494e-123">Nazwa reguły sieci wirtualnej platformy Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4494e-123">Azure Sql Server Virtual Network Rule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4494e-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="4494e-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="4494e-125">Identyfikator podsieci sieci wirtualnej określający dane firmy Microsoft. Network</span><span class="sxs-lookup"><span data-stu-id="4494e-125">The Virtual Network Subnet Id that specifies the Microsoft.Network details</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4494e-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4494e-126">-Confirm</span></span>
<span data-ttu-id="4494e-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4494e-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4494e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4494e-128">-WhatIf</span></span>
<span data-ttu-id="4494e-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4494e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4494e-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4494e-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4494e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4494e-131">CommonParameters</span></span>
<span data-ttu-id="4494e-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4494e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4494e-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4494e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4494e-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4494e-134">INPUTS</span></span>

### <span data-ttu-id="4494e-135">System. String</span><span class="sxs-lookup"><span data-stu-id="4494e-135">System.String</span></span>

## <span data-ttu-id="4494e-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4494e-136">OUTPUTS</span></span>

### <span data-ttu-id="4494e-137">Microsoft. Azure. Commands. SQL. VirtualNetworkRule. model. AzureSqlServerVirtualNetworkRuleModel</span><span class="sxs-lookup"><span data-stu-id="4494e-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="4494e-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4494e-138">NOTES</span></span>

## <span data-ttu-id="4494e-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4494e-139">RELATED LINKS</span></span>
