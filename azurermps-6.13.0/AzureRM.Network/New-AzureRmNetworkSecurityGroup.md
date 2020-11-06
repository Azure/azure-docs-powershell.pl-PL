---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A420B3E7-2FE9-4D0B-803E-AC28E5F23C59
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: 1ffcad92a50cc332fdcab71337112b8d0c436388
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547455"
---
# <span data-ttu-id="16663-101">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="16663-101">New-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="16663-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="16663-102">SYNOPSIS</span></span>
<span data-ttu-id="16663-103">Tworzy grupę zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="16663-103">Creates a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16663-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="16663-104">SYNTAX</span></span>

```
New-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -Location <String>
 [-SecurityRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSecurityRule]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="16663-105">Opis</span><span class="sxs-lookup"><span data-stu-id="16663-105">DESCRIPTION</span></span>
<span data-ttu-id="16663-106">Polecenie cmdlet **New-AzureRmNetworkSecurityGroup** tworzy grupę zabezpieczeń sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="16663-106">The **New-AzureRmNetworkSecurityGroup** cmdlet creates an Azure network security group.</span></span>

## <span data-ttu-id="16663-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="16663-107">EXAMPLES</span></span>

### <span data-ttu-id="16663-108">1: Tworzenie nowej grupy zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="16663-108">1: Create a new network security group</span></span>
```
New-AzureRmNetworkSecurityGroup -Name "nsg1" -ResourceGroupName "rg1"  -Location  "westus"
```

<span data-ttu-id="16663-109">To polecenie tworzy nową grupę zabezpieczeń sieci Azure o nazwie "nsg1" w grupie zasobów "RG1" w lokalizacji "zachód".</span><span class="sxs-lookup"><span data-stu-id="16663-109">This command creates a new Azure network security group named "nsg1" in resource group "rg1" in location "westus".</span></span>

### <span data-ttu-id="16663-110">2: Tworzenie szczegółowej grupy zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="16663-110">2: Create a detailed network security group</span></span>
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

<span data-ttu-id="16663-111">Krok: 1 Tworzenie reguły zabezpieczeń umożliwiającej dostęp z Internetu do portu 3389.</span><span class="sxs-lookup"><span data-stu-id="16663-111">Step:1 Create a security rule allowing access from the Internet to port 3389.</span></span>
<span data-ttu-id="16663-112">Krok: 2 Tworzenie reguły zabezpieczeń umożliwiającej dostęp z Internetu do portu 80.</span><span class="sxs-lookup"><span data-stu-id="16663-112">Step:2 Create a security rule allowing access from the Internet to port 80.</span></span>
<span data-ttu-id="16663-113">Krok: 3 Dodaj reguły utworzone powyżej do nowego NSG o nazwie NSG-fronton.</span><span class="sxs-lookup"><span data-stu-id="16663-113">Step:3 Add the rules created above to a new NSG named NSG-FrontEnd.</span></span>

## <span data-ttu-id="16663-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="16663-114">PARAMETERS</span></span>

### <span data-ttu-id="16663-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="16663-115">-AsJob</span></span>
<span data-ttu-id="16663-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="16663-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="16663-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16663-117">-DefaultProfile</span></span>
<span data-ttu-id="16663-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="16663-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16663-119">-Force</span><span class="sxs-lookup"><span data-stu-id="16663-119">-Force</span></span>
<span data-ttu-id="16663-120">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="16663-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="16663-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="16663-121">-Location</span></span>
<span data-ttu-id="16663-122">Określa region, dla którego ma zostać utworzona grupa zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="16663-122">Specifies the region for which to create a network security group.</span></span>

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

### <span data-ttu-id="16663-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="16663-123">-Name</span></span>
<span data-ttu-id="16663-124">Określa nazwę grupy zabezpieczeń sieci do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="16663-124">Specifies the name of the network security group to create.</span></span>

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

### <span data-ttu-id="16663-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16663-125">-ResourceGroupName</span></span>
<span data-ttu-id="16663-126">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="16663-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="16663-127">To polecenie cmdlet tworzy grupę zabezpieczeń sieci w grupie zasobów, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="16663-127">This cmdlet creates a network security group in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="16663-128">-SecurityRules</span><span class="sxs-lookup"><span data-stu-id="16663-128">-SecurityRules</span></span>
<span data-ttu-id="16663-129">Określa listę obiektów reguł zabezpieczeń sieci, które należy utworzyć w grupie zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="16663-129">Specifies a list of network security rule objects to create in a network security group.</span></span>

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

### <span data-ttu-id="16663-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="16663-130">-Tag</span></span>
<span data-ttu-id="16663-131">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="16663-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="16663-132">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="16663-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="16663-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="16663-133">-Confirm</span></span>
<span data-ttu-id="16663-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16663-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16663-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16663-135">-WhatIf</span></span>
<span data-ttu-id="16663-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16663-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16663-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="16663-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16663-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16663-138">CommonParameters</span></span>
<span data-ttu-id="16663-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16663-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16663-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16663-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16663-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="16663-141">INPUTS</span></span>

### <span data-ttu-id="16663-142">System. String</span><span class="sxs-lookup"><span data-stu-id="16663-142">System.String</span></span>

### <span data-ttu-id="16663-143">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. Network. MODELES. PSSecurityRule; Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="16663-143">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSSecurityRule, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="16663-144">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="16663-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="16663-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="16663-145">OUTPUTS</span></span>

### <span data-ttu-id="16663-146">Microsoft. Azure. Commands. Network. models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="16663-146">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="16663-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="16663-147">NOTES</span></span>

## <span data-ttu-id="16663-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="16663-148">RELATED LINKS</span></span>

[<span data-ttu-id="16663-149">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="16663-149">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="16663-150">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="16663-150">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="16663-151">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="16663-151">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)
