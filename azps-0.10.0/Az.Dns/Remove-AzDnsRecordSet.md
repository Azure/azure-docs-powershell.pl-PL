---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
ms.openlocfilehash: 10cd4936ad406be85f840b25c175d7900d66d679
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893158"
---
# <span data-ttu-id="88352-101">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="88352-101">Remove-AzDnsRecordSet</span></span>

## <span data-ttu-id="88352-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="88352-102">SYNOPSIS</span></span>
<span data-ttu-id="88352-103">Usuwa zestaw rekordów.</span><span class="sxs-lookup"><span data-stu-id="88352-103">Deletes a record set.</span></span>

## <span data-ttu-id="88352-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="88352-104">SYNTAX</span></span>

### <span data-ttu-id="88352-105">Field</span><span class="sxs-lookup"><span data-stu-id="88352-105">Fields</span></span>
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String>
 -ResourceGroupName <String> [-Force] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88352-106">Karoten</span><span class="sxs-lookup"><span data-stu-id="88352-106">Mixed</span></span>
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-Force] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88352-107">Stream</span><span class="sxs-lookup"><span data-stu-id="88352-107">Object</span></span>
```
Remove-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-Force] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="88352-108">Opis</span><span class="sxs-lookup"><span data-stu-id="88352-108">DESCRIPTION</span></span>
<span data-ttu-id="88352-109">Polecenie cmdlet **Remove-AzDnsRecordSet** umożliwia usunięcie określonego zestawu rekordów z określonej strefy.</span><span class="sxs-lookup"><span data-stu-id="88352-109">The **Remove-AzDnsRecordSet** cmdlet deletes the specified record set from the specified zone.</span></span>
<span data-ttu-id="88352-110">Nie można usuwać rekordów serwera SOA ani serwerów nazw (NS), które są tworzone automatycznie w strefie Apex.</span><span class="sxs-lookup"><span data-stu-id="88352-110">You cannot delete SOA or name server (NS) records that are automatically created at the zone apex.</span></span>

<span data-ttu-id="88352-111">Do tego polecenia cmdlet można przekazać obiekt **Recordset** za pomocą operatora potoku lub jako parametru.</span><span class="sxs-lookup"><span data-stu-id="88352-111">You can pass a **RecordSet** object to this cmdlet by using the pipeline operator or as a parameter.</span></span>
<span data-ttu-id="88352-112">Aby zidentyfikować zestaw rekordów i wpisać go bez użycia obiektu **Recordset** , należy przekazać strefę jako obiekt **dnsZone** do tego polecenia cmdlet, korzystając z operatora potoku lub jako parametru lub można też określić parametry *zonename* i *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="88352-112">To identify a record set by name and type without using a **RecordSet** object, you must pass the zone as a **DnsZone** object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="88352-113">Za pomocą zmiennej Confirm i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="88352-113">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="88352-114">Podczas określania zestawu rekordów za pomocą obiektu **Recordset** zestaw rekordów nie jest usuwany, jeśli został zmieniony w usłudze DNS Azure, ponieważ został pobrany lokalny obiekt **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="88352-114">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="88352-115">Zapewnia to ochronę współbieżnych zmian.</span><span class="sxs-lookup"><span data-stu-id="88352-115">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="88352-116">Można to pominąć, używając parametru *zastępowania* , który usuwa zestaw rekordów bez względu na zmiany współbieżne.</span><span class="sxs-lookup"><span data-stu-id="88352-116">You can suppress this by using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="88352-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="88352-117">EXAMPLES</span></span>

### <span data-ttu-id="88352-118">Przykład 1: usuwanie zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="88352-118">Example 1: Remove a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="88352-119">Pierwsze polecenie pobiera określony zestaw rekordów, a następnie zapisuje go w zmiennej $RecordSet. Drugie polecenie usuwa zestaw rekordów w $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="88352-119">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="88352-120">Przykład 2: usunięcie zestawu rekordów i pominięcie wszystkich potwierdzeń</span><span class="sxs-lookup"><span data-stu-id="88352-120">Example 2: Remove a record set and suppress all confirmation</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="88352-121">Pierwsze polecenie pobiera określony zestaw rekordów.</span><span class="sxs-lookup"><span data-stu-id="88352-121">The first command gets the specified record set.</span></span>

<span data-ttu-id="88352-122">Drugie polecenie usuwa zestaw rekordów, nawet jeśli został on zmieniony w międzyczasie.</span><span class="sxs-lookup"><span data-stu-id="88352-122">The second command deletes the record set, even if it has changed in the meantime.</span></span>
<span data-ttu-id="88352-123">Monity o potwierdzenie są pomijane.</span><span class="sxs-lookup"><span data-stu-id="88352-123">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="88352-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="88352-124">PARAMETERS</span></span>

### <span data-ttu-id="88352-125">-Force</span><span class="sxs-lookup"><span data-stu-id="88352-125">-Force</span></span>
<span data-ttu-id="88352-126">Ten parametr jest przestarzały dla tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88352-126">This parameter is deprecated for this cmdlet.</span></span>
<span data-ttu-id="88352-127">Zostanie on usunięty w przyszłym wydaniu.</span><span class="sxs-lookup"><span data-stu-id="88352-127">It will be removed in a future release.</span></span>

<span data-ttu-id="88352-128">Aby określić, czy to polecenie cmdlet monituje o potwierdzenie, użyj parametru *Confirm* .</span><span class="sxs-lookup"><span data-stu-id="88352-128">To control whether this cmdlet prompts you for confirmation, use the *Confirm* parameter.</span></span>

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

### <span data-ttu-id="88352-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="88352-129">-Name</span></span>
<span data-ttu-id="88352-130">Określa nazwę **zestawu rekordów** , który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="88352-130">Specifies the name of the **RecordSet** to remove.</span></span>
<span data-ttu-id="88352-131">Podczas określania zestawu rekordów według nazwy strefa DNS musi być określona przy użyciu parametru *Zone* lub parametry *zonename* i *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="88352-131">When specifying the record set by name, the DNS zone must be specified using either the *Zone* parameter or the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="88352-132">Zestaw rekordów można też określić za pomocą obiektu **Recordset** , przekazano przy użyciu parametru *Recordset* .</span><span class="sxs-lookup"><span data-stu-id="88352-132">Alternatively, the record set can be specified using a **RecordSet** object, passed using the *RecordSet* parameter.</span></span>

```yaml
Type: String
Parameter Sets: Fields, Mixed
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88352-133">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="88352-133">-Overwrite</span></span>
<span data-ttu-id="88352-134">Podczas określania zestawu rekordów za pomocą obiektu **Recordset** zestaw rekordów nie jest usuwany, jeśli został zmieniony w usłudze DNS Azure, ponieważ został pobrany lokalny obiekt **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="88352-134">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="88352-135">Zapewnia to ochronę współbieżnych zmian.</span><span class="sxs-lookup"><span data-stu-id="88352-135">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="88352-136">Można to pominąć za pomocą parametru *overwrite* , co powoduje usunięcie zestawu rekordów bez względu na jednoczesne zmiany.</span><span class="sxs-lookup"><span data-stu-id="88352-136">This can be suppressed using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="88352-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="88352-137">-PassThru</span></span>
<span data-ttu-id="88352-138">passthru</span><span class="sxs-lookup"><span data-stu-id="88352-138">passthru</span></span>

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

### <span data-ttu-id="88352-139">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="88352-139">-RecordSet</span></span>
<span data-ttu-id="88352-140">Określa obiekt **zestawu rekordów** , który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="88352-140">Specifies the **RecordSet** object to remove.</span></span>

<span data-ttu-id="88352-141">Zestaw rekordów można też określić przy użyciu parametrów *name* i *Zone* albo za pomocą parametrów *name* , *zonename* i *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="88352-141">Alternatively, the record set can be specified using the *Name* and *Zone* parameters, or using the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

```yaml
Type: DnsRecordSet
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88352-142">-Records</span><span class="sxs-lookup"><span data-stu-id="88352-142">-RecordType</span></span>
<span data-ttu-id="88352-143">Określa typ rekordu DNS.</span><span class="sxs-lookup"><span data-stu-id="88352-143">Specifies the type of DNS record.</span></span>

<span data-ttu-id="88352-144">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="88352-144">Valid values are:</span></span>

- <span data-ttu-id="88352-145">Sieci</span><span class="sxs-lookup"><span data-stu-id="88352-145">A</span></span>
- <span data-ttu-id="88352-146">AAAA</span><span class="sxs-lookup"><span data-stu-id="88352-146">AAAA</span></span>
- <span data-ttu-id="88352-147">REKORD</span><span class="sxs-lookup"><span data-stu-id="88352-147">CNAME</span></span>
- <span data-ttu-id="88352-148">MX</span><span class="sxs-lookup"><span data-stu-id="88352-148">MX</span></span>
- <span data-ttu-id="88352-149">REKORDU</span><span class="sxs-lookup"><span data-stu-id="88352-149">NS</span></span>
- <span data-ttu-id="88352-150">SYSTEMU</span><span class="sxs-lookup"><span data-stu-id="88352-150">PTR</span></span>
- <span data-ttu-id="88352-151">SRV</span><span class="sxs-lookup"><span data-stu-id="88352-151">SRV</span></span>
- <span data-ttu-id="88352-152">ROZSZERZENIEM</span><span class="sxs-lookup"><span data-stu-id="88352-152">TXT</span></span>

<span data-ttu-id="88352-153">Rekordy SOA są usuwane automatycznie po usunięciu strefy.</span><span class="sxs-lookup"><span data-stu-id="88352-153">SOA records are deleted automatically when the zone is deleted.</span></span>
<span data-ttu-id="88352-154">Nie można ręcznie usunąć rekordów SOA.</span><span class="sxs-lookup"><span data-stu-id="88352-154">You cannot manually delete SOA records.</span></span>

```yaml
Type: RecordType
Parameter Sets: Fields, Mixed
Aliases: 
Accepted values: A, AAAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88352-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88352-155">-ResourceGroupName</span></span>
<span data-ttu-id="88352-156">Określa grupę zasobów zawierającą strefę DNS zawierającą **zestaw rekordów** do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="88352-156">Specifies the resource group that contains the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="88352-157">Ten parametr jest stosowany tylko wtedy, gdy zestaw rekordów i strefa DNS są określone przy użyciu parametrów *name* i *zonename* .</span><span class="sxs-lookup"><span data-stu-id="88352-157">This parameter is applicable only when the record set and DNS zone are specified using the *Name* and *ZoneName* parameters.</span></span>

<span data-ttu-id="88352-158">Możesz też określić zestaw rekordów przy użyciu parametru *zestaw rekordów* lub *nazwy* i parametrów *strefy* .</span><span class="sxs-lookup"><span data-stu-id="88352-158">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="88352-159">-Zone</span><span class="sxs-lookup"><span data-stu-id="88352-159">-Zone</span></span>
<span data-ttu-id="88352-160">Określa strefę DNS zawierającą **zestaw rekordów** do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="88352-160">Specifies the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="88352-161">Ten parametr ma zastosowanie tylko podczas określania zestawu rekordów przy użyciu parametru *name* .</span><span class="sxs-lookup"><span data-stu-id="88352-161">This parameter is applicable only when specifying the record set using the *Name* parameter.</span></span>

<span data-ttu-id="88352-162">Możesz też określić zestaw rekordów przy użyciu parametru *zestaw rekordów* albo parametrów *name* , *zonename* i *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="88352-162">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

```yaml
Type: DnsZone
Parameter Sets: Mixed
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88352-163">-Nazwa_strefy</span><span class="sxs-lookup"><span data-stu-id="88352-163">-ZoneName</span></span>
<span data-ttu-id="88352-164">Określa nazwę strefy zawierającej **zestaw rekordów** do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="88352-164">Specifies the name of the zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="88352-165">Musisz również określić *nazwę* i parametry *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="88352-165">You must also specify the *Name* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="88352-166">Zestaw rekordów można też określić przy użyciu parametru *zestaw rekordów* albo *nazwy* i parametrów *strefy* .</span><span class="sxs-lookup"><span data-stu-id="88352-166">Alternatively, the record set can be specified using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="88352-167">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="88352-167">-Confirm</span></span>
<span data-ttu-id="88352-168">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88352-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88352-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88352-169">-WhatIf</span></span>
<span data-ttu-id="88352-170">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88352-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88352-171">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="88352-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88352-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88352-172">CommonParameters</span></span>
<span data-ttu-id="88352-173">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88352-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88352-174">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88352-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88352-175">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88352-175">INPUTS</span></span>

### <span data-ttu-id="88352-176">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="88352-176">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="88352-177">Do tego polecenia cmdlet można przetworzyć obiekt **zestawu rekordów** .</span><span class="sxs-lookup"><span data-stu-id="88352-177">You can pipe a **RecordSet** object to this cmdlet.</span></span>

## <span data-ttu-id="88352-178">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="88352-178">OUTPUTS</span></span>

### <span data-ttu-id="88352-179">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="88352-179">None</span></span>
<span data-ttu-id="88352-180">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="88352-180">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="88352-181">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="88352-181">NOTES</span></span>
<span data-ttu-id="88352-182">Za pomocą parametru *Confirm* można kontrolować, czy to polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="88352-182">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="88352-183">Domyślnie polecenie cmdlet monituje o potwierdzenie, jeśli zmienna $ConfirmPreference Windows PowerShell ma wartość średnią lub niższą.</span><span class="sxs-lookup"><span data-stu-id="88352-183">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="88352-184">Jeśli określisz pozycję *Potwierdź* lub *Potwierdź: $true* , to polecenie cmdlet wyświetli monit o potwierdzenie przed jego uruchomieniem.</span><span class="sxs-lookup"><span data-stu-id="88352-184">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="88352-185">Jeśli określisz pozycję *Confirm (Potwierdź): $false* , polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="88352-185">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="88352-186">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="88352-186">RELATED LINKS</span></span>

[<span data-ttu-id="88352-187">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="88352-187">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="88352-188">Nowe — AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="88352-188">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="88352-189">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="88352-189">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
