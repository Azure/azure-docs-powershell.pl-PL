---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/remove-azurermdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsRecordSet.md
ms.openlocfilehash: 129177c93d48b55cf8dfe5675d7ffc30ec7f46ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552095"
---
# <span data-ttu-id="24699-101">Remove-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="24699-101">Remove-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="24699-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="24699-102">SYNOPSIS</span></span>
<span data-ttu-id="24699-103">Usuwa zestaw rekordów.</span><span class="sxs-lookup"><span data-stu-id="24699-103">Deletes a record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24699-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="24699-104">SYNTAX</span></span>

### <span data-ttu-id="24699-105">Field</span><span class="sxs-lookup"><span data-stu-id="24699-105">Fields</span></span>
```
Remove-AzureRmDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24699-106">Karoten</span><span class="sxs-lookup"><span data-stu-id="24699-106">Mixed</span></span>
```
Remove-AzureRmDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24699-107">Stream</span><span class="sxs-lookup"><span data-stu-id="24699-107">Object</span></span>
```
Remove-AzureRmDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24699-108">Opis</span><span class="sxs-lookup"><span data-stu-id="24699-108">DESCRIPTION</span></span>
<span data-ttu-id="24699-109">Polecenie cmdlet **Remove-AzureRmDnsRecordSet** umożliwia usunięcie określonego zestawu rekordów z określonej strefy.</span><span class="sxs-lookup"><span data-stu-id="24699-109">The **Remove-AzureRmDnsRecordSet** cmdlet deletes the specified record set from the specified zone.</span></span>
<span data-ttu-id="24699-110">Nie można usuwać rekordów serwera SOA ani serwerów nazw (NS), które są tworzone automatycznie w strefie Apex.</span><span class="sxs-lookup"><span data-stu-id="24699-110">You cannot delete SOA or name server (NS) records that are automatically created at the zone apex.</span></span>
<span data-ttu-id="24699-111">Do tego polecenia cmdlet można przekazać obiekt **Recordset** za pomocą operatora potoku lub jako parametru.</span><span class="sxs-lookup"><span data-stu-id="24699-111">You can pass a **RecordSet** object to this cmdlet by using the pipeline operator or as a parameter.</span></span>
<span data-ttu-id="24699-112">Aby zidentyfikować zestaw rekordów i wpisać go bez użycia obiektu **Recordset** , należy przekazać strefę jako obiekt **dnsZone** do tego polecenia cmdlet, korzystając z operatora potoku lub jako parametru lub można też określić parametry *zonename* i *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="24699-112">To identify a record set by name and type without using a **RecordSet** object, you must pass the zone as a **DnsZone** object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="24699-113">Za pomocą zmiennej Confirm i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="24699-113">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="24699-114">Podczas określania zestawu rekordów za pomocą obiektu **Recordset** zestaw rekordów nie jest usuwany, jeśli został zmieniony w usłudze DNS Azure, ponieważ został pobrany lokalny obiekt **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="24699-114">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="24699-115">Zapewnia to ochronę współbieżnych zmian.</span><span class="sxs-lookup"><span data-stu-id="24699-115">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="24699-116">Można to pominąć, używając parametru *zastępowania* , który usuwa zestaw rekordów bez względu na zmiany współbieżne.</span><span class="sxs-lookup"><span data-stu-id="24699-116">You can suppress this by using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="24699-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="24699-117">EXAMPLES</span></span>

### <span data-ttu-id="24699-118">Przykład 1: usuwanie zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="24699-118">Example 1: Remove a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="24699-119">Pierwsze polecenie pobiera określony zestaw rekordów, a następnie zapisuje go w zmiennej $RecordSet. Drugie polecenie usuwa zestaw rekordów w $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="24699-119">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="24699-120">Przykład 2: usunięcie zestawu rekordów i pominięcie wszystkich potwierdzeń</span><span class="sxs-lookup"><span data-stu-id="24699-120">Example 2: Remove a record set and suppress all confirmation</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzureRmDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzureRmDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="24699-121">Pierwsze polecenie pobiera określony zestaw rekordów.</span><span class="sxs-lookup"><span data-stu-id="24699-121">The first command gets the specified record set.</span></span>
<span data-ttu-id="24699-122">Drugie polecenie usuwa zestaw rekordów, nawet jeśli został on zmieniony w międzyczasie.</span><span class="sxs-lookup"><span data-stu-id="24699-122">The second command deletes the record set, even if it has changed in the meantime.</span></span>
<span data-ttu-id="24699-123">Monity o potwierdzenie są pomijane.</span><span class="sxs-lookup"><span data-stu-id="24699-123">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="24699-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="24699-124">PARAMETERS</span></span>

### <span data-ttu-id="24699-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24699-125">-DefaultProfile</span></span>
<span data-ttu-id="24699-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="24699-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24699-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="24699-127">-Name</span></span>
<span data-ttu-id="24699-128">Określa nazwę **zestawu rekordów** , który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="24699-128">Specifies the name of the **RecordSet** to remove.</span></span>
<span data-ttu-id="24699-129">Podczas określania zestawu rekordów według nazwy strefa DNS musi być określona przy użyciu parametru *Zone* lub parametry *zonename* i *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="24699-129">When specifying the record set by name, the DNS zone must be specified using either the *Zone* parameter or the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="24699-130">Zestaw rekordów można też określić za pomocą obiektu **Recordset** , przekazano przy użyciu parametru *Recordset* .</span><span class="sxs-lookup"><span data-stu-id="24699-130">Alternatively, the record set can be specified using a **RecordSet** object, passed using the *RecordSet* parameter.</span></span>

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

### <span data-ttu-id="24699-131">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="24699-131">-Overwrite</span></span>
<span data-ttu-id="24699-132">Podczas określania zestawu rekordów za pomocą obiektu **Recordset** zestaw rekordów nie jest usuwany, jeśli został zmieniony w usłudze DNS Azure, ponieważ został pobrany lokalny obiekt **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="24699-132">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="24699-133">Zapewnia to ochronę współbieżnych zmian.</span><span class="sxs-lookup"><span data-stu-id="24699-133">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="24699-134">Można to pominąć za pomocą parametru *overwrite* , co powoduje usunięcie zestawu rekordów bez względu na jednoczesne zmiany.</span><span class="sxs-lookup"><span data-stu-id="24699-134">This can be suppressed using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="24699-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24699-135">-PassThru</span></span>
<span data-ttu-id="24699-136">passthru</span><span class="sxs-lookup"><span data-stu-id="24699-136">passthru</span></span>

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

### <span data-ttu-id="24699-137">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="24699-137">-RecordSet</span></span>
<span data-ttu-id="24699-138">Określa obiekt **zestawu rekordów** , który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="24699-138">Specifies the **RecordSet** object to remove.</span></span>
<span data-ttu-id="24699-139">Zestaw rekordów można też określić przy użyciu parametrów *name* i *Zone* albo za pomocą parametrów *name* , *zonename* i *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="24699-139">Alternatively, the record set can be specified using the *Name* and *Zone* parameters, or using the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="24699-140">-Records</span><span class="sxs-lookup"><span data-stu-id="24699-140">-RecordType</span></span>
<span data-ttu-id="24699-141">Określa typ rekordu DNS.</span><span class="sxs-lookup"><span data-stu-id="24699-141">Specifies the type of DNS record.</span></span>
<span data-ttu-id="24699-142">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="24699-142">Valid values are:</span></span>
- <span data-ttu-id="24699-143">Sieci</span><span class="sxs-lookup"><span data-stu-id="24699-143">A</span></span>
- <span data-ttu-id="24699-144">AAAA</span><span class="sxs-lookup"><span data-stu-id="24699-144">AAAA</span></span>
- <span data-ttu-id="24699-145">REKORD</span><span class="sxs-lookup"><span data-stu-id="24699-145">CNAME</span></span>
- <span data-ttu-id="24699-146">MX</span><span class="sxs-lookup"><span data-stu-id="24699-146">MX</span></span>
- <span data-ttu-id="24699-147">REKORDU</span><span class="sxs-lookup"><span data-stu-id="24699-147">NS</span></span>
- <span data-ttu-id="24699-148">SYSTEMU</span><span class="sxs-lookup"><span data-stu-id="24699-148">PTR</span></span>
- <span data-ttu-id="24699-149">SRV</span><span class="sxs-lookup"><span data-stu-id="24699-149">SRV</span></span>
- <span data-ttu-id="24699-150">Rekordy SOA (TXT) są usuwane automatycznie po usunięciu strefy.</span><span class="sxs-lookup"><span data-stu-id="24699-150">TXT SOA records are deleted automatically when the zone is deleted.</span></span>
<span data-ttu-id="24699-151">Nie można ręcznie usunąć rekordów SOA.</span><span class="sxs-lookup"><span data-stu-id="24699-151">You cannot manually delete SOA records.</span></span>

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

### <span data-ttu-id="24699-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24699-152">-ResourceGroupName</span></span>
<span data-ttu-id="24699-153">Określa grupę zasobów zawierającą strefę DNS zawierającą **zestaw rekordów** do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="24699-153">Specifies the resource group that contains the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="24699-154">Ten parametr jest stosowany tylko wtedy, gdy zestaw rekordów i strefa DNS są określone przy użyciu parametrów *name* i *zonename* .</span><span class="sxs-lookup"><span data-stu-id="24699-154">This parameter is applicable only when the record set and DNS zone are specified using the *Name* and *ZoneName* parameters.</span></span>
<span data-ttu-id="24699-155">Możesz też określić zestaw rekordów przy użyciu parametru *zestaw rekordów* lub *nazwy* i parametrów *strefy* .</span><span class="sxs-lookup"><span data-stu-id="24699-155">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="24699-156">-Zone</span><span class="sxs-lookup"><span data-stu-id="24699-156">-Zone</span></span>
<span data-ttu-id="24699-157">Określa strefę DNS zawierającą **zestaw rekordów** do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="24699-157">Specifies the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="24699-158">Ten parametr ma zastosowanie tylko podczas określania zestawu rekordów przy użyciu parametru *name* .</span><span class="sxs-lookup"><span data-stu-id="24699-158">This parameter is applicable only when specifying the record set using the *Name* parameter.</span></span>
<span data-ttu-id="24699-159">Możesz też określić zestaw rekordów przy użyciu parametru *zestaw rekordów* albo parametrów *name* , *zonename* i *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="24699-159">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="24699-160">-Nazwa_strefy</span><span class="sxs-lookup"><span data-stu-id="24699-160">-ZoneName</span></span>
<span data-ttu-id="24699-161">Określa nazwę strefy zawierającej **zestaw rekordów** do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="24699-161">Specifies the name of the zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="24699-162">Musisz również określić *nazwę* i parametry *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="24699-162">You must also specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="24699-163">Zestaw rekordów można też określić przy użyciu parametru *zestaw rekordów* albo *nazwy* i parametrów *strefy* .</span><span class="sxs-lookup"><span data-stu-id="24699-163">Alternatively, the record set can be specified using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="24699-164">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="24699-164">-Confirm</span></span>
<span data-ttu-id="24699-165">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24699-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24699-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24699-166">-WhatIf</span></span>
<span data-ttu-id="24699-167">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24699-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24699-168">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="24699-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24699-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24699-169">CommonParameters</span></span>
<span data-ttu-id="24699-170">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24699-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24699-171">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24699-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24699-172">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24699-172">INPUTS</span></span>

### <span data-ttu-id="24699-173">Microsoft. Azure. Management. DNS. MODELES. recordType</span><span class="sxs-lookup"><span data-stu-id="24699-173">Microsoft.Azure.Management.Dns.Models.RecordType</span></span>

### <span data-ttu-id="24699-174">System. String</span><span class="sxs-lookup"><span data-stu-id="24699-174">System.String</span></span>

### <span data-ttu-id="24699-175">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="24699-175">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="24699-176">Parametry: Zone (ByValue)</span><span class="sxs-lookup"><span data-stu-id="24699-176">Parameters: Zone (ByValue)</span></span>

### <span data-ttu-id="24699-177">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="24699-177">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="24699-178">Parametry: zestaw rekordów (ByValue)</span><span class="sxs-lookup"><span data-stu-id="24699-178">Parameters: RecordSet (ByValue)</span></span>

## <span data-ttu-id="24699-179">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="24699-179">OUTPUTS</span></span>

### <span data-ttu-id="24699-180">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="24699-180">System.Boolean</span></span>

## <span data-ttu-id="24699-181">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="24699-181">NOTES</span></span>
<span data-ttu-id="24699-182">Za pomocą parametru *Confirm* można kontrolować, czy to polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="24699-182">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="24699-183">Domyślnie polecenie cmdlet monituje o potwierdzenie, jeśli zmienna $ConfirmPreference Windows PowerShell ma wartość średnią lub niższą.</span><span class="sxs-lookup"><span data-stu-id="24699-183">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="24699-184">Jeśli określisz pozycję *Potwierdź* lub *Potwierdź: $true* , to polecenie cmdlet wyświetli monit o potwierdzenie przed jego uruchomieniem.</span><span class="sxs-lookup"><span data-stu-id="24699-184">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="24699-185">Jeśli określisz pozycję *Confirm (Potwierdź): $false* , polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="24699-185">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="24699-186">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="24699-186">RELATED LINKS</span></span>

[<span data-ttu-id="24699-187">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="24699-187">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="24699-188">Nowe — AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="24699-188">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="24699-189">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="24699-189">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)
