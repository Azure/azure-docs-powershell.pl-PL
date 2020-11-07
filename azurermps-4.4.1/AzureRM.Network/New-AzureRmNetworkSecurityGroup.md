---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A420B3E7-2FE9-4D0B-803E-AC28E5F23C59
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: f2d9781f205df70e5becbc53f597f27791ca6495
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717172"
---
# <span data-ttu-id="a8ac8-101">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a8ac8-101">New-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="a8ac8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a8ac8-102">SYNOPSIS</span></span>
<span data-ttu-id="a8ac8-103">Tworzy grupę zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="a8ac8-103">Creates a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8ac8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a8ac8-104">SYNTAX</span></span>

```
New-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -Location <String>
 [-SecurityRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSecurityRule]>]
 [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a8ac8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a8ac8-105">DESCRIPTION</span></span>
<span data-ttu-id="a8ac8-106">Polecenie cmdlet **New-AzureRmNetworkSecurityGroup** tworzy grupę zabezpieczeń sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="a8ac8-106">The **New-AzureRmNetworkSecurityGroup** cmdlet creates an Azure network security group.</span></span>

## <span data-ttu-id="a8ac8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a8ac8-107">EXAMPLES</span></span>

### <span data-ttu-id="a8ac8-108">1: Tworzenie nowej grupy zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="a8ac8-108">1: Create a new network security group</span></span>
```
New-AzureRmNetworkSecurityGroup -Name "nsg1" -ResourceGroupName "rg1"  -Location  "westus"
```

<span data-ttu-id="a8ac8-109">To polecenie tworzy nową grupę zabezpieczeń sieci Azure o nazwie "nsg1" w grupie zasobów "RG1" w lokalizacji "zachód".</span><span class="sxs-lookup"><span data-stu-id="a8ac8-109">This command creates a new Azure network security group named "nsg1" in resource group "rg1" in location "westus".</span></span>

### <span data-ttu-id="a8ac8-110">2: Tworzenie szczegółowej grupy zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="a8ac8-110">2: Create a detailed network security group</span></span>
```
$rule1 = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP"
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$rule2 = New-AzureRmNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP"
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80

$nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName TestRG -Location westus -Name
    "NSG-FrontEnd" -SecurityRules $rule1,$rule2
```

<span data-ttu-id="a8ac8-111">Krok: 1 Tworzenie reguły zabezpieczeń umożliwiającej dostęp z Internetu do portu 3389.</span><span class="sxs-lookup"><span data-stu-id="a8ac8-111">Step:1 Create a security rule allowing access from the Internet to port 3389.</span></span>
<span data-ttu-id="a8ac8-112">Krok: 2 Tworzenie reguły zabezpieczeń umożliwiającej dostęp z Internetu do portu 80.</span><span class="sxs-lookup"><span data-stu-id="a8ac8-112">Step:2 Create a security rule allowing access from the Internet to port 80.</span></span>
<span data-ttu-id="a8ac8-113">Krok: 3 Dodaj reguły utworzone powyżej do nowego NSG o nazwie NSG-fronton.</span><span class="sxs-lookup"><span data-stu-id="a8ac8-113">Step:3 Add the rules created above to a new NSG named NSG-FrontEnd.</span></span>

## <span data-ttu-id="a8ac8-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a8ac8-114">PARAMETERS</span></span>

### <span data-ttu-id="a8ac8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a8ac8-115">-Force</span></span>
<span data-ttu-id="a8ac8-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a8ac8-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a8ac8-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a8ac8-117">-Location</span></span>
<span data-ttu-id="a8ac8-118">Określa region, dla którego ma zostać utworzona grupa zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="a8ac8-118">Specifies the region for which to create a network security group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ac8-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a8ac8-119">-Name</span></span>
<span data-ttu-id="a8ac8-120">Określa nazwę grupy zabezpieczeń sieci do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="a8ac8-120">Specifies the name of the network security group to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ac8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8ac8-121">-ResourceGroupName</span></span>
<span data-ttu-id="a8ac8-122">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a8ac8-122">Specifies the name of a resource group.</span></span>
<span data-ttu-id="a8ac8-123">To polecenie cmdlet tworzy grupę zabezpieczeń sieci w grupie zasobów, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="a8ac8-123">This cmdlet creates a network security group in the resource group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ac8-124">-SecurityRules</span><span class="sxs-lookup"><span data-stu-id="a8ac8-124">-SecurityRules</span></span>
<span data-ttu-id="a8ac8-125">Określa listę obiektów reguł zabezpieczeń sieci, które należy utworzyć w grupie zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="a8ac8-125">Specifies a list of network security rule objects to create in a network security group.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSecurityRule]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ac8-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="a8ac8-126">-Tag</span></span>
<span data-ttu-id="a8ac8-127">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="a8ac8-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a8ac8-128">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="a8ac8-128">For example:</span></span>

<span data-ttu-id="a8ac8-129">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="a8ac8-129">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ac8-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a8ac8-130">-Confirm</span></span>
<span data-ttu-id="a8ac8-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8ac8-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8ac8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8ac8-132">-WhatIf</span></span>
<span data-ttu-id="a8ac8-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8ac8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8ac8-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a8ac8-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8ac8-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8ac8-135">-DefaultProfile</span></span>
<span data-ttu-id="a8ac8-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a8ac8-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8ac8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8ac8-137">CommonParameters</span></span>
<span data-ttu-id="a8ac8-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8ac8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8ac8-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8ac8-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8ac8-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a8ac8-140">INPUTS</span></span>

## <span data-ttu-id="a8ac8-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a8ac8-141">OUTPUTS</span></span>

### <span data-ttu-id="a8ac8-142">Microsoft. Azure. Commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a8ac8-142">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="a8ac8-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a8ac8-143">NOTES</span></span>

## <span data-ttu-id="a8ac8-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a8ac8-144">RELATED LINKS</span></span>

[<span data-ttu-id="a8ac8-145">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a8ac8-145">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="a8ac8-146">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a8ac8-146">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="a8ac8-147">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a8ac8-147">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)
