---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsVirtualNetworkLink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 3ffcc30dc0291be06c27ee53ee0ee7ea14f3e2c1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179018"
---
# <span data-ttu-id="d8104-101">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="d8104-101">Set-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="d8104-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8104-102">SYNOPSIS</span></span>
<span data-ttu-id="d8104-103">Aktualizuje/ustawia link sieci wirtualnej skojarzony ze strefą prywatną i grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="d8104-103">Updates/Sets a virtual network link associated with a private zone and a resource group.</span></span>

## <span data-ttu-id="d8104-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d8104-104">SYNTAX</span></span>

### <span data-ttu-id="d8104-105">Pola (domyślne)</span><span class="sxs-lookup"><span data-stu-id="d8104-105">Fields (Default)</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8104-106">Obiekt</span><span class="sxs-lookup"><span data-stu-id="d8104-106">Object</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-Overwrite] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8104-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8104-107">ResourceId</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8104-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d8104-108">DESCRIPTION</span></span>
<span data-ttu-id="d8104-109">Polecenie **cmdlet Set-AzPrivateDnsVirtualNetworkLink** aktualizuje link skojarzony ze strefą z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d8104-109">The **Set-AzPrivateDnsVirtualNetworkLink** cmdlet updates a link associated with a zone from a specified resource group.</span></span>
<span data-ttu-id="d8104-110">Obiekt **PSPrivateDnsVirtualNetworkLink** można przekazać za pomocą *parametru Link* lub operatora potoku   albo określić parametry Nazwa Strefy i *NazwaGrupy* Zasobów.</span><span class="sxs-lookup"><span data-stu-id="d8104-110">You can pass a **PSPrivateDnsVirtualNetworkLink** object using the *Link* parameter or by using the pipeline operator, or alternatively you can specify the *Name* *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="d8104-111">Możesz użyć parametru Confirm i $ConfirmPreference zmienną programu Windows PowerShell, aby określić, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d8104-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="d8104-112">Podczas określania strefy za pomocą obiektu **PSPrivateDnsVirtualNetworkLink**  (przekazywanego za pośrednictwem parametru potoku lub linku) link nie jest aktualizowany, jeśli został zmieniony w usłudze Azure DNS od czasu pobrania lokalnego obiektu **PSPrivateDnsVirtualNetworkLink.**</span><span class="sxs-lookup"><span data-stu-id="d8104-112">When specifying the zone using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not updated if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span> <span data-ttu-id="d8104-113">Zapewnia to ochronę przed jednoczesnymi zmianami łączy.</span><span class="sxs-lookup"><span data-stu-id="d8104-113">This provides protection for concurrent link changes.</span></span> <span data-ttu-id="d8104-114">Można to pominąć przy użyciu *parametru Zastąp,* który aktualizuje link niezależnie od jednoczesnych zmian.</span><span class="sxs-lookup"><span data-stu-id="d8104-114">This can be suppressed using the *Overwrite* parameter, which updates the link regardless of concurrent changes.</span></span>

## <span data-ttu-id="d8104-115">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d8104-115">EXAMPLES</span></span>

### <span data-ttu-id="d8104-116">Przykład 1. Ustawianie linku</span><span class="sxs-lookup"><span data-stu-id="d8104-116">Example 1: Set a link</span></span>
```
PS C:\>Set-AzPrivateDnsVirtualNetworkLink -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Name "mylink" -Tag @{} -IsRegistrationEnabled $true

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

<span data-ttu-id="d8104-117">To polecenie ustawia wartość IsRegistrationEnabled na Prawda dla linku o nazwie mylink, połączonego ze strefą o nazwie myzone.com z grupy zasobów o nazwie MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d8104-117">This command sets IsRegistrationEnabled to True for the link named mylink, linked to zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="d8104-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8104-118">PARAMETERS</span></span>

### <span data-ttu-id="d8104-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8104-119">-DefaultProfile</span></span>
<span data-ttu-id="d8104-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="d8104-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8104-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8104-121">-InputObject</span></span>
<span data-ttu-id="d8104-122">Obiekt łącza sieci wirtualnej, który należy ustawić.</span><span class="sxs-lookup"><span data-stu-id="d8104-122">The virtual network link object to set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8104-123">-IsRegistrationEnabled</span><span class="sxs-lookup"><span data-stu-id="d8104-123">-IsRegistrationEnabled</span></span>
<span data-ttu-id="d8104-124">Wartość logiczna reprezentująca, jeśli rejestracja jest włączona w linku sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d8104-124">Boolean that represents if registration is enabled on the virtual network link.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8104-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d8104-125">-Name</span></span>
<span data-ttu-id="d8104-126">Określa nazwę łącza, które usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8104-126">Specifies the name of the link that this cmdlet removes.</span></span>
<span data-ttu-id="d8104-127">Musisz także określić parametr *ResourceGroupName* i *ZoneName.*</span><span class="sxs-lookup"><span data-stu-id="d8104-127">You must also specify the *ResourceGroupName* and *ZoneName* parameter.</span></span>
<span data-ttu-id="d8104-128">Możesz również określić prywatny link DNS, używając *parametru linku.*</span><span class="sxs-lookup"><span data-stu-id="d8104-128">Alternatively, you can specify the private DNS link using the *link* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8104-129">— Zastąp</span><span class="sxs-lookup"><span data-stu-id="d8104-129">-Overwrite</span></span>
<span data-ttu-id="d8104-130">Podczas określania linku przy użyciu obiektu **PSPrivateDnsVirtualNetworkLink** (przekazywanego za pośrednictwem potoku lub parametru *Link)* link nie jest usuwany, jeśli został zmieniony w usłudze Azure DNS od czasu pobrania lokalnego obiektu **PSPrivateDnsVirtualNetworkLink.**</span><span class="sxs-lookup"><span data-stu-id="d8104-130">When specifying the link using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not deleted if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span>
<span data-ttu-id="d8104-131">Zapewnia to ochronę przed jednoczesnymi zmianami łączy.</span><span class="sxs-lookup"><span data-stu-id="d8104-131">This provides protection for concurrent link changes.</span></span>
<span data-ttu-id="d8104-132">Można to pominąć przy użyciu *parametru Zastąp,* który usuwa link niezależnie od jednoczesnych zmian.</span><span class="sxs-lookup"><span data-stu-id="d8104-132">This can be suppressed using the *Overwrite* parameter, which deletes the link regardless of concurrent changes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8104-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8104-133">-ResourceGroupName</span></span>
<span data-ttu-id="d8104-134">Określa nazwę grupy zasobów zawierającej link do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="d8104-134">Specifies the name of the resource group that contains the link to remove.</span></span>
<span data-ttu-id="d8104-135">Musisz także określić parametr *ZoneName (Nazwa* *strefy) i Name (Nazwa).*</span><span class="sxs-lookup"><span data-stu-id="d8104-135">You must also specify the *ZoneName* and *Name* parameter.</span></span>
<span data-ttu-id="d8104-136">Alternatywnie możesz określić wirtualny link sieciowy przy użyciu obiektu **PSPrivateDnsVirtualNetworkLink** przekazywanego za pośrednictwem potoku lub *parametru Link.*</span><span class="sxs-lookup"><span data-stu-id="d8104-136">Alternatively, you can specify the virtual network link using a **PSPrivateDnsVirtualNetworkLink** object, passed via either the pipeline or the *Link* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8104-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8104-137">-ResourceId</span></span>
<span data-ttu-id="d8104-138">Private DNS Zone ResourceID (Prywatny adres DNS Strefy ResourceID).</span><span class="sxs-lookup"><span data-stu-id="d8104-138">Private DNS Zone ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8104-139">— Tag</span><span class="sxs-lookup"><span data-stu-id="d8104-139">-Tag</span></span>
<span data-ttu-id="d8104-140">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="d8104-140">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="d8104-141">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="d8104-141">-ZoneName</span></span>
<span data-ttu-id="d8104-142">Określa nazwę strefy DNS, która jest usuwana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8104-142">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="d8104-143">Musisz także określić parametr *Name (Nazwa) i* *ResourceGroupName (Nazwa grupy zasobów).*</span><span class="sxs-lookup"><span data-stu-id="d8104-143">You must also specify the *Name* and *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="d8104-144">Możesz również określić prywatny link DNS, używając *parametru linku.*</span><span class="sxs-lookup"><span data-stu-id="d8104-144">Alternatively, you can specify the private DNS link using the *link* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8104-145">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d8104-145">-Confirm</span></span>
<span data-ttu-id="d8104-146">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d8104-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8104-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8104-147">-WhatIf</span></span>
<span data-ttu-id="d8104-148">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8104-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8104-149">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d8104-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8104-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8104-150">CommonParameters</span></span>
<span data-ttu-id="d8104-151">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8104-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8104-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8104-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8104-153">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8104-153">INPUTS</span></span>

### <span data-ttu-id="d8104-154">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="d8104-154">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

### <span data-ttu-id="d8104-155">System.String</span><span class="sxs-lookup"><span data-stu-id="d8104-155">System.String</span></span>

## <span data-ttu-id="d8104-156">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d8104-156">OUTPUTS</span></span>

### <span data-ttu-id="d8104-157">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="d8104-157">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="d8104-158">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d8104-158">NOTES</span></span>

## <span data-ttu-id="d8104-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d8104-159">RELATED LINKS</span></span>

[<span data-ttu-id="d8104-160">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="d8104-160">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="d8104-161">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="d8104-161">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="d8104-162">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="d8104-162">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)
