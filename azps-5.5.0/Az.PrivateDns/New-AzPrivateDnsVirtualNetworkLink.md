---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/New-AzPrivateDnsVirtualNetworkLink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: be1480b68c4b0fd66328a7ff417517ee86cb88df
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202114"
---
# <span data-ttu-id="dd4c4-101">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="dd4c4-101">New-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="dd4c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd4c4-102">SYNOPSIS</span></span>
<span data-ttu-id="dd4c4-103">Tworzy nowy prywatny link sieci wirtualnej DNS.</span><span class="sxs-lookup"><span data-stu-id="dd4c4-103">Creates a new private DNS virtual network link.</span></span>

## <span data-ttu-id="dd4c4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dd4c4-104">SYNTAX</span></span>

### <span data-ttu-id="dd4c4-105">VirtualNetworkId (domyślne)</span><span class="sxs-lookup"><span data-stu-id="dd4c4-105">VirtualNetworkId (Default)</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -VirtualNetworkId <String> [-EnableRegistration] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd4c4-106">VirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="dd4c4-106">VirtualNetworkObject</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -VirtualNetwork <VirtualNetwork> [-EnableRegistration] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd4c4-107">RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="dd4c4-107">RemoteVirtualNetworkId</span></span>
```
New-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-EnableRegistration] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd4c4-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="dd4c4-108">DESCRIPTION</span></span>
<span data-ttu-id="dd4c4-109">Polecenie cmdlet **New-AzPrivateDnsVirtualNetworkLink** tworzy nowy link sieci wirtualnej DNS (Domain Name System) w określonej grupie zasobów i strefie prywatnej.</span><span class="sxs-lookup"><span data-stu-id="dd4c4-109">The **New-AzPrivateDnsVirtualNetworkLink** cmdlet creates a new private Domain Name System (DNS) virtual network link in the specified resource group and private zone.</span></span> <span data-ttu-id="dd4c4-110">Musisz określić unikatową nazwę linku dla *parametru Name* lub polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="dd4c4-110">You must specify a unique link name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="dd4c4-111">Za pomocą *parametru Confirm* i $ConfirmPreference programu Windows PowerShell możesz kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="dd4c4-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="dd4c4-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dd4c4-112">EXAMPLES</span></span>

### <span data-ttu-id="dd4c4-113">Przykład 1. Tworzenie linku do prywatnej wirtualnej sieci DNS</span><span class="sxs-lookup"><span data-stu-id="dd4c4-113">Example 1: Create a Private DNS virtual network link</span></span>
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

<span data-ttu-id="dd4c4-114">To polecenie tworzy nowy wirtualny link sieciowy skojarzony z prywatną strefą DNS o nazwie myzone.com i sieci wirtualnej "myvirtualnetwork" (która została już utworzona w grupie zasobów) w określonej grupie zasobów, a następnie zapisuje go w zmiennej $Link.</span><span class="sxs-lookup"><span data-stu-id="dd4c4-114">This command creates a new virtual network link associated with the private DNS zone named myzone.com and virtual network "myvirtualnetwork" (which has already been created in the resource group) in the specified resource group, and then stores it in the $Link variable.</span></span>

## <span data-ttu-id="dd4c4-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd4c4-115">PARAMETERS</span></span>

### <span data-ttu-id="dd4c4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd4c4-116">-DefaultProfile</span></span>
<span data-ttu-id="dd4c4-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="dd4c4-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dd4c4-118">-EnableRegistration</span><span class="sxs-lookup"><span data-stu-id="dd4c4-118">-EnableRegistration</span></span>
<span data-ttu-id="dd4c4-119">Parametr przełącznika reprezentujący, czy link jest włączony, czy nie.</span><span class="sxs-lookup"><span data-stu-id="dd4c4-119">Switch parameter that represents if the link is registration enabled or not.</span></span>

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

### <span data-ttu-id="dd4c4-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="dd4c4-120">-Name</span></span>
<span data-ttu-id="dd4c4-121">Określa nazwę linku sieci wirtualnej do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="dd4c4-121">Specifies the name of the virtual network link to create.</span></span>

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

### <span data-ttu-id="dd4c4-122">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="dd4c4-122">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="dd4c4-123">Identyfikator zasobu sieci wirtualnej w innej dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="dd4c4-123">The resource id of the virtual network in another tenant.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoteVirtualNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd4c4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd4c4-124">-ResourceGroupName</span></span>
<span data-ttu-id="dd4c4-125">Określa grupę zasobów, w której ma być tworzyć link.</span><span class="sxs-lookup"><span data-stu-id="dd4c4-125">Specifies the resource group in which to create the link.</span></span>

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

### <span data-ttu-id="dd4c4-126">— Tag</span><span class="sxs-lookup"><span data-stu-id="dd4c4-126">-Tag</span></span>
<span data-ttu-id="dd4c4-127">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="dd4c4-127">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="dd4c4-128">— VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="dd4c4-128">-VirtualNetwork</span></span>
<span data-ttu-id="dd4c4-129">Obiekt sieci wirtualnej skojarzony z linkiem.</span><span class="sxs-lookup"><span data-stu-id="dd4c4-129">The virtual network object associated with the link.</span></span>

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

### <span data-ttu-id="dd4c4-130">- VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="dd4c4-130">-VirtualNetworkId</span></span>
<span data-ttu-id="dd4c4-131">Identyfikator zasobu sieci wirtualnej skojarzonej z linkiem.</span><span class="sxs-lookup"><span data-stu-id="dd4c4-131">The resource id of the virtual network associated with the link.</span></span>

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

### <span data-ttu-id="dd4c4-132">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="dd4c4-132">-ZoneName</span></span>
<span data-ttu-id="dd4c4-133">Określa nazwę strefy, która zostanie połączona z łączem sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="dd4c4-133">Specifies the name of the zone which will be linked to the virtual network link.</span></span>

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

### <span data-ttu-id="dd4c4-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dd4c4-134">-Confirm</span></span>
<span data-ttu-id="dd4c4-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="dd4c4-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd4c4-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd4c4-136">-WhatIf</span></span>
<span data-ttu-id="dd4c4-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd4c4-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dd4c4-138">Polecenie cmdlet nie zostanie uruchomione. Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd4c4-138">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dd4c4-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="dd4c4-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd4c4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd4c4-140">CommonParameters</span></span>
<span data-ttu-id="dd4c4-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd4c4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd4c4-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dd4c4-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd4c4-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd4c4-143">INPUTS</span></span>

### <span data-ttu-id="dd4c4-144">Brak</span><span class="sxs-lookup"><span data-stu-id="dd4c4-144">None</span></span>

## <span data-ttu-id="dd4c4-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd4c4-145">OUTPUTS</span></span>

### <span data-ttu-id="dd4c4-146">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="dd4c4-146">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="dd4c4-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dd4c4-147">NOTES</span></span>

## <span data-ttu-id="dd4c4-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dd4c4-148">RELATED LINKS</span></span>

[<span data-ttu-id="dd4c4-149">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="dd4c4-149">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="dd4c4-150">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="dd4c4-150">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="dd4c4-151">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="dd4c4-151">Remove-AzPrivateDnsVirtualNetworkLink</span></span>](./Remove-AzPrivateDnsVirtualNetworkLink.md)
