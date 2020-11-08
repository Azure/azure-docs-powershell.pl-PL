---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
ms.openlocfilehash: f5d7075322bb2b5a4b61635400664f0e909f126d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049912"
---
# <span data-ttu-id="f94ee-101">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f94ee-101">Remove-AzDnsRecordSet</span></span>

## <span data-ttu-id="f94ee-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f94ee-102">SYNOPSIS</span></span>
<span data-ttu-id="f94ee-103">Usuwa zestaw rekordów.</span><span class="sxs-lookup"><span data-stu-id="f94ee-103">Deletes a record set.</span></span>

## <span data-ttu-id="f94ee-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f94ee-104">SYNTAX</span></span>

### <span data-ttu-id="f94ee-105">Field</span><span class="sxs-lookup"><span data-stu-id="f94ee-105">Fields</span></span>
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String> -ResourceGroupName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f94ee-106">Karoten</span><span class="sxs-lookup"><span data-stu-id="f94ee-106">Mixed</span></span>
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f94ee-107">Stream</span><span class="sxs-lookup"><span data-stu-id="f94ee-107">Object</span></span>
```
Remove-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f94ee-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f94ee-108">DESCRIPTION</span></span>
<span data-ttu-id="f94ee-109">Polecenie cmdlet **Remove-AzDnsRecordSet** umożliwia usunięcie określonego zestawu rekordów z określonej strefy.</span><span class="sxs-lookup"><span data-stu-id="f94ee-109">The **Remove-AzDnsRecordSet** cmdlet deletes the specified record set from the specified zone.</span></span>
<span data-ttu-id="f94ee-110">Nie można usuwać rekordów serwera SOA ani serwerów nazw (NS), które są tworzone automatycznie w strefie Apex.</span><span class="sxs-lookup"><span data-stu-id="f94ee-110">You cannot delete SOA or name server (NS) records that are automatically created at the zone apex.</span></span>
<span data-ttu-id="f94ee-111">Do tego polecenia cmdlet można przekazać obiekt **Recordset** za pomocą operatora potoku lub jako parametru.</span><span class="sxs-lookup"><span data-stu-id="f94ee-111">You can pass a **RecordSet** object to this cmdlet by using the pipeline operator or as a parameter.</span></span>
<span data-ttu-id="f94ee-112">Aby zidentyfikować zestaw rekordów i wpisać go bez użycia obiektu **Recordset** , należy przekazać strefę jako obiekt **dnsZone** do tego polecenia cmdlet, korzystając z operatora potoku lub jako parametru lub można też określić parametry *zonename* i *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="f94ee-112">To identify a record set by name and type without using a **RecordSet** object, you must pass the zone as a **DnsZone** object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="f94ee-113">Za pomocą zmiennej Confirm i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f94ee-113">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="f94ee-114">Podczas określania zestawu rekordów za pomocą obiektu **Recordset** zestaw rekordów nie jest usuwany, jeśli został zmieniony w usłudze DNS Azure, ponieważ został pobrany lokalny obiekt **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="f94ee-114">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="f94ee-115">Zapewnia to ochronę współbieżnych zmian.</span><span class="sxs-lookup"><span data-stu-id="f94ee-115">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="f94ee-116">Można to pominąć, używając parametru *zastępowania* , który usuwa zestaw rekordów bez względu na zmiany współbieżne.</span><span class="sxs-lookup"><span data-stu-id="f94ee-116">You can suppress this by using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="f94ee-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f94ee-117">EXAMPLES</span></span>

### <span data-ttu-id="f94ee-118">Przykład 1: usuwanie zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="f94ee-118">Example 1: Remove a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="f94ee-119">Pierwsze polecenie pobiera określony zestaw rekordów, a następnie zapisuje go w zmiennej $RecordSet. Drugie polecenie usuwa zestaw rekordów w $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="f94ee-119">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="f94ee-120">Przykład 2: usunięcie zestawu rekordów i pominięcie wszystkich potwierdzeń</span><span class="sxs-lookup"><span data-stu-id="f94ee-120">Example 2: Remove a record set and suppress all confirmation</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="f94ee-121">Pierwsze polecenie pobiera określony zestaw rekordów.</span><span class="sxs-lookup"><span data-stu-id="f94ee-121">The first command gets the specified record set.</span></span>
<span data-ttu-id="f94ee-122">Drugie polecenie usuwa zestaw rekordów, nawet jeśli został on zmieniony w międzyczasie.</span><span class="sxs-lookup"><span data-stu-id="f94ee-122">The second command deletes the record set, even if it has changed in the meantime.</span></span>
<span data-ttu-id="f94ee-123">Monity o potwierdzenie są pomijane.</span><span class="sxs-lookup"><span data-stu-id="f94ee-123">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="f94ee-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f94ee-124">PARAMETERS</span></span>

### <span data-ttu-id="f94ee-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f94ee-125">-DefaultProfile</span></span>
<span data-ttu-id="f94ee-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f94ee-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f94ee-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f94ee-127">-Name</span></span>
<span data-ttu-id="f94ee-128">Określa nazwę **zestawu rekordów** , który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="f94ee-128">Specifies the name of the **RecordSet** to remove.</span></span>
<span data-ttu-id="f94ee-129">Podczas określania zestawu rekordów według nazwy strefa DNS musi być określona przy użyciu parametru *Zone* lub parametry *zonename* i *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="f94ee-129">When specifying the record set by name, the DNS zone must be specified using either the *Zone* parameter or the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="f94ee-130">Zestaw rekordów można też określić za pomocą obiektu **Recordset** , przekazano przy użyciu parametru *Recordset* .</span><span class="sxs-lookup"><span data-stu-id="f94ee-130">Alternatively, the record set can be specified using a **RecordSet** object, passed using the *RecordSet* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f94ee-131">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="f94ee-131">-Overwrite</span></span>
<span data-ttu-id="f94ee-132">Podczas określania zestawu rekordów za pomocą obiektu **Recordset** zestaw rekordów nie jest usuwany, jeśli został zmieniony w usłudze DNS Azure, ponieważ został pobrany lokalny obiekt **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="f94ee-132">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="f94ee-133">Zapewnia to ochronę współbieżnych zmian.</span><span class="sxs-lookup"><span data-stu-id="f94ee-133">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="f94ee-134">Można to pominąć za pomocą parametru *overwrite* , co powoduje usunięcie zestawu rekordów bez względu na jednoczesne zmiany.</span><span class="sxs-lookup"><span data-stu-id="f94ee-134">This can be suppressed using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="f94ee-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f94ee-135">-PassThru</span></span>
<span data-ttu-id="f94ee-136">passthru</span><span class="sxs-lookup"><span data-stu-id="f94ee-136">passthru</span></span>

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

### <span data-ttu-id="f94ee-137">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="f94ee-137">-RecordSet</span></span>
<span data-ttu-id="f94ee-138">Określa obiekt **zestawu rekordów** , który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="f94ee-138">Specifies the **RecordSet** object to remove.</span></span>
<span data-ttu-id="f94ee-139">Zestaw rekordów można też określić przy użyciu parametrów *name* i *Zone* albo za pomocą parametrów *name* , *zonename* i *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="f94ee-139">Alternatively, the record set can be specified using the *Name* and *Zone* parameters, or using the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f94ee-140">-Records</span><span class="sxs-lookup"><span data-stu-id="f94ee-140">-RecordType</span></span>
<span data-ttu-id="f94ee-141">Określa typ rekordu DNS.</span><span class="sxs-lookup"><span data-stu-id="f94ee-141">Specifies the type of DNS record.</span></span>
<span data-ttu-id="f94ee-142">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="f94ee-142">Valid values are:</span></span>
- <span data-ttu-id="f94ee-143">Sieci</span><span class="sxs-lookup"><span data-stu-id="f94ee-143">A</span></span>
- <span data-ttu-id="f94ee-144">AAAA</span><span class="sxs-lookup"><span data-stu-id="f94ee-144">AAAA</span></span>
- <span data-ttu-id="f94ee-145">REKORD</span><span class="sxs-lookup"><span data-stu-id="f94ee-145">CNAME</span></span>
- <span data-ttu-id="f94ee-146">MX</span><span class="sxs-lookup"><span data-stu-id="f94ee-146">MX</span></span>
- <span data-ttu-id="f94ee-147">REKORDU</span><span class="sxs-lookup"><span data-stu-id="f94ee-147">NS</span></span>
- <span data-ttu-id="f94ee-148">SYSTEMU</span><span class="sxs-lookup"><span data-stu-id="f94ee-148">PTR</span></span>
- <span data-ttu-id="f94ee-149">SRV</span><span class="sxs-lookup"><span data-stu-id="f94ee-149">SRV</span></span>
- <span data-ttu-id="f94ee-150">Rekordy SOA (TXT) są usuwane automatycznie po usunięciu strefy.</span><span class="sxs-lookup"><span data-stu-id="f94ee-150">TXT SOA records are deleted automatically when the zone is deleted.</span></span>
<span data-ttu-id="f94ee-151">Nie można ręcznie usunąć rekordów SOA.</span><span class="sxs-lookup"><span data-stu-id="f94ee-151">You cannot manually delete SOA records.</span></span>

```yaml
Type: Microsoft.Azure.Management.Dns.Models.RecordType
Parameter Sets: Fields, Mixed
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f94ee-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f94ee-152">-ResourceGroupName</span></span>
<span data-ttu-id="f94ee-153">Określa grupę zasobów zawierającą strefę DNS zawierającą **zestaw rekordów** do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="f94ee-153">Specifies the resource group that contains the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="f94ee-154">Ten parametr jest stosowany tylko wtedy, gdy zestaw rekordów i strefa DNS są określone przy użyciu parametrów *name* i *zonename* .</span><span class="sxs-lookup"><span data-stu-id="f94ee-154">This parameter is applicable only when the record set and DNS zone are specified using the *Name* and *ZoneName* parameters.</span></span>
<span data-ttu-id="f94ee-155">Możesz też określić zestaw rekordów przy użyciu parametru *zestaw rekordów* lub *nazwy* i parametrów *strefy* .</span><span class="sxs-lookup"><span data-stu-id="f94ee-155">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="f94ee-156">-Zone</span><span class="sxs-lookup"><span data-stu-id="f94ee-156">-Zone</span></span>
<span data-ttu-id="f94ee-157">Określa strefę DNS zawierającą **zestaw rekordów** do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="f94ee-157">Specifies the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="f94ee-158">Ten parametr ma zastosowanie tylko podczas określania zestawu rekordów przy użyciu parametru *name* .</span><span class="sxs-lookup"><span data-stu-id="f94ee-158">This parameter is applicable only when specifying the record set using the *Name* parameter.</span></span>
<span data-ttu-id="f94ee-159">Możesz też określić zestaw rekordów przy użyciu parametru *zestaw rekordów* albo parametrów *name* , *zonename* i *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="f94ee-159">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f94ee-160">-Nazwa_strefy</span><span class="sxs-lookup"><span data-stu-id="f94ee-160">-ZoneName</span></span>
<span data-ttu-id="f94ee-161">Określa nazwę strefy zawierającej **zestaw rekordów** do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="f94ee-161">Specifies the name of the zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="f94ee-162">Musisz również określić *nazwę* i parametry *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="f94ee-162">You must also specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="f94ee-163">Zestaw rekordów można też określić przy użyciu parametru *zestaw rekordów* albo *nazwy* i parametrów *strefy* .</span><span class="sxs-lookup"><span data-stu-id="f94ee-163">Alternatively, the record set can be specified using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="f94ee-164">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f94ee-164">-Confirm</span></span>
<span data-ttu-id="f94ee-165">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f94ee-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f94ee-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f94ee-166">-WhatIf</span></span>
<span data-ttu-id="f94ee-167">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f94ee-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f94ee-168">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f94ee-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f94ee-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f94ee-169">CommonParameters</span></span>
<span data-ttu-id="f94ee-170">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f94ee-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f94ee-171">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f94ee-171">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f94ee-172">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f94ee-172">INPUTS</span></span>

### <span data-ttu-id="f94ee-173">Microsoft. Azure. Management. DNS. MODELES. recordType</span><span class="sxs-lookup"><span data-stu-id="f94ee-173">Microsoft.Azure.Management.Dns.Models.RecordType</span></span>

### <span data-ttu-id="f94ee-174">System. String</span><span class="sxs-lookup"><span data-stu-id="f94ee-174">System.String</span></span>

### <span data-ttu-id="f94ee-175">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="f94ee-175">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="f94ee-176">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f94ee-176">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="f94ee-177">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f94ee-177">OUTPUTS</span></span>

### <span data-ttu-id="f94ee-178">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f94ee-178">System.Boolean</span></span>

## <span data-ttu-id="f94ee-179">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f94ee-179">NOTES</span></span>
<span data-ttu-id="f94ee-180">Za pomocą parametru *Confirm* można kontrolować, czy to polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f94ee-180">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="f94ee-181">Domyślnie polecenie cmdlet monituje o potwierdzenie, jeśli zmienna $ConfirmPreference Windows PowerShell ma wartość średnią lub niższą.</span><span class="sxs-lookup"><span data-stu-id="f94ee-181">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="f94ee-182">Jeśli określisz pozycję *Potwierdź* lub *Potwierdź: $true* , to polecenie cmdlet wyświetli monit o potwierdzenie przed jego uruchomieniem.</span><span class="sxs-lookup"><span data-stu-id="f94ee-182">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="f94ee-183">Jeśli określisz pozycję *Confirm (Potwierdź): $false* , polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f94ee-183">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="f94ee-184">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f94ee-184">RELATED LINKS</span></span>

[<span data-ttu-id="f94ee-185">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f94ee-185">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="f94ee-186">Nowe — AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f94ee-186">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="f94ee-187">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f94ee-187">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
