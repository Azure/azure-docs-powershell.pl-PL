---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/get-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsRecordSet.md
ms.openlocfilehash: ade9d95b6388a667f55df24db107a2326fa001ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202138"
---
# <span data-ttu-id="73bde-101">Get-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="73bde-101">Get-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="73bde-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73bde-102">SYNOPSIS</span></span>
<span data-ttu-id="73bde-103">Pobiera zestaw rekordów z prywatnej strefy DNS.</span><span class="sxs-lookup"><span data-stu-id="73bde-103">Gets a record set from a Private DNS zone.</span></span>

## <span data-ttu-id="73bde-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="73bde-104">SYNTAX</span></span>

### <span data-ttu-id="73bde-105">FieldsWithNoName (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="73bde-105">FieldsWithNoName (Default)</span></span>
```
Get-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73bde-106">Pola</span><span class="sxs-lookup"><span data-stu-id="73bde-106">Fields</span></span>
```
Get-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73bde-107">Obiekt</span><span class="sxs-lookup"><span data-stu-id="73bde-107">Object</span></span>
```
Get-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73bde-108">ObjectWithNoName</span><span class="sxs-lookup"><span data-stu-id="73bde-108">ObjectWithNoName</span></span>
```
Get-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73bde-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="73bde-109">ResourceId</span></span>
```
Get-AzPrivateDnsRecordSet -ParentResourceId <String> -Name <String> -RecordType <RecordType>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73bde-110">ResourceIdWithNoName</span><span class="sxs-lookup"><span data-stu-id="73bde-110">ResourceIdWithNoName</span></span>
```
Get-AzPrivateDnsRecordSet -ParentResourceId <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73bde-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="73bde-111">DESCRIPTION</span></span>
<span data-ttu-id="73bde-112">Polecenie Get-AzPrivateDnsRecordSet pobiera zestaw rekordów DNS (Private Domain Name System) o określonej nazwie i typie w określonej strefie prywatnej.</span><span class="sxs-lookup"><span data-stu-id="73bde-112">The Get-AzPrivateDnsRecordSet cmdlet gets the Private Domain Name System (DNS) record set with the specified name and type, in the specified private zone.</span></span> <span data-ttu-id="73bde-113">Jeśli nie określisz parametrów Name (Nazwa) lub RecordType (Typ Rekordu), to polecenie cmdlet zwróci wszystkie zestawy rekordów określonego typu w strefie prywatnej.</span><span class="sxs-lookup"><span data-stu-id="73bde-113">If you do not specify the Name or RecordType parameters, this cmdlet returns all record sets of the specified type in the private zone.</span></span> <span data-ttu-id="73bde-114">Jeśli określisz parametr RecordType, ale nie parametr Name, to polecenie cmdlet zwróci wszystkie zestawy rekordów określonego typu rekordu.</span><span class="sxs-lookup"><span data-stu-id="73bde-114">If you specify the RecordType parameter but not the Name parameter, this cmdlet returns all record sets of the specified record type.</span></span> <span data-ttu-id="73bde-115">Za pomocą operatora potoku możesz przekazać obiekt PSPrivateDnsZone do tego polecenia cmdlet lub przekazać obiekt PSPrivateDnsZone jako parametr Zone lub możesz również określić nazwę grupy zasobów i strefy.</span><span class="sxs-lookup"><span data-stu-id="73bde-115">You can use the pipeline operator to pass a PSPrivateDnsZone object to this cmdlet, or you can pass a PSPrivateDnsZone object as the Zone parameter, or alternatively you can specify the zone and resource group by name.</span></span> <span data-ttu-id="73bde-116">Możesz także określić strefę prywatną przy użyciu identyfikatora zasobu strefy prywatnej.</span><span class="sxs-lookup"><span data-stu-id="73bde-116">You can also specify the private zone using the Resource Id of the private zone.</span></span>

## <span data-ttu-id="73bde-117">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="73bde-117">EXAMPLES</span></span>

### <span data-ttu-id="73bde-118">Przykład 1. Uzyskiwanie zestawów rekordów o określonej nazwie i typie</span><span class="sxs-lookup"><span data-stu-id="73bde-118">Example 1: Get record sets with a specified name and type</span></span>
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

<span data-ttu-id="73bde-119">To polecenie pobiera zestaw rekordów typu A o nazwie www w określonej grupie zasobów i strefie prywatnej, a następnie przechowuje go w $RecordSet zmienną.</span><span class="sxs-lookup"><span data-stu-id="73bde-119">This command gets the record set of record type A named www in the specified resource group and private zone, and then stores it in the $RecordSet variable.</span></span> <span data-ttu-id="73bde-120">Ponieważ parametry Name (Nazwa) i RecordType (Typ Rekordu) są określone, zwracany jest tylko jeden obiekt RecordSet.</span><span class="sxs-lookup"><span data-stu-id="73bde-120">Because the Name and RecordType parameters are specified, only one RecordSet object is returned.</span></span>

### <span data-ttu-id="73bde-121">Przykład 2. Uzyskiwanie zestawów rekordów określonego typu</span><span class="sxs-lookup"><span data-stu-id="73bde-121">Example 2: Get record sets of a specified type</span></span>
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

<span data-ttu-id="73bde-122">To polecenie pobiera tablicę wszystkich zestawów rekordów typu A w strefie prywatnej o nazwie myzone.com w grupie zasobów o nazwie MyResourceGroup, a następnie przechowuje je w $RecordSets danych.</span><span class="sxs-lookup"><span data-stu-id="73bde-122">This command gets an array of all record sets of record type A in the private zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="73bde-123">Przykład 3. Uzyskiwanie wszystkich zestawów rekordów w strefie prywatnej</span><span class="sxs-lookup"><span data-stu-id="73bde-123">Example 3: Get all record sets in a private zone</span></span>
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

<span data-ttu-id="73bde-124">To polecenie pobiera tablicę wszystkich zestawów rekordów w strefie prywatnej o nazwie myzone.com w grupie zasobów o nazwie MyResourceGroup, a następnie przechowuje je w zmiennej $RecordSets zasobów.</span><span class="sxs-lookup"><span data-stu-id="73bde-124">This command gets an array of all record sets in the private zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="73bde-125">Przykład 4. Uzyskiwanie wszystkich zestawów rekordów w strefie prywatnej przy użyciu obiektu PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="73bde-125">Example 4: Get all record sets in a private zone, using a PSPrivateDnsZone object</span></span>
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

<span data-ttu-id="73bde-126">Ten przykład jest odpowiednikiem powyższego przykładu 3.</span><span class="sxs-lookup"><span data-stu-id="73bde-126">This example is equivalent to Example 3 above.</span></span> <span data-ttu-id="73bde-127">Tym razem strefa prywatna jest określana przy użyciu obiektu strefy prywatnej.</span><span class="sxs-lookup"><span data-stu-id="73bde-127">This time, the private zone is specified using a private zone object.</span></span>

## <span data-ttu-id="73bde-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73bde-128">PARAMETERS</span></span>

### <span data-ttu-id="73bde-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73bde-129">-DefaultProfile</span></span>
<span data-ttu-id="73bde-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="73bde-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73bde-131">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="73bde-131">-Name</span></span>
<span data-ttu-id="73bde-132">Nazwa rekordów w tym zestawie rekordów (względem nazwy strefy i bez kropki kończącej).</span><span class="sxs-lookup"><span data-stu-id="73bde-132">The name of the records in this record set (relative to the name of the zone and without a terminating dot).</span></span>

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

### <span data-ttu-id="73bde-133">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="73bde-133">-ParentResourceId</span></span>
<span data-ttu-id="73bde-134">Private DNS Zone ResourceID (Prywatny adres DNS Strefy ResourceID).</span><span class="sxs-lookup"><span data-stu-id="73bde-134">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="73bde-135">-RecordType</span><span class="sxs-lookup"><span data-stu-id="73bde-135">-RecordType</span></span>
<span data-ttu-id="73bde-136">Typ rekordów DNS w tym zestawie rekordów.</span><span class="sxs-lookup"><span data-stu-id="73bde-136">The type of DNS records in this record set.</span></span>

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

### <span data-ttu-id="73bde-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73bde-137">-ResourceGroupName</span></span>
<span data-ttu-id="73bde-138">Grupa zasobów, do której należy strefa.</span><span class="sxs-lookup"><span data-stu-id="73bde-138">The resource group to which the zone belongs.</span></span>

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

### <span data-ttu-id="73bde-139">— Strefa</span><span class="sxs-lookup"><span data-stu-id="73bde-139">-Zone</span></span>
<span data-ttu-id="73bde-140">Obiekt DnsZone reprezentujący strefę, w której należy utworzyć zestaw rekordów.</span><span class="sxs-lookup"><span data-stu-id="73bde-140">The DnsZone object representing the zone in which to create the record set.</span></span>

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

### <span data-ttu-id="73bde-141">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="73bde-141">-ZoneName</span></span>
<span data-ttu-id="73bde-142">Strefa, w której należy utworzyć zestaw rekordów (bez kropki kończącej).</span><span class="sxs-lookup"><span data-stu-id="73bde-142">The zone in which to create the record set (without a terminating dot).</span></span>

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

### <span data-ttu-id="73bde-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73bde-143">CommonParameters</span></span>
<span data-ttu-id="73bde-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73bde-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73bde-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73bde-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73bde-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="73bde-146">INPUTS</span></span>

### <span data-ttu-id="73bde-147">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="73bde-147">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="73bde-148">System.String</span><span class="sxs-lookup"><span data-stu-id="73bde-148">System.String</span></span>

## <span data-ttu-id="73bde-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="73bde-149">OUTPUTS</span></span>

### <span data-ttu-id="73bde-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="73bde-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="73bde-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="73bde-151">NOTES</span></span>

## <span data-ttu-id="73bde-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="73bde-152">RELATED LINKS</span></span>
