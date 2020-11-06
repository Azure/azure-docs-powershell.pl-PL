---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/set-azurermdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsZone.md
ms.openlocfilehash: da504f6b8110335e6297d0c7efb2a1a27106e0e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526829"
---
# <span data-ttu-id="a905c-101">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="a905c-101">Set-AzureRmDnsZone</span></span>

## <span data-ttu-id="a905c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a905c-102">SYNOPSIS</span></span>
<span data-ttu-id="a905c-103">Aktualizuje właściwości strefy DNS.</span><span class="sxs-lookup"><span data-stu-id="a905c-103">Updates the properties of a DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a905c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a905c-104">SYNTAX</span></span>

### <span data-ttu-id="a905c-105">Pola (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="a905c-105">Fields (Default)</span></span>
```
Set-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a905c-106">FieldsObjects</span><span class="sxs-lookup"><span data-stu-id="a905c-106">FieldsObjects</span></span>
```
Set-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a905c-107">Stream</span><span class="sxs-lookup"><span data-stu-id="a905c-107">Object</span></span>
```
Set-AzureRmDnsZone -Zone <DnsZone> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a905c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a905c-108">DESCRIPTION</span></span>
<span data-ttu-id="a905c-109">Polecenie cmdlet **Set-AzureRmDnsZone** aktualizuje określoną strefę DNS w usłudze DNS Azure.</span><span class="sxs-lookup"><span data-stu-id="a905c-109">The **Set-AzureRmDnsZone** cmdlet updates the specified DNS zone in the Azure DNS service.</span></span>
<span data-ttu-id="a905c-110">To polecenie cmdlet nie powoduje zaktualizowania zestawów rekordów w strefie.</span><span class="sxs-lookup"><span data-stu-id="a905c-110">This cmdlet does not update the record sets in the zone.</span></span>

<span data-ttu-id="a905c-111">Obiekt **dnsZone** można przekazać jako parametr lub za pomocą operatora potoku albo też można określić parametry *zonename* i *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="a905c-111">You can pass a **DnsZone** object as a parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="a905c-112">Za pomocą zmiennej *Confirm* i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a905c-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="a905c-113">Gdy przepuszczasz strefę DNS jako obiekt (za pomocą obiektu Zone lub za pośrednictwem rurociągu), nie zostanie ona zaktualizowana, jeśli została ona zmieniona w usłudze DNS Azure, ponieważ został pobrany lokalny obiekt DnsZone.</span><span class="sxs-lookup"><span data-stu-id="a905c-113">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="a905c-114">Zapewnia to ochronę współbieżnych zmian.</span><span class="sxs-lookup"><span data-stu-id="a905c-114">This provides protection for concurrent changes.</span></span> <span data-ttu-id="a905c-115">Możesz pominąć to zachowanie przy użyciu parametru *overwrite* , który aktualizuje strefę bez względu na współbieżne zmiany.</span><span class="sxs-lookup"><span data-stu-id="a905c-115">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="a905c-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a905c-116">EXAMPLES</span></span>

### <span data-ttu-id="a905c-117">Przykład 1: aktualizowanie strefy DNS</span><span class="sxs-lookup"><span data-stu-id="a905c-117">Example 1: Update a DNS zone</span></span>
```
PS C:\>$Zone = Get-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzureRmDnsZone -Zone $Zone
```

<span data-ttu-id="a905c-118">Pierwsze polecenie pobiera strefę o nazwie myzone.com z określonej grupy zasobów, a następnie zapisuje ją w zmiennej $Zone.</span><span class="sxs-lookup"><span data-stu-id="a905c-118">The first command gets the zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

<span data-ttu-id="a905c-119">Drugie polecenie aktualizuje znaczniki $Zone.</span><span class="sxs-lookup"><span data-stu-id="a905c-119">The second command updates the tags for $Zone.</span></span>

<span data-ttu-id="a905c-120">Polecenie ostatnie zatwierdza zmianę.</span><span class="sxs-lookup"><span data-stu-id="a905c-120">The final command commits the change.</span></span>

### <span data-ttu-id="a905c-121">Przykład 2: aktualizowanie znaczników dla strefy</span><span class="sxs-lookup"><span data-stu-id="a905c-121">Example 2: Update tags for a zone</span></span>
```
PS C:\>Set-AzureRmDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

<span data-ttu-id="a905c-122">To polecenie aktualizuje znaczniki strefy o nazwie myzone.com bez uprzedniego uzyskania tej strefy.</span><span class="sxs-lookup"><span data-stu-id="a905c-122">This command updates the tags for the zone named myzone.com without first explicitly getting the zone.</span></span>

### <span data-ttu-id="a905c-123">Przykład 3: Kojarzenie strefy prywatnej z siecią wirtualną przez określenie jej identyfikatora</span><span class="sxs-lookup"><span data-stu-id="a905c-123">Example 3: Associating a private zone with a virtual network by specifying its ID</span></span>
```
PS C:\>$vnet = Get-AzureRmVirualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzureRmDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetworkId @($vnet.Id)
```

<span data-ttu-id="a905c-124">To polecenie kojarzy prywatną strefę DNS myprivatezone.com z myvnet sieci wirtualnej jako siecią rejestracji, określając jej identyfikator.</span><span class="sxs-lookup"><span data-stu-id="a905c-124">This command associates the Private DNS zone myprivatezone.com with the virtual network myvnet as a registration network by specifying its ID.</span></span>

### <span data-ttu-id="a905c-125">Przykład 4: Kojarzenie strefy prywatnej z siecią wirtualną przez określenie obiektu sieci.</span><span class="sxs-lookup"><span data-stu-id="a905c-125">Example 4: Associating a private zone with a virtual network by specifying the network object.</span></span>
```
PS C:\>$vnet = Get-AzureRmVirualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzureRmDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetwork @($vnet)
```

<span data-ttu-id="a905c-126">To polecenie kojarzy prywatną strefę DNS myprivatezone.com z myvnet sieci wirtualnej jako siecią rejestracji, przechodząc do obiektu sieci wirtualnej reprezentowanego przez zmienną $vnet za pomocą polecenia cmdlet Set-AzureRmDnsZone.</span><span class="sxs-lookup"><span data-stu-id="a905c-126">This command associates the Private DNS zone myprivatezone.com with the virtual network myvnet as a registration network by passing the virtual network object represented by $vnet variable to the Set-AzureRmDnsZone cmdlet.</span></span>

## <span data-ttu-id="a905c-127">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a905c-127">PARAMETERS</span></span>

### <span data-ttu-id="a905c-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a905c-128">-DefaultProfile</span></span>
<span data-ttu-id="a905c-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a905c-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a905c-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a905c-130">-Name</span></span>
<span data-ttu-id="a905c-131">Określa nazwę strefy DNS do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="a905c-131">Specifies the name of the DNS zone to update.</span></span>

```yaml
Type: String
Parameter Sets: Fields, FieldsObjects
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a905c-132">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="a905c-132">-Overwrite</span></span>
<span data-ttu-id="a905c-133">Gdy przepuszczasz strefę DNS jako obiekt (za pomocą obiektu Zone lub za pośrednictwem rurociągu), nie zostanie ona zaktualizowana, jeśli została ona zmieniona w usłudze DNS Azure, ponieważ został pobrany lokalny obiekt DnsZone.</span><span class="sxs-lookup"><span data-stu-id="a905c-133">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="a905c-134">Zapewnia to ochronę współbieżnych zmian.</span><span class="sxs-lookup"><span data-stu-id="a905c-134">This provides protection for concurrent changes.</span></span> <span data-ttu-id="a905c-135">Możesz pominąć to zachowanie przy użyciu parametru *overwrite* , który aktualizuje strefę bez względu na współbieżne zmiany.</span><span class="sxs-lookup"><span data-stu-id="a905c-135">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a905c-136">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a905c-136">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="a905c-137">Lista sieci wirtualnych, które rejestrują rekordy hosta maszyny wirtualnej w tej strefie DNS, są dostępne tylko dla stref prywatnych.</span><span class="sxs-lookup"><span data-stu-id="a905c-137">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="a905c-138">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="a905c-138">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="a905c-139">Lista identyfikatorów sieci wirtualnych, które będą rejestrowały rekordy hosta maszyny wirtualnej w tej strefie DNS, są dostępne tylko dla stref prywatnych.</span><span class="sxs-lookup"><span data-stu-id="a905c-139">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="a905c-140">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a905c-140">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="a905c-141">Lista sieci wirtualnych zdolnych do tłumaczenia rekordów w tej strefie DNS, które są dostępne tylko dla stref prywatnych.</span><span class="sxs-lookup"><span data-stu-id="a905c-141">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="a905c-142">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="a905c-142">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="a905c-143">Lista identyfikatorów sieci wirtualnych, które mogą rozpoznawać rekordy w tej strefie DNS, są dostępne tylko dla stref prywatnych.</span><span class="sxs-lookup"><span data-stu-id="a905c-143">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="a905c-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a905c-144">-ResourceGroupName</span></span>
<span data-ttu-id="a905c-145">Określa nazwę grupy zasobów zawierającej strefę do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="a905c-145">Specifies the name of the resource group that contains the zone to update.</span></span>
<span data-ttu-id="a905c-146">Należy również określić parametr zonename.</span><span class="sxs-lookup"><span data-stu-id="a905c-146">You must also specify the ZoneName parameter.</span></span>

<span data-ttu-id="a905c-147">Możesz też określić strefę za pomocą obiektu DnsZone z parametrem *Zone* lub Pipeline.</span><span class="sxs-lookup"><span data-stu-id="a905c-147">Alternatively, you can specify the zone using a DnsZone object with the *Zone* parameter or the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: Fields, FieldsObjects
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a905c-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="a905c-148">-Tag</span></span>
<span data-ttu-id="a905c-149">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="a905c-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a905c-150">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="a905c-150">For example:</span></span>

<span data-ttu-id="a905c-151">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="a905c-151">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: Fields, FieldsObjects
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a905c-152">-Zone</span><span class="sxs-lookup"><span data-stu-id="a905c-152">-Zone</span></span>
<span data-ttu-id="a905c-153">Określa strefę DNS do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="a905c-153">Specifies the DNS zone to update.</span></span>

<span data-ttu-id="a905c-154">Możesz też określić strefę przy użyciu parametrów *zonename* i *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="a905c-154">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: DnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a905c-155">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a905c-155">-Confirm</span></span>
<span data-ttu-id="a905c-156">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a905c-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a905c-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a905c-157">-WhatIf</span></span>
<span data-ttu-id="a905c-158">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a905c-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a905c-159">Polecenie cmdlet nie jest uruchamiane. Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a905c-159">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a905c-160">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a905c-160">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a905c-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a905c-161">CommonParameters</span></span>
<span data-ttu-id="a905c-162">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a905c-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a905c-163">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a905c-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a905c-164">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a905c-164">INPUTS</span></span>

### <span data-ttu-id="a905c-165">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="a905c-165">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="a905c-166">Do tego polecenia cmdlet można nawiązać obiekt DnsZone.</span><span class="sxs-lookup"><span data-stu-id="a905c-166">You can pipe a DnsZone object to this cmdlet.</span></span>

## <span data-ttu-id="a905c-167">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a905c-167">OUTPUTS</span></span>

### <span data-ttu-id="a905c-168">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="a905c-168">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="a905c-169">To polecenie cmdlet zwraca obiekt DnsZone, który reprezentuje zaktualizowaną strefę DNS przy użyciu nowego elementu ETag.</span><span class="sxs-lookup"><span data-stu-id="a905c-169">This cmdlet returns a DnsZone object that represents the updated DNS zone with a new Etag.</span></span>

## <span data-ttu-id="a905c-170">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a905c-170">NOTES</span></span>
<span data-ttu-id="a905c-171">Za pomocą parametru *Confirm* można kontrolować, czy to polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a905c-171">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="a905c-172">Domyślnie polecenie cmdlet monituje o potwierdzenie, jeśli zmienna $ConfirmPreference Windows PowerShell ma wartość średnią lub niższą.</span><span class="sxs-lookup"><span data-stu-id="a905c-172">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="a905c-173">Jeśli określisz pozycję *Potwierdź* lub *Potwierdź: $true* , to polecenie cmdlet wyświetli monit o potwierdzenie przed jego uruchomieniem.</span><span class="sxs-lookup"><span data-stu-id="a905c-173">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="a905c-174">Jeśli określisz pozycję *Confirm (Potwierdź): $false* , polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a905c-174">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="a905c-175">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a905c-175">RELATED LINKS</span></span>

[<span data-ttu-id="a905c-176">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="a905c-176">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="a905c-177">Nowe — AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="a905c-177">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="a905c-178">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="a905c-178">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)
