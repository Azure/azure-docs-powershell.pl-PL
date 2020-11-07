---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5A0D9326-3A8A-4156-8372-EBA93C1BB4E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworksecurityruleconfig
schema: 2.0.0
ms.openlocfilehash: 55f2ad108b6392a2f17c7b1539c5ebe7cccc3c19
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899268"
---
# <span data-ttu-id="93e08-101">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="93e08-101">Get-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="93e08-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="93e08-102">SYNOPSIS</span></span>
<span data-ttu-id="93e08-103">Uzyskaj konfigurację reguły zabezpieczeń sieci dla grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="93e08-103">Get a network security rule configuration for a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93e08-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="93e08-104">SYNTAX</span></span>

```
Get-AzureRmNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultRules] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93e08-105">Opis</span><span class="sxs-lookup"><span data-stu-id="93e08-105">DESCRIPTION</span></span>
<span data-ttu-id="93e08-106">Polecenie cmdlet **Get-AzureRmNetworkSecurityRuleConfig** Pobiera konfigurację reguły zabezpieczeń sieci dla grupy zabezpieczeń sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="93e08-106">The **Get-AzureRmNetworkSecurityRuleConfig** cmdlet gets a network security rule configuration for an Azure network security group.</span></span>

## <span data-ttu-id="93e08-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="93e08-107">EXAMPLES</span></span>

### <span data-ttu-id="93e08-108">1: Pobieranie konfiguracji reguł zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="93e08-108">1: Retrieving a network security rule config</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 
    | Get-AzureRmNetworkSecurityRuleConfig -Name AllowInternetOutBound -DefaultRules
```

<span data-ttu-id="93e08-109">To polecenie pobiera domyślną regułę o nazwie "AllowInternetOutBound" z grupy zabezpieczeń sieci Azure o nazwie "nsg1" w grupie zasobów "RG1".</span><span class="sxs-lookup"><span data-stu-id="93e08-109">This command retrieves the default rule named "AllowInternetOutBound" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

### <span data-ttu-id="93e08-110">2: Pobieranie konfiguracji reguł zabezpieczeń sieci przy użyciu samej nazwy</span><span class="sxs-lookup"><span data-stu-id="93e08-110">2: Retrieving a network security rule config using only the name</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 
    | Get-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule"
```

<span data-ttu-id="93e08-111">To polecenie pobiera regułę zdefiniowaną przez użytkownika o nazwie "RDP-Rule" z grupy zabezpieczeń sieci Azure o nazwie "nsg1" w grupie zasobów "RG1".</span><span class="sxs-lookup"><span data-stu-id="93e08-111">This command retrieves user defined rule named "rdp-rule" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="93e08-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="93e08-112">PARAMETERS</span></span>

### <span data-ttu-id="93e08-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93e08-113">-DefaultProfile</span></span>
<span data-ttu-id="93e08-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="93e08-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93e08-115">-DefaultRules</span><span class="sxs-lookup"><span data-stu-id="93e08-115">-DefaultRules</span></span>
<span data-ttu-id="93e08-116">Wskazuje, czy to polecenie cmdlet umożliwia pobieranie konfiguracji reguły utworzonej przez użytkownika, czy domyślnej konfiguracji reguły.</span><span class="sxs-lookup"><span data-stu-id="93e08-116">Indicates whether this cmdlet gets a user-created rule configuration or a default rule configuration.</span></span>

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

### <span data-ttu-id="93e08-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="93e08-117">-Name</span></span>
<span data-ttu-id="93e08-118">Określa nazwę konfiguracji reguł zabezpieczeń sieci do pobrania.</span><span class="sxs-lookup"><span data-stu-id="93e08-118">Specifies the name of the network security rule configuration to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93e08-119">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="93e08-119">-NetworkSecurityGroup</span></span>
<span data-ttu-id="93e08-120">Określa obiekt **NetworkSecurityGroup** , który zawiera konfigurację reguły zabezpieczeń sieci do pobrania.</span><span class="sxs-lookup"><span data-stu-id="93e08-120">Specifies a **NetworkSecurityGroup** object that contains the network security rule configuration to get.</span></span>

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93e08-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93e08-121">CommonParameters</span></span>
<span data-ttu-id="93e08-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93e08-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93e08-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93e08-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93e08-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="93e08-124">INPUTS</span></span>

### <span data-ttu-id="93e08-125">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="93e08-125">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="93e08-126">Parametr "NetworkSecurityGroup" akceptuje wartość typu "PSNetworkSecurityGroup" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="93e08-126">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="93e08-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="93e08-127">OUTPUTS</span></span>

### <span data-ttu-id="93e08-128">Microsoft. Azure. Commands. Network. models. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="93e08-128">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="93e08-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="93e08-129">NOTES</span></span>

## <span data-ttu-id="93e08-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="93e08-130">RELATED LINKS</span></span>

[<span data-ttu-id="93e08-131">Dodaj-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="93e08-131">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="93e08-132">Nowe — AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="93e08-132">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="93e08-133">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="93e08-133">Remove-AzureRmNetworkSecurityRuleConfig</span></span>](./Remove-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="93e08-134">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="93e08-134">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)


