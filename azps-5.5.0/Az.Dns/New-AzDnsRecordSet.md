---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
ms.openlocfilehash: bb2e9a9729ed911902e493422109cae764ad6d5f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243683"
---
# <span data-ttu-id="72281-101">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="72281-101">New-AzDnsRecordSet</span></span>

## <span data-ttu-id="72281-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72281-102">SYNOPSIS</span></span>
<span data-ttu-id="72281-103">Tworzy zestaw rekordów DNS.</span><span class="sxs-lookup"><span data-stu-id="72281-103">Creates a DNS record set.</span></span>

## <span data-ttu-id="72281-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="72281-104">SYNTAX</span></span>

### <span data-ttu-id="72281-105">Pola (domyślne)</span><span class="sxs-lookup"><span data-stu-id="72281-105">Fields (Default)</span></span>
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72281-106">AliasFields</span><span class="sxs-lookup"><span data-stu-id="72281-106">AliasFields</span></span>
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> [-Ttl <UInt32>]
 -RecordType <RecordType> -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72281-107">Obiekt</span><span class="sxs-lookup"><span data-stu-id="72281-107">Object</span></span>
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72281-108">AliasObject</span><span class="sxs-lookup"><span data-stu-id="72281-108">AliasObject</span></span>
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> [-Ttl <UInt32>] -RecordType <RecordType>
 -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72281-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="72281-109">DESCRIPTION</span></span>
<span data-ttu-id="72281-110">Polecenie **cmdlet New-AzDnsRecordSet** tworzy nowy zestaw rekordów DNS (Domain Name System) o określonej nazwie i wpisz w określonej strefie.</span><span class="sxs-lookup"><span data-stu-id="72281-110">The **New-AzDnsRecordSet** cmdlet creates a new Domain Name System (DNS) record set with the specified name and type in the specified zone.</span></span>
<span data-ttu-id="72281-111">Obiekt **RecordSet** to zestaw rekordów DNS o tej samej nazwie i typie.</span><span class="sxs-lookup"><span data-stu-id="72281-111">A **RecordSet** object is a set of DNS records with the same name and type.</span></span>
<span data-ttu-id="72281-112">Pamiętaj, że nazwa jest względna dla strefy, a nie do w pełni kwalifikowanej nazwy.</span><span class="sxs-lookup"><span data-stu-id="72281-112">Note that the name is relative to the zone and not the fully qualified name.</span></span>
<span data-ttu-id="72281-113">Parametr *DnsRecords* określa rekordy w zestawie rekordów.</span><span class="sxs-lookup"><span data-stu-id="72281-113">The *DnsRecords* parameter specifies the records in the record set.</span></span>
<span data-ttu-id="72281-114">Ten parametr pobiera tablicę rekordów DNS skonstruowanych przy użyciu narzędzia New-AzDnsRecordConfig.</span><span class="sxs-lookup"><span data-stu-id="72281-114">This parameter takes an array of DNS records, constructed using New-AzDnsRecordConfig.</span></span>
<span data-ttu-id="72281-115">Za pomocą operatora potoku możesz przekazać obiekt **DnsZone** do tego polecenia cmdlet lub przekazać obiekt **DnsZone** jako parametr *Zone* lub alternatywnie możesz określić strefę według nazwy.</span><span class="sxs-lookup"><span data-stu-id="72281-115">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone by name.</span></span>
<span data-ttu-id="72281-116">Za pomocą *parametru Confirm* i $ConfirmPreference programu Windows PowerShell możesz kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="72281-116">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="72281-117">Jeśli zgodny zestaw **rekordów** już istnieje (nazwa i typ rekordu), musisz określić parametr *Zastąp,* w przeciwnym razie polecenie cmdlet nie utworzy **nowego zestawu rekordów.**</span><span class="sxs-lookup"><span data-stu-id="72281-117">If a matching **RecordSet** already exists (same name and record type), you must specify the *Overwrite* parameter, otherwise the cmdlet will not create a new **RecordSet** .</span></span>

## <span data-ttu-id="72281-118">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="72281-118">EXAMPLES</span></span>

### <span data-ttu-id="72281-119">Przykład 1. Tworzenie zestawu rekordów typu A</span><span class="sxs-lookup"><span data-stu-id="72281-119">Example 1: Create a RecordSet of type A</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -IPv4Address 1.2.3.4)

# To create a record set containing multiple records, use New-AzDnsRecordConfig to add each record to the $Records array,
# then call New-AzDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="72281-120">W tym przykładzie **jest owany zestaw rekordów** o nazwie www w strefie myzone.com.</span><span class="sxs-lookup"><span data-stu-id="72281-120">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="72281-121">Zestaw rekordów jest typu A i ma czas wygaśnięcia 1 godziny (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="72281-121">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="72281-122">Zawiera jeden rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="72281-122">It contains a single DNS record.</span></span>

### <span data-ttu-id="72281-123">Przykład 2. Tworzenie zestawu rekordów typu AAAA</span><span class="sxs-lookup"><span data-stu-id="72281-123">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="72281-124">W tym przykładzie **jest owany zestaw rekordów** o nazwie www w strefie myzone.com.</span><span class="sxs-lookup"><span data-stu-id="72281-124">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="72281-125">Zestaw rekordów jest typu AAAA i ma czas wygaśnięcia 1 godziny (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="72281-125">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="72281-126">Zawiera jeden rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="72281-126">It contains a single DNS record.</span></span>
<span data-ttu-id="72281-127">Aby utworzyć zestaw **rekordów tylko** przy użyciu jednego wiersza pn_PowerShell_short lub utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="72281-127">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="72281-128">Przykład 3. Tworzenie zestawu rekordów typu CNAME</span><span class="sxs-lookup"><span data-stu-id="72281-128">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="72281-129">W tym przykładzie **jest owany zestaw rekordów** o nazwie www w strefie myzone.com.</span><span class="sxs-lookup"><span data-stu-id="72281-129">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="72281-130">Zestaw rekordów jest typu CNAME i ma czas wygaśnięcia 1 godziny (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="72281-130">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="72281-131">Zawiera jeden rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="72281-131">It contains a single DNS record.</span></span>
<span data-ttu-id="72281-132">Aby utworzyć zestaw **rekordów tylko** przy użyciu jednego wiersza pn_PowerShell_short lub utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="72281-132">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="72281-133">Przykład 4. Tworzenie zestawu rekordów typu MX</span><span class="sxs-lookup"><span data-stu-id="72281-133">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "mail" -RecordType MX -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="72281-134">To polecenie tworzy zestaw **rekordów** o nazwie www w strefie myzone.com.</span><span class="sxs-lookup"><span data-stu-id="72281-134">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="72281-135">Zestaw rekordów jest typu MX i ma czas wygaśnięcia 1 godziny (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="72281-135">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="72281-136">Zawiera jeden rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="72281-136">It contains a single DNS record.</span></span>
<span data-ttu-id="72281-137">Aby utworzyć zestaw **rekordów tylko** przy użyciu jednego wiersza pn_PowerShell_short lub utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="72281-137">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="72281-138">Przykład 5. Tworzenie zestawu rekordów typu NS</span><span class="sxs-lookup"><span data-stu-id="72281-138">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="72281-139">To polecenie tworzy zestaw **rekordów** o nazwie ns1 w strefie myzone.com.</span><span class="sxs-lookup"><span data-stu-id="72281-139">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="72281-140">Zestaw rekordów jest typu NS i ma czas wygaśnięcia 1 godziny (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="72281-140">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="72281-141">Zawiera jeden rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="72281-141">It contains a single DNS record.</span></span>
<span data-ttu-id="72281-142">Aby utworzyć zestaw **rekordów tylko** przy użyciu jednego wiersza pn_PowerShell_short lub utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="72281-142">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="72281-143">Przykład 6. Tworzenie zestawu rekordów typu PTR</span><span class="sxs-lookup"><span data-stu-id="72281-143">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="72281-144">To polecenie tworzy zestaw **rekordów o** nazwie 4 w strefie 3.2.1.in-addr.arpa.</span><span class="sxs-lookup"><span data-stu-id="72281-144">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="72281-145">Zestaw rekordów jest typu PTR i ma czas wygaśnięcia 1 godziny (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="72281-145">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="72281-146">Zawiera jeden rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="72281-146">It contains a single DNS record.</span></span>
<span data-ttu-id="72281-147">Aby utworzyć zestaw **rekordów tylko** przy użyciu jednego wiersza pn_PowerShell_short lub utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="72281-147">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="72281-148">Przykład 7. Tworzenie zestawu rekordów typu SRV</span><span class="sxs-lookup"><span data-stu-id="72281-148">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="72281-149">To polecenie tworzy **zestaw** rekordów o nazwie _sip._tcp w strefie myzone.com.</span><span class="sxs-lookup"><span data-stu-id="72281-149">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="72281-150">Zestaw rekordów jest typu SRV i ma czas wygaśnięcia 1 godziny (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="72281-150">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="72281-151">Zawiera ona jeden rekord DNS, który wskaże adres IP 2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="72281-151">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>
<span data-ttu-id="72281-152">Usługa (sip) i protokół (tcp) są określone jako część nazwy zestawu rekordów, a nie jako część danych rekordu.</span><span class="sxs-lookup"><span data-stu-id="72281-152">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>
<span data-ttu-id="72281-153">Aby utworzyć zestaw **rekordów tylko** przy użyciu jednego wiersza pn_PowerShell_short lub utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="72281-153">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="72281-154">Przykład 8. Tworzenie zestawu rekordów typu TXT</span><span class="sxs-lookup"><span data-stu-id="72281-154">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="72281-155">To polecenie tworzy **nazwany tekst zestawu** rekordów w strefie myzone.com.</span><span class="sxs-lookup"><span data-stu-id="72281-155">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="72281-156">Zestaw rekordów jest typu TXT i ma czas wygaśnięcia 1 godziny (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="72281-156">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="72281-157">Zawiera jeden rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="72281-157">It contains a single DNS record.</span></span>
<span data-ttu-id="72281-158">Aby utworzyć zestaw **rekordów tylko** przy użyciu jednego wiersza pn_PowerShell_short lub utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="72281-158">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="72281-159">Przykład 9. Tworzenie zestawu rekordów w wierzchołku strefy</span><span class="sxs-lookup"><span data-stu-id="72281-159">Example 9: Create a RecordSet at the zone apex</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="72281-160">To polecenie tworzy **zestaw rekordów na** wierzchu (lub katalogu głównym) strefy myzone.com.</span><span class="sxs-lookup"><span data-stu-id="72281-160">This command creates a **RecordSet** at the apex (or root) of the zone myzone.com.</span></span>
<span data-ttu-id="72281-161">W tym celu nazwa zestawu rekordów zostanie określona jako "@" (łącznie z cudzysłowami podwójnymi).</span><span class="sxs-lookup"><span data-stu-id="72281-161">To do this, the record set name is specified as "@" (including the double-quotes).</span></span>
<span data-ttu-id="72281-162">Nie można tworzyć rekordów CNAME na początku strefy.</span><span class="sxs-lookup"><span data-stu-id="72281-162">You cannot create CNAME records at the apex of a zone.</span></span>
<span data-ttu-id="72281-163">Jest to ograniczenie standardów DNS. nie jest to ograniczenie systemu Azure DNS.</span><span class="sxs-lookup"><span data-stu-id="72281-163">This is a constraint of the DNS standards; it is not a limitation of Azure DNS.</span></span>
<span data-ttu-id="72281-164">Aby utworzyć zestaw **rekordów tylko** przy użyciu jednego wiersza pn_PowerShell_short lub utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="72281-164">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="72281-165">Przykład 10. Tworzenie zestawu rekordów z symbolami wieloznacznych</span><span class="sxs-lookup"><span data-stu-id="72281-165">Example 10: Create a wildcard Record Set</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="72281-166">To polecenie tworzy zestaw rekordów **o** nazwie \* w strefie myzone.com.</span><span class="sxs-lookup"><span data-stu-id="72281-166">This command creates a **RecordSet** named \* in the zone myzone.com.</span></span>
<span data-ttu-id="72281-167">Jest to zestaw rekordów z symbolami wieloznacznych.</span><span class="sxs-lookup"><span data-stu-id="72281-167">This is a wildcard record set.</span></span>
<span data-ttu-id="72281-168">Aby utworzyć zestaw **rekordów tylko** przy użyciu jednego wiersza pn_PowerShell_short lub utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="72281-168">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="72281-169">Przykład 11. Tworzenie pustego zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="72281-169">Example 11: Create an empty record set</span></span>
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

<span data-ttu-id="72281-170">To polecenie tworzy zestaw **rekordów** o nazwie www w strefie myzone.com.</span><span class="sxs-lookup"><span data-stu-id="72281-170">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="72281-171">Zestaw rekordów jest typu A i ma czas wygaśnięcia 1 godziny (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="72281-171">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="72281-172">Jest to pusty zestaw rekordów, który pełni rolę symbolu zastępczego, do którego można później dodawać rekordy.</span><span class="sxs-lookup"><span data-stu-id="72281-172">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="72281-173">Przykład 12. Tworzenie zestawu rekordów i pomijanie wszystkich potwierdzeń</span><span class="sxs-lookup"><span data-stu-id="72281-173">Example 12: Create a record set and suppress all confirmation</span></span>
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="72281-174">To polecenie tworzy zestaw **rekordów.**</span><span class="sxs-lookup"><span data-stu-id="72281-174">This command creates a **RecordSet**.</span></span>
<span data-ttu-id="72281-175">Parametr *Zastąp* gwarantuje, że ten zestaw rekordów zastąpi istniejący wcześniej zestaw rekordów o takiej samej nazwie i typie (istniejące rekordy w tym zestawie rekordów zostaną utracone).</span><span class="sxs-lookup"><span data-stu-id="72281-175">The *Overwrite* parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span>
<span data-ttu-id="72281-176">Parametr *Confirm* z wartością $False pomija monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="72281-176">The *Confirm* parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="72281-177">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72281-177">PARAMETERS</span></span>

### <span data-ttu-id="72281-178">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72281-178">-DefaultProfile</span></span>
<span data-ttu-id="72281-179">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="72281-179">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72281-180">- DnsRecords</span><span class="sxs-lookup"><span data-stu-id="72281-180">-DnsRecords</span></span>
<span data-ttu-id="72281-181">Określa tablicę rekordów DNS, które mają być dołączane do zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="72281-181">Specifies the array of DNS records to include in the record set.</span></span>
<span data-ttu-id="72281-182">Możesz użyć polecenia cmdlet New-AzDnsRecordConfig do tworzenia obiektów rekordów DNS.</span><span class="sxs-lookup"><span data-stu-id="72281-182">You can use the New-AzDnsRecordConfig cmdlet to create DNS record objects.</span></span>
<span data-ttu-id="72281-183">Zobacz przykłady, aby uzyskać więcej informacji.</span><span class="sxs-lookup"><span data-stu-id="72281-183">See the examples for more information.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordBase[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72281-184">— Metadane</span><span class="sxs-lookup"><span data-stu-id="72281-184">-Metadata</span></span>
<span data-ttu-id="72281-185">Określa tablicę metadanych do skojarzenia z zestawem rekordów.</span><span class="sxs-lookup"><span data-stu-id="72281-185">Specifies an array of metadata to associate with the RecordSet.</span></span>
<span data-ttu-id="72281-186">Metadane są określane przy użyciu par nazwa-wartość, które są reprezentowane jako tabele skrótów, na przykład @{"dept"="shopping";" env"="production"}.</span><span class="sxs-lookup"><span data-stu-id="72281-186">Metadata is specified using name-value pairs that are represented as hash tables, for example @{"dept"="shopping";"env"="production"}.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72281-187">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="72281-187">-Name</span></span>
<span data-ttu-id="72281-188">Określa nazwę zestawu rekordów **do** utworzenia.</span><span class="sxs-lookup"><span data-stu-id="72281-188">Specifies the name of the **RecordSet** to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72281-189">— Zastąp</span><span class="sxs-lookup"><span data-stu-id="72281-189">-Overwrite</span></span>
<span data-ttu-id="72281-190">Wskazuje, że to polecenie cmdlet zastępuje określony zestaw **rekordów,** jeśli już istnieje.</span><span class="sxs-lookup"><span data-stu-id="72281-190">Indicates that this cmdlet overwrites the specified **RecordSet** if it already exists.</span></span>

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

### <span data-ttu-id="72281-191">-RecordType</span><span class="sxs-lookup"><span data-stu-id="72281-191">-RecordType</span></span>
<span data-ttu-id="72281-192">Określa typ rekordu DNS do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="72281-192">Specifies the type of DNS record to create.</span></span>
<span data-ttu-id="72281-193">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="72281-193">Valid values are:</span></span>
- <span data-ttu-id="72281-194">A</span><span class="sxs-lookup"><span data-stu-id="72281-194">A</span></span>
- <span data-ttu-id="72281-195">AAAA</span><span class="sxs-lookup"><span data-stu-id="72281-195">AAAA</span></span>
- <span data-ttu-id="72281-196">CNAME</span><span class="sxs-lookup"><span data-stu-id="72281-196">CNAME</span></span>
- <span data-ttu-id="72281-197">MX</span><span class="sxs-lookup"><span data-stu-id="72281-197">MX</span></span>
- <span data-ttu-id="72281-198">NS</span><span class="sxs-lookup"><span data-stu-id="72281-198">NS</span></span>
- <span data-ttu-id="72281-199">PTR</span><span class="sxs-lookup"><span data-stu-id="72281-199">PTR</span></span>
- <span data-ttu-id="72281-200">SRV</span><span class="sxs-lookup"><span data-stu-id="72281-200">SRV</span></span>
- <span data-ttu-id="72281-201">Rekordy SOA TXT są tworzone automatycznie po utworzeniu strefy i nie można ich utworzyć ręcznie.</span><span class="sxs-lookup"><span data-stu-id="72281-201">TXT SOA records are created automatically when the zone is created and cannot be created manually.</span></span>

```yaml
Type: Microsoft.Azure.Management.Dns.Models.RecordType
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72281-202">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72281-202">-ResourceGroupName</span></span>
<span data-ttu-id="72281-203">Określa grupę zasobów zawierającą strefę DNS.</span><span class="sxs-lookup"><span data-stu-id="72281-203">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="72281-204">Aby określić nazwę strefy, musisz także określić parametr *ZoneName.*</span><span class="sxs-lookup"><span data-stu-id="72281-204">You must also specify the *ZoneName* parameter to specify the zone name.</span></span>
<span data-ttu-id="72281-205">Możesz również określić strefę i grupę zasobów, przechodząc do obiektu DNS Zone przy użyciu *parametru Zone.*</span><span class="sxs-lookup"><span data-stu-id="72281-205">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, AliasFields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72281-206">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="72281-206">-TargetResourceId</span></span>
<span data-ttu-id="72281-207">Identyfikator zasobu docelowego aliasu.</span><span class="sxs-lookup"><span data-stu-id="72281-207">Alias Target Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AliasFields, AliasObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72281-208">— Ttl</span><span class="sxs-lookup"><span data-stu-id="72281-208">-Ttl</span></span>
<span data-ttu-id="72281-209">Określa czas wygaśnięcia (TTL) zestawu rekordów DNS.</span><span class="sxs-lookup"><span data-stu-id="72281-209">Specifies the Time to Live (TTL) for the DNS RecordSet.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: Fields, Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.UInt32
Parameter Sets: AliasFields, AliasObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72281-210">— Strefa</span><span class="sxs-lookup"><span data-stu-id="72281-210">-Zone</span></span>
<span data-ttu-id="72281-211">Określa strefę DnsZone, w której ma być **tworzyć zestaw rekordów.**</span><span class="sxs-lookup"><span data-stu-id="72281-211">Specifies the DnsZone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="72281-212">Można również określić strefę, używając parametrów *Nazwa_strefy* i *NazwaGrupy Zasobów.*</span><span class="sxs-lookup"><span data-stu-id="72281-212">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object, AliasObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72281-213">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="72281-213">-ZoneName</span></span>
<span data-ttu-id="72281-214">Określa nazwę strefy, w której ma być tworzyć **zestaw rekordów.**</span><span class="sxs-lookup"><span data-stu-id="72281-214">Specifies the name of the zone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="72281-215">Grupę zasobów zawierającą strefę należy także określić przy użyciu *parametru ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="72281-215">You must also specify the resource group containing the zone using the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="72281-216">Możesz również określić strefę i grupę zasobów, przechodząc do obiektu DNS Zone przy użyciu *parametru Zone.*</span><span class="sxs-lookup"><span data-stu-id="72281-216">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, AliasFields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72281-217">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="72281-217">-Confirm</span></span>
<span data-ttu-id="72281-218">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="72281-218">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72281-219">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72281-219">-WhatIf</span></span>
<span data-ttu-id="72281-220">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72281-220">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72281-221">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="72281-221">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72281-222">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72281-222">CommonParameters</span></span>
<span data-ttu-id="72281-223">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72281-223">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72281-224">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72281-224">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72281-225">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="72281-225">INPUTS</span></span>

### <span data-ttu-id="72281-226">System.String</span><span class="sxs-lookup"><span data-stu-id="72281-226">System.String</span></span>

### <span data-ttu-id="72281-227">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="72281-227">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="72281-228">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="72281-228">System.UInt32</span></span>

### <span data-ttu-id="72281-229">Microsoft.Azure.Management.Dns.Models.RecordType</span><span class="sxs-lookup"><span data-stu-id="72281-229">Microsoft.Azure.Management.Dns.Models.RecordType</span></span>

### <span data-ttu-id="72281-230">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="72281-230">System.Collections.Hashtable</span></span>

### <span data-ttu-id="72281-231">Microsoft.Azure.Commands.Dns.DnsRecordBase[]</span><span class="sxs-lookup"><span data-stu-id="72281-231">Microsoft.Azure.Commands.Dns.DnsRecordBase[]</span></span>

## <span data-ttu-id="72281-232">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="72281-232">OUTPUTS</span></span>

### <span data-ttu-id="72281-233">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="72281-233">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="72281-234">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="72281-234">NOTES</span></span>
<span data-ttu-id="72281-235">Za pomocą *parametru Confirm* można określić, czy to polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="72281-235">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="72281-236">Domyślnie polecenie cmdlet wyświetla monit o potwierdzenie, jeśli zmienna programu Windows PowerShell $ConfirmPreference wartość średnią lub niższą.</span><span class="sxs-lookup"><span data-stu-id="72281-236">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="72281-237">Jeśli określisz *potwierdź* *lub potwierdź:$True,* to polecenie cmdlet wyświetli monit o potwierdzenie przed jego rozpoczęciem.</span><span class="sxs-lookup"><span data-stu-id="72281-237">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="72281-238">Jeśli określisz *polecenie Potwierdź:$False,* polecenie cmdlet nie wyświetli monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="72281-238">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="72281-239">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="72281-239">RELATED LINKS</span></span>

[<span data-ttu-id="72281-240">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="72281-240">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="72281-241">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="72281-241">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="72281-242">New-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="72281-242">New-AzDnsRecordConfig</span></span>](./New-AzDnsRecordConfig.md)

[<span data-ttu-id="72281-243">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="72281-243">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

[<span data-ttu-id="72281-244">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="72281-244">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
