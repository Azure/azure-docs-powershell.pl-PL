---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/get-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsRecordSet.md
ms.openlocfilehash: a0b527a0931c5c3423e5e64bad0abb7128fc3497
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872872"
---
# <span data-ttu-id="dcbd2-101">Get-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="dcbd2-101">Get-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="dcbd2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dcbd2-102">SYNOPSIS</span></span>
<span data-ttu-id="dcbd2-103">Pobiera zestaw rekordów z prywatnej strefy DNS.</span><span class="sxs-lookup"><span data-stu-id="dcbd2-103">Gets a record set from a Private DNS zone.</span></span>

## <span data-ttu-id="dcbd2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dcbd2-104">SYNTAX</span></span>

### <span data-ttu-id="dcbd2-105">FieldsWithNoName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="dcbd2-105">FieldsWithNoName (Default)</span></span>
```
Get-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dcbd2-106">Field</span><span class="sxs-lookup"><span data-stu-id="dcbd2-106">Fields</span></span>
```
Get-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dcbd2-107">Stream</span><span class="sxs-lookup"><span data-stu-id="dcbd2-107">Object</span></span>
```
Get-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dcbd2-108">ObjectWithNoName</span><span class="sxs-lookup"><span data-stu-id="dcbd2-108">ObjectWithNoName</span></span>
```
Get-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dcbd2-109">Zasobów</span><span class="sxs-lookup"><span data-stu-id="dcbd2-109">ResourceId</span></span>
```
Get-AzPrivateDnsRecordSet -ParentResourceId <String> -Name <String> -RecordType <RecordType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dcbd2-110">ResourceIdWithNoName</span><span class="sxs-lookup"><span data-stu-id="dcbd2-110">ResourceIdWithNoName</span></span>
```
Get-AzPrivateDnsRecordSet -ParentResourceId <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dcbd2-111">Opis</span><span class="sxs-lookup"><span data-stu-id="dcbd2-111">DESCRIPTION</span></span>
<span data-ttu-id="dcbd2-112">Polecenie cmdlet Get-AzPrivateDnsRecordSet powoduje wyświetlenie zestawu rekordów prywatnego (Domain Name System) z określoną nazwą i typem w określonej strefie prywatnej.</span><span class="sxs-lookup"><span data-stu-id="dcbd2-112">The Get-AzPrivateDnsRecordSet cmdlet gets the Private Domain Name System (DNS) record set with the specified name and type, in the specified private zone.</span></span> <span data-ttu-id="dcbd2-113">Jeśli nie określisz parametrów Name lub recordType, to polecenie cmdlet zwróci wszystkie zestawy rekordów określonego typu w strefie prywatnej.</span><span class="sxs-lookup"><span data-stu-id="dcbd2-113">If you do not specify the Name or RecordType parameters, this cmdlet returns all record sets of the specified type in the private zone.</span></span> <span data-ttu-id="dcbd2-114">Jeśli określisz parametr recordType, a nie parametr name, to polecenie cmdlet zwróci wszystkie zestawy rekordów określonego typu rekordu.</span><span class="sxs-lookup"><span data-stu-id="dcbd2-114">If you specify the RecordType parameter but not the Name parameter, this cmdlet returns all record sets of the specified record type.</span></span> <span data-ttu-id="dcbd2-115">Za pomocą operatora potoku można przekazać obiekt PSPrivateDnsZone do tego polecenia cmdlet lub przekazać obiekt PSPrivateDnsZone jako parametr Zone lub można też określić nazwę strefy i grupy zasobów według nazwy.</span><span class="sxs-lookup"><span data-stu-id="dcbd2-115">You can use the pipeline operator to pass a PSPrivateDnsZone object to this cmdlet, or you can pass a PSPrivateDnsZone object as the Zone parameter, or alternatively you can specify the zone and resource group by name.</span></span> <span data-ttu-id="dcbd2-116">Możesz również określić strefę prywatną przy użyciu identyfikatora zasobu strefy prywatnej.</span><span class="sxs-lookup"><span data-stu-id="dcbd2-116">You can also specify the private zone using the Resource Id of the private zone.</span></span>

## <span data-ttu-id="dcbd2-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dcbd2-117">EXAMPLES</span></span>

### <span data-ttu-id="dcbd2-118">Przykład 1: pobieranie zestawów rekordów o określonej nazwie i typie</span><span class="sxs-lookup"><span data-stu-id="dcbd2-118">Example 1: Get record sets with a specified name and type</span></span>
```powershell
PS C:\>$RecordSet = Get-AzPrivateDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="dcbd2-119">To polecenie pobiera zestaw rekordów typu rekordu o nazwie www w określonej grupie zasobów i strefie prywatnej, a następnie zapisuje go w zmiennej $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="dcbd2-119">This command gets the record set of record type A named www in the specified resource group and private zone, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="dcbd2-120">Ponieważ określono parametry Name i recordType, zwracany jest tylko pojedynczy obiekt RecordSet.</span><span class="sxs-lookup"><span data-stu-id="dcbd2-120">Because the Name and RecordType parameters are specified, only one RecordSet object is returned.</span></span>

### <span data-ttu-id="dcbd2-121">Przykład 2: pobieranie zestawów rekordów określonego typu</span><span class="sxs-lookup"><span data-stu-id="dcbd2-121">Example 2: Get record sets of a specified type</span></span>
```powershell
PS C:\>$RecordSets = Get-AzPrivateDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www2
Name              : www2
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {2.3.4.5}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="dcbd2-122">To polecenie pobiera tablicę wszystkich zestawów rekordów typu rekord A w strefie prywatnej o nazwie myzone.com w grupie zasób o nazwie Moja zasobów, a następnie zapisuje je w zmiennej $RecordSets.</span><span class="sxs-lookup"><span data-stu-id="dcbd2-122">This command gets an array of all record sets of record type A in the private zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="dcbd2-123">Przykład 3: pobieranie wszystkich zestawów rekordów w strefie prywatnej</span><span class="sxs-lookup"><span data-stu-id="dcbd2-123">Example 3: Get all record sets in a private zone</span></span>
```powershell
PS C:\>$RecordSets = Get-AzPrivateDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:DB80:4009:1803::1005}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="dcbd2-124">To polecenie pobiera tablicę wszystkich zestawów rekordów w strefie prywatnej o nazwie myzone.com w grupie zasobów o nazwie Moja zasobów, a następnie zapisuje je w zmiennej $RecordSets.</span><span class="sxs-lookup"><span data-stu-id="dcbd2-124">This command gets an array of all record sets in the private zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="dcbd2-125">Przykład 4: pobieranie wszystkich zestawów rekordów w strefie prywatnej za pomocą obiektu PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="dcbd2-125">Example 4: Get all record sets in a private zone, using a PSPrivateDnsZone object</span></span>
```powershell
PS C:\> $Zone = Get-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzPrivateDnsRecordSet -Zone $Zone

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www1
Name              : www1
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:DB80:4009:1803::1005}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="dcbd2-126">Ten przykład jest równoważny przykładowi 3 powyżej.</span><span class="sxs-lookup"><span data-stu-id="dcbd2-126">This example is equivalent to Example 3 above.</span></span> <span data-ttu-id="dcbd2-127">W tym czasie strefa prywatna jest określana za pomocą obiektu strefy prywatnej.</span><span class="sxs-lookup"><span data-stu-id="dcbd2-127">This time, the private zone is specified using a private zone object.</span></span>

## <span data-ttu-id="dcbd2-128">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dcbd2-128">PARAMETERS</span></span>

### <span data-ttu-id="dcbd2-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcbd2-129">-DefaultProfile</span></span>
<span data-ttu-id="dcbd2-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dcbd2-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcbd2-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dcbd2-131">-Name</span></span>
<span data-ttu-id="dcbd2-132">Nazwy rekordów w tym zestawie rekordów (w odniesieniu do nazwy strefy i bez kropki przerywanej).</span><span class="sxs-lookup"><span data-stu-id="dcbd2-132">The name of the records in this record set (relative to the name of the zone and without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, Object, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcbd2-133">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="dcbd2-133">-ParentResourceId</span></span>
<span data-ttu-id="dcbd2-134">Identyfikator zasobu prywatnej strefy DNS.</span><span class="sxs-lookup"><span data-stu-id="dcbd2-134">Private DNS Zone ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId, ResourceIdWithNoName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcbd2-135">-Records</span><span class="sxs-lookup"><span data-stu-id="dcbd2-135">-RecordType</span></span>
<span data-ttu-id="dcbd2-136">Typ rekordów DNS w tym zestawie rekordów.</span><span class="sxs-lookup"><span data-stu-id="dcbd2-136">The type of DNS records in this record set.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.PrivateDns.Models.RecordType]
Parameter Sets: FieldsWithNoName, ObjectWithNoName, ResourceIdWithNoName
Aliases:
Accepted values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.PrivateDns.Models.RecordType]
Parameter Sets: Fields, Object, ResourceId
Aliases:
Accepted values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcbd2-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcbd2-137">-ResourceGroupName</span></span>
<span data-ttu-id="dcbd2-138">Grupa zasobów, do której należy strefa.</span><span class="sxs-lookup"><span data-stu-id="dcbd2-138">The resource group to which the zone belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: FieldsWithNoName, Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcbd2-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="dcbd2-139">-Zone</span></span>
<span data-ttu-id="dcbd2-140">Obiekt DnsZone reprezentujący strefę, w której ma zostać utworzony zestaw rekordów.</span><span class="sxs-lookup"><span data-stu-id="dcbd2-140">The DnsZone object representing the zone in which to create the record set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object, ObjectWithNoName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dcbd2-141">-Nazwa_strefy</span><span class="sxs-lookup"><span data-stu-id="dcbd2-141">-ZoneName</span></span>
<span data-ttu-id="dcbd2-142">Strefa, w której ma zostać utworzony zestaw rekordów (bez przerywanej kropki).</span><span class="sxs-lookup"><span data-stu-id="dcbd2-142">The zone in which to create the record set (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: FieldsWithNoName, Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcbd2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcbd2-143">CommonParameters</span></span>
<span data-ttu-id="dcbd2-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcbd2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcbd2-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcbd2-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcbd2-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dcbd2-146">INPUTS</span></span>

### <span data-ttu-id="dcbd2-147">Microsoft. Azure. Commands. PrivateDns. models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="dcbd2-147">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="dcbd2-148">System. String</span><span class="sxs-lookup"><span data-stu-id="dcbd2-148">System.String</span></span>

## <span data-ttu-id="dcbd2-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dcbd2-149">OUTPUTS</span></span>

### <span data-ttu-id="dcbd2-150">Microsoft. Azure. Commands. PrivateDns. models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="dcbd2-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="dcbd2-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dcbd2-151">NOTES</span></span>

## <span data-ttu-id="dcbd2-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dcbd2-152">RELATED LINKS</span></span>
