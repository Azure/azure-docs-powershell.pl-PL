---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A420B3E7-2FE9-4D0B-803E-AC28E5F23C59
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkSecurityGroup.md
ms.openlocfilehash: 593891c19b9748c7a32019cfdaee0d069329cbea
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202775"
---
# <span data-ttu-id="8f336-101">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8f336-101">New-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="8f336-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f336-102">SYNOPSIS</span></span>
<span data-ttu-id="8f336-103">Tworzy grupę zabezpieczeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="8f336-103">Creates a network security group.</span></span>

## <span data-ttu-id="8f336-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8f336-104">SYNTAX</span></span>

```
New-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -Location <String>
 [-SecurityRules <PSSecurityRule[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f336-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8f336-105">DESCRIPTION</span></span>
<span data-ttu-id="8f336-106">Polecenie **cmdlet New-AzNetworkSecurityGroup** tworzy grupę zabezpieczeń sieci platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8f336-106">The **New-AzNetworkSecurityGroup** cmdlet creates an Azure network security group.</span></span>

## <span data-ttu-id="8f336-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8f336-107">EXAMPLES</span></span>

### <span data-ttu-id="8f336-108">Przykład 1. Tworzenie nowej grupy zabezpieczeń sieciowych</span><span class="sxs-lookup"><span data-stu-id="8f336-108">Example 1: Create a new network security group</span></span>
```powershell
New-AzNetworkSecurityGroup -Name "nsg1" -ResourceGroupName "rg1"  -Location  "westus"
```

<span data-ttu-id="8f336-109">To polecenie tworzy nową grupę zabezpieczeń sieci platformy Azure o nazwie "nsg1" w grupie zasobów "rg1" w lokalizacji "westus".</span><span class="sxs-lookup"><span data-stu-id="8f336-109">This command creates a new Azure network security group named "nsg1" in resource group "rg1" in location "westus".</span></span>

### <span data-ttu-id="8f336-110">Przykład 2. Tworzenie szczegółowej grupy zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="8f336-110">Example 2: Create a detailed network security group</span></span>
```powershell
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP" `
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix `
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80

$nsg = New-AzNetworkSecurityGroup -ResourceGroupName TestRG -Location westus -Name `
    "NSG-FrontEnd" -SecurityRules $rule1,$rule2
```

<span data-ttu-id="8f336-111">Krok:1 Utwórz regułę zabezpieczeń zezwalającą na dostęp z Internetu do portu 3389.</span><span class="sxs-lookup"><span data-stu-id="8f336-111">Step:1 Create a security rule allowing access from the Internet to port 3389.</span></span>
<span data-ttu-id="8f336-112">Krok:2 Tworzenie reguły zabezpieczeń umożliwiającej dostęp z Internetu do portu 80.</span><span class="sxs-lookup"><span data-stu-id="8f336-112">Step:2 Create a security rule allowing access from the Internet to port 80.</span></span>
<span data-ttu-id="8f336-113">Krok:3 Dodawanie reguł utworzonych powyżej do nowej nazwy NSG o nazwie NSG-FrontEnd.</span><span class="sxs-lookup"><span data-stu-id="8f336-113">Step:3 Add the rules created above to a new NSG named NSG-FrontEnd.</span></span>

## <span data-ttu-id="8f336-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f336-114">PARAMETERS</span></span>

### <span data-ttu-id="8f336-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="8f336-115">-AsJob</span></span>
<span data-ttu-id="8f336-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="8f336-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8f336-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f336-117">-DefaultProfile</span></span>
<span data-ttu-id="8f336-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8f336-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f336-119">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="8f336-119">-Force</span></span>
<span data-ttu-id="8f336-120">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="8f336-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8f336-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="8f336-121">-Location</span></span>
<span data-ttu-id="8f336-122">Określa region, dla którego ma być tworzyć grupę zabezpieczeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="8f336-122">Specifies the region for which to create a network security group.</span></span>

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

### <span data-ttu-id="8f336-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8f336-123">-Name</span></span>
<span data-ttu-id="8f336-124">Określa nazwę grupy zabezpieczeń sieci, która ma być tworzyć.</span><span class="sxs-lookup"><span data-stu-id="8f336-124">Specifies the name of the network security group to create.</span></span>

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

### <span data-ttu-id="8f336-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f336-125">-ResourceGroupName</span></span>
<span data-ttu-id="8f336-126">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8f336-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="8f336-127">To polecenie cmdlet tworzy w grupie zasobów grupę zabezpieczeń sieci, która jest określana przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="8f336-127">This cmdlet creates a network security group in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="8f336-128">— SecurityRules</span><span class="sxs-lookup"><span data-stu-id="8f336-128">-SecurityRules</span></span>
<span data-ttu-id="8f336-129">Określa listę obiektów reguł zabezpieczeń sieciowych do utworzenia w grupie zabezpieczeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="8f336-129">Specifies a list of network security rule objects to create in a network security group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSecurityRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f336-130">— Tag</span><span class="sxs-lookup"><span data-stu-id="8f336-130">-Tag</span></span>
<span data-ttu-id="8f336-131">Pary klucz-wartość w postaci tabeli skrótu.</span><span class="sxs-lookup"><span data-stu-id="8f336-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8f336-132">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="8f336-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="8f336-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8f336-133">-Confirm</span></span>
<span data-ttu-id="8f336-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8f336-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f336-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f336-135">-WhatIf</span></span>
<span data-ttu-id="8f336-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f336-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f336-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8f336-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f336-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f336-138">CommonParameters</span></span>
<span data-ttu-id="8f336-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f336-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f336-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f336-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f336-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8f336-141">INPUTS</span></span>

### <span data-ttu-id="8f336-142">System.String</span><span class="sxs-lookup"><span data-stu-id="8f336-142">System.String</span></span>

### <span data-ttu-id="8f336-143">Microsoft.Azure.Commands.Network.Models.PSSecurityRule[]</span><span class="sxs-lookup"><span data-stu-id="8f336-143">Microsoft.Azure.Commands.Network.Models.PSSecurityRule[]</span></span>

### <span data-ttu-id="8f336-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="8f336-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8f336-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8f336-145">OUTPUTS</span></span>

### <span data-ttu-id="8f336-146">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8f336-146">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="8f336-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8f336-147">NOTES</span></span>

## <span data-ttu-id="8f336-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8f336-148">RELATED LINKS</span></span>

[<span data-ttu-id="8f336-149">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8f336-149">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="8f336-150">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8f336-150">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)

[<span data-ttu-id="8f336-151">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8f336-151">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)
