---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsZone.md
ms.openlocfilehash: 9d4e0e376e611e1373d30ab6b3aeafb51f363c31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718532"
---
# <span data-ttu-id="0af62-101">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="0af62-101">Set-AzureRmDnsZone</span></span>

## <span data-ttu-id="0af62-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0af62-102">SYNOPSIS</span></span>
<span data-ttu-id="0af62-103">Aktualizuje właściwości strefy DNS.</span><span class="sxs-lookup"><span data-stu-id="0af62-103">Updates the properties of a DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0af62-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0af62-104">SYNTAX</span></span>

### <span data-ttu-id="0af62-105">Field</span><span class="sxs-lookup"><span data-stu-id="0af62-105">Fields</span></span>
```
Set-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0af62-106">Stream</span><span class="sxs-lookup"><span data-stu-id="0af62-106">Object</span></span>
```
Set-AzureRmDnsZone -Zone <DnsZone> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0af62-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0af62-107">DESCRIPTION</span></span>
<span data-ttu-id="0af62-108">Polecenie cmdlet **Set-AzureRmDnsZone** aktualizuje określoną strefę DNS w usłudze DNS Azure.</span><span class="sxs-lookup"><span data-stu-id="0af62-108">The **Set-AzureRmDnsZone** cmdlet updates the specified DNS zone in the Azure DNS service.</span></span>
<span data-ttu-id="0af62-109">To polecenie cmdlet nie powoduje zaktualizowania zestawów rekordów w strefie.</span><span class="sxs-lookup"><span data-stu-id="0af62-109">This cmdlet does not update the record sets in the zone.</span></span>

<span data-ttu-id="0af62-110">Obiekt **dnsZone** można przekazać jako parametr lub za pomocą operatora potoku albo też można określić parametry *zonename* i *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="0af62-110">You can pass a **DnsZone** object as a parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="0af62-111">Za pomocą zmiennej *Confirm* i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0af62-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="0af62-112">Gdy przepuszczasz strefę DNS jako obiekt (za pomocą obiektu Zone lub za pośrednictwem rurociągu), nie zostanie ona zaktualizowana, jeśli została ona zmieniona w usłudze DNS Azure, ponieważ został pobrany lokalny obiekt DnsZone.</span><span class="sxs-lookup"><span data-stu-id="0af62-112">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="0af62-113">Zapewnia to ochronę współbieżnych zmian.</span><span class="sxs-lookup"><span data-stu-id="0af62-113">This provides protection for concurrent changes.</span></span> <span data-ttu-id="0af62-114">Możesz pominąć to zachowanie przy użyciu parametru *overwrite* , który aktualizuje strefę bez względu na współbieżne zmiany.</span><span class="sxs-lookup"><span data-stu-id="0af62-114">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="0af62-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0af62-115">EXAMPLES</span></span>

### <span data-ttu-id="0af62-116">Przykład 1: aktualizowanie strefy DNS</span><span class="sxs-lookup"><span data-stu-id="0af62-116">Example 1: Update a DNS zone</span></span>
```
PS C:\>$Zone = Get-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzureRmDnsZone -Zone $Zone
```

<span data-ttu-id="0af62-117">Pierwsze polecenie pobiera strefę o nazwie myzone.com z określonej grupy zasobów, a następnie zapisuje ją w zmiennej $Zone.</span><span class="sxs-lookup"><span data-stu-id="0af62-117">The first command gets the zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

<span data-ttu-id="0af62-118">Drugie polecenie aktualizuje znaczniki $Zone.</span><span class="sxs-lookup"><span data-stu-id="0af62-118">The second command updates the tags for $Zone.</span></span>

<span data-ttu-id="0af62-119">Polecenie ostatnie zatwierdza zmianę.</span><span class="sxs-lookup"><span data-stu-id="0af62-119">The final command commits the change.</span></span>

### <span data-ttu-id="0af62-120">Przykład 2: aktualizowanie znaczników dla strefy</span><span class="sxs-lookup"><span data-stu-id="0af62-120">Example 2: Update tags for a zone</span></span>
```
PS C:\>Set-AzureRmDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

<span data-ttu-id="0af62-121">To polecenie aktualizuje znaczniki strefy o nazwie myzone.com bez uprzedniego uzyskania tej strefy.</span><span class="sxs-lookup"><span data-stu-id="0af62-121">This command updates the tags for the zone named myzone.com without first explicitly getting the zone.</span></span>

## <span data-ttu-id="0af62-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0af62-122">PARAMETERS</span></span>

### <span data-ttu-id="0af62-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0af62-123">-Name</span></span>
<span data-ttu-id="0af62-124">Określa nazwę strefy DNS do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="0af62-124">Specifies the name of the DNS zone to update.</span></span>

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

### <span data-ttu-id="0af62-125">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="0af62-125">-Overwrite</span></span>
<span data-ttu-id="0af62-126">Gdy przepuszczasz strefę DNS jako obiekt (za pomocą obiektu Zone lub za pośrednictwem rurociągu), nie zostanie ona zaktualizowana, jeśli została ona zmieniona w usłudze DNS Azure, ponieważ został pobrany lokalny obiekt DnsZone.</span><span class="sxs-lookup"><span data-stu-id="0af62-126">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="0af62-127">Zapewnia to ochronę współbieżnych zmian.</span><span class="sxs-lookup"><span data-stu-id="0af62-127">This provides protection for concurrent changes.</span></span> <span data-ttu-id="0af62-128">Możesz pominąć to zachowanie przy użyciu parametru *overwrite* , który aktualizuje strefę bez względu na współbieżne zmiany.</span><span class="sxs-lookup"><span data-stu-id="0af62-128">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="0af62-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0af62-129">-ResourceGroupName</span></span>
<span data-ttu-id="0af62-130">Określa nazwę grupy zasobów zawierającej strefę do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="0af62-130">Specifies the name of the resource group that contains the zone to update.</span></span>
<span data-ttu-id="0af62-131">Należy również określić parametr zonename.</span><span class="sxs-lookup"><span data-stu-id="0af62-131">You must also specify the ZoneName parameter.</span></span>

<span data-ttu-id="0af62-132">Możesz też określić strefę za pomocą obiektu DnsZone z parametrem *Zone* lub Pipeline.</span><span class="sxs-lookup"><span data-stu-id="0af62-132">Alternatively, you can specify the zone using a DnsZone object with the *Zone* parameter or the pipeline.</span></span>

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

### <span data-ttu-id="0af62-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="0af62-133">-Tag</span></span>
<span data-ttu-id="0af62-134">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="0af62-134">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0af62-135">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="0af62-135">For example:</span></span>

<span data-ttu-id="0af62-136">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="0af62-136">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Fields
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0af62-137">-Zone</span><span class="sxs-lookup"><span data-stu-id="0af62-137">-Zone</span></span>
<span data-ttu-id="0af62-138">Określa strefę DNS do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="0af62-138">Specifies the DNS zone to update.</span></span>

<span data-ttu-id="0af62-139">Możesz też określić strefę przy użyciu parametrów *zonename* i *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="0af62-139">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="0af62-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0af62-140">-Confirm</span></span>
<span data-ttu-id="0af62-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0af62-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0af62-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0af62-142">-WhatIf</span></span>
<span data-ttu-id="0af62-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0af62-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0af62-144">Polecenie cmdlet nie jest uruchamiane. Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0af62-144">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0af62-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0af62-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0af62-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0af62-146">-DefaultProfile</span></span>
<span data-ttu-id="0af62-147">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0af62-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0af62-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0af62-148">CommonParameters</span></span>
<span data-ttu-id="0af62-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0af62-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0af62-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0af62-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0af62-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0af62-151">INPUTS</span></span>

### <span data-ttu-id="0af62-152">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="0af62-152">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="0af62-153">Do tego polecenia cmdlet można nawiązać obiekt DnsZone.</span><span class="sxs-lookup"><span data-stu-id="0af62-153">You can pipe a DnsZone object to this cmdlet.</span></span>

## <span data-ttu-id="0af62-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0af62-154">OUTPUTS</span></span>

### <span data-ttu-id="0af62-155">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="0af62-155">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="0af62-156">To polecenie cmdlet zwraca obiekt DnsZone, który reprezentuje zaktualizowaną strefę DNS przy użyciu nowego elementu ETag.</span><span class="sxs-lookup"><span data-stu-id="0af62-156">This cmdlet returns a DnsZone object that represents the updated DNS zone with a new Etag.</span></span>

## <span data-ttu-id="0af62-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0af62-157">NOTES</span></span>
<span data-ttu-id="0af62-158">Za pomocą parametru *Confirm* można kontrolować, czy to polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0af62-158">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="0af62-159">Domyślnie polecenie cmdlet monituje o potwierdzenie, jeśli zmienna $ConfirmPreference Windows PowerShell ma wartość średnią lub niższą.</span><span class="sxs-lookup"><span data-stu-id="0af62-159">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="0af62-160">Jeśli określisz pozycję *Potwierdź* lub *Potwierdź: $true* , to polecenie cmdlet wyświetli monit o potwierdzenie przed jego uruchomieniem.</span><span class="sxs-lookup"><span data-stu-id="0af62-160">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="0af62-161">Jeśli określisz pozycję *Confirm (Potwierdź): $false* , polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0af62-161">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="0af62-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0af62-162">RELATED LINKS</span></span>

[<span data-ttu-id="0af62-163">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="0af62-163">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="0af62-164">Nowe — AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="0af62-164">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="0af62-165">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="0af62-165">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)
