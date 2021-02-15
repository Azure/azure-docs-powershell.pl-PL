---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
ms.openlocfilehash: f5d7075322bb2b5a4b61635400664f0e909f126d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180747"
---
# <span data-ttu-id="1715d-101">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="1715d-101">Remove-AzDnsRecordSet</span></span>

## <span data-ttu-id="1715d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1715d-102">SYNOPSIS</span></span>
<span data-ttu-id="1715d-103">Usuwa zestaw rekordów.</span><span class="sxs-lookup"><span data-stu-id="1715d-103">Deletes a record set.</span></span>

## <span data-ttu-id="1715d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1715d-104">SYNTAX</span></span>

### <span data-ttu-id="1715d-105">Pola</span><span class="sxs-lookup"><span data-stu-id="1715d-105">Fields</span></span>
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String> -ResourceGroupName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1715d-106">Mieszany</span><span class="sxs-lookup"><span data-stu-id="1715d-106">Mixed</span></span>
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1715d-107">Obiekt</span><span class="sxs-lookup"><span data-stu-id="1715d-107">Object</span></span>
```
Remove-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1715d-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="1715d-108">DESCRIPTION</span></span>
<span data-ttu-id="1715d-109">Polecenie **cmdlet Remove-AzDnsRecordSet** usuwa określony zestaw rekordów z określonej strefy.</span><span class="sxs-lookup"><span data-stu-id="1715d-109">The **Remove-AzDnsRecordSet** cmdlet deletes the specified record set from the specified zone.</span></span>
<span data-ttu-id="1715d-110">Nie można usuwać rekordów SOA ani nazw serwera nazw, które są automatycznie tworzone w wierzchołku strefy.</span><span class="sxs-lookup"><span data-stu-id="1715d-110">You cannot delete SOA or name server (NS) records that are automatically created at the zone apex.</span></span>
<span data-ttu-id="1715d-111">Obiekt **RecordSet** można przekazać do tego polecenia cmdlet, używając operatora potoku lub parametru.</span><span class="sxs-lookup"><span data-stu-id="1715d-111">You can pass a **RecordSet** object to this cmdlet by using the pipeline operator or as a parameter.</span></span>
<span data-ttu-id="1715d-112">Aby zidentyfikować zestaw rekordów według nazwy i typu bez użycia obiektu **RecordSet,** należy przekazać strefę jako obiekt **DnsZone** do tego polecenia cmdlet przy użyciu operatora potoku lub parametru albo określić parametry *ZoneName* i *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="1715d-112">To identify a record set by name and type without using a **RecordSet** object, you must pass the zone as a **DnsZone** object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="1715d-113">Możesz użyć parametru Confirm i $ConfirmPreference zmienną programu Windows PowerShell, aby określić, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1715d-113">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="1715d-114">Podczas określania zestawu rekordów przy użyciu obiektu **RecordSet** zestaw rekordów nie jest usuwany, jeśli został zmieniony w systemie Azure DNS od czasu pobrania lokalnego obiektu **RecordSet.**</span><span class="sxs-lookup"><span data-stu-id="1715d-114">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="1715d-115">Zapewnia to ochronę w przypadku jednoczesnych zmian.</span><span class="sxs-lookup"><span data-stu-id="1715d-115">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="1715d-116">Można to pominąć przy użyciu *parametru Zastąp,* który usuwa zestaw rekordów niezależnie od jednoczesnych zmian.</span><span class="sxs-lookup"><span data-stu-id="1715d-116">You can suppress this by using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="1715d-117">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1715d-117">EXAMPLES</span></span>

### <span data-ttu-id="1715d-118">Przykład 1. Usuwanie zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="1715d-118">Example 1: Remove a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="1715d-119">Pierwsze polecenie pobiera określony zestaw rekordów, a następnie zapisuje go w $RecordSet zmienną. Drugie polecenie usuwa zestaw rekordów z $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="1715d-119">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="1715d-120">Przykład 2. Usuwanie zestawu rekordów i pomijanie wszystkich potwierdzeń</span><span class="sxs-lookup"><span data-stu-id="1715d-120">Example 2: Remove a record set and suppress all confirmation</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="1715d-121">Pierwsze polecenie pobiera określony zestaw rekordów.</span><span class="sxs-lookup"><span data-stu-id="1715d-121">The first command gets the specified record set.</span></span>
<span data-ttu-id="1715d-122">Drugie polecenie usuwa zestaw rekordów, nawet jeśli zmienił się w międzyczasie.</span><span class="sxs-lookup"><span data-stu-id="1715d-122">The second command deletes the record set, even if it has changed in the meantime.</span></span>
<span data-ttu-id="1715d-123">Monity o potwierdzenie są pomijane.</span><span class="sxs-lookup"><span data-stu-id="1715d-123">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="1715d-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1715d-124">PARAMETERS</span></span>

### <span data-ttu-id="1715d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1715d-125">-DefaultProfile</span></span>
<span data-ttu-id="1715d-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="1715d-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1715d-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1715d-127">-Name</span></span>
<span data-ttu-id="1715d-128">Określa nazwę zestawu rekordów **do** usunięcia.</span><span class="sxs-lookup"><span data-stu-id="1715d-128">Specifies the name of the **RecordSet** to remove.</span></span>
<span data-ttu-id="1715d-129">Podczas określania rekordu ustawionego według nazwy należy określić strefę DNS przy użyciu parametrów *Zone* lub *ZoneName* i *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="1715d-129">When specifying the record set by name, the DNS zone must be specified using either the *Zone* parameter or the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="1715d-130">Ewentualnie zestaw rekordów można określić przy użyciu obiektu **RecordSet** przekazywanego przy użyciu *parametru RecordSet.*</span><span class="sxs-lookup"><span data-stu-id="1715d-130">Alternatively, the record set can be specified using a **RecordSet** object, passed using the *RecordSet* parameter.</span></span>

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

### <span data-ttu-id="1715d-131">— Zastąp</span><span class="sxs-lookup"><span data-stu-id="1715d-131">-Overwrite</span></span>
<span data-ttu-id="1715d-132">Podczas określania zestawu rekordów przy użyciu obiektu **RecordSet** zestaw rekordów nie jest usuwany, jeśli został zmieniony w systemie Azure DNS od czasu pobrania lokalnego obiektu **RecordSet.**</span><span class="sxs-lookup"><span data-stu-id="1715d-132">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="1715d-133">Zapewnia to ochronę w przypadku jednoczesnych zmian.</span><span class="sxs-lookup"><span data-stu-id="1715d-133">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="1715d-134">Można to pominąć przy użyciu *parametru Zastąp,* który usuwa zestaw rekordów niezależnie od jednoczesnych zmian.</span><span class="sxs-lookup"><span data-stu-id="1715d-134">This can be suppressed using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="1715d-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1715d-135">-PassThru</span></span>
<span data-ttu-id="1715d-136">passthru</span><span class="sxs-lookup"><span data-stu-id="1715d-136">passthru</span></span>

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

### <span data-ttu-id="1715d-137">- RecordSet</span><span class="sxs-lookup"><span data-stu-id="1715d-137">-RecordSet</span></span>
<span data-ttu-id="1715d-138">Określa obiekt **RecordSet** do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="1715d-138">Specifies the **RecordSet** object to remove.</span></span>
<span data-ttu-id="1715d-139">Można również określić zestaw rekordów za  pomocą  parametrów Nazwa i Strefa lub przy użyciu parametrów *Nazwa,* Nazwa Strefy *i* *NazwaGrupy Zasobów.*</span><span class="sxs-lookup"><span data-stu-id="1715d-139">Alternatively, the record set can be specified using the *Name* and *Zone* parameters, or using the *Name*, *ZoneName*, and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="1715d-140">-RecordType</span><span class="sxs-lookup"><span data-stu-id="1715d-140">-RecordType</span></span>
<span data-ttu-id="1715d-141">Określa typ rekordu DNS.</span><span class="sxs-lookup"><span data-stu-id="1715d-141">Specifies the type of DNS record.</span></span>
<span data-ttu-id="1715d-142">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="1715d-142">Valid values are:</span></span>
- <span data-ttu-id="1715d-143">A</span><span class="sxs-lookup"><span data-stu-id="1715d-143">A</span></span>
- <span data-ttu-id="1715d-144">AAAA</span><span class="sxs-lookup"><span data-stu-id="1715d-144">AAAA</span></span>
- <span data-ttu-id="1715d-145">CNAME</span><span class="sxs-lookup"><span data-stu-id="1715d-145">CNAME</span></span>
- <span data-ttu-id="1715d-146">MX</span><span class="sxs-lookup"><span data-stu-id="1715d-146">MX</span></span>
- <span data-ttu-id="1715d-147">NS</span><span class="sxs-lookup"><span data-stu-id="1715d-147">NS</span></span>
- <span data-ttu-id="1715d-148">PTR</span><span class="sxs-lookup"><span data-stu-id="1715d-148">PTR</span></span>
- <span data-ttu-id="1715d-149">SRV</span><span class="sxs-lookup"><span data-stu-id="1715d-149">SRV</span></span>
- <span data-ttu-id="1715d-150">Rekordy TXT SOA są usuwane automatycznie po usunięciu strefy.</span><span class="sxs-lookup"><span data-stu-id="1715d-150">TXT SOA records are deleted automatically when the zone is deleted.</span></span>
<span data-ttu-id="1715d-151">Nie można ręcznie usuwać rekordów SOA.</span><span class="sxs-lookup"><span data-stu-id="1715d-151">You cannot manually delete SOA records.</span></span>

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

### <span data-ttu-id="1715d-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1715d-152">-ResourceGroupName</span></span>
<span data-ttu-id="1715d-153">Określa grupę zasobów zawierającą strefę DNS zawierającą **zestaw rekordów do** usunięcia.</span><span class="sxs-lookup"><span data-stu-id="1715d-153">Specifies the resource group that contains the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="1715d-154">Ten parametr ma zastosowanie tylko wtedy, gdy zestaw rekordów i strefa DNS są określone przy użyciu *parametrów Name (Nazwa)* *i ZoneName (Nazwa strefy).*</span><span class="sxs-lookup"><span data-stu-id="1715d-154">This parameter is applicable only when the record set and DNS zone are specified using the *Name* and *ZoneName* parameters.</span></span>
<span data-ttu-id="1715d-155">Możesz również określić zestaw rekordów, używając parametru *RecordSet* lub *parametrów Name* i *Zone.*</span><span class="sxs-lookup"><span data-stu-id="1715d-155">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="1715d-156">— Strefa</span><span class="sxs-lookup"><span data-stu-id="1715d-156">-Zone</span></span>
<span data-ttu-id="1715d-157">Określa strefę DNS zawierającą **zestaw rekordów do** usunięcia.</span><span class="sxs-lookup"><span data-stu-id="1715d-157">Specifies the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="1715d-158">Ten parametr ma zastosowanie tylko podczas określania zestawu rekordów przy użyciu *parametru Name.*</span><span class="sxs-lookup"><span data-stu-id="1715d-158">This parameter is applicable only when specifying the record set using the *Name* parameter.</span></span>
<span data-ttu-id="1715d-159">Możesz również określić zestaw rekordów za pomocą parametru *RecordSet* lub *parametrów Name* *(Nazwa* strefy) i *ResourceGroupName (Nazwa strefy) i ResourceGroupName (Nazwa* Grupy Zasobów).</span><span class="sxs-lookup"><span data-stu-id="1715d-159">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name*, *ZoneName*, and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="1715d-160">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="1715d-160">-ZoneName</span></span>
<span data-ttu-id="1715d-161">Określa nazwę strefy zawierającej zestaw **rekordów do** usunięcia.</span><span class="sxs-lookup"><span data-stu-id="1715d-161">Specifies the name of the zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="1715d-162">Należy także określić parametry *Name (Nazwa) i* *ResourceGroupName (Nazwa grupy zasobów).*</span><span class="sxs-lookup"><span data-stu-id="1715d-162">You must also specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="1715d-163">Ewentualnie zestaw rekordów można określić za pomocą parametru *RecordSet* lub *parametrów Name* i *Zone.*</span><span class="sxs-lookup"><span data-stu-id="1715d-163">Alternatively, the record set can be specified using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="1715d-164">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1715d-164">-Confirm</span></span>
<span data-ttu-id="1715d-165">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1715d-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1715d-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1715d-166">-WhatIf</span></span>
<span data-ttu-id="1715d-167">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1715d-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1715d-168">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1715d-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1715d-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1715d-169">CommonParameters</span></span>
<span data-ttu-id="1715d-170">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1715d-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1715d-171">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1715d-171">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1715d-172">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1715d-172">INPUTS</span></span>

### <span data-ttu-id="1715d-173">Microsoft.Azure.Management.Dns.Models.RecordType</span><span class="sxs-lookup"><span data-stu-id="1715d-173">Microsoft.Azure.Management.Dns.Models.RecordType</span></span>

### <span data-ttu-id="1715d-174">System.String</span><span class="sxs-lookup"><span data-stu-id="1715d-174">System.String</span></span>

### <span data-ttu-id="1715d-175">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="1715d-175">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="1715d-176">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="1715d-176">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="1715d-177">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1715d-177">OUTPUTS</span></span>

### <span data-ttu-id="1715d-178">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1715d-178">System.Boolean</span></span>

## <span data-ttu-id="1715d-179">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1715d-179">NOTES</span></span>
<span data-ttu-id="1715d-180">Za pomocą *parametru Confirm* można określić, czy to polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1715d-180">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="1715d-181">Domyślnie polecenie cmdlet wyświetla monit o potwierdzenie, jeśli zmienna programu Windows PowerShell $ConfirmPreference wartość średnią lub niższą.</span><span class="sxs-lookup"><span data-stu-id="1715d-181">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="1715d-182">Jeśli określisz *potwierdź* *lub potwierdź:$True,* to polecenie cmdlet wyświetli monit o potwierdzenie przed jego rozpoczęciem.</span><span class="sxs-lookup"><span data-stu-id="1715d-182">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="1715d-183">Jeśli określisz *polecenie Potwierdź:$False,* polecenie cmdlet nie wyświetli monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1715d-183">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="1715d-184">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1715d-184">RELATED LINKS</span></span>

[<span data-ttu-id="1715d-185">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="1715d-185">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="1715d-186">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="1715d-186">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="1715d-187">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="1715d-187">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
