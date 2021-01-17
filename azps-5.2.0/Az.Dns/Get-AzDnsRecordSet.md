---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
ms.openlocfilehash: b64432364b9c86a1153ba9a535d70645cf15d4d1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346897"
---
# <span data-ttu-id="e2e66-101">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="e2e66-101">Get-AzDnsRecordSet</span></span>

## <span data-ttu-id="e2e66-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e2e66-102">SYNOPSIS</span></span>
<span data-ttu-id="e2e66-103">Pobiera zestaw rekordów DNS.</span><span class="sxs-lookup"><span data-stu-id="e2e66-103">Gets a DNS record set.</span></span>

## <span data-ttu-id="e2e66-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e2e66-104">SYNTAX</span></span>

### <span data-ttu-id="e2e66-105">Field</span><span class="sxs-lookup"><span data-stu-id="e2e66-105">Fields</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2e66-106">Stream</span><span class="sxs-lookup"><span data-stu-id="e2e66-106">Object</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2e66-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e2e66-107">DESCRIPTION</span></span>
<span data-ttu-id="e2e66-108">Polecenie cmdlet **Get-AzDnsRecordSet** Pobiera zestaw rekordów DNS (Domain Name System) o określonej nazwie i typie w określonej strefie.</span><span class="sxs-lookup"><span data-stu-id="e2e66-108">The **Get-AzDnsRecordSet** cmdlet gets the Domain Name System (DNS) record set with the specified name and type, in the specified zone.</span></span>
<span data-ttu-id="e2e66-109">Jeśli nie określisz parametrów *name* lub *recordType* , to polecenie cmdlet zwróci wszystkie zestawy rekordów określonego typu w strefie.</span><span class="sxs-lookup"><span data-stu-id="e2e66-109">If you do not specify the *Name* or *RecordType* parameters, this cmdlet returns all record sets of the specified type in the zone.</span></span>
<span data-ttu-id="e2e66-110">Jeśli określisz parametr *recordType* , a nie parametr *name* , to polecenie cmdlet zwróci wszystkie zestawy rekordów określonego typu rekordu.</span><span class="sxs-lookup"><span data-stu-id="e2e66-110">If you specify the *RecordType* parameter but not the *Name* parameter, this cmdlet returns all record sets of the specified record type.</span></span>
<span data-ttu-id="e2e66-111">Za pomocą operatora potoku można przekazać obiekt **dnsZone** do tego polecenia cmdlet lub przekazać obiekt **dnsZone** jako parametr *Zone* lub można też określić nazwę strefy i grupy zasobów według nazwy.</span><span class="sxs-lookup"><span data-stu-id="e2e66-111">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone and resource group by name.</span></span>

## <span data-ttu-id="e2e66-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e2e66-112">EXAMPLES</span></span>

### <span data-ttu-id="e2e66-113">Przykład 1: pobieranie zestawów rekordów o określonej nazwie i typie</span><span class="sxs-lookup"><span data-stu-id="e2e66-113">Example 1: Get record sets with a specified name and type</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

<span data-ttu-id="e2e66-114">To polecenie pobiera zestaw rekordów typu rekordu o nazwie www w określonej grupie zasobów i strefie, a następnie zapisuje go w zmiennej $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="e2e66-114">This command gets the record set of record type A named www in the specified resource group and zone, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="e2e66-115">Ponieważ określono parametry *name* i *recordType* , zwracany jest tylko pojedynczy obiekt **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="e2e66-115">Because the *Name* and *RecordType* parameters are specified, only one **RecordSet** object is returned.</span></span>

### <span data-ttu-id="e2e66-116">Przykład 2: pobieranie zestawów rekordów określonego typu</span><span class="sxs-lookup"><span data-stu-id="e2e66-116">Example 2: Get record sets of a specified type</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

<span data-ttu-id="e2e66-117">To polecenie pobiera tablicę wszystkich zestawów rekordów typu rekord A w strefie o nazwie myzone.com w grupie zasób o nazwie Moja zasobów, a następnie zapisuje je w zmiennej $RecordSets.</span><span class="sxs-lookup"><span data-stu-id="e2e66-117">This command gets an array of all record sets of record type A in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="e2e66-118">Przykład 3: pobieranie wszystkich zestawów rekordów w strefie</span><span class="sxs-lookup"><span data-stu-id="e2e66-118">Example 3: Get all record sets in a zone</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

<span data-ttu-id="e2e66-119">To polecenie pobiera tablicę wszystkich zestawów rekordów w strefie o nazwie myzone.com w grupie zasób o nazwie moja grupa, a następnie zapisuje je w zmiennej $RecordSets.</span><span class="sxs-lookup"><span data-stu-id="e2e66-119">This command gets an array of all record sets in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="e2e66-120">Przykład 4: pobieranie wszystkich zestawów rekordów w strefie przy użyciu obiektu DnsZone</span><span class="sxs-lookup"><span data-stu-id="e2e66-120">Example 4: Get all record sets in a zone, using a DnsZone object</span></span>
```
PS C:\> $Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzDnsRecordSet -Zone $Zone
```

<span data-ttu-id="e2e66-121">Ten przykład jest równoważny przykładowi 3 powyżej.</span><span class="sxs-lookup"><span data-stu-id="e2e66-121">This example is equivalent to Example 3 above.</span></span>
<span data-ttu-id="e2e66-122">W tym czasie strefa jest określana za pomocą obiektu strefy.</span><span class="sxs-lookup"><span data-stu-id="e2e66-122">This time, the zone is specified using a zone object.</span></span>

## <span data-ttu-id="e2e66-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e2e66-123">PARAMETERS</span></span>

### <span data-ttu-id="e2e66-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2e66-124">-DefaultProfile</span></span>
<span data-ttu-id="e2e66-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e2e66-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2e66-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e2e66-126">-Name</span></span>
<span data-ttu-id="e2e66-127">Określa nazwę **zestawu rekordów** , który ma zostać wyświetlony.</span><span class="sxs-lookup"><span data-stu-id="e2e66-127">Specifies the name of the **RecordSet** to get.</span></span>
<span data-ttu-id="e2e66-128">Jeśli parametr *name* nie jest określony, zwracane są wszystkie zestawy rekordów określonego typu.</span><span class="sxs-lookup"><span data-stu-id="e2e66-128">If you do not specify the *Name* parameter, all record sets of the specified type are returned.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e66-129">-Records</span><span class="sxs-lookup"><span data-stu-id="e2e66-129">-RecordType</span></span>
<span data-ttu-id="e2e66-130">Określa typ rekordu DNS, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2e66-130">Specifies the type of DNS record that this cmdlet gets.</span></span>
<span data-ttu-id="e2e66-131">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="e2e66-131">Valid values are:</span></span> 
- <span data-ttu-id="e2e66-132">Sieci</span><span class="sxs-lookup"><span data-stu-id="e2e66-132">A</span></span>
- <span data-ttu-id="e2e66-133">AAAA</span><span class="sxs-lookup"><span data-stu-id="e2e66-133">AAAA</span></span>
- <span data-ttu-id="e2e66-134">REKORD</span><span class="sxs-lookup"><span data-stu-id="e2e66-134">CNAME</span></span>
- <span data-ttu-id="e2e66-135">MX</span><span class="sxs-lookup"><span data-stu-id="e2e66-135">MX</span></span>
- <span data-ttu-id="e2e66-136">REKORDU</span><span class="sxs-lookup"><span data-stu-id="e2e66-136">NS</span></span>
- <span data-ttu-id="e2e66-137">SYSTEMU</span><span class="sxs-lookup"><span data-stu-id="e2e66-137">PTR</span></span>
- <span data-ttu-id="e2e66-138">REKORD</span><span class="sxs-lookup"><span data-stu-id="e2e66-138">SOA</span></span>
- <span data-ttu-id="e2e66-139">SRV</span><span class="sxs-lookup"><span data-stu-id="e2e66-139">SRV</span></span>
- <span data-ttu-id="e2e66-140">TXT Jeśli parametr *recordType* nie jest określony, należy także pominąć parametr *name* .</span><span class="sxs-lookup"><span data-stu-id="e2e66-140">TXT If you do not specify the *RecordType* parameter, you must also omit the *Name* parameter.</span></span> <span data-ttu-id="e2e66-141">To polecenie cmdlet zwraca następnie wszystkie zestawy rekordów w strefie (wszystkie nazwy i typy).</span><span class="sxs-lookup"><span data-stu-id="e2e66-141">This cmdlet then returns all record sets in the zone (of all names and types).</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Dns.Models.RecordType]
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2e66-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2e66-142">-ResourceGroupName</span></span>
<span data-ttu-id="e2e66-143">Określa grupę zasobów zawierającą strefę DNS.</span><span class="sxs-lookup"><span data-stu-id="e2e66-143">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="e2e66-144">Nazwę strefy należy również określić przy użyciu parametru *zonename* .</span><span class="sxs-lookup"><span data-stu-id="e2e66-144">The zone name must also be specified, using the *ZoneName* parameter.</span></span>
<span data-ttu-id="e2e66-145">Możesz też określić strefę i grupę zasobów, przechodząc do obiektu **dnsZone** przy użyciu parametru *Zone* .</span><span class="sxs-lookup"><span data-stu-id="e2e66-145">Alternatively, you can specify the zone and resource group by passing in a **DnsZone** object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="e2e66-146">-Zone</span><span class="sxs-lookup"><span data-stu-id="e2e66-146">-Zone</span></span>
<span data-ttu-id="e2e66-147">Określa strefę DNS zawierającą zestaw rekordów, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2e66-147">Specifies the DNS zone that contains the record set that this cmdlet gets.</span></span>
<span data-ttu-id="e2e66-148">Możesz też określić strefę przy użyciu parametrów *zonename* i *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="e2e66-148">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="e2e66-149">-Nazwa_strefy</span><span class="sxs-lookup"><span data-stu-id="e2e66-149">-ZoneName</span></span>
<span data-ttu-id="e2e66-150">Określa nazwę strefy DNS zawierającej zestaw rekordów do pobrania.</span><span class="sxs-lookup"><span data-stu-id="e2e66-150">Specifies the name of the DNS zone that contains the record set to get.</span></span>
<span data-ttu-id="e2e66-151">Grupa zasobów zawierająca strefę musi być również określona przy użyciu parametru *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="e2e66-151">The resource group containing the zone must also be specified, using the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="e2e66-152">Możesz też określić strefę i grupę zasobów, przechodząc do obiektu strefy DNS przy użyciu parametru *Zone* .</span><span class="sxs-lookup"><span data-stu-id="e2e66-152">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="e2e66-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2e66-153">CommonParameters</span></span>
<span data-ttu-id="e2e66-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2e66-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2e66-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2e66-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2e66-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e2e66-156">INPUTS</span></span>

### <span data-ttu-id="e2e66-157">System. String</span><span class="sxs-lookup"><span data-stu-id="e2e66-157">System.String</span></span>

### <span data-ttu-id="e2e66-158">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="e2e66-158">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="e2e66-159">System. Nullable "1 [[Microsoft. Azure. Management. DNS. models. Records, Microsoft. Azure. Management. DNS, Version = 3.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="e2e66-159">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.RecordType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="e2e66-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e2e66-160">OUTPUTS</span></span>

### <span data-ttu-id="e2e66-161">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="e2e66-161">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="e2e66-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e2e66-162">NOTES</span></span>

## <span data-ttu-id="e2e66-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e2e66-163">RELATED LINKS</span></span>

[<span data-ttu-id="e2e66-164">Nowe — AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="e2e66-164">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="e2e66-165">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="e2e66-165">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

[<span data-ttu-id="e2e66-166">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="e2e66-166">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)


