---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: https://docs.microsoft.com/powershell/module/az.dns/set-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsZone.md
ms.openlocfilehash: d1b5fb606262b680d4e83f9c8e0a9ea166070ed4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984698"
---
# <span data-ttu-id="dc6bd-101">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="dc6bd-101">Set-AzDnsZone</span></span>

## <span data-ttu-id="dc6bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc6bd-102">SYNOPSIS</span></span>
<span data-ttu-id="dc6bd-103">Aktualizuje właściwości strefy DNS.</span><span class="sxs-lookup"><span data-stu-id="dc6bd-103">Updates the properties of a DNS zone.</span></span>

## <span data-ttu-id="dc6bd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dc6bd-104">SYNTAX</span></span>

### <span data-ttu-id="dc6bd-105">Pola (domyślne)</span><span class="sxs-lookup"><span data-stu-id="dc6bd-105">Fields (Default)</span></span>
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc6bd-106">FieldsObjects</span><span class="sxs-lookup"><span data-stu-id="dc6bd-106">FieldsObjects</span></span>
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc6bd-107">Obiekt</span><span class="sxs-lookup"><span data-stu-id="dc6bd-107">Object</span></span>
```
Set-AzDnsZone -Zone <DnsZone> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dc6bd-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="dc6bd-108">DESCRIPTION</span></span>
<span data-ttu-id="dc6bd-109">Polecenie **cmdlet Set-AzDnsZone** aktualizuje określoną strefę DNS w usłudze Azure DNS.</span><span class="sxs-lookup"><span data-stu-id="dc6bd-109">The **Set-AzDnsZone** cmdlet updates the specified DNS zone in the Azure DNS service.</span></span>
<span data-ttu-id="dc6bd-110">To polecenie cmdlet nie aktualizuje zestawów rekordów w strefie.</span><span class="sxs-lookup"><span data-stu-id="dc6bd-110">This cmdlet does not update the record sets in the zone.</span></span>
<span data-ttu-id="dc6bd-111">Obiekt **DnsZone** można przekazać jako parametr lub za pomocą operatora potoku albo określić parametry *ZoneName* (Nazwa_strefy) i *ResourceGroupName* (Nazwa Grupy Zasobów).</span><span class="sxs-lookup"><span data-stu-id="dc6bd-111">You can pass a **DnsZone** object as a parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="dc6bd-112">Możesz użyć *parametru Confirm* i $ConfirmPreference zmienną programu Windows PowerShell, aby określić, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="dc6bd-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="dc6bd-113">Podczas przekazywania strefy DNS jako obiektu (przy użyciu obiektu Zone lub przez potok) nie jest ona aktualizowana, jeśli została zmieniona w systemie Azure DNS od czasu pobrania lokalnego obiektu DnsZone.</span><span class="sxs-lookup"><span data-stu-id="dc6bd-113">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="dc6bd-114">Zapewnia to ochronę w przypadku jednoczesnych zmian.</span><span class="sxs-lookup"><span data-stu-id="dc6bd-114">This provides protection for concurrent changes.</span></span> <span data-ttu-id="dc6bd-115">To zachowanie można pominąć za pomocą *parametru Zastąp,* który aktualizuje strefę niezależnie od jednoczesnych zmian.</span><span class="sxs-lookup"><span data-stu-id="dc6bd-115">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="dc6bd-116">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dc6bd-116">EXAMPLES</span></span>

### <span data-ttu-id="dc6bd-117">Przykład 1. Aktualizowanie strefy DNS</span><span class="sxs-lookup"><span data-stu-id="dc6bd-117">Example 1: Update a DNS zone</span></span>
```
PS C:\>$Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzDnsZone -Zone $Zone
```

<span data-ttu-id="dc6bd-118">Pierwsze polecenie pobiera strefę o nazwie myzone.com z określonej grupy zasobów, a następnie zapisuje ją w $Zone zmienną.</span><span class="sxs-lookup"><span data-stu-id="dc6bd-118">The first command gets the zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>
<span data-ttu-id="dc6bd-119">Drugie polecenie aktualizuje tagi dla $Zone.</span><span class="sxs-lookup"><span data-stu-id="dc6bd-119">The second command updates the tags for $Zone.</span></span>
<span data-ttu-id="dc6bd-120">Ostatnie polecenie zatwierdza zmianę.</span><span class="sxs-lookup"><span data-stu-id="dc6bd-120">The final command commits the change.</span></span>

### <span data-ttu-id="dc6bd-121">Przykład 2. Aktualizowanie tagów dla strefy</span><span class="sxs-lookup"><span data-stu-id="dc6bd-121">Example 2: Update tags for a zone</span></span>
```
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

<span data-ttu-id="dc6bd-122">To polecenie aktualizuje tagi dla strefy o nazwie myzone.com bez uprzedniego jawnego uzyskania strefy.</span><span class="sxs-lookup"><span data-stu-id="dc6bd-122">This command updates the tags for the zone named myzone.com without first explicitly getting the zone.</span></span>

### <span data-ttu-id="dc6bd-123">Przykład 3. Kojarzenie strefy prywatnej z siecią wirtualną przez podanie jej identyfikatora</span><span class="sxs-lookup"><span data-stu-id="dc6bd-123">Example 3: Associating a private zone with a virtual network by specifying its ID</span></span>
```
PS C:\>$vnet = Get-AzVirtualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetworkId @($vnet.Id)
```

<span data-ttu-id="dc6bd-124">To polecenie skojarzy prywatną strefę DNS myprivatezone.com z siecią wirtualną Myvnet jako siecią rejestracji, określając jej identyfikator.</span><span class="sxs-lookup"><span data-stu-id="dc6bd-124">This command associates the Private DNS zone myprivatezone.com with the virtual network myvnet as a registration network by specifying its ID.</span></span>

### <span data-ttu-id="dc6bd-125">Przykład 4. Kojarzenie strefy prywatnej z siecią wirtualną przez określenie obiektu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="dc6bd-125">Example 4: Associating a private zone with a virtual network by specifying the network object.</span></span>
```
PS C:\>$vnet = Get-AzVirtualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetwork @($vnet)
```

<span data-ttu-id="dc6bd-126">To polecenie kojarzy prywatną strefę DNS myprivatezone.com z siecią wirtualną Myvnet jako siecią rejestracji, przechodząc do polecenia cmdlet sieci wirtualnej reprezentowanej przez zmienną $vnet do Set-AzDnsZone cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc6bd-126">This command associates the Private DNS zone myprivatezone.com with the virtual network myvnet as a registration network by passing the virtual network object represented by $vnet variable to the Set-AzDnsZone cmdlet.</span></span>

## <span data-ttu-id="dc6bd-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc6bd-127">PARAMETERS</span></span>

### <span data-ttu-id="dc6bd-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc6bd-128">-DefaultProfile</span></span>
<span data-ttu-id="dc6bd-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="dc6bd-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dc6bd-130">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="dc6bd-130">-Name</span></span>
<span data-ttu-id="dc6bd-131">Określa nazwę strefy DNS do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="dc6bd-131">Specifies the name of the DNS zone to update.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, FieldsObjects
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc6bd-132">— Zastąp</span><span class="sxs-lookup"><span data-stu-id="dc6bd-132">-Overwrite</span></span>
<span data-ttu-id="dc6bd-133">Podczas przekazywania strefy DNS jako obiektu (przy użyciu obiektu Zone lub przez potok) nie jest ona aktualizowana, jeśli została zmieniona w systemie Azure DNS od czasu pobrania lokalnego obiektu DnsZone.</span><span class="sxs-lookup"><span data-stu-id="dc6bd-133">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="dc6bd-134">Zapewnia to ochronę w przypadku jednoczesnych zmian.</span><span class="sxs-lookup"><span data-stu-id="dc6bd-134">This provides protection for concurrent changes.</span></span> <span data-ttu-id="dc6bd-135">To zachowanie można pominąć za pomocą *parametru Zastąp,* który aktualizuje strefę niezależnie od jednoczesnych zmian.</span><span class="sxs-lookup"><span data-stu-id="dc6bd-135">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="dc6bd-136">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="dc6bd-136">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="dc6bd-137">Lista sieci wirtualnych, które będą rejestrować rekordy nazw hostów maszyn wirtualnych w tej strefie DNS, dostępna tylko dla stref prywatnych.</span><span class="sxs-lookup"><span data-stu-id="dc6bd-137">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: FieldsObjects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc6bd-138">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="dc6bd-138">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="dc6bd-139">Lista identyfikatorów sieci wirtualnej, które będą rejestrować rekordy nazw hostów maszyn wirtualnych w tej strefie DNS, która jest dostępna tylko dla stref prywatnych.</span><span class="sxs-lookup"><span data-stu-id="dc6bd-139">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc6bd-140">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="dc6bd-140">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="dc6bd-141">Lista sieci wirtualnych, które mogą rozwiązując rekordy w tej strefie DNS, dostępna tylko dla stref prywatnych.</span><span class="sxs-lookup"><span data-stu-id="dc6bd-141">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: FieldsObjects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc6bd-142">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="dc6bd-142">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="dc6bd-143">Lista identyfikatorów sieci wirtualnych, które mogą rozstrzygić rekordy w tej strefie DNS, dostępna tylko dla stref prywatnych.</span><span class="sxs-lookup"><span data-stu-id="dc6bd-143">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc6bd-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc6bd-144">-ResourceGroupName</span></span>
<span data-ttu-id="dc6bd-145">Określa nazwę grupy zasobów zawierającej strefę do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="dc6bd-145">Specifies the name of the resource group that contains the zone to update.</span></span>
<span data-ttu-id="dc6bd-146">Musisz także określić parametr ZoneName.</span><span class="sxs-lookup"><span data-stu-id="dc6bd-146">You must also specify the ZoneName parameter.</span></span>
<span data-ttu-id="dc6bd-147">Można również określić strefę przy użyciu obiektu DnsZone z *parametrem Zone* lub potokiem.</span><span class="sxs-lookup"><span data-stu-id="dc6bd-147">Alternatively, you can specify the zone using a DnsZone object with the *Zone* parameter or the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, FieldsObjects
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc6bd-148">— Tag</span><span class="sxs-lookup"><span data-stu-id="dc6bd-148">-Tag</span></span>
<span data-ttu-id="dc6bd-149">Pary klucz-wartość w postaci tabeli skrótu.</span><span class="sxs-lookup"><span data-stu-id="dc6bd-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="dc6bd-150">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="dc6bd-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Fields, FieldsObjects
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc6bd-151">— Strefa</span><span class="sxs-lookup"><span data-stu-id="dc6bd-151">-Zone</span></span>
<span data-ttu-id="dc6bd-152">Określa strefę DNS do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="dc6bd-152">Specifies the DNS zone to update.</span></span>
<span data-ttu-id="dc6bd-153">Można również określić strefę przy użyciu parametrów *Nazwa_strefy* i *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="dc6bd-153">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc6bd-154">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dc6bd-154">-Confirm</span></span>
<span data-ttu-id="dc6bd-155">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="dc6bd-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc6bd-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc6bd-156">-WhatIf</span></span>
<span data-ttu-id="dc6bd-157">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc6bd-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dc6bd-158">Polecenie cmdlet nie zostanie uruchomione. Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc6bd-158">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dc6bd-159">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="dc6bd-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc6bd-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc6bd-160">CommonParameters</span></span>
<span data-ttu-id="dc6bd-161">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc6bd-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc6bd-162">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc6bd-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc6bd-163">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dc6bd-163">INPUTS</span></span>

### <span data-ttu-id="dc6bd-164">System.String</span><span class="sxs-lookup"><span data-stu-id="dc6bd-164">System.String</span></span>

### <span data-ttu-id="dc6bd-165">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="dc6bd-165">System.Collections.Hashtable</span></span>

### <span data-ttu-id="dc6bd-166">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="dc6bd-166">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="dc6bd-167">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="dc6bd-167">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="dc6bd-168">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="dc6bd-168">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="dc6bd-169">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dc6bd-169">OUTPUTS</span></span>

### <span data-ttu-id="dc6bd-170">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="dc6bd-170">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="dc6bd-171">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dc6bd-171">NOTES</span></span>
<span data-ttu-id="dc6bd-172">Za pomocą *parametru Confirm* można określić, czy to polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="dc6bd-172">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="dc6bd-173">Domyślnie polecenie cmdlet wyświetla monit o potwierdzenie, jeśli zmienna programu Windows PowerShell $ConfirmPreference wartość średnią lub niższą.</span><span class="sxs-lookup"><span data-stu-id="dc6bd-173">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="dc6bd-174">Jeśli określisz *potwierdź* *lub potwierdź:$True,* to polecenie cmdlet wyświetli monit o potwierdzenie przed jego rozpoczęciem.</span><span class="sxs-lookup"><span data-stu-id="dc6bd-174">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="dc6bd-175">Jeśli określisz *polecenie Potwierdź:$False,* polecenie cmdlet nie wyświetli monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="dc6bd-175">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="dc6bd-176">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dc6bd-176">RELATED LINKS</span></span>

[<span data-ttu-id="dc6bd-177">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="dc6bd-177">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="dc6bd-178">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="dc6bd-178">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="dc6bd-179">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="dc6bd-179">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)
