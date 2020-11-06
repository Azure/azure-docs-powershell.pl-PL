---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/remove-azurermdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsZone.md
ms.openlocfilehash: f5dd34c15745707df8bb0b91f7a4716e5c0bba6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548676"
---
# <span data-ttu-id="e751f-101">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="e751f-101">Remove-AzureRmDnsZone</span></span>

## <span data-ttu-id="e751f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e751f-102">SYNOPSIS</span></span>
<span data-ttu-id="e751f-103">Usuwa strefę DNS z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e751f-103">Removes a DNS zone from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e751f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e751f-104">SYNTAX</span></span>

### <span data-ttu-id="e751f-105">Field</span><span class="sxs-lookup"><span data-stu-id="e751f-105">Fields</span></span>
```
Remove-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e751f-106">Stream</span><span class="sxs-lookup"><span data-stu-id="e751f-106">Object</span></span>
```
Remove-AzureRmDnsZone -Zone <DnsZone> [-Overwrite] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e751f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e751f-107">DESCRIPTION</span></span>
<span data-ttu-id="e751f-108">Polecenie cmdlet **Remove-AzureRmDnsZone** trwale usuwa strefę DNS (Domain Name System) z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e751f-108">The **Remove-AzureRmDnsZone** cmdlet permanently deletes a Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="e751f-109">Wszystkie zestawy rekordów zawarte w tej strefie również zostaną usunięte.</span><span class="sxs-lookup"><span data-stu-id="e751f-109">All record sets contained in the zone are also deleted.</span></span>
<span data-ttu-id="e751f-110">Obiekt **dnsZone** można przekazać przy użyciu parametru *name* lub za pomocą operatora potoku lub można też określić parametry *zonename* i *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="e751f-110">You can pass a **DnsZone** object using the *Name* parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="e751f-111">Za pomocą zmiennej Confirm i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e751f-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="e751f-112">Podczas określania strefy za pomocą obiektu **dnsZone** (przekazywanego za pośrednictwem parametru rurociągu lub *strefy* ) strefa nie jest usuwana, jeśli została zmieniona w usłudze DNS Azure od momentu pobrania lokalnego obiektu **dnsZone** (tylko operacje bezpośrednio dotyczące liczby zasobów stref DNS jako zmian, operacje na zestawach rekordów w strefie nie są).</span><span class="sxs-lookup"><span data-stu-id="e751f-112">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="e751f-113">Zapewnia to ochronę współbieżnych zmian stref.</span><span class="sxs-lookup"><span data-stu-id="e751f-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="e751f-114">Można to pominąć przy użyciu parametru *overwrite* , który usuwa strefę bez względu na współbieżne zmiany.</span><span class="sxs-lookup"><span data-stu-id="e751f-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="e751f-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e751f-115">EXAMPLES</span></span>

### <span data-ttu-id="e751f-116">Przykład 1. Usuń strefę</span><span class="sxs-lookup"><span data-stu-id="e751f-116">Example 1: Remove a zone</span></span>
```
PS C:\>Remove-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="e751f-117">To polecenie usuwa strefę o nazwie myzone.com z grupy zasobów o nazwie Moja zasobów.</span><span class="sxs-lookup"><span data-stu-id="e751f-117">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="e751f-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e751f-118">PARAMETERS</span></span>

### <span data-ttu-id="e751f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e751f-119">-DefaultProfile</span></span>
<span data-ttu-id="e751f-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e751f-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e751f-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e751f-121">-Name</span></span>
<span data-ttu-id="e751f-122">Określa nazwę strefy DNS, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e751f-122">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="e751f-123">Musisz również określić parametr *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="e751f-123">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="e751f-124">Możesz też określić strefę DNS przy użyciu parametru *Zone* .</span><span class="sxs-lookup"><span data-stu-id="e751f-124">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e751f-125">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="e751f-125">-Overwrite</span></span>
<span data-ttu-id="e751f-126">Podczas określania strefy za pomocą obiektu **dnsZone** (przekazywanego za pośrednictwem parametru rurociągu lub *strefy* ) strefa nie jest usuwana, jeśli została zmieniona w usłudze DNS Azure od momentu pobrania lokalnego obiektu **dnsZone** (tylko operacje bezpośrednio dotyczące liczby zasobów stref DNS jako zmian, operacje na zestawach rekordów w strefie nie są).</span><span class="sxs-lookup"><span data-stu-id="e751f-126">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="e751f-127">Zapewnia to ochronę współbieżnych zmian stref.</span><span class="sxs-lookup"><span data-stu-id="e751f-127">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="e751f-128">Można to pominąć przy użyciu parametru *overwrite* , który usuwa strefę bez względu na współbieżne zmiany.</span><span class="sxs-lookup"><span data-stu-id="e751f-128">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="e751f-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e751f-129">-PassThru</span></span>
<span data-ttu-id="e751f-130">passthru</span><span class="sxs-lookup"><span data-stu-id="e751f-130">passthru</span></span>

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

### <span data-ttu-id="e751f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e751f-131">-ResourceGroupName</span></span>
<span data-ttu-id="e751f-132">Określa nazwę grupy zasobów zawierającej strefę do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="e751f-132">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="e751f-133">Należy również określić parametr *zonename* .</span><span class="sxs-lookup"><span data-stu-id="e751f-133">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="e751f-134">Możesz też określić strefę DNS za pomocą obiektu **dnsZone** , przekazaną za pośrednictwem potoku lub parametru *Zone* .</span><span class="sxs-lookup"><span data-stu-id="e751f-134">Alternatively, you can specify the DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e751f-135">-Zone</span><span class="sxs-lookup"><span data-stu-id="e751f-135">-Zone</span></span>
<span data-ttu-id="e751f-136">Określa strefę DNS do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="e751f-136">Specifies the DNS zone to delete.</span></span>
<span data-ttu-id="e751f-137">Przekazany obiekt **dnsZone** można również przekazywać za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="e751f-137">The **DnsZone** object passed can also be passed via the pipeline.</span></span>
<span data-ttu-id="e751f-138">Możesz też określić strefę DNS do usunięcia przy użyciu parametrów *zonename* i *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="e751f-138">Alternatively, you can specify the DNS zone to delete by using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="e751f-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e751f-139">-Confirm</span></span>
<span data-ttu-id="e751f-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e751f-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e751f-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e751f-141">-WhatIf</span></span>
<span data-ttu-id="e751f-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e751f-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e751f-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e751f-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e751f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e751f-144">CommonParameters</span></span>
<span data-ttu-id="e751f-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e751f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e751f-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e751f-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e751f-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e751f-147">INPUTS</span></span>

### <span data-ttu-id="e751f-148">System. String</span><span class="sxs-lookup"><span data-stu-id="e751f-148">System.String</span></span>

### <span data-ttu-id="e751f-149">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="e751f-149">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="e751f-150">Parametry: Zone (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e751f-150">Parameters: Zone (ByValue)</span></span>

## <span data-ttu-id="e751f-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e751f-151">OUTPUTS</span></span>

### <span data-ttu-id="e751f-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e751f-152">System.Boolean</span></span>

## <span data-ttu-id="e751f-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e751f-153">NOTES</span></span>
<span data-ttu-id="e751f-154">Ze względu na potencjalnie wysoki wpływ usunięcia strefy DNS to polecenie cmdlet domyślnie monituje o potwierdzenie, jeśli zmienna $ConfirmPreference Windows PowerShell ma dowolną wartość inną niż none.</span><span class="sxs-lookup"><span data-stu-id="e751f-154">Due to the potentially high impact of deleting a DNS zone, by default, this cmdlet prompts for confirmation if the $ConfirmPreference Windows PowerShell variable has any value other than None.</span></span>
<span data-ttu-id="e751f-155">Jeśli określisz pozycję *Potwierdź* lub *Potwierdź: $true* , to polecenie cmdlet wyświetli monit o potwierdzenie przed jego uruchomieniem.</span><span class="sxs-lookup"><span data-stu-id="e751f-155">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="e751f-156">Jeśli określisz pozycję *Confirm (Potwierdź): $false* , polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e751f-156">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="e751f-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e751f-157">RELATED LINKS</span></span>

[<span data-ttu-id="e751f-158">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="e751f-158">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="e751f-159">Nowe — AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="e751f-159">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="e751f-160">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="e751f-160">Set-AzureRmDnsZone</span></span>](./Set-AzureRmDnsZone.md)
