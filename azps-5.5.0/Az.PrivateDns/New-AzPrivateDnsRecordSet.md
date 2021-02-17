---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/new-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 1a7042c94457f23302aa8d2899475d7b117e65b4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189346"
---
# <span data-ttu-id="61309-101">New-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="61309-101">New-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="61309-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61309-102">SYNOPSIS</span></span>
<span data-ttu-id="61309-103">Tworzy zestaw rekordów w prywatnej strefie DNS.</span><span class="sxs-lookup"><span data-stu-id="61309-103">Creates a record set in a Private DNS zone.</span></span>

## <span data-ttu-id="61309-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="61309-104">SYNTAX</span></span>

### <span data-ttu-id="61309-105">Pola (domyślne)</span><span class="sxs-lookup"><span data-stu-id="61309-105">Fields (Default)</span></span>
```
New-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> -Ttl <UInt32> [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61309-106">Obiekt</span><span class="sxs-lookup"><span data-stu-id="61309-106">Object</span></span>
```
New-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType> -Ttl <UInt32>
 [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61309-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="61309-107">ResourceId</span></span>
```
New-AzPrivateDnsRecordSet -ParentResourceId <String> -Name <String> -RecordType <RecordType> -Ttl <UInt32>
 [-Metadata <Hashtable>] [-PrivateDnsRecord <PSPrivateDnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61309-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="61309-108">DESCRIPTION</span></span>
<span data-ttu-id="61309-109">Polecenie New-AzPrivateDnsRecordSet cmdlet tworzy nowy zestaw rekordów DNS (Private Domain Name System) o określonej nazwie i wpisz go w określonej strefie prywatnej.</span><span class="sxs-lookup"><span data-stu-id="61309-109">The New-AzPrivateDnsRecordSet cmdlet creates a new Private Domain Name System (DNS) record set with the specified name and type in the specified private zone.</span></span> <span data-ttu-id="61309-110">Obiekt RecordSet to zestaw prywatnych rekordów DNS o takiej samej nazwie i typie.</span><span class="sxs-lookup"><span data-stu-id="61309-110">A RecordSet object is a set of Private DNS records with the same name and type.</span></span> <span data-ttu-id="61309-111">Pamiętaj, że nazwa jest względna dla strefy prywatnej, a nie do w pełni kwalifikowanej nazwy.</span><span class="sxs-lookup"><span data-stu-id="61309-111">Note that the name is relative to the private zone and not the fully qualified name.</span></span> <span data-ttu-id="61309-112">Parametr PrivateDnsRecord określa rekordy w zestawie rekordów.</span><span class="sxs-lookup"><span data-stu-id="61309-112">The PrivateDnsRecord parameter specifies the records in the record set.</span></span> <span data-ttu-id="61309-113">Ten parametr pobiera tablicę prywatnych rekordów DNS skonstruowanych przy użyciu parametru New-AzPrivateDnsRecordConfig.</span><span class="sxs-lookup"><span data-stu-id="61309-113">This parameter takes an array of Private DNS records, constructed using New-AzPrivateDnsRecordConfig.</span></span> <span data-ttu-id="61309-114">Za pomocą operatora potoku można przekazać obiekt PSPrivateDnsZone do tego polecenia cmdlet lub przekazać obiekt PSPrivateDnsZone jako parametr Zone lub określić strefę według jej parametru ResourceId lub możesz też określić strefę według nazwy.</span><span class="sxs-lookup"><span data-stu-id="61309-114">You can use the pipeline operator to pass a PSPrivateDnsZone object to this cmdlet, or you can pass a PSPrivateDnsZone object as the Zone parameter, or you can specify the zone by its ResourceId, or alternatively you can specify the zone by name.</span></span> <span data-ttu-id="61309-115">Możesz użyć parametru Confirm i $ConfirmPreference zmienną programu Windows PowerShell, aby określić, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="61309-115">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="61309-116">Jeśli zgodny zestaw rekordów już istnieje (nazwa i typ rekordu), musisz określić parametr Zastąp, w przeciwnym razie polecenie cmdlet nie utworzy nowego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="61309-116">If a matching RecordSet already exists (same name and record type), you must specify the Overwrite parameter, otherwise the cmdlet will not create a new RecordSet .</span></span>

## <span data-ttu-id="61309-117">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="61309-117">EXAMPLES</span></span>

### <span data-ttu-id="61309-118">Przykład 1. Tworzenie zestawu rekordów typu A</span><span class="sxs-lookup"><span data-stu-id="61309-118">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="61309-119">W tym przykładzie jest owany zestaw rekordów o nazwie www w strefie myzone.com.</span><span class="sxs-lookup"><span data-stu-id="61309-119">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="61309-120">Zestaw rekordów jest typu A i ma czas wygaśnięcia 1 godziny (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="61309-120">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="61309-121">Zawiera ona jeden prywatny rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="61309-121">It contains a single Private DNS record.</span></span>

### <span data-ttu-id="61309-122">Przykład 2. Tworzenie zestawu rekordów typu AAAA</span><span class="sxs-lookup"><span data-stu-id="61309-122">Example 2: Create a RecordSet of type AAAA</span></span>
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

<span data-ttu-id="61309-123">W tym przykładzie jest owany zestaw rekordów o nazwie www w strefie myzone.com.</span><span class="sxs-lookup"><span data-stu-id="61309-123">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="61309-124">Zestaw rekordów jest typu AAAA i ma czas wygaśnięcia 1 godziny (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="61309-124">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="61309-125">Zawiera ona jeden prywatny rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="61309-125">It contains a single Private DNS record.</span></span> <span data-ttu-id="61309-126">Aby utworzyć zestaw rekordów tylko przy użyciu jednego wiersza pn_PowerShell_short lub utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="61309-126">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="61309-127">Przykład 3. Tworzenie zestawu rekordów typu CNAME</span><span class="sxs-lookup"><span data-stu-id="61309-127">Example 3: Create a RecordSet of type CNAME</span></span>
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

<span data-ttu-id="61309-128">W tym przykładzie jest owany zestaw rekordów o nazwie www w strefie myzone.com.</span><span class="sxs-lookup"><span data-stu-id="61309-128">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="61309-129">Zestaw rekordów jest typu CNAME i ma czas wygaśnięcia 1 godziny (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="61309-129">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="61309-130">Zawiera ona jeden prywatny rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="61309-130">It contains a single Private DNS record.</span></span> <span data-ttu-id="61309-131">Aby utworzyć zestaw rekordów tylko przy użyciu jednego wiersza pn_PowerShell_short lub utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="61309-131">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="61309-132">Przykład 4. Tworzenie zestawu rekordów typu MX</span><span class="sxs-lookup"><span data-stu-id="61309-132">Example 4: Create a RecordSet of type MX</span></span>
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

<span data-ttu-id="61309-133">To polecenie tworzy zestaw rekordów o nazwie www w strefie myzone.com.</span><span class="sxs-lookup"><span data-stu-id="61309-133">This command creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="61309-134">Zestaw rekordów jest typu MX i ma czas wygaśnięcia 1 godziny (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="61309-134">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="61309-135">Zawiera ona jeden prywatny rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="61309-135">It contains a single Private DNS record.</span></span> <span data-ttu-id="61309-136">Aby utworzyć zestaw rekordów tylko przy użyciu jednego wiersza pn_PowerShell_short lub utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="61309-136">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="61309-137">Przykład 5. Tworzenie zestawu rekordów typu PTR</span><span class="sxs-lookup"><span data-stu-id="61309-137">Example 5: Create a RecordSet of type PTR</span></span>
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

<span data-ttu-id="61309-138">To polecenie tworzy zestaw rekordów o nazwie 4 w strefie 3.2.1.in-addr.arpa.</span><span class="sxs-lookup"><span data-stu-id="61309-138">This command creates a RecordSet named 4 in the private zone 3.2.1.in-addr.arpa.</span></span> <span data-ttu-id="61309-139">Zestaw rekordów jest typu PTR i ma czas wygaśnięcia 1 godziny (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="61309-139">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="61309-140">Zawiera ona jeden prywatny rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="61309-140">It contains a single Private DNS record.</span></span> <span data-ttu-id="61309-141">Aby utworzyć zestaw rekordów tylko przy użyciu jednego wiersza pn_PowerShell_short lub utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="61309-141">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="61309-142">Przykład 6. Tworzenie zestawu rekordów typu SRV</span><span class="sxs-lookup"><span data-stu-id="61309-142">Example 6: Create a RecordSet of type SRV</span></span>
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

<span data-ttu-id="61309-143">To polecenie tworzy zestaw rekordów o nazwie _sip._tcp w strefie myzone.com.</span><span class="sxs-lookup"><span data-stu-id="61309-143">This command creates a RecordSet named _sip._tcp in the private zone myzone.com.</span></span> <span data-ttu-id="61309-144">Zestaw rekordów jest typu SRV i ma czas wygaśnięcia 1 godziny (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="61309-144">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="61309-145">Zawiera ona jeden prywatny rekord DNS, który wskaże adres IP 2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="61309-145">It contains a single Private DNS record, pointing to the IP address 2001.2.3.4.</span></span> <span data-ttu-id="61309-146">Usługa (sip) i protokół (tcp) są określone jako część nazwy zestawu rekordów, a nie jako część danych rekordu.</span><span class="sxs-lookup"><span data-stu-id="61309-146">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span> <span data-ttu-id="61309-147">Aby utworzyć zestaw rekordów tylko przy użyciu jednego wiersza pn_PowerShell_short lub utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="61309-147">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="61309-148">Przykład 7. Tworzenie zestawu rekordów typu TXT</span><span class="sxs-lookup"><span data-stu-id="61309-148">Example 7: Create a RecordSet of type TXT</span></span>
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

<span data-ttu-id="61309-149">To polecenie tworzy nazwany tekst zestawu rekordów w strefie myzone.com.</span><span class="sxs-lookup"><span data-stu-id="61309-149">This command creates a RecordSet named text in the private zone myzone.com.</span></span> <span data-ttu-id="61309-150">Zestaw rekordów jest typu TXT i ma czas wygaśnięcia 1 godziny (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="61309-150">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="61309-151">Zawiera ona jeden prywatny rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="61309-151">It contains a single Private DNS record.</span></span> <span data-ttu-id="61309-152">Aby utworzyć zestaw rekordów tylko przy użyciu jednego wiersza pn_PowerShell_short lub utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="61309-152">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="61309-153">Przykład 8. Tworzenie zestawu rekordów w wierzchołku strefy</span><span class="sxs-lookup"><span data-stu-id="61309-153">Example 8:  Create a RecordSet at the zone apex</span></span>
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

<span data-ttu-id="61309-154">To polecenie tworzy zestaw rekordów na wierzchu (lub katalogu głównym) strefy myzone.com.</span><span class="sxs-lookup"><span data-stu-id="61309-154">This command creates a RecordSet at the apex (or root) of the private zone myzone.com.</span></span> <span data-ttu-id="61309-155">W tym celu nazwa zestawu rekordów zostanie określona jako "@" (łącznie z cudzysłowami podwójnymi).</span><span class="sxs-lookup"><span data-stu-id="61309-155">To do this, the record set name is specified as "@" (including the double-quotes).</span></span> <span data-ttu-id="61309-156">Nie można tworzyć rekordów CNAME na początku strefy.</span><span class="sxs-lookup"><span data-stu-id="61309-156">You cannot create CNAME records at the apex of a zone.</span></span> <span data-ttu-id="61309-157">Jest to ograniczenie standardów DNS. nie jest to ograniczenie usługi Azure Private DNS.</span><span class="sxs-lookup"><span data-stu-id="61309-157">This is a constraint of the DNS standards; it is not a limitation of Azure Private DNS.</span></span> <span data-ttu-id="61309-158">Aby utworzyć zestaw rekordów tylko przy użyciu jednego wiersza pn_PowerShell_short lub utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="61309-158">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="61309-159">Przykład 9. Tworzenie zestawu rekordów z symbolami wieloznacznych</span><span class="sxs-lookup"><span data-stu-id="61309-159">Example 9:  Create a wildcard Record Set</span></span>

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

<span data-ttu-id="61309-160">To polecenie tworzy zestaw rekordów o nazwie \* w strefie myzone.com.</span><span class="sxs-lookup"><span data-stu-id="61309-160">This command creates a RecordSet named \* in the private zone myzone.com.</span></span> <span data-ttu-id="61309-161">Jest to zestaw rekordów z symbolami wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="61309-161">This is a wildcard record set.</span></span> <span data-ttu-id="61309-162">Aby utworzyć zestaw rekordów tylko przy użyciu jednego wiersza pn_PowerShell_short lub utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="61309-162">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="61309-163">Przykład 10. Tworzenie pustego zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="61309-163">Example 10:  Create an empty Record Set</span></span>

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

<span data-ttu-id="61309-164">To polecenie tworzy zestaw rekordów o nazwie \* w strefie myzone.com.</span><span class="sxs-lookup"><span data-stu-id="61309-164">This command creates a RecordSet named \* in the private zone myzone.com.</span></span> <span data-ttu-id="61309-165">Zestaw rekordów jest typu A i ma czas wygaśnięcia 1 godziny (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="61309-165">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="61309-166">Jest to pusty zestaw rekordów, który pełni rolę symbolu zastępczego, do którego można później dodawać rekordy.</span><span class="sxs-lookup"><span data-stu-id="61309-166">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="61309-167">Przykład 11. Tworzenie zestawu rekordów i pomijanie wszystkich potwierdzeń</span><span class="sxs-lookup"><span data-stu-id="61309-167">Example 11:  Create a record set and suppress all confirmation</span></span>

```powershell
PS C:\>$RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="61309-168">To polecenie tworzy zestaw rekordów.</span><span class="sxs-lookup"><span data-stu-id="61309-168">This command creates a RecordSet.</span></span> <span data-ttu-id="61309-169">Parametr Zastąp gwarantuje, że ten zestaw rekordów zastąpi istniejący wcześniej zestaw rekordów o takiej samej nazwie i typie (istniejące rekordy w tym zestawie rekordów zostaną utracone).</span><span class="sxs-lookup"><span data-stu-id="61309-169">The Overwrite parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span> <span data-ttu-id="61309-170">Parametr Confirm z wartością $False pomija monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="61309-170">The Confirm parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="61309-171">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61309-171">PARAMETERS</span></span>

### <span data-ttu-id="61309-172">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61309-172">-DefaultProfile</span></span>
<span data-ttu-id="61309-173">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="61309-173">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61309-174">— Metadane</span><span class="sxs-lookup"><span data-stu-id="61309-174">-Metadata</span></span>
<span data-ttu-id="61309-175">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="61309-175">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="61309-176">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="61309-176">-Name</span></span>
<span data-ttu-id="61309-177">Nazwa rekordów w tym zestawie rekordów (względem nazwy strefy i bez kropki kończącej).</span><span class="sxs-lookup"><span data-stu-id="61309-177">The name of the records in this record set (relative to the name of the zone and without a terminating dot).</span></span>

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

### <span data-ttu-id="61309-178">— Zastąp</span><span class="sxs-lookup"><span data-stu-id="61309-178">-Overwrite</span></span>
<span data-ttu-id="61309-179">Nie zawiedzie, jeśli zestaw rekordów już istnieje.</span><span class="sxs-lookup"><span data-stu-id="61309-179">Do not fail if the record set already exists.</span></span>

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

### <span data-ttu-id="61309-180">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="61309-180">-ParentResourceId</span></span>
<span data-ttu-id="61309-181">Private DNS Zone ResourceID (Prywatny adres DNS Strefy ResourceID).</span><span class="sxs-lookup"><span data-stu-id="61309-181">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="61309-182">-PrivateDnsRecord</span><span class="sxs-lookup"><span data-stu-id="61309-182">-PrivateDnsRecord</span></span>
<span data-ttu-id="61309-183">Prywatne rekordy DNS, które są częścią tego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="61309-183">The private dns records that are part of this record set.</span></span>

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

### <span data-ttu-id="61309-184">-RecordType</span><span class="sxs-lookup"><span data-stu-id="61309-184">-RecordType</span></span>
<span data-ttu-id="61309-185">Typ prywatnych rekordów DNS w tym zestawie rekordów.</span><span class="sxs-lookup"><span data-stu-id="61309-185">The type of Private DNS records in this record set.</span></span>

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

### <span data-ttu-id="61309-186">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61309-186">-ResourceGroupName</span></span>
<span data-ttu-id="61309-187">Grupa zasobów, do której należy strefa.</span><span class="sxs-lookup"><span data-stu-id="61309-187">The resource group to which the zone belongs.</span></span>

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

### <span data-ttu-id="61309-188">— Ttl</span><span class="sxs-lookup"><span data-stu-id="61309-188">-Ttl</span></span>
<span data-ttu-id="61309-189">Wartość TTL (Czas wygaśnięcia) wszystkich rekordów w tym zestawie rekordów.</span><span class="sxs-lookup"><span data-stu-id="61309-189">The TTL value of all the records in this record set.</span></span>

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

### <span data-ttu-id="61309-190">— Strefa</span><span class="sxs-lookup"><span data-stu-id="61309-190">-Zone</span></span>
<span data-ttu-id="61309-191">Obiekt PrivateDnsZone reprezentujący strefę, w której należy utworzyć zestaw rekordów.</span><span class="sxs-lookup"><span data-stu-id="61309-191">The PrivateDnsZone object representing the zone in which to create the record set.</span></span>

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

### <span data-ttu-id="61309-192">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="61309-192">-ZoneName</span></span>
<span data-ttu-id="61309-193">Strefa, w której należy utworzyć zestaw rekordów (bez kropki kończącej).</span><span class="sxs-lookup"><span data-stu-id="61309-193">The zone in which to create the record set (without a terminating dot).</span></span>

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

### <span data-ttu-id="61309-194">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="61309-194">-Confirm</span></span>
<span data-ttu-id="61309-195">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="61309-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61309-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61309-196">-WhatIf</span></span>
<span data-ttu-id="61309-197">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61309-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61309-198">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="61309-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61309-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61309-199">CommonParameters</span></span>
<span data-ttu-id="61309-200">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61309-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61309-201">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61309-201">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61309-202">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="61309-202">INPUTS</span></span>

### <span data-ttu-id="61309-203">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="61309-203">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="61309-204">System.String</span><span class="sxs-lookup"><span data-stu-id="61309-204">System.String</span></span>

## <span data-ttu-id="61309-205">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="61309-205">OUTPUTS</span></span>

### <span data-ttu-id="61309-206">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="61309-206">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="61309-207">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="61309-207">NOTES</span></span>

## <span data-ttu-id="61309-208">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="61309-208">RELATED LINKS</span></span>
