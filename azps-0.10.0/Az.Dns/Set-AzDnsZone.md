---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Set-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Set-AzDnsZone.md
ms.openlocfilehash: 9b6d84f9007a872db0e41efa78d8e16d7269eb02
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891530"
---
# <span data-ttu-id="ab5ce-101">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="ab5ce-101">Set-AzDnsZone</span></span>

## <span data-ttu-id="ab5ce-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ab5ce-102">SYNOPSIS</span></span>
<span data-ttu-id="ab5ce-103">Aktualizuje właściwości strefy DNS.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-103">Updates the properties of a DNS zone.</span></span>

## <span data-ttu-id="ab5ce-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ab5ce-104">SYNTAX</span></span>

### <span data-ttu-id="ab5ce-105">Field</span><span class="sxs-lookup"><span data-stu-id="ab5ce-105">Fields</span></span>
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ab5ce-106">Stream</span><span class="sxs-lookup"><span data-stu-id="ab5ce-106">Object</span></span>
```
Set-AzDnsZone -Zone <DnsZone> [-Overwrite] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab5ce-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ab5ce-107">DESCRIPTION</span></span>
<span data-ttu-id="ab5ce-108">Polecenie cmdlet **Set-AzDnsZone** aktualizuje określoną strefę DNS w usłudze DNS Azure.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-108">The **Set-AzDnsZone** cmdlet updates the specified DNS zone in the Azure DNS service.</span></span>
<span data-ttu-id="ab5ce-109">To polecenie cmdlet nie powoduje zaktualizowania zestawów rekordów w strefie.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-109">This cmdlet does not update the record sets in the zone.</span></span>

<span data-ttu-id="ab5ce-110">Obiekt **dnsZone** można przekazać jako parametr lub za pomocą operatora potoku albo też można określić parametry *zonename* i *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="ab5ce-110">You can pass a **DnsZone** object as a parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="ab5ce-111">Za pomocą zmiennej *Confirm* i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="ab5ce-112">Gdy przepuszczasz strefę DNS jako obiekt (za pomocą obiektu Zone lub za pośrednictwem rurociągu), nie zostanie ona zaktualizowana, jeśli została ona zmieniona w usłudze DNS Azure, ponieważ został pobrany lokalny obiekt DnsZone.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-112">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="ab5ce-113">Zapewnia to ochronę współbieżnych zmian.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-113">This provides protection for concurrent changes.</span></span> <span data-ttu-id="ab5ce-114">Możesz pominąć to zachowanie przy użyciu parametru *overwrite* , który aktualizuje strefę bez względu na współbieżne zmiany.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-114">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="ab5ce-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ab5ce-115">EXAMPLES</span></span>

### <span data-ttu-id="ab5ce-116">Przykład 1: aktualizowanie strefy DNS</span><span class="sxs-lookup"><span data-stu-id="ab5ce-116">Example 1: Update a DNS zone</span></span>
```
PS C:\>$Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzDnsZone -Zone $Zone
```

<span data-ttu-id="ab5ce-117">Pierwsze polecenie pobiera strefę o nazwie myzone.com z określonej grupy zasobów, a następnie zapisuje ją w zmiennej $Zone.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-117">The first command gets the zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

<span data-ttu-id="ab5ce-118">Drugie polecenie aktualizuje znaczniki $Zone.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-118">The second command updates the tags for $Zone.</span></span>

<span data-ttu-id="ab5ce-119">Polecenie ostatnie zatwierdza zmianę.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-119">The final command commits the change.</span></span>

### <span data-ttu-id="ab5ce-120">Przykład 2: aktualizowanie znaczników dla strefy</span><span class="sxs-lookup"><span data-stu-id="ab5ce-120">Example 2: Update tags for a zone</span></span>
```
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

<span data-ttu-id="ab5ce-121">To polecenie aktualizuje znaczniki strefy o nazwie myzone.com bez uprzedniego uzyskania tej strefy.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-121">This command updates the tags for the zone named myzone.com without first explicitly getting the zone.</span></span>

## <span data-ttu-id="ab5ce-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ab5ce-122">PARAMETERS</span></span>

### <span data-ttu-id="ab5ce-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ab5ce-123">-Name</span></span>
<span data-ttu-id="ab5ce-124">Określa nazwę strefy DNS do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-124">Specifies the name of the DNS zone to update.</span></span>

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

### <span data-ttu-id="ab5ce-125">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="ab5ce-125">-Overwrite</span></span>
<span data-ttu-id="ab5ce-126">Gdy przepuszczasz strefę DNS jako obiekt (za pomocą obiektu Zone lub za pośrednictwem rurociągu), nie zostanie ona zaktualizowana, jeśli została ona zmieniona w usłudze DNS Azure, ponieważ został pobrany lokalny obiekt DnsZone.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-126">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="ab5ce-127">Zapewnia to ochronę współbieżnych zmian.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-127">This provides protection for concurrent changes.</span></span> <span data-ttu-id="ab5ce-128">Możesz pominąć to zachowanie przy użyciu parametru *overwrite* , który aktualizuje strefę bez względu na współbieżne zmiany.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-128">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="ab5ce-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab5ce-129">-ResourceGroupName</span></span>
<span data-ttu-id="ab5ce-130">Określa nazwę grupy zasobów zawierającej strefę do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-130">Specifies the name of the resource group that contains the zone to update.</span></span>
<span data-ttu-id="ab5ce-131">Należy również określić parametr zonename.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-131">You must also specify the ZoneName parameter.</span></span>

<span data-ttu-id="ab5ce-132">Możesz też określić strefę za pomocą obiektu DnsZone z parametrem *Zone* lub Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-132">Alternatively, you can specify the zone using a DnsZone object with the *Zone* parameter or the pipeline.</span></span>

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

### <span data-ttu-id="ab5ce-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="ab5ce-133">-Tag</span></span>
<span data-ttu-id="ab5ce-134">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-134">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ab5ce-135">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="ab5ce-135">For example:</span></span>

<span data-ttu-id="ab5ce-136">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="ab5ce-136">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: Fields
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab5ce-137">-Zone</span><span class="sxs-lookup"><span data-stu-id="ab5ce-137">-Zone</span></span>
<span data-ttu-id="ab5ce-138">Określa strefę DNS do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-138">Specifies the DNS zone to update.</span></span>

<span data-ttu-id="ab5ce-139">Możesz też określić strefę przy użyciu parametrów *zonename* i *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="ab5ce-139">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="ab5ce-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ab5ce-140">-Confirm</span></span>
<span data-ttu-id="ab5ce-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab5ce-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab5ce-142">-WhatIf</span></span>
<span data-ttu-id="ab5ce-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ab5ce-144">Polecenie cmdlet nie jest uruchamiane. Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-144">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ab5ce-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab5ce-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab5ce-146">CommonParameters</span></span>
<span data-ttu-id="ab5ce-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab5ce-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab5ce-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab5ce-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab5ce-149">INPUTS</span></span>

### <span data-ttu-id="ab5ce-150">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="ab5ce-150">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="ab5ce-151">Do tego polecenia cmdlet można nawiązać obiekt DnsZone.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-151">You can pipe a DnsZone object to this cmdlet.</span></span>

## <span data-ttu-id="ab5ce-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ab5ce-152">OUTPUTS</span></span>

### <span data-ttu-id="ab5ce-153">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="ab5ce-153">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="ab5ce-154">To polecenie cmdlet zwraca obiekt DnsZone, który reprezentuje zaktualizowaną strefę DNS przy użyciu nowego elementu ETag.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-154">This cmdlet returns a DnsZone object that represents the updated DNS zone with a new Etag.</span></span>

## <span data-ttu-id="ab5ce-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ab5ce-155">NOTES</span></span>
<span data-ttu-id="ab5ce-156">Za pomocą parametru *Confirm* można kontrolować, czy to polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-156">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="ab5ce-157">Domyślnie polecenie cmdlet monituje o potwierdzenie, jeśli zmienna $ConfirmPreference Windows PowerShell ma wartość średnią lub niższą.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-157">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="ab5ce-158">Jeśli określisz pozycję *Potwierdź* lub *Potwierdź: $true* , to polecenie cmdlet wyświetli monit o potwierdzenie przed jego uruchomieniem.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-158">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="ab5ce-159">Jeśli określisz pozycję *Confirm (Potwierdź): $false* , polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-159">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="ab5ce-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ab5ce-160">RELATED LINKS</span></span>

[<span data-ttu-id="ab5ce-161">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="ab5ce-161">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="ab5ce-162">Nowe — AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="ab5ce-162">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="ab5ce-163">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="ab5ce-163">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)