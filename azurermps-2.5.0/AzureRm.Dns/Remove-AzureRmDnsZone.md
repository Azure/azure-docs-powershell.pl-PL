---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: ''
schema: 2.0.0
ms.openlocfilehash: c12c5532a85bacb5cd854f4f2ad87ad0d8b68178
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899348"
---
# <span data-ttu-id="866da-101">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="866da-101">Remove-AzureRmDnsZone</span></span>

## <span data-ttu-id="866da-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="866da-102">SYNOPSIS</span></span>
<span data-ttu-id="866da-103">Usuwa strefę DNS z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="866da-103">Removes a DNS zone from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="866da-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="866da-104">SYNTAX</span></span>

### <span data-ttu-id="866da-105">Field</span><span class="sxs-lookup"><span data-stu-id="866da-105">Fields</span></span>
```
Remove-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="866da-106">Stream</span><span class="sxs-lookup"><span data-stu-id="866da-106">Object</span></span>
```
Remove-AzureRmDnsZone -Zone <DnsZone> [-Overwrite] [-Force] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="866da-107">Opis</span><span class="sxs-lookup"><span data-stu-id="866da-107">DESCRIPTION</span></span>
<span data-ttu-id="866da-108">Polecenie cmdlet **Remove-AzureRmDnsZone** trwale usuwa strefę DNS (Domain Name System) z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="866da-108">The **Remove-AzureRmDnsZone** cmdlet permanently deletes a Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="866da-109">Wszystkie zestawy rekordów zawarte w tej strefie również zostaną usunięte.</span><span class="sxs-lookup"><span data-stu-id="866da-109">All record sets contained in the zone are also deleted.</span></span>

<span data-ttu-id="866da-110">Obiekt **dnsZone** można przekazać przy użyciu parametru *name* lub za pomocą operatora potoku lub można też określić parametry *zonename* i *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="866da-110">You can pass a **DnsZone** object using the *Name* parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="866da-111">Za pomocą zmiennej Confirm i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="866da-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="866da-112">Podczas określania strefy za pomocą obiektu **dnsZone** (przekazywanego za pośrednictwem parametru rurociągu lub *strefy* ) strefa nie jest usuwana, jeśli została zmieniona w usłudze DNS Azure od momentu pobrania lokalnego obiektu **dnsZone** (tylko operacje bezpośrednio dotyczące liczby zasobów stref DNS jako zmian, operacje na zestawach rekordów w strefie nie są).</span><span class="sxs-lookup"><span data-stu-id="866da-112">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="866da-113">Zapewnia to ochronę współbieżnych zmian stref.</span><span class="sxs-lookup"><span data-stu-id="866da-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="866da-114">Można to pominąć przy użyciu parametru *overwrite* , który usuwa strefę bez względu na współbieżne zmiany.</span><span class="sxs-lookup"><span data-stu-id="866da-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="866da-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="866da-115">EXAMPLES</span></span>

### <span data-ttu-id="866da-116">Przykład 1. Usuń strefę</span><span class="sxs-lookup"><span data-stu-id="866da-116">Example 1: Remove a zone</span></span>
```
PS C:\>Remove-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="866da-117">To polecenie usuwa strefę o nazwie myzone.com z grupy zasobów o nazwie Moja zasobów.</span><span class="sxs-lookup"><span data-stu-id="866da-117">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="866da-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="866da-118">PARAMETERS</span></span>

### <span data-ttu-id="866da-119">-Force</span><span class="sxs-lookup"><span data-stu-id="866da-119">-Force</span></span>
<span data-ttu-id="866da-120">Ten parametr jest przestarzały dla tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="866da-120">This parameter is deprecated for this cmdlet.</span></span>
<span data-ttu-id="866da-121">Zostanie on usunięty w przyszłym wydaniu.</span><span class="sxs-lookup"><span data-stu-id="866da-121">It will be removed in a future release.</span></span>

<span data-ttu-id="866da-122">Aby określić, czy to polecenie cmdlet monituje o potwierdzenie, użyj parametru *Confirm* .</span><span class="sxs-lookup"><span data-stu-id="866da-122">To control whether this cmdlet prompts you for confirmation, use the *Confirm* parameter.</span></span>

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

### <span data-ttu-id="866da-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="866da-123">-Name</span></span>
<span data-ttu-id="866da-124">Określa nazwę strefy DNS, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="866da-124">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="866da-125">Musisz również określić parametr *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="866da-125">You must also specify the *ResourceGroupName* parameter.</span></span>

<span data-ttu-id="866da-126">Możesz też określić strefę DNS przy użyciu parametru *Zone* .</span><span class="sxs-lookup"><span data-stu-id="866da-126">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="866da-127">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="866da-127">-Overwrite</span></span>
<span data-ttu-id="866da-128">Podczas określania strefy za pomocą obiektu **dnsZone** (przekazywanego za pośrednictwem parametru rurociągu lub *strefy* ) strefa nie jest usuwana, jeśli została zmieniona w usłudze DNS Azure od momentu pobrania lokalnego obiektu **dnsZone** (tylko operacje bezpośrednio dotyczące liczby zasobów stref DNS jako zmian, operacje na zestawach rekordów w strefie nie są).</span><span class="sxs-lookup"><span data-stu-id="866da-128">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="866da-129">Zapewnia to ochronę współbieżnych zmian stref.</span><span class="sxs-lookup"><span data-stu-id="866da-129">This provides protection for concurrent zone changes.</span></span>

<span data-ttu-id="866da-130">Można to pominąć przy użyciu parametru *overwrite* , który usuwa strefę bez względu na współbieżne zmiany.</span><span class="sxs-lookup"><span data-stu-id="866da-130">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="866da-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="866da-131">-PassThru</span></span>
<span data-ttu-id="866da-132">passthru</span><span class="sxs-lookup"><span data-stu-id="866da-132">passthru</span></span>

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

### <span data-ttu-id="866da-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="866da-133">-ResourceGroupName</span></span>
<span data-ttu-id="866da-134">Określa nazwę grupy zasobów zawierającej strefę do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="866da-134">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="866da-135">Należy również określić parametr *zonename* .</span><span class="sxs-lookup"><span data-stu-id="866da-135">You must also specify the *ZoneName* parameter.</span></span>

<span data-ttu-id="866da-136">Możesz też określić strefę DNS za pomocą obiektu **dnsZone** , przekazaną za pośrednictwem potoku lub parametru *Zone* .</span><span class="sxs-lookup"><span data-stu-id="866da-136">Alternatively, you can specify the DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="866da-137">-Zone</span><span class="sxs-lookup"><span data-stu-id="866da-137">-Zone</span></span>
<span data-ttu-id="866da-138">Określa strefę DNS do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="866da-138">Specifies the DNS zone to delete.</span></span>
<span data-ttu-id="866da-139">Przekazany obiekt **dnsZone** można również przekazywać za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="866da-139">The **DnsZone** object passed can also be passed via the pipeline.</span></span>

<span data-ttu-id="866da-140">Możesz też określić strefę DNS do usunięcia przy użyciu parametrów *zonename* i *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="866da-140">Alternatively, you can specify the DNS zone to delete by using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="866da-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="866da-141">-Confirm</span></span>
<span data-ttu-id="866da-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="866da-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="866da-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="866da-143">-WhatIf</span></span>
<span data-ttu-id="866da-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="866da-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="866da-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="866da-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="866da-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="866da-146">CommonParameters</span></span>
<span data-ttu-id="866da-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="866da-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="866da-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="866da-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="866da-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="866da-149">INPUTS</span></span>

### <span data-ttu-id="866da-150">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="866da-150">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="866da-151">Do tego polecenia cmdlet można nawiązać obiekt **dnsZone** .</span><span class="sxs-lookup"><span data-stu-id="866da-151">You can pipe a **DnsZone** object to this cmdlet.</span></span>

## <span data-ttu-id="866da-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="866da-152">OUTPUTS</span></span>

### <span data-ttu-id="866da-153">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="866da-153">None</span></span>
<span data-ttu-id="866da-154">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="866da-154">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="866da-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="866da-155">NOTES</span></span>
<span data-ttu-id="866da-156">Ze względu na potencjalnie wysoki wpływ usunięcia strefy DNS to polecenie cmdlet domyślnie monituje o potwierdzenie, jeśli zmienna $ConfirmPreference Windows PowerShell ma dowolną wartość inną niż none.</span><span class="sxs-lookup"><span data-stu-id="866da-156">Due to the potentially high impact of deleting a DNS zone, by default, this cmdlet prompts for confirmation if the $ConfirmPreference Windows PowerShell variable has any value other than None.</span></span>

<span data-ttu-id="866da-157">Jeśli określisz pozycję *Potwierdź* lub *Potwierdź: $true* , to polecenie cmdlet wyświetli monit o potwierdzenie przed jego uruchomieniem.</span><span class="sxs-lookup"><span data-stu-id="866da-157">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="866da-158">Jeśli określisz pozycję *Confirm (Potwierdź): $false* , polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="866da-158">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="866da-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="866da-159">RELATED LINKS</span></span>

[<span data-ttu-id="866da-160">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="866da-160">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="866da-161">Nowe — AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="866da-161">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="866da-162">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="866da-162">Set-AzureRmDnsZone</span></span>](./Set-AzureRmDnsZone.md)
