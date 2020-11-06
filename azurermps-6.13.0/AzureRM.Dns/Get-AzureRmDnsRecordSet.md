---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/get-azurermdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsRecordSet.md
ms.openlocfilehash: c45fc33ec45ce0843fe7ef832a70ec622b14af8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549383"
---
# <span data-ttu-id="ae6c9-101">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ae6c9-101">Get-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="ae6c9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ae6c9-102">SYNOPSIS</span></span>
<span data-ttu-id="ae6c9-103">Pobiera zestaw rekordów DNS.</span><span class="sxs-lookup"><span data-stu-id="ae6c9-103">Gets a DNS record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae6c9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ae6c9-104">SYNTAX</span></span>

### <span data-ttu-id="ae6c9-105">Field</span><span class="sxs-lookup"><span data-stu-id="ae6c9-105">Fields</span></span>
```
Get-AzureRmDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String>
 [-RecordType <RecordType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae6c9-106">Stream</span><span class="sxs-lookup"><span data-stu-id="ae6c9-106">Object</span></span>
```
Get-AzureRmDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae6c9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ae6c9-107">DESCRIPTION</span></span>
<span data-ttu-id="ae6c9-108">Polecenie cmdlet **Get-AzureRmDnsRecordSet** Pobiera zestaw rekordów DNS (Domain Name System) o określonej nazwie i typie w określonej strefie.</span><span class="sxs-lookup"><span data-stu-id="ae6c9-108">The **Get-AzureRmDnsRecordSet** cmdlet gets the Domain Name System (DNS) record set with the specified name and type, in the specified zone.</span></span>
<span data-ttu-id="ae6c9-109">Jeśli nie określisz parametrów *name* lub *recordType* , to polecenie cmdlet zwróci wszystkie zestawy rekordów określonego typu w strefie.</span><span class="sxs-lookup"><span data-stu-id="ae6c9-109">If you do not specify the *Name* or *RecordType* parameters, this cmdlet returns all record sets of the specified type in the zone.</span></span>
<span data-ttu-id="ae6c9-110">Jeśli określisz parametr *recordType* , a nie parametr *name* , to polecenie cmdlet zwróci wszystkie zestawy rekordów określonego typu rekordu.</span><span class="sxs-lookup"><span data-stu-id="ae6c9-110">If you specify the *RecordType* parameter but not the *Name* parameter, this cmdlet returns all record sets of the specified record type.</span></span>
<span data-ttu-id="ae6c9-111">Za pomocą operatora potoku można przekazać obiekt **dnsZone** do tego polecenia cmdlet lub przekazać obiekt **dnsZone** jako parametr *Zone* lub można też określić nazwę strefy i grupy zasobów według nazwy.</span><span class="sxs-lookup"><span data-stu-id="ae6c9-111">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone and resource group by name.</span></span>

## <span data-ttu-id="ae6c9-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ae6c9-112">EXAMPLES</span></span>

### <span data-ttu-id="ae6c9-113">Przykład 1: pobieranie zestawów rekordów o określonej nazwie i typie</span><span class="sxs-lookup"><span data-stu-id="ae6c9-113">Example 1: Get record sets with a specified name and type</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

<span data-ttu-id="ae6c9-114">To polecenie pobiera zestaw rekordów typu rekordu o nazwie www w określonej grupie zasobów i strefie, a następnie zapisuje go w zmiennej $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="ae6c9-114">This command gets the record set of record type A named www in the specified resource group and zone, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="ae6c9-115">Ponieważ określono parametry *name* i *recordType* , zwracany jest tylko pojedynczy obiekt **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="ae6c9-115">Because the *Name* and *RecordType* parameters are specified, only one **RecordSet** object is returned.</span></span>

### <span data-ttu-id="ae6c9-116">Przykład 2: pobieranie zestawów rekordów określonego typu</span><span class="sxs-lookup"><span data-stu-id="ae6c9-116">Example 2: Get record sets of a specified type</span></span>
```
PS C:\>$RecordSets = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

<span data-ttu-id="ae6c9-117">To polecenie pobiera tablicę wszystkich zestawów rekordów typu rekord A w strefie o nazwie myzone.com w grupie zasób o nazwie Moja zasobów, a następnie zapisuje je w zmiennej $RecordSets.</span><span class="sxs-lookup"><span data-stu-id="ae6c9-117">This command gets an array of all record sets of record type A in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="ae6c9-118">Przykład 3: pobieranie wszystkich zestawów rekordów w strefie</span><span class="sxs-lookup"><span data-stu-id="ae6c9-118">Example 3: Get all record sets in a zone</span></span>
```
PS C:\>$RecordSets = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

<span data-ttu-id="ae6c9-119">To polecenie pobiera tablicę wszystkich zestawów rekordów w strefie o nazwie myzone.com w grupie zasób o nazwie moja grupa, a następnie zapisuje je w zmiennej $RecordSets.</span><span class="sxs-lookup"><span data-stu-id="ae6c9-119">This command gets an array of all record sets in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="ae6c9-120">Przykład 4: pobieranie wszystkich zestawów rekordów w strefie przy użyciu obiektu DnsZone</span><span class="sxs-lookup"><span data-stu-id="ae6c9-120">Example 4: Get all record sets in a zone, using a DnsZone object</span></span>
```
PS C:\> $Zone = Get-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzureRmDnsRecordSet -Zone $Zone
```

<span data-ttu-id="ae6c9-121">Ten przykład jest równoważny przykładowi 3 powyżej.</span><span class="sxs-lookup"><span data-stu-id="ae6c9-121">This example is equivalent to Example 3 above.</span></span>
<span data-ttu-id="ae6c9-122">W tym czasie strefa jest określana za pomocą obiektu strefy.</span><span class="sxs-lookup"><span data-stu-id="ae6c9-122">This time, the zone is specified using a zone object.</span></span>

## <span data-ttu-id="ae6c9-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ae6c9-123">PARAMETERS</span></span>

### <span data-ttu-id="ae6c9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae6c9-124">-DefaultProfile</span></span>
<span data-ttu-id="ae6c9-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ae6c9-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae6c9-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ae6c9-126">-Name</span></span>
<span data-ttu-id="ae6c9-127">Określa nazwę **zestawu rekordów** , który ma zostać wyświetlony.</span><span class="sxs-lookup"><span data-stu-id="ae6c9-127">Specifies the name of the **RecordSet** to get.</span></span>
<span data-ttu-id="ae6c9-128">Jeśli parametr *name* nie jest określony, zwracane są wszystkie zestawy rekordów określonego typu.</span><span class="sxs-lookup"><span data-stu-id="ae6c9-128">If you do not specify the *Name* parameter, all record sets of the specified type are returned.</span></span>

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

### <span data-ttu-id="ae6c9-129">-Records</span><span class="sxs-lookup"><span data-stu-id="ae6c9-129">-RecordType</span></span>
<span data-ttu-id="ae6c9-130">Określa typ rekordu DNS, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae6c9-130">Specifies the type of DNS record that this cmdlet gets.</span></span>
<span data-ttu-id="ae6c9-131">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="ae6c9-131">Valid values are:</span></span> 
- <span data-ttu-id="ae6c9-132">Sieci</span><span class="sxs-lookup"><span data-stu-id="ae6c9-132">A</span></span>
- <span data-ttu-id="ae6c9-133">AAAA</span><span class="sxs-lookup"><span data-stu-id="ae6c9-133">AAAA</span></span>
- <span data-ttu-id="ae6c9-134">REKORD</span><span class="sxs-lookup"><span data-stu-id="ae6c9-134">CNAME</span></span>
- <span data-ttu-id="ae6c9-135">MX</span><span class="sxs-lookup"><span data-stu-id="ae6c9-135">MX</span></span>
- <span data-ttu-id="ae6c9-136">REKORDU</span><span class="sxs-lookup"><span data-stu-id="ae6c9-136">NS</span></span>
- <span data-ttu-id="ae6c9-137">SYSTEMU</span><span class="sxs-lookup"><span data-stu-id="ae6c9-137">PTR</span></span>
- <span data-ttu-id="ae6c9-138">REKORD</span><span class="sxs-lookup"><span data-stu-id="ae6c9-138">SOA</span></span>
- <span data-ttu-id="ae6c9-139">SRV</span><span class="sxs-lookup"><span data-stu-id="ae6c9-139">SRV</span></span>
- <span data-ttu-id="ae6c9-140">TXT Jeśli parametr *recordType* nie jest określony, należy także pominąć parametr *name* .</span><span class="sxs-lookup"><span data-stu-id="ae6c9-140">TXT If you do not specify the *RecordType* parameter, you must also omit the *Name* parameter.</span></span> <span data-ttu-id="ae6c9-141">To polecenie cmdlet zwraca następnie wszystkie zestawy rekordów w strefie (wszystkie nazwy i typy).</span><span class="sxs-lookup"><span data-stu-id="ae6c9-141">This cmdlet then returns all record sets in the zone (of all names and types).</span></span>

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

### <span data-ttu-id="ae6c9-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae6c9-142">-ResourceGroupName</span></span>
<span data-ttu-id="ae6c9-143">Określa grupę zasobów zawierającą strefę DNS.</span><span class="sxs-lookup"><span data-stu-id="ae6c9-143">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="ae6c9-144">Nazwę strefy należy również określić przy użyciu parametru *zonename* .</span><span class="sxs-lookup"><span data-stu-id="ae6c9-144">The zone name must also be specified, using the *ZoneName* parameter.</span></span>
<span data-ttu-id="ae6c9-145">Możesz też określić strefę i grupę zasobów, przechodząc do obiektu **dnsZone** przy użyciu parametru *Zone* .</span><span class="sxs-lookup"><span data-stu-id="ae6c9-145">Alternatively, you can specify the zone and resource group by passing in a **DnsZone** object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="ae6c9-146">-Zone</span><span class="sxs-lookup"><span data-stu-id="ae6c9-146">-Zone</span></span>
<span data-ttu-id="ae6c9-147">Określa strefę DNS zawierającą zestaw rekordów, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae6c9-147">Specifies the DNS zone that contains the record set that this cmdlet gets.</span></span>
<span data-ttu-id="ae6c9-148">Możesz też określić strefę przy użyciu parametrów *zonename* i *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="ae6c9-148">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="ae6c9-149">-Nazwa_strefy</span><span class="sxs-lookup"><span data-stu-id="ae6c9-149">-ZoneName</span></span>
<span data-ttu-id="ae6c9-150">Określa nazwę strefy DNS zawierającej zestaw rekordów do pobrania.</span><span class="sxs-lookup"><span data-stu-id="ae6c9-150">Specifies the name of the DNS zone that contains the record set to get.</span></span>
<span data-ttu-id="ae6c9-151">Grupa zasobów zawierająca strefę musi być również określona przy użyciu parametru *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="ae6c9-151">The resource group containing the zone must also be specified, using the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="ae6c9-152">Możesz też określić strefę i grupę zasobów, przechodząc do obiektu strefy DNS przy użyciu parametru *Zone* .</span><span class="sxs-lookup"><span data-stu-id="ae6c9-152">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="ae6c9-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae6c9-153">CommonParameters</span></span>
<span data-ttu-id="ae6c9-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae6c9-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae6c9-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae6c9-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae6c9-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae6c9-156">INPUTS</span></span>

### <span data-ttu-id="ae6c9-157">System. String</span><span class="sxs-lookup"><span data-stu-id="ae6c9-157">System.String</span></span>

### <span data-ttu-id="ae6c9-158">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="ae6c9-158">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="ae6c9-159">Parametry: Zone (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ae6c9-159">Parameters: Zone (ByValue)</span></span>

### <span data-ttu-id="ae6c9-160">System. Nullable "1 [[Microsoft. Azure. Management. DNS. models. Records, Microsoft. Azure. Management. DNS, Version = 2.1.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="ae6c9-160">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.RecordType, Microsoft.Azure.Management.Dns, Version=2.1.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="ae6c9-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ae6c9-161">OUTPUTS</span></span>

### <span data-ttu-id="ae6c9-162">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ae6c9-162">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="ae6c9-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ae6c9-163">NOTES</span></span>

## <span data-ttu-id="ae6c9-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae6c9-164">RELATED LINKS</span></span>

[<span data-ttu-id="ae6c9-165">Nowe — AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ae6c9-165">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="ae6c9-166">Remove-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ae6c9-166">Remove-AzureRmDnsRecordSet</span></span>](./Remove-AzureRmDnsRecordSet.md)

[<span data-ttu-id="ae6c9-167">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ae6c9-167">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)


