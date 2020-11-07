---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5A0D9326-3A8A-4156-8372-EBA93C1BB4E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 184e1291f134b52ee57a239327bb45da4a4481ff
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890750"
---
# <span data-ttu-id="ba724-101">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ba724-101">Get-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="ba724-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ba724-102">SYNOPSIS</span></span>
<span data-ttu-id="ba724-103">Uzyskaj konfigurację reguły zabezpieczeń sieci dla grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="ba724-103">Get a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="ba724-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ba724-104">SYNTAX</span></span>

```
Get-AzNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultRules] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba724-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ba724-105">DESCRIPTION</span></span>
<span data-ttu-id="ba724-106">Polecenie cmdlet **Get-AzNetworkSecurityRuleConfig** Pobiera konfigurację reguły zabezpieczeń sieci dla grupy zabezpieczeń sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="ba724-106">The **Get-AzNetworkSecurityRuleConfig** cmdlet gets a network security rule configuration for an Azure network security group.</span></span>

## <span data-ttu-id="ba724-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ba724-107">EXAMPLES</span></span>

### <span data-ttu-id="ba724-108">1: Pobieranie konfiguracji reguł zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="ba724-108">1: Retrieving a network security rule config</span></span>
```
Get-AzNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 
    | Get-AzNetworkSecurityRuleConfig -Name AllowInternetOutBound -DefaultRules
```

<span data-ttu-id="ba724-109">To polecenie pobiera domyślną regułę o nazwie "AllowInternetOutBound" z grupy zabezpieczeń sieci Azure o nazwie "nsg1" w grupie zasobów "RG1".</span><span class="sxs-lookup"><span data-stu-id="ba724-109">This command retrieves the default rule named "AllowInternetOutBound" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

### <span data-ttu-id="ba724-110">2: Pobieranie konfiguracji reguł zabezpieczeń sieci przy użyciu samej nazwy</span><span class="sxs-lookup"><span data-stu-id="ba724-110">2: Retrieving a network security rule config using only the name</span></span>
```
Get-AzNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 
    | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
```

<span data-ttu-id="ba724-111">To polecenie pobiera regułę zdefiniowaną przez użytkownika o nazwie "RDP-Rule" z grupy zabezpieczeń sieci Azure o nazwie "nsg1" w grupie zasobów "RG1".</span><span class="sxs-lookup"><span data-stu-id="ba724-111">This command retrieves user defined rule named "rdp-rule" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="ba724-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ba724-112">PARAMETERS</span></span>

### <span data-ttu-id="ba724-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba724-113">-DefaultProfile</span></span>
<span data-ttu-id="ba724-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ba724-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba724-115">-DefaultRules</span><span class="sxs-lookup"><span data-stu-id="ba724-115">-DefaultRules</span></span>
<span data-ttu-id="ba724-116">Wskazuje, czy to polecenie cmdlet umożliwia pobieranie konfiguracji reguły utworzonej przez użytkownika, czy domyślnej konfiguracji reguły.</span><span class="sxs-lookup"><span data-stu-id="ba724-116">Indicates whether this cmdlet gets a user-created rule configuration or a default rule configuration.</span></span>

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

### <span data-ttu-id="ba724-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ba724-117">-Name</span></span>
<span data-ttu-id="ba724-118">Określa nazwę konfiguracji reguł zabezpieczeń sieci do pobrania.</span><span class="sxs-lookup"><span data-stu-id="ba724-118">Specifies the name of the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="ba724-119">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ba724-119">-NetworkSecurityGroup</span></span>
<span data-ttu-id="ba724-120">Określa obiekt **NetworkSecurityGroup** , który zawiera konfigurację reguły zabezpieczeń sieci do pobrania.</span><span class="sxs-lookup"><span data-stu-id="ba724-120">Specifies a **NetworkSecurityGroup** object that contains the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="ba724-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba724-121">CommonParameters</span></span>
<span data-ttu-id="ba724-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba724-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba724-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba724-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba724-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ba724-124">INPUTS</span></span>

### <span data-ttu-id="ba724-125">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ba724-125">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="ba724-126">Parametr "NetworkSecurityGroup" akceptuje wartość typu "PSNetworkSecurityGroup" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="ba724-126">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="ba724-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ba724-127">OUTPUTS</span></span>

### <span data-ttu-id="ba724-128">Microsoft. Azure. Commands. Network. models. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="ba724-128">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="ba724-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ba724-129">NOTES</span></span>

## <span data-ttu-id="ba724-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ba724-130">RELATED LINKS</span></span>

[<span data-ttu-id="ba724-131">Dodaj-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ba724-131">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="ba724-132">Nowe — AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ba724-132">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="ba724-133">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ba724-133">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="ba724-134">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ba724-134">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


