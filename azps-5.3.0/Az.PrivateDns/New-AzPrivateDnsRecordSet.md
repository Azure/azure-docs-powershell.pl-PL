---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/new-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 1a7042c94457f23302aa8d2899475d7b117e65b4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498585"
---
# <span data-ttu-id="b8dbb-101">New-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b8dbb-101">New-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="b8dbb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b8dbb-102">SYNOPSIS</span></span>
<span data-ttu-id="b8dbb-103">Tworzy zestaw rekordów w prywatnej strefie DNS.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-103">Creates a record set in a Private DNS zone.</span></span>

## <span data-ttu-id="b8dbb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b8dbb-104">SYNTAX</span></span>

### <span data-ttu-id="b8dbb-105">Pola (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="b8dbb-105">Fields (Default)</span></span>
```
New-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> -Ttl <UInt32> [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8dbb-106">Stream</span><span class="sxs-lookup"><span data-stu-id="b8dbb-106">Object</span></span>
```
New-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType> -Ttl <UInt32>
 [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8dbb-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="b8dbb-107">ResourceId</span></span>
```
New-AzPrivateDnsRecordSet -ParentResourceId <String> -Name <String> -RecordType <RecordType> -Ttl <UInt32>
 [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8dbb-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b8dbb-108">DESCRIPTION</span></span>
<span data-ttu-id="b8dbb-109">Polecenie cmdlet New-AzPrivateDnsRecordSet tworzy nowy, prywatny zestaw rekordów DNS (Domain Name System) z określoną nazwą i typem w określonej strefie prywatnej.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-109">The New-AzPrivateDnsRecordSet cmdlet creates a new Private Domain Name System (DNS) record set with the specified name and type in the specified private zone.</span></span> <span data-ttu-id="b8dbb-110">Obiekt RecordSet jest zestawem prywatnych rekordów DNS o tej samej nazwie i typie.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-110">A RecordSet object is a set of Private DNS records with the same name and type.</span></span> <span data-ttu-id="b8dbb-111">Należy pamiętać, że nazwa jest określana względem strefy prywatnej, a nie w pełni kwalifikowanej nazwie.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-111">Note that the name is relative to the private zone and not the fully qualified name.</span></span> <span data-ttu-id="b8dbb-112">Parametr PrivateDnsRecord określa rekordy w zestawie rekordów.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-112">The PrivateDnsRecord parameter specifies the records in the record set.</span></span> <span data-ttu-id="b8dbb-113">Ten parametr pobiera tablicę prywatnych rekordów DNS zbudowanych przy użyciu funkcji New-AzPrivateDnsRecordConfig.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-113">This parameter takes an array of Private DNS records, constructed using New-AzPrivateDnsRecordConfig.</span></span> <span data-ttu-id="b8dbb-114">Za pomocą operatora potoku możesz przekazać obiekt PSPrivateDnsZone do tego polecenia cmdlet lub przekazać obiekt PSPrivateDnsZone jako parametr Zone lub określić strefę jako identyfikator zasobu, lub możesz określić strefę według nazwy.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-114">You can use the pipeline operator to pass a PSPrivateDnsZone object to this cmdlet, or you can pass a PSPrivateDnsZone object as the Zone parameter, or you can specify the zone by its ResourceId, or alternatively you can specify the zone by name.</span></span> <span data-ttu-id="b8dbb-115">Za pomocą zmiennej Confirm i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-115">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="b8dbb-116">Jeśli pasujący zestaw rekordów już istnieje (ta sama nazwa i typ rekordu), należy określić parametr zastępowania, w przeciwnym razie polecenie cmdlet nie spowoduje utworzenia nowego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-116">If a matching RecordSet already exists (same name and record type), you must specify the Overwrite parameter, otherwise the cmdlet will not create a new RecordSet .</span></span>

## <span data-ttu-id="b8dbb-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b8dbb-117">EXAMPLES</span></span>

### <span data-ttu-id="b8dbb-118">Przykład 1. Tworzenie zestawu rekordów typu A</span><span class="sxs-lookup"><span data-stu-id="b8dbb-118">Example 1: Create a RecordSet of type A</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords (New-AzPrivateDnsRecordConfig -IPv4Address 1.2.3.4)

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Netwo
                    rk/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :


# To create a record set containing multiple records, use New-AzPrivateDnsRecordConfig to add each record to the $Records array,
# then call New-AzPrivateDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzPrivateDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Netwo
                    rk/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4, 5.6.7.8}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="b8dbb-119">W tym przykładzie przedstawiono tworzenie zestawu rekordów o nazwie www w strefie prywatnej myzone.com.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-119">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="b8dbb-120">Zestaw rekordów jest typu A i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="b8dbb-120">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="b8dbb-121">Zawiera jeden prywatny rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-121">It contains a single Private DNS record.</span></span>

### <span data-ttu-id="b8dbb-122">Przykład 2: Tworzenie zestawu rekordów typu AAAA</span><span class="sxs-lookup"><span data-stu-id="b8dbb-122">Example 2: Create a RecordSet of type AAAA</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:db8::1}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="b8dbb-123">W tym przykładzie przedstawiono tworzenie zestawu rekordów o nazwie www w strefie prywatnej myzone.com.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-123">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="b8dbb-124">Zestaw rekordów jest typu AAAA i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="b8dbb-124">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="b8dbb-125">Zawiera jeden prywatny rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-125">It contains a single Private DNS record.</span></span> <span data-ttu-id="b8dbb-126">Aby utworzyć zestaw rekordów przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-126">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="b8dbb-127">Przykład 3: Tworzenie zestawu rekordów typu CNAME</span><span class="sxs-lookup"><span data-stu-id="b8dbb-127">Example 3: Create a RecordSet of type CNAME</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/CNAME/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : CNAME
Records           : {www.contoso.com}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="b8dbb-128">W tym przykładzie przedstawiono tworzenie zestawu rekordów o nazwie www w strefie prywatnej myzone.com.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-128">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="b8dbb-129">Zestaw rekordów jest typu CNAME i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="b8dbb-129">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="b8dbb-130">Zawiera jeden prywatny rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-130">It contains a single Private DNS record.</span></span> <span data-ttu-id="b8dbb-131">Aby utworzyć zestaw rekordów przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-131">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="b8dbb-132">Przykład 4: Tworzenie zestawu rekordów typu MX</span><span class="sxs-lookup"><span data-stu-id="b8dbb-132">Example 4: Create a RecordSet of type MX</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType MX -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/MX/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : MX
Records           : {[5,mail.microsoft.com]}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="b8dbb-133">To polecenie tworzy zestaw rekordów o nazwie www w strefie prywatnej myzone.com.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-133">This command creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="b8dbb-134">Zestaw rekordów jest typu MX i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="b8dbb-134">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="b8dbb-135">Zawiera jeden prywatny rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-135">It contains a single Private DNS record.</span></span> <span data-ttu-id="b8dbb-136">Aby utworzyć zestaw rekordów przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-136">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="b8dbb-137">Przykład 5: Tworzenie zestawu rekordów typu PTR</span><span class="sxs-lookup"><span data-stu-id="b8dbb-137">Example 5: Create a RecordSet of type PTR</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/3.2.1.in-addr.arpa/PTR/4
Name              : 4
ZoneName          : 3.2.1.in-addr.arpa
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : PTR
Records           : {www.contoso.com}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="b8dbb-138">To polecenie tworzy zestaw rekordów o nazwie 4 w strefie prywatnej 3.2.1.in-addr. arpa.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-138">This command creates a RecordSet named 4 in the private zone 3.2.1.in-addr.arpa.</span></span> <span data-ttu-id="b8dbb-139">Zestaw rekordów jest typu PTR i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="b8dbb-139">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="b8dbb-140">Zawiera jeden prywatny rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-140">It contains a single Private DNS record.</span></span> <span data-ttu-id="b8dbb-141">Aby utworzyć zestaw rekordów przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-141">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="b8dbb-142">Przykład 6: Tworzenie zestawu rekordów typu SRV</span><span class="sxs-lookup"><span data-stu-id="b8dbb-142">Example 6: Create a RecordSet of type SRV</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/SRV/_sip._tcp
Name              : _sip._tcp
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : SRV
Records           : {[0,5,8080,sipservice.contoso.com]}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="b8dbb-143">To polecenie tworzy zestaw rekordów o nazwie _sip. _tcp w strefie prywatnej myzone.com.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-143">This command creates a RecordSet named _sip._tcp in the private zone myzone.com.</span></span> <span data-ttu-id="b8dbb-144">Zestaw rekordów jest typu SRV i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="b8dbb-144">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="b8dbb-145">Zawiera pojedynczy prywatny rekord DNS, wskazujący adres IP 2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-145">It contains a single Private DNS record, pointing to the IP address 2001.2.3.4.</span></span> <span data-ttu-id="b8dbb-146">Usługa (SIP) i protokół (TCP) są określone jako część nazwy zestawu rekordów, a nie jako część danych rekordu.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-146">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span> <span data-ttu-id="b8dbb-147">Aby utworzyć zestaw rekordów przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-147">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="b8dbb-148">Przykład 7: Tworzenie zestawu rekordów typu TXT</span><span class="sxs-lookup"><span data-stu-id="b8dbb-148">Example 7: Create a RecordSet of type TXT</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/TXT/text
Name              : text
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : TXT
Records           : {This is a TXT Record}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="b8dbb-149">To polecenie tworzy zestaw rekordów o nazwie tekst w strefie prywatnej myzone.com.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-149">This command creates a RecordSet named text in the private zone myzone.com.</span></span> <span data-ttu-id="b8dbb-150">Zestaw rekordów jest typu TXT i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="b8dbb-150">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="b8dbb-151">Zawiera jeden prywatny rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-151">It contains a single Private DNS record.</span></span> <span data-ttu-id="b8dbb-152">Aby utworzyć zestaw rekordów przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-152">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="b8dbb-153">Przykład 8: Tworzenie zestawu rekordów w strefie Apex</span><span class="sxs-lookup"><span data-stu-id="b8dbb-153">Example 8:  Create a RecordSet at the zone apex</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/@
Name              : @
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="b8dbb-154">To polecenie tworzy zestaw rekordów na wierzchołku (lub korzeniu) strefy myzone.com.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-154">This command creates a RecordSet at the apex (or root) of the private zone myzone.com.</span></span> <span data-ttu-id="b8dbb-155">W tym celu nazwa zestawu rekordów jest określana jako "@" (łącznie z cudzysłowami podwójnymi).</span><span class="sxs-lookup"><span data-stu-id="b8dbb-155">To do this, the record set name is specified as "@" (including the double-quotes).</span></span> <span data-ttu-id="b8dbb-156">Nie można utworzyć rekordów CNAME na wierzchołku strefy.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-156">You cannot create CNAME records at the apex of a zone.</span></span> <span data-ttu-id="b8dbb-157">Jest to ograniczenie standardów DNS. nie jest to ograniczenie dotyczące prywatnego systemu DNS platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-157">This is a constraint of the DNS standards; it is not a limitation of Azure Private DNS.</span></span> <span data-ttu-id="b8dbb-158">Aby utworzyć zestaw rekordów przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-158">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="b8dbb-159">Przykład 9: Tworzenie zestawu rekordów symboli wieloznacznych</span><span class="sxs-lookup"><span data-stu-id="b8dbb-159">Example 9:  Create a wildcard Record Set</span></span>

```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/@
Name              : *
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="b8dbb-160">To polecenie tworzy zestaw rekordów o nazwie \* w strefie prywatnej myzone.com.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-160">This command creates a RecordSet named \* in the private zone myzone.com.</span></span> <span data-ttu-id="b8dbb-161">To jest zestaw rekordów z symbolami wieloznacznymi.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-161">This is a wildcard record set.</span></span> <span data-ttu-id="b8dbb-162">Aby utworzyć zestaw rekordów przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-162">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="b8dbb-163">Przykład 10: Tworzenie pustego zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="b8dbb-163">Example 10:  Create an empty Record Set</span></span>

```powershell
PS C:\>$RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords @()

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/@
Name              : *
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="b8dbb-164">To polecenie tworzy zestaw rekordów o nazwie \* w strefie prywatnej myzone.com.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-164">This command creates a RecordSet named \* in the private zone myzone.com.</span></span> <span data-ttu-id="b8dbb-165">Zestaw rekordów jest typu A i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="b8dbb-165">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="b8dbb-166">To jest pusty zestaw rekordów, który działa jako symbol zastępczy, do którego można później dodawać rekordy.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-166">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="b8dbb-167">Przykład 11: Tworzenie zestawu rekordów i pomijanie wszystkich potwierdzeń</span><span class="sxs-lookup"><span data-stu-id="b8dbb-167">Example 11:  Create a record set and suppress all confirmation</span></span>

```powershell
PS C:\>$RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="b8dbb-168">To polecenie tworzy zestaw rekordów.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-168">This command creates a RecordSet.</span></span> <span data-ttu-id="b8dbb-169">Parametr overwrite zapewnia, że ten zestaw rekordów zastępuje dowolny już istniejący zestaw rekordów o tej samej nazwie i typie (istniejące rekordy w tym zestawie rekordów zostaną utracone).</span><span class="sxs-lookup"><span data-stu-id="b8dbb-169">The Overwrite parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span> <span data-ttu-id="b8dbb-170">Parametr Confirm z wartością $False powoduje pominięcie monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-170">The Confirm parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="b8dbb-171">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b8dbb-171">PARAMETERS</span></span>

### <span data-ttu-id="b8dbb-172">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8dbb-172">-DefaultProfile</span></span>
<span data-ttu-id="b8dbb-173">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-173">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8dbb-174">-Metadata</span><span class="sxs-lookup"><span data-stu-id="b8dbb-174">-Metadata</span></span>
<span data-ttu-id="b8dbb-175">Tabela skrótów reprezentująca znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-175">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8dbb-176">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b8dbb-176">-Name</span></span>
<span data-ttu-id="b8dbb-177">Nazwy rekordów w tym zestawie rekordów (w odniesieniu do nazwy strefy i bez kropki przerywanej).</span><span class="sxs-lookup"><span data-stu-id="b8dbb-177">The name of the records in this record set (relative to the name of the zone and without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8dbb-178">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="b8dbb-178">-Overwrite</span></span>
<span data-ttu-id="b8dbb-179">Nie kończy się niepowodzeniem, jeśli zestaw rekordów już istnieje.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-179">Do not fail if the record set already exists.</span></span>

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

### <span data-ttu-id="b8dbb-180">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b8dbb-180">-ParentResourceId</span></span>
<span data-ttu-id="b8dbb-181">Identyfikator zasobu prywatnej strefy DNS.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-181">Private DNS Zone ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8dbb-182">-PrivateDnsRecord</span><span class="sxs-lookup"><span data-stu-id="b8dbb-182">-PrivateDnsRecord</span></span>
<span data-ttu-id="b8dbb-183">Prywatne rekordy DNS, które są częścią tego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-183">The private dns records that are part of this record set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordBase[]
Parameter Sets: (All)
Aliases: PrivateDnsRecords

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8dbb-184">-Records</span><span class="sxs-lookup"><span data-stu-id="b8dbb-184">-RecordType</span></span>
<span data-ttu-id="b8dbb-185">Typ prywatnych rekordów DNS w tym zestawie rekordów.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-185">The type of Private DNS records in this record set.</span></span>

```yaml
Type: Microsoft.Azure.Management.PrivateDns.Models.RecordType
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8dbb-186">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8dbb-186">-ResourceGroupName</span></span>
<span data-ttu-id="b8dbb-187">Grupa zasobów, do której należy strefa.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-187">The resource group to which the zone belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8dbb-188">-TTL</span><span class="sxs-lookup"><span data-stu-id="b8dbb-188">-Ttl</span></span>
<span data-ttu-id="b8dbb-189">Wartość TTL wszystkich rekordów w tym zestawie rekordów.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-189">The TTL value of all the records in this record set.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8dbb-190">-Zone</span><span class="sxs-lookup"><span data-stu-id="b8dbb-190">-Zone</span></span>
<span data-ttu-id="b8dbb-191">Obiekt PrivateDnsZone reprezentujący strefę, w której ma zostać utworzony zestaw rekordów.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-191">The PrivateDnsZone object representing the zone in which to create the record set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8dbb-192">-Nazwa_strefy</span><span class="sxs-lookup"><span data-stu-id="b8dbb-192">-ZoneName</span></span>
<span data-ttu-id="b8dbb-193">Strefa, w której ma zostać utworzony zestaw rekordów (bez przerywanej kropki).</span><span class="sxs-lookup"><span data-stu-id="b8dbb-193">The zone in which to create the record set (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8dbb-194">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b8dbb-194">-Confirm</span></span>
<span data-ttu-id="b8dbb-195">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-195">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8dbb-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8dbb-196">-WhatIf</span></span>
<span data-ttu-id="b8dbb-197">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8dbb-198">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-198">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8dbb-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8dbb-199">CommonParameters</span></span>
<span data-ttu-id="b8dbb-200">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8dbb-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8dbb-201">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8dbb-201">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8dbb-202">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b8dbb-202">INPUTS</span></span>

### <span data-ttu-id="b8dbb-203">Microsoft. Azure. Commands. PrivateDns. models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="b8dbb-203">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="b8dbb-204">System. String</span><span class="sxs-lookup"><span data-stu-id="b8dbb-204">System.String</span></span>

## <span data-ttu-id="b8dbb-205">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b8dbb-205">OUTPUTS</span></span>

### <span data-ttu-id="b8dbb-206">Microsoft. Azure. Commands. PrivateDns. models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b8dbb-206">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="b8dbb-207">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b8dbb-207">NOTES</span></span>

## <span data-ttu-id="b8dbb-208">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b8dbb-208">RELATED LINKS</span></span>
