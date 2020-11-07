---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/New-AzPrivateDnsVirtualNetworkLink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 7d2a9a399e6582e2ff3815447570548ac62f6676
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708747"
---
# <span data-ttu-id="127d5-101">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="127d5-101">New-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="127d5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="127d5-102">SYNOPSIS</span></span>
<span data-ttu-id="127d5-103">Tworzy nowe prywatne łącze sieci wirtualnej DNS.</span><span class="sxs-lookup"><span data-stu-id="127d5-103">Creates a new private DNS virtual network link.</span></span>

## <span data-ttu-id="127d5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="127d5-104">SYNTAX</span></span>

### <span data-ttu-id="127d5-105">VirtualNetworkId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="127d5-105">VirtualNetworkId (Default)</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -VirtualNetworkId <String> [-EnableRegistration] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="127d5-106">VirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="127d5-106">VirtualNetworkObject</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -VirtualNetwork <VirtualNetwork> [-EnableRegistration] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="127d5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="127d5-107">DESCRIPTION</span></span>
<span data-ttu-id="127d5-108">Polecenie cmdlet **New-AzPrivateDnsVirtualNetworkLink** tworzy nowe łącze sieci wirtualnej DNS (Private Name System) w określonej grupie zasobów i prywatnej strefie.</span><span class="sxs-lookup"><span data-stu-id="127d5-108">The **New-AzPrivateDnsVirtualNetworkLink** cmdlet creates a new private Domain Name System (DNS) virtual network link in the specified resource group and private zone.</span></span> <span data-ttu-id="127d5-109">Musisz określić unikatową nazwę linku dla parametru *name* lub polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="127d5-109">You must specify a unique link name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="127d5-110">Za pomocą zmiennej *Confirm* i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="127d5-110">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="127d5-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="127d5-111">EXAMPLES</span></span>

### <span data-ttu-id="127d5-112">Przykład 1. Tworzenie prywatnego łącza wirtualnej sieci DNS</span><span class="sxs-lookup"><span data-stu-id="127d5-112">Example 1: Create a Private DNS virtual network link</span></span>
```
PS C:\>$Link = New-AzPrivateDnsVirtualNetworkLink -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Name "mylink" -VirtualNetworkId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork" -EnableRegistration

Name                    : mylink
ResourceId              : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/privateDnsZones/myzone.com/virtualNetworkLinks/mylink
ResourceGroupName       : MyResourceGroup
ZoneName                : myzone.com
VirtualNetworkId        : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.N
                          etwork/virtualNetworks/myvirtualnetwork
Location                :
Etag                    : "xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
Tags                    : {}
RegistrationEnabled     : True
VirtualNetworkLinkState : Completed
ProvisioningState       : Succeeded
```

<span data-ttu-id="127d5-113">To polecenie tworzy nowe łącze sieci wirtualnej skojarzone z prywatną strefą DNS o nazwie myzone.com i Virtual Network "myvirtualnetwork" (która została już utworzona w grupie zasobów) w określonej grupie zasobów, a następnie zapisuje ją w zmiennej $Link.</span><span class="sxs-lookup"><span data-stu-id="127d5-113">This command creates a new virtual network link associated with the private DNS zone named myzone.com and virtual network "myvirtualnetwork" (which has already been created in the resource group) in the specified resource group, and then stores it in the $Link variable.</span></span>

## <span data-ttu-id="127d5-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="127d5-114">PARAMETERS</span></span>

### <span data-ttu-id="127d5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="127d5-115">-DefaultProfile</span></span>
<span data-ttu-id="127d5-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="127d5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="127d5-117">-EnableRegistration</span><span class="sxs-lookup"><span data-stu-id="127d5-117">-EnableRegistration</span></span>
<span data-ttu-id="127d5-118">Parametr przełącznika reprezentujący, że link jest włączony lub nie.</span><span class="sxs-lookup"><span data-stu-id="127d5-118">Switch parameter that represents if the link is registration enabled or not.</span></span>

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

### <span data-ttu-id="127d5-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="127d5-119">-Name</span></span>
<span data-ttu-id="127d5-120">Określa nazwę linku sieci wirtualnej, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="127d5-120">Specifies the name of the virtual network link to create.</span></span>

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

### <span data-ttu-id="127d5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="127d5-121">-ResourceGroupName</span></span>
<span data-ttu-id="127d5-122">Określa grupę zasobów, w której ma zostać utworzone łącze.</span><span class="sxs-lookup"><span data-stu-id="127d5-122">Specifies the resource group in which to create the link.</span></span>

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

### <span data-ttu-id="127d5-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="127d5-123">-Tag</span></span>
<span data-ttu-id="127d5-124">Tabela skrótów reprezentująca znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="127d5-124">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="127d5-125">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="127d5-125">-VirtualNetwork</span></span>
<span data-ttu-id="127d5-126">Wirtualny obiekt sieciowy skojarzony z linkiem.</span><span class="sxs-lookup"><span data-stu-id="127d5-126">The virtual network object associated with the link.</span></span>

```yaml
Type: Microsoft.Azure.Management.Internal.Network.Common.IVirtualNetwork
Parameter Sets: VirtualNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="127d5-127">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="127d5-127">-VirtualNetworkId</span></span>
<span data-ttu-id="127d5-128">Identyfikator zasobu sieci wirtualnej skojarzonego z linkiem.</span><span class="sxs-lookup"><span data-stu-id="127d5-128">The resource id of the virtual network associated with the link.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="127d5-129">-Nazwa_strefy</span><span class="sxs-lookup"><span data-stu-id="127d5-129">-ZoneName</span></span>
<span data-ttu-id="127d5-130">Określa nazwę strefy, która będzie połączona z łączem sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="127d5-130">Specifies the name of the zone which will be linked to the virtual network link.</span></span>

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

### <span data-ttu-id="127d5-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="127d5-131">-Confirm</span></span>
<span data-ttu-id="127d5-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="127d5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="127d5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="127d5-133">-WhatIf</span></span>
<span data-ttu-id="127d5-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="127d5-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="127d5-135">Polecenie cmdlet nie jest uruchamiane. Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="127d5-135">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="127d5-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="127d5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="127d5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="127d5-137">CommonParameters</span></span>
<span data-ttu-id="127d5-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="127d5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="127d5-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="127d5-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="127d5-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="127d5-140">INPUTS</span></span>

### <span data-ttu-id="127d5-141">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="127d5-141">None</span></span>

## <span data-ttu-id="127d5-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="127d5-142">OUTPUTS</span></span>

### <span data-ttu-id="127d5-143">Microsoft. Azure. Commands. PrivateDns. models. PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="127d5-143">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="127d5-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="127d5-144">NOTES</span></span>

## <span data-ttu-id="127d5-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="127d5-145">RELATED LINKS</span></span>

[<span data-ttu-id="127d5-146">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="127d5-146">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="127d5-147">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="127d5-147">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="127d5-148">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="127d5-148">Remove-AzPrivateDnsVirtualNetworkLink</span></span>](./Remove-AzPrivateDnsVirtualNetworkLink.md)
