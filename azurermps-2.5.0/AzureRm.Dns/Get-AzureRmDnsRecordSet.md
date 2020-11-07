---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4027b13fb398d69bee09be5c0a939ff86a099e39
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898930"
---
# <span data-ttu-id="b0ffb-101">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b0ffb-101">Get-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="b0ffb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b0ffb-102">SYNOPSIS</span></span>
<span data-ttu-id="b0ffb-103">Pobiera zestaw rekordów DNS.</span><span class="sxs-lookup"><span data-stu-id="b0ffb-103">Gets a DNS record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0ffb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b0ffb-104">SYNTAX</span></span>

### <span data-ttu-id="b0ffb-105">Field</span><span class="sxs-lookup"><span data-stu-id="b0ffb-105">Fields</span></span>
```
Get-AzureRmDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String>
 [-RecordType <RecordType>] [<CommonParameters>]
```

### <span data-ttu-id="b0ffb-106">Stream</span><span class="sxs-lookup"><span data-stu-id="b0ffb-106">Object</span></span>
```
Get-AzureRmDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>] [<CommonParameters>]
```

## <span data-ttu-id="b0ffb-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b0ffb-107">DESCRIPTION</span></span>
<span data-ttu-id="b0ffb-108">Polecenie cmdlet **Get-AzureRmDnsRecordSet** Pobiera zestaw rekordów DNS (Domain Name System) o określonej nazwie i typie w określonej strefie.</span><span class="sxs-lookup"><span data-stu-id="b0ffb-108">The **Get-AzureRmDnsRecordSet** cmdlet gets the Domain Name System (DNS) record set with the specified name and type, in the specified zone.</span></span>

<span data-ttu-id="b0ffb-109">Jeśli nie określisz parametrów *name* lub *recordType* , to polecenie cmdlet zwróci wszystkie zestawy rekordów określonego typu w strefie.</span><span class="sxs-lookup"><span data-stu-id="b0ffb-109">If you do not specify the *Name* or *RecordType* parameters, this cmdlet returns all record sets of the specified type in the zone.</span></span>
<span data-ttu-id="b0ffb-110">Jeśli określisz parametr *recordType* , a nie parametr *name* , to polecenie cmdlet zwróci wszystkie zestawy rekordów określonego typu rekordu.</span><span class="sxs-lookup"><span data-stu-id="b0ffb-110">If you specify the *RecordType* parameter but not the *Name* parameter, this cmdlet returns all record sets of the specified record type.</span></span>

<span data-ttu-id="b0ffb-111">Za pomocą operatora potoku można przekazać obiekt **dnsZone** do tego polecenia cmdlet lub przekazać obiekt **dnsZone** jako parametr *Zone* lub można też określić nazwę strefy i grupy zasobów według nazwy.</span><span class="sxs-lookup"><span data-stu-id="b0ffb-111">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone and resource group by name.</span></span>

## <span data-ttu-id="b0ffb-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b0ffb-112">EXAMPLES</span></span>

### <span data-ttu-id="b0ffb-113">Przykład 1: pobieranie zestawów rekordów o określonej nazwie i typie</span><span class="sxs-lookup"><span data-stu-id="b0ffb-113">Example 1: Get record sets with a specified name and type</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

<span data-ttu-id="b0ffb-114">To polecenie pobiera zestaw rekordów typu rekordu o nazwie www w określonej grupie zasobów i strefie, a następnie zapisuje go w zmiennej $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="b0ffb-114">This command gets the record set of record type A named www in the specified resource group and zone, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="b0ffb-115">Ponieważ określono parametry *name* i *recordType* , zwracany jest tylko pojedynczy obiekt **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="b0ffb-115">Because the *Name* and *RecordType* parameters are specified, only one **RecordSet** object is returned.</span></span>

### <span data-ttu-id="b0ffb-116">Przykład 2: pobieranie zestawów rekordów określonego typu</span><span class="sxs-lookup"><span data-stu-id="b0ffb-116">Example 2: Get record sets of a specified type</span></span>
```
PS C:\>$RecordSets = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

<span data-ttu-id="b0ffb-117">To polecenie pobiera tablicę wszystkich zestawów rekordów typu rekord A w strefie o nazwie myzone.com w grupie zasób o nazwie Moja zasobów, a następnie zapisuje je w zmiennej $RecordSets.</span><span class="sxs-lookup"><span data-stu-id="b0ffb-117">This command gets an array of all record sets of record type A in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="b0ffb-118">Przykład 3: pobieranie wszystkich zestawów rekordów w strefie</span><span class="sxs-lookup"><span data-stu-id="b0ffb-118">Example 3: Get all record sets in a zone</span></span>
```
PS C:\>$RecordSets = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

<span data-ttu-id="b0ffb-119">To polecenie pobiera tablicę wszystkich zestawów rekordów w strefie o nazwie myzone.com w grupie zasób o nazwie moja grupa, a następnie zapisuje je w zmiennej $RecordSets.</span><span class="sxs-lookup"><span data-stu-id="b0ffb-119">This command gets an array of all record sets in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="b0ffb-120">Przykład 4: pobieranie wszystkich zestawów rekordów w strefie przy użyciu obiektu DnsZone</span><span class="sxs-lookup"><span data-stu-id="b0ffb-120">Example 4: Get all record sets in a zone, using a DnsZone object</span></span>
```
PS C:\> $Zone = Get-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzureRmDnsRecordSet -Zone $Zone
```

<span data-ttu-id="b0ffb-121">Ten przykład jest równoważny przykładowi 3 powyżej.</span><span class="sxs-lookup"><span data-stu-id="b0ffb-121">This example is equivalent to Example 3 above.</span></span>
<span data-ttu-id="b0ffb-122">W tym czasie strefa jest określana za pomocą obiektu strefy.</span><span class="sxs-lookup"><span data-stu-id="b0ffb-122">This time, the zone is specified using a zone object.</span></span>

## <span data-ttu-id="b0ffb-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b0ffb-123">PARAMETERS</span></span>

### <span data-ttu-id="b0ffb-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b0ffb-124">-Name</span></span>
<span data-ttu-id="b0ffb-125">Określa nazwę **zestawu rekordów** , który ma zostać wyświetlony.</span><span class="sxs-lookup"><span data-stu-id="b0ffb-125">Specifies the name of the **RecordSet** to get.</span></span>
<span data-ttu-id="b0ffb-126">Jeśli parametr *name* nie jest określony, zwracane są wszystkie zestawy rekordów określonego typu.</span><span class="sxs-lookup"><span data-stu-id="b0ffb-126">If you do not specify the *Name* parameter, all record sets of the specified type are returned.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Object
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0ffb-127">-Records</span><span class="sxs-lookup"><span data-stu-id="b0ffb-127">-RecordType</span></span>
<span data-ttu-id="b0ffb-128">Określa typ rekordu DNS, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0ffb-128">Specifies the type of DNS record that this cmdlet gets.</span></span>

<span data-ttu-id="b0ffb-129">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="b0ffb-129">Valid values are:</span></span> 

- <span data-ttu-id="b0ffb-130">Sieci</span><span class="sxs-lookup"><span data-stu-id="b0ffb-130">A</span></span>
- <span data-ttu-id="b0ffb-131">AAAA</span><span class="sxs-lookup"><span data-stu-id="b0ffb-131">AAAA</span></span>
- <span data-ttu-id="b0ffb-132">REKORD</span><span class="sxs-lookup"><span data-stu-id="b0ffb-132">CNAME</span></span>
- <span data-ttu-id="b0ffb-133">MX</span><span class="sxs-lookup"><span data-stu-id="b0ffb-133">MX</span></span>
- <span data-ttu-id="b0ffb-134">REKORDU</span><span class="sxs-lookup"><span data-stu-id="b0ffb-134">NS</span></span>
- <span data-ttu-id="b0ffb-135">SYSTEMU</span><span class="sxs-lookup"><span data-stu-id="b0ffb-135">PTR</span></span>
- <span data-ttu-id="b0ffb-136">REKORD</span><span class="sxs-lookup"><span data-stu-id="b0ffb-136">SOA</span></span>
- <span data-ttu-id="b0ffb-137">SRV</span><span class="sxs-lookup"><span data-stu-id="b0ffb-137">SRV</span></span>
- <span data-ttu-id="b0ffb-138">ROZSZERZENIEM</span><span class="sxs-lookup"><span data-stu-id="b0ffb-138">TXT</span></span>

<span data-ttu-id="b0ffb-139">Jeśli nie określono parametru *recordType* , należy także pominąć parametr *name* .</span><span class="sxs-lookup"><span data-stu-id="b0ffb-139">If you do not specify the *RecordType* parameter, you must also omit the *Name* parameter.</span></span> <span data-ttu-id="b0ffb-140">To polecenie cmdlet zwraca następnie wszystkie zestawy rekordów w strefie (wszystkie nazwy i typy).</span><span class="sxs-lookup"><span data-stu-id="b0ffb-140">This cmdlet then returns all record sets in the zone (of all names and types).</span></span>

```yaml
Type: RecordType
Parameter Sets: (All)
Aliases: 
Accepted values: A, AAAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0ffb-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0ffb-141">-ResourceGroupName</span></span>
<span data-ttu-id="b0ffb-142">Określa grupę zasobów zawierającą strefę DNS.</span><span class="sxs-lookup"><span data-stu-id="b0ffb-142">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="b0ffb-143">Nazwę strefy należy również określić przy użyciu parametru *zonename* .</span><span class="sxs-lookup"><span data-stu-id="b0ffb-143">The zone name must also be specified, using the *ZoneName* parameter.</span></span>

<span data-ttu-id="b0ffb-144">Możesz też określić strefę i grupę zasobów, przechodząc do obiektu **dnsZone** przy użyciu parametru *Zone* .</span><span class="sxs-lookup"><span data-stu-id="b0ffb-144">Alternatively, you can specify the zone and resource group by passing in a **DnsZone** object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="b0ffb-145">-Zone</span><span class="sxs-lookup"><span data-stu-id="b0ffb-145">-Zone</span></span>
<span data-ttu-id="b0ffb-146">Określa strefę DNS zawierającą zestaw rekordów, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0ffb-146">Specifies the DNS zone that contains the record set that this cmdlet gets.</span></span>
<span data-ttu-id="b0ffb-147">Możesz też określić strefę przy użyciu parametrów *zonename* i *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="b0ffb-147">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="b0ffb-148">-Nazwa_strefy</span><span class="sxs-lookup"><span data-stu-id="b0ffb-148">-ZoneName</span></span>
<span data-ttu-id="b0ffb-149">Określa nazwę strefy DNS zawierającej zestaw rekordów do pobrania.</span><span class="sxs-lookup"><span data-stu-id="b0ffb-149">Specifies the name of the DNS zone that contains the record set to get.</span></span>
<span data-ttu-id="b0ffb-150">Grupa zasobów zawierająca strefę musi być również określona przy użyciu parametru *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="b0ffb-150">The resource group containing the zone must also be specified, using the *ResourceGroupName* parameter.</span></span>

<span data-ttu-id="b0ffb-151">Możesz też określić strefę i grupę zasobów, przechodząc do obiektu strefy DNS przy użyciu parametru *Zone* .</span><span class="sxs-lookup"><span data-stu-id="b0ffb-151">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="b0ffb-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0ffb-152">CommonParameters</span></span>
<span data-ttu-id="b0ffb-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0ffb-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0ffb-154">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0ffb-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0ffb-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b0ffb-155">INPUTS</span></span>

### <span data-ttu-id="b0ffb-156">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="b0ffb-156">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="b0ffb-157">Do tego polecenia cmdlet można nawiązać obiekt **dnsZone** .</span><span class="sxs-lookup"><span data-stu-id="b0ffb-157">You can pipe a **DnsZone** object to this cmdlet.</span></span>
<span data-ttu-id="b0ffb-158">Obiekt **dnsZone** reprezentuje strefę, w której należy szukać obiektu **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="b0ffb-158">The **DnsZone** object represents the zone in which to look for the **RecordSet** object.</span></span>

## <span data-ttu-id="b0ffb-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b0ffb-159">OUTPUTS</span></span>

### <span data-ttu-id="b0ffb-160">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b0ffb-160">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="b0ffb-161">To polecenie cmdlet zwraca co najmniej jeden obiekt reprezentujący znalezione zestawy rekordów.</span><span class="sxs-lookup"><span data-stu-id="b0ffb-161">This cmdlet returns one or more objects that represents the record sets that are found.</span></span>
<span data-ttu-id="b0ffb-162">Jeśli jest określony parametr *name* and *recordType* , zostanie zwróconych co najwyżej jeden **zestaw rekordów** , w przeciwnym razie wiele obiektów **Recordset** jest zwracanych jako tablica.</span><span class="sxs-lookup"><span data-stu-id="b0ffb-162">There will be at most one **RecordSet** returned if the *Name* and *RecordType* parameters are specified, otherwise multiple **RecordSet** objects are returned as an array.</span></span>

## <span data-ttu-id="b0ffb-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b0ffb-163">NOTES</span></span>

## <span data-ttu-id="b0ffb-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b0ffb-164">RELATED LINKS</span></span>

[<span data-ttu-id="b0ffb-165">Nowe — AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b0ffb-165">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="b0ffb-166">Remove-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b0ffb-166">Remove-AzureRmDnsRecordSet</span></span>](./Remove-AzureRmDnsRecordSet.md)

[<span data-ttu-id="b0ffb-167">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b0ffb-167">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)


