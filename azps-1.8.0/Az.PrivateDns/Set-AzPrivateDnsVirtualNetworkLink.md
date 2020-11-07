---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsVirtualNetworkLink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: d2d00df48cbaf4bff1d6e9dac648004d73e65f2c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708732"
---
# <span data-ttu-id="a9e2b-101">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="a9e2b-101">Set-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="a9e2b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a9e2b-102">SYNOPSIS</span></span>
<span data-ttu-id="a9e2b-103">Updates/ustawia łącze sieci wirtualnej skojarzone z prywatną strefą i grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="a9e2b-103">Updates/Sets a virtual network link associated with a private zone and a resource group.</span></span>

## <span data-ttu-id="a9e2b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a9e2b-104">SYNTAX</span></span>

### <span data-ttu-id="a9e2b-105">Pola (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="a9e2b-105">Fields (Default)</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9e2b-106">Stream</span><span class="sxs-lookup"><span data-stu-id="a9e2b-106">Object</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink>
 [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>] [-Overwrite] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9e2b-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="a9e2b-107">ResourceId</span></span>
```
Set-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-IsRegistrationEnabled <Boolean>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9e2b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a9e2b-108">DESCRIPTION</span></span>
<span data-ttu-id="a9e2b-109">Polecenie cmdlet **Set-AzPrivateDnsVirtualNetworkLink** umożliwia zaktualizowanie linku skojarzonego z strefą z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a9e2b-109">The **Set-AzPrivateDnsVirtualNetworkLink** cmdlet updates a link associated with a zone from a specified resource group.</span></span>
<span data-ttu-id="a9e2b-110">Obiekt **PSPrivateDnsVirtualNetworkLink** można przekazać przy użyciu parametru *link* lub za pomocą operatora potoku lub można też określić parametry *name (nazwa* *strefy* ) i *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="a9e2b-110">You can pass a **PSPrivateDnsVirtualNetworkLink** object using the *Link* parameter or by using the pipeline operator, or alternatively you can specify the *Name* *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="a9e2b-111">Za pomocą zmiennej Confirm i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a9e2b-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="a9e2b-112">Podczas określania strefy za pomocą obiektu **PSPrivateDnsVirtualNetworkLink** (przekazywanego za pośrednictwem parametru rurociągu lub *linku* ) link nie jest aktualizowany, jeśli został zmieniony w usłudze DNS Azure, ponieważ został pobrany lokalny obiekt **PSPrivateDnsVirtualNetworkLink** .</span><span class="sxs-lookup"><span data-stu-id="a9e2b-112">When specifying the zone using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not updated if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span> <span data-ttu-id="a9e2b-113">Zapewnia to ochronę współbieżnych zmian łączy.</span><span class="sxs-lookup"><span data-stu-id="a9e2b-113">This provides protection for concurrent link changes.</span></span> <span data-ttu-id="a9e2b-114">Można to pominąć za pomocą parametru *overwrite* , co powoduje zaktualizowanie linku bez względu na jednoczesne zmiany.</span><span class="sxs-lookup"><span data-stu-id="a9e2b-114">This can be suppressed using the *Overwrite* parameter, which updates the link regardless of concurrent changes.</span></span>

## <span data-ttu-id="a9e2b-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a9e2b-115">EXAMPLES</span></span>

### <span data-ttu-id="a9e2b-116">Przykład 1: Ustawianie linku</span><span class="sxs-lookup"><span data-stu-id="a9e2b-116">Example 1: Set a link</span></span>
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

<span data-ttu-id="a9e2b-117">To polecenie ustawia IsRegistrationEnabled na wartość true dla linku o nazwie Moja link, połączonego z strefą o nazwie myzone.com z grupy zasobów o nazwie Moja zasobów.</span><span class="sxs-lookup"><span data-stu-id="a9e2b-117">This command sets IsRegistrationEnabled to True for the link named mylink, linked to zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="a9e2b-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a9e2b-118">PARAMETERS</span></span>

### <span data-ttu-id="a9e2b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9e2b-119">-DefaultProfile</span></span>
<span data-ttu-id="a9e2b-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a9e2b-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9e2b-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a9e2b-121">-InputObject</span></span>
<span data-ttu-id="a9e2b-122">Obiekt link sieci wirtualnej do ustawienia.</span><span class="sxs-lookup"><span data-stu-id="a9e2b-122">The virtual network link object to set.</span></span>

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

### <span data-ttu-id="a9e2b-123">-IsRegistrationEnabled</span><span class="sxs-lookup"><span data-stu-id="a9e2b-123">-IsRegistrationEnabled</span></span>
<span data-ttu-id="a9e2b-124">Wartość logiczna określająca, czy rejestracja jest włączona w łączu sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a9e2b-124">Boolean that represents if registration is enabled on the virtual network link.</span></span>

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

### <span data-ttu-id="a9e2b-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a9e2b-125">-Name</span></span>
<span data-ttu-id="a9e2b-126">Określa nazwę linku usuniętego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9e2b-126">Specifies the name of the link that this cmdlet removes.</span></span>
<span data-ttu-id="a9e2b-127">Musisz również określić parametr *ResourceGroupName* oraz *zonename* .</span><span class="sxs-lookup"><span data-stu-id="a9e2b-127">You must also specify the *ResourceGroupName* and *ZoneName* parameter.</span></span>
<span data-ttu-id="a9e2b-128">Możesz też określić prywatne łącze DNS przy użyciu parametru *link* .</span><span class="sxs-lookup"><span data-stu-id="a9e2b-128">Alternatively, you can specify the private DNS link using the *link* parameter.</span></span>

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

### <span data-ttu-id="a9e2b-129">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="a9e2b-129">-Overwrite</span></span>
<span data-ttu-id="a9e2b-130">Podczas określania linku przy użyciu obiektu **PSPrivateDnsVirtualNetworkLink** (przekazywanego za pośrednictwem parametru rurociągu lub *linku* ) link nie jest usuwany, jeśli został zmieniony w usłudze DNS Azure, ponieważ został pobrany lokalny obiekt **PSPrivateDnsVirtualNetworkLink** .</span><span class="sxs-lookup"><span data-stu-id="a9e2b-130">When specifying the link using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not deleted if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span>
<span data-ttu-id="a9e2b-131">Zapewnia to ochronę współbieżnych zmian łączy.</span><span class="sxs-lookup"><span data-stu-id="a9e2b-131">This provides protection for concurrent link changes.</span></span>
<span data-ttu-id="a9e2b-132">Można to pominąć za pomocą parametru *overwrite* , który usuwa łącze bez względu na jednoczesne zmiany.</span><span class="sxs-lookup"><span data-stu-id="a9e2b-132">This can be suppressed using the *Overwrite* parameter, which deletes the link regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="a9e2b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9e2b-133">-ResourceGroupName</span></span>
<span data-ttu-id="a9e2b-134">Określa nazwę grupy zasobów zawierającej łącze do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="a9e2b-134">Specifies the name of the resource group that contains the link to remove.</span></span>
<span data-ttu-id="a9e2b-135">Należy również określić parametr *zonename* i *name* .</span><span class="sxs-lookup"><span data-stu-id="a9e2b-135">You must also specify the *ZoneName* and *Name* parameter.</span></span>
<span data-ttu-id="a9e2b-136">Możesz też określić łącze sieci wirtualnej za pomocą obiektu **PSPrivateDnsVirtualNetworkLink** , przechodzą za pośrednictwem rurociągu lub parametru *link* .</span><span class="sxs-lookup"><span data-stu-id="a9e2b-136">Alternatively, you can specify the virtual network link using a **PSPrivateDnsVirtualNetworkLink** object, passed via either the pipeline or the *Link* parameter.</span></span>

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

### <span data-ttu-id="a9e2b-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9e2b-137">-ResourceId</span></span>
<span data-ttu-id="a9e2b-138">Identyfikator zasobu prywatnej strefy DNS.</span><span class="sxs-lookup"><span data-stu-id="a9e2b-138">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="a9e2b-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="a9e2b-139">-Tag</span></span>
<span data-ttu-id="a9e2b-140">Tabela skrótów reprezentująca znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="a9e2b-140">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="a9e2b-141">-Nazwa_strefy</span><span class="sxs-lookup"><span data-stu-id="a9e2b-141">-ZoneName</span></span>
<span data-ttu-id="a9e2b-142">Określa nazwę strefy DNS, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9e2b-142">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="a9e2b-143">Musisz również określić *nazwę* i parametr *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="a9e2b-143">You must also specify the *Name* and *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="a9e2b-144">Możesz też określić prywatne łącze DNS przy użyciu parametru *link* .</span><span class="sxs-lookup"><span data-stu-id="a9e2b-144">Alternatively, you can specify the private DNS link using the *link* parameter.</span></span>

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

### <span data-ttu-id="a9e2b-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a9e2b-145">-Confirm</span></span>
<span data-ttu-id="a9e2b-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9e2b-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9e2b-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9e2b-147">-WhatIf</span></span>
<span data-ttu-id="a9e2b-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9e2b-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9e2b-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a9e2b-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9e2b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9e2b-150">CommonParameters</span></span>
<span data-ttu-id="a9e2b-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9e2b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9e2b-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9e2b-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9e2b-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9e2b-153">INPUTS</span></span>

### <span data-ttu-id="a9e2b-154">Microsoft. Azure. Commands. PrivateDns. models. PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="a9e2b-154">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

### <span data-ttu-id="a9e2b-155">System. String</span><span class="sxs-lookup"><span data-stu-id="a9e2b-155">System.String</span></span>

## <span data-ttu-id="a9e2b-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a9e2b-156">OUTPUTS</span></span>

### <span data-ttu-id="a9e2b-157">Microsoft. Azure. Commands. PrivateDns. models. PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="a9e2b-157">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="a9e2b-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a9e2b-158">NOTES</span></span>

## <span data-ttu-id="a9e2b-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9e2b-159">RELATED LINKS</span></span>

[<span data-ttu-id="a9e2b-160">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="a9e2b-160">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="a9e2b-161">Nowe — AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="a9e2b-161">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="a9e2b-162">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="a9e2b-162">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)
