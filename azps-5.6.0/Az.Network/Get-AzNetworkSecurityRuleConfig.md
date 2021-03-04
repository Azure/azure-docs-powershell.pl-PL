---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5A0D9326-3A8A-4156-8372-EBA93C1BB4E4
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: c45df01f86abcd7a2f475b62b517765f3045cb10
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006321"
---
# <span data-ttu-id="b9004-101">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b9004-101">Get-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="b9004-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9004-102">SYNOPSIS</span></span>
<span data-ttu-id="b9004-103">Uzyskaj konfigurację reguł zabezpieczeń sieciowych dla grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="b9004-103">Get a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="b9004-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b9004-104">SYNTAX</span></span>

```
Get-AzNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup> [-DefaultRules]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9004-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b9004-105">DESCRIPTION</span></span>
<span data-ttu-id="b9004-106">Polecenie **cmdlet Get-AzNetworkSecurityRuleConfig** pobiera konfigurację reguły zabezpieczeń sieciowych dla grupy zabezpieczeń sieci platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b9004-106">The **Get-AzNetworkSecurityRuleConfig** cmdlet gets a network security rule configuration for an Azure network security group.</span></span>

## <span data-ttu-id="b9004-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b9004-107">EXAMPLES</span></span>

### <span data-ttu-id="b9004-108">1. Pobieranie konfiguracji reguły zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="b9004-108">1: Retrieving a network security rule config</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 
    | Get-AzNetworkSecurityRuleConfig -Name AllowInternetOutBound -DefaultRules
```

<span data-ttu-id="b9004-109">To polecenie pobiera regułę domyślną o nazwie "AllowInternetOutBound" z grupy zabezpieczeń sieci platformy Azure o nazwie "nsg1" w grupie zasobów "rg1"</span><span class="sxs-lookup"><span data-stu-id="b9004-109">This command retrieves the default rule named "AllowInternetOutBound" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

### <span data-ttu-id="b9004-110">2. Pobieranie konfiguracji reguły zabezpieczeń sieci przy użyciu tylko nazwy</span><span class="sxs-lookup"><span data-stu-id="b9004-110">2: Retrieving a network security rule config using only the name</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 
    | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
```

<span data-ttu-id="b9004-111">To polecenie pobiera regułę zdefiniowaną przez użytkownika o nazwie "reguła rdp" z grupy zabezpieczeń sieci platformy Azure o nazwie "nsg1" w grupie zasobów "rg1"</span><span class="sxs-lookup"><span data-stu-id="b9004-111">This command retrieves user defined rule named "rdp-rule" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="b9004-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9004-112">PARAMETERS</span></span>

### <span data-ttu-id="b9004-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9004-113">-DefaultProfile</span></span>
<span data-ttu-id="b9004-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b9004-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9004-115">-DefaultRules</span><span class="sxs-lookup"><span data-stu-id="b9004-115">-DefaultRules</span></span>
<span data-ttu-id="b9004-116">Wskazuje, czy to polecenie cmdlet pobiera konfigurację reguł utworzoną przez użytkownika, czy domyślną konfigurację reguł.</span><span class="sxs-lookup"><span data-stu-id="b9004-116">Indicates whether this cmdlet gets a user-created rule configuration or a default rule configuration.</span></span>

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

### <span data-ttu-id="b9004-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b9004-117">-Name</span></span>
<span data-ttu-id="b9004-118">Określa nazwę konfiguracji reguły zabezpieczeń sieci do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="b9004-118">Specifies the name of the network security rule configuration to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9004-119">- NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b9004-119">-NetworkSecurityGroup</span></span>
<span data-ttu-id="b9004-120">Określa obiekt **NetworkSecurityGroup** zawierający konfigurację reguły zabezpieczeń sieci do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="b9004-120">Specifies a **NetworkSecurityGroup** object that contains the network security rule configuration to get.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9004-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9004-121">CommonParameters</span></span>
<span data-ttu-id="b9004-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9004-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9004-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b9004-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9004-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b9004-124">INPUTS</span></span>

### <span data-ttu-id="b9004-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b9004-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="b9004-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b9004-126">OUTPUTS</span></span>

### <span data-ttu-id="b9004-127">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="b9004-127">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="b9004-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b9004-128">NOTES</span></span>

## <span data-ttu-id="b9004-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b9004-129">RELATED LINKS</span></span>

[<span data-ttu-id="b9004-130">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b9004-130">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="b9004-131">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b9004-131">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="b9004-132">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b9004-132">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="b9004-133">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b9004-133">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


