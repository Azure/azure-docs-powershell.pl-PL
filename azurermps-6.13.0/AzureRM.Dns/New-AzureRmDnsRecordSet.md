---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/new-azurermdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsRecordSet.md
ms.openlocfilehash: 7f271ee6a946356fe9cbf09379e2e620a240b733
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546652"
---
# <span data-ttu-id="13962-101">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="13962-101">New-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="13962-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="13962-102">SYNOPSIS</span></span>
<span data-ttu-id="13962-103">Tworzy zestaw rekordów DNS.</span><span class="sxs-lookup"><span data-stu-id="13962-103">Creates a DNS record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13962-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="13962-104">SYNTAX</span></span>

### <span data-ttu-id="13962-105">Pola (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="13962-105">Fields (Default)</span></span>
```
New-AzureRmDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13962-106">AliasFields</span><span class="sxs-lookup"><span data-stu-id="13962-106">AliasFields</span></span>
```
New-AzureRmDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> [-Ttl <UInt32>]
 -RecordType <RecordType> -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13962-107">Stream</span><span class="sxs-lookup"><span data-stu-id="13962-107">Object</span></span>
```
New-AzureRmDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13962-108">Alias</span><span class="sxs-lookup"><span data-stu-id="13962-108">AliasObject</span></span>
```
New-AzureRmDnsRecordSet -Name <String> -Zone <DnsZone> [-Ttl <UInt32>] -RecordType <RecordType>
 -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13962-109">Opis</span><span class="sxs-lookup"><span data-stu-id="13962-109">DESCRIPTION</span></span>
<span data-ttu-id="13962-110">Polecenie cmdlet **New-AzureRmDnsRecordSet** tworzy nowy zestaw rekordów DNS (Domain Name System) o określonej nazwie i wpisz w określonej strefie.</span><span class="sxs-lookup"><span data-stu-id="13962-110">The **New-AzureRmDnsRecordSet** cmdlet creates a new Domain Name System (DNS) record set with the specified name and type in the specified zone.</span></span>
<span data-ttu-id="13962-111">Obiekt **Recordset** to zestaw rekordów DNS o tej samej nazwie i typie.</span><span class="sxs-lookup"><span data-stu-id="13962-111">A **RecordSet** object is a set of DNS records with the same name and type.</span></span>
<span data-ttu-id="13962-112">Zauważ, że nazwa jest względna względem strefy, a nie w pełni kwalifikowanej nazwy.</span><span class="sxs-lookup"><span data-stu-id="13962-112">Note that the name is relative to the zone and not the fully qualified name.</span></span>
<span data-ttu-id="13962-113">Parametr *DnsRecords* określa rekordy w zestawie rekordów.</span><span class="sxs-lookup"><span data-stu-id="13962-113">The *DnsRecords* parameter specifies the records in the record set.</span></span>
<span data-ttu-id="13962-114">Ten parametr pobiera tablicę rekordów DNS konstruowaną przy użyciu funkcji New-AzureRmDnsRecordConfig.</span><span class="sxs-lookup"><span data-stu-id="13962-114">This parameter takes an array of DNS records, constructed using New-AzureRmDnsRecordConfig.</span></span>
<span data-ttu-id="13962-115">Za pomocą operatora potoku można przekazać obiekt **dnsZone** do tego polecenia cmdlet lub przekazać obiekt **dnsZone** jako parametr *Zone* lub można też określić nazwę strefy według nazwy.</span><span class="sxs-lookup"><span data-stu-id="13962-115">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone by name.</span></span>
<span data-ttu-id="13962-116">Za pomocą zmiennej *Confirm* i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="13962-116">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="13962-117">Jeśli pasujący **zestaw rekordów** już istnieje (ta sama nazwa i typ rekordu), należy określić parametr *zastępowania* , w przeciwnym razie polecenie cmdlet nie spowoduje utworzenia nowego **zestawu rekordów** .</span><span class="sxs-lookup"><span data-stu-id="13962-117">If a matching **RecordSet** already exists (same name and record type), you must specify the *Overwrite* parameter, otherwise the cmdlet will not create a new **RecordSet** .</span></span>

## <span data-ttu-id="13962-118">Przykłady</span><span class="sxs-lookup"><span data-stu-id="13962-118">EXAMPLES</span></span>

### <span data-ttu-id="13962-119">Przykład 1. Tworzenie zestawu rekordów typu A</span><span class="sxs-lookup"><span data-stu-id="13962-119">Example 1: Create a RecordSet of type A</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4)

# To create a record set containing multiple records, use New-AzureRmDnsRecordConfig to add each record to the $Records array,
# then call New-AzureRmDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="13962-120">W tym przykładzie przedstawiono tworzenie **zestawu rekordów** o nazwie www w strefie MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="13962-120">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="13962-121">Zestaw rekordów jest typu A i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="13962-121">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="13962-122">Zawiera jeden rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="13962-122">It contains a single DNS record.</span></span>

### <span data-ttu-id="13962-123">Przykład 2: Tworzenie zestawu rekordów typu AAAA</span><span class="sxs-lookup"><span data-stu-id="13962-123">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="13962-124">W tym przykładzie przedstawiono tworzenie **zestawu rekordów** o nazwie www w strefie MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="13962-124">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="13962-125">Zestaw rekordów jest typu AAAA i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="13962-125">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="13962-126">Zawiera jeden rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="13962-126">It contains a single DNS record.</span></span>
<span data-ttu-id="13962-127">Aby utworzyć **zestaw rekordów** przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="13962-127">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="13962-128">Przykład 3: Tworzenie zestawu rekordów typu CNAME</span><span class="sxs-lookup"><span data-stu-id="13962-128">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="13962-129">W tym przykładzie przedstawiono tworzenie **zestawu rekordów** o nazwie www w strefie MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="13962-129">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="13962-130">Zestaw rekordów jest typu CNAME i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="13962-130">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="13962-131">Zawiera jeden rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="13962-131">It contains a single DNS record.</span></span>
<span data-ttu-id="13962-132">Aby utworzyć **zestaw rekordów** przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="13962-132">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="13962-133">Przykład 4: Tworzenie zestawu rekordów typu MX</span><span class="sxs-lookup"><span data-stu-id="13962-133">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="13962-134">To polecenie tworzy **zestaw rekordów** o nazwie www w strefie MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="13962-134">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="13962-135">Zestaw rekordów jest typu MX i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="13962-135">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="13962-136">Zawiera jeden rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="13962-136">It contains a single DNS record.</span></span>
<span data-ttu-id="13962-137">Aby utworzyć **zestaw rekordów** przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="13962-137">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="13962-138">Przykład 5: Tworzenie zestawu rekordów typu NS</span><span class="sxs-lookup"><span data-stu-id="13962-138">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="13962-139">To polecenie tworzy **zestaw rekordów** o nazwie ns1 w strefie MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="13962-139">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="13962-140">Zestaw rekordów jest typu NS i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="13962-140">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="13962-141">Zawiera jeden rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="13962-141">It contains a single DNS record.</span></span>
<span data-ttu-id="13962-142">Aby utworzyć **zestaw rekordów** przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="13962-142">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="13962-143">Przykład 6: Tworzenie zestawu rekordów typu PTR</span><span class="sxs-lookup"><span data-stu-id="13962-143">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="13962-144">To polecenie tworzy **zestaw rekordów** o nazwie 4 w strefie 3.2.1.in-addr. arpa.</span><span class="sxs-lookup"><span data-stu-id="13962-144">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="13962-145">Zestaw rekordów jest typu PTR i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="13962-145">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="13962-146">Zawiera jeden rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="13962-146">It contains a single DNS record.</span></span>
<span data-ttu-id="13962-147">Aby utworzyć **zestaw rekordów** przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="13962-147">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="13962-148">Przykład 7: Tworzenie zestawu rekordów typu SRV</span><span class="sxs-lookup"><span data-stu-id="13962-148">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="13962-149">To polecenie tworzy **zestaw rekordów** o nazwie _sip. _tcp w strefie MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="13962-149">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="13962-150">Zestaw rekordów jest typu SRV i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="13962-150">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="13962-151">Zawiera jeden rekord DNS wskazujący adres IP 2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="13962-151">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>
<span data-ttu-id="13962-152">Usługa (SIP) i protokół (TCP) są określone jako część nazwy zestawu rekordów, a nie jako część danych rekordu.</span><span class="sxs-lookup"><span data-stu-id="13962-152">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>
<span data-ttu-id="13962-153">Aby utworzyć **zestaw rekordów** przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="13962-153">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="13962-154">Przykład 8: Tworzenie zestawu rekordów typu TXT</span><span class="sxs-lookup"><span data-stu-id="13962-154">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="13962-155">To polecenie tworzy **zestaw rekordów** o nazwie tekst w strefie MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="13962-155">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="13962-156">Zestaw rekordów jest typu TXT i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="13962-156">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="13962-157">Zawiera jeden rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="13962-157">It contains a single DNS record.</span></span>
<span data-ttu-id="13962-158">Aby utworzyć **zestaw rekordów** przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="13962-158">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="13962-159">Przykład 9: Tworzenie zestawu rekordów w strefie Apex</span><span class="sxs-lookup"><span data-stu-id="13962-159">Example 9: Create a RecordSet at the zone apex</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="13962-160">To polecenie tworzy **zestaw rekordów** według wierzchołka (lub głównego) strefy MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="13962-160">This command creates a **RecordSet** at the apex (or root) of the zone myzone.com.</span></span>
<span data-ttu-id="13962-161">W tym celu nazwa zestawu rekordów jest określana jako "@" (łącznie z cudzysłowami podwójnymi).</span><span class="sxs-lookup"><span data-stu-id="13962-161">To do this, the record set name is specified as "@" (including the double-quotes).</span></span>
<span data-ttu-id="13962-162">Nie można utworzyć rekordów CNAME na wierzchołku strefy.</span><span class="sxs-lookup"><span data-stu-id="13962-162">You cannot create CNAME records at the apex of a zone.</span></span>
<span data-ttu-id="13962-163">Jest to ograniczenie standardów DNS. nie jest to ograniczenie dotyczące usługi Azure DNS.</span><span class="sxs-lookup"><span data-stu-id="13962-163">This is a constraint of the DNS standards; it is not a limitation of Azure DNS.</span></span>
<span data-ttu-id="13962-164">Aby utworzyć **zestaw rekordów** przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="13962-164">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="13962-165">Przykład 10: Tworzenie zestawu rekordów symboli wieloznacznych</span><span class="sxs-lookup"><span data-stu-id="13962-165">Example 10: Create a wildcard Record Set</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="13962-166">To polecenie tworzy **zestaw rekordów** o nazwie \* w strefie MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="13962-166">This command creates a **RecordSet** named \* in the zone myzone.com.</span></span>
<span data-ttu-id="13962-167">To jest zestaw rekordów z symbolami wieloznacznymi.</span><span class="sxs-lookup"><span data-stu-id="13962-167">This is a wildcard record set.</span></span>
<span data-ttu-id="13962-168">Aby utworzyć **zestaw rekordów** przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="13962-168">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="13962-169">Przykład 11: Tworzenie pustego zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="13962-169">Example 11: Create an empty record set</span></span>
```
PS C:\>$RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

<span data-ttu-id="13962-170">To polecenie tworzy **zestaw rekordów** o nazwie www w strefie MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="13962-170">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="13962-171">Zestaw rekordów jest typu A i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="13962-171">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="13962-172">To jest pusty zestaw rekordów, który działa jako symbol zastępczy, do którego można później dodawać rekordy.</span><span class="sxs-lookup"><span data-stu-id="13962-172">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="13962-173">Przykład 12: Tworzenie zestawu rekordów i pomijanie wszystkich potwierdzeń</span><span class="sxs-lookup"><span data-stu-id="13962-173">Example 12: Create a record set and suppress all confirmation</span></span>
```
PS C:\>$RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="13962-174">To polecenie tworzy **zestaw rekordów**.</span><span class="sxs-lookup"><span data-stu-id="13962-174">This command creates a **RecordSet**.</span></span>
<span data-ttu-id="13962-175">Parametr *overwrite* zapewnia, że ten zestaw rekordów zastępuje dowolny już istniejący zestaw rekordów o tej samej nazwie i typie (istniejące rekordy w tym zestawie rekordów zostaną utracone).</span><span class="sxs-lookup"><span data-stu-id="13962-175">The *Overwrite* parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span>
<span data-ttu-id="13962-176">Parametr *Confirm* z wartością $false powoduje pominięcie monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="13962-176">The *Confirm* parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="13962-177">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="13962-177">PARAMETERS</span></span>

### <span data-ttu-id="13962-178">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13962-178">-DefaultProfile</span></span>
<span data-ttu-id="13962-179">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="13962-179">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="13962-180">-DnsRecords</span><span class="sxs-lookup"><span data-stu-id="13962-180">-DnsRecords</span></span>
<span data-ttu-id="13962-181">Określa tablicę rekordów DNS, które mają zostać uwzględnione w zestawie rekordów.</span><span class="sxs-lookup"><span data-stu-id="13962-181">Specifies the array of DNS records to include in the record set.</span></span>
<span data-ttu-id="13962-182">Za pomocą polecenia cmdlet New-AzureRmDnsRecordConfig możesz tworzyć obiekty rekordów DNS.</span><span class="sxs-lookup"><span data-stu-id="13962-182">You can use the New-AzureRmDnsRecordConfig cmdlet to create DNS record objects.</span></span>
<span data-ttu-id="13962-183">Zobacz przykłady, aby uzyskać więcej informacji.</span><span class="sxs-lookup"><span data-stu-id="13962-183">See the examples for more information.</span></span>

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

### <span data-ttu-id="13962-184">-Metadata</span><span class="sxs-lookup"><span data-stu-id="13962-184">-Metadata</span></span>
<span data-ttu-id="13962-185">Określa tablicę metadanych, które należy skojarzyć z zestawem rekordów.</span><span class="sxs-lookup"><span data-stu-id="13962-185">Specifies an array of metadata to associate with the RecordSet.</span></span>
<span data-ttu-id="13962-186">Metadane są określane za pomocą par nazwa-wartość, które są reprezentowane jako tabele skrótów, na przykład @ (@ {"name" = "Dept"; "Wartość" = "zakupy"}, @ {"nazwa" = "ENV"; "Wartość" = "produkcja"}).</span><span class="sxs-lookup"><span data-stu-id="13962-186">Metadata is specified using name-value pairs that are represented as hash tables, for example @(@{"Name"="dept"; "Value"="shopping"}, @{"Name"="env"; "Value"="production"}).</span></span>

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

### <span data-ttu-id="13962-187">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="13962-187">-Name</span></span>
<span data-ttu-id="13962-188">Określa nazwę **zestawu rekordów** , który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="13962-188">Specifies the name of the **RecordSet** to create.</span></span>

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

### <span data-ttu-id="13962-189">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="13962-189">-Overwrite</span></span>
<span data-ttu-id="13962-190">Wskazuje, że to polecenie cmdlet zastąpi określony **zestaw rekordów** , jeśli już istnieje.</span><span class="sxs-lookup"><span data-stu-id="13962-190">Indicates that this cmdlet overwrites the specified **RecordSet** if it already exists.</span></span>

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

### <span data-ttu-id="13962-191">-Records</span><span class="sxs-lookup"><span data-stu-id="13962-191">-RecordType</span></span>
<span data-ttu-id="13962-192">Określa typ rekordu DNS, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="13962-192">Specifies the type of DNS record to create.</span></span>
<span data-ttu-id="13962-193">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="13962-193">Valid values are:</span></span>
- <span data-ttu-id="13962-194">Sieci</span><span class="sxs-lookup"><span data-stu-id="13962-194">A</span></span>
- <span data-ttu-id="13962-195">AAAA</span><span class="sxs-lookup"><span data-stu-id="13962-195">AAAA</span></span>
- <span data-ttu-id="13962-196">REKORD</span><span class="sxs-lookup"><span data-stu-id="13962-196">CNAME</span></span>
- <span data-ttu-id="13962-197">MX</span><span class="sxs-lookup"><span data-stu-id="13962-197">MX</span></span>
- <span data-ttu-id="13962-198">REKORDU</span><span class="sxs-lookup"><span data-stu-id="13962-198">NS</span></span>
- <span data-ttu-id="13962-199">SYSTEMU</span><span class="sxs-lookup"><span data-stu-id="13962-199">PTR</span></span>
- <span data-ttu-id="13962-200">SRV</span><span class="sxs-lookup"><span data-stu-id="13962-200">SRV</span></span>
- <span data-ttu-id="13962-201">Rekordy SOA (TXT) są tworzone automatycznie podczas tworzenia strefy i nie można ich tworzyć ręcznie.</span><span class="sxs-lookup"><span data-stu-id="13962-201">TXT SOA records are created automatically when the zone is created and cannot be created manually.</span></span>

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

### <span data-ttu-id="13962-202">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13962-202">-ResourceGroupName</span></span>
<span data-ttu-id="13962-203">Określa grupę zasobów zawierającą strefę DNS.</span><span class="sxs-lookup"><span data-stu-id="13962-203">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="13962-204">Aby określić nazwę strefy, należy również określić parametr *zonename* .</span><span class="sxs-lookup"><span data-stu-id="13962-204">You must also specify the *ZoneName* parameter to specify the zone name.</span></span>
<span data-ttu-id="13962-205">Możesz też określić strefę i grupę zasobów, przechodząc do obiektu strefy DNS przy użyciu parametru *Zone* .</span><span class="sxs-lookup"><span data-stu-id="13962-205">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="13962-206">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="13962-206">-TargetResourceId</span></span>
<span data-ttu-id="13962-207">Identyfikator zasobu docelowego aliasu.</span><span class="sxs-lookup"><span data-stu-id="13962-207">Alias Target Resource Id.</span></span>

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

### <span data-ttu-id="13962-208">-TTL</span><span class="sxs-lookup"><span data-stu-id="13962-208">-Ttl</span></span>
<span data-ttu-id="13962-209">Określa czas wygaśnięcia zestawu rekordów DNS (TTL).</span><span class="sxs-lookup"><span data-stu-id="13962-209">Specifies the Time to Live (TTL) for the DNS RecordSet.</span></span>

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

### <span data-ttu-id="13962-210">-Zone</span><span class="sxs-lookup"><span data-stu-id="13962-210">-Zone</span></span>
<span data-ttu-id="13962-211">Określa DnsZone, w którym ma zostać utworzony **zestaw rekordów**.</span><span class="sxs-lookup"><span data-stu-id="13962-211">Specifies the DnsZone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="13962-212">Możesz też określić strefę przy użyciu parametrów *zonename* i *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="13962-212">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="13962-213">-Nazwa_strefy</span><span class="sxs-lookup"><span data-stu-id="13962-213">-ZoneName</span></span>
<span data-ttu-id="13962-214">Określa nazwę strefy, w której ma zostać utworzony **zestaw rekordów**.</span><span class="sxs-lookup"><span data-stu-id="13962-214">Specifies the name of the zone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="13962-215">Należy także określić grupę zasobów zawierającą strefę za pomocą parametru *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="13962-215">You must also specify the resource group containing the zone using the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="13962-216">Możesz też określić strefę i grupę zasobów, przechodząc do obiektu strefy DNS przy użyciu parametru *Zone* .</span><span class="sxs-lookup"><span data-stu-id="13962-216">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="13962-217">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="13962-217">-Confirm</span></span>
<span data-ttu-id="13962-218">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13962-218">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13962-219">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13962-219">-WhatIf</span></span>
<span data-ttu-id="13962-220">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13962-220">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13962-221">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="13962-221">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13962-222">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13962-222">CommonParameters</span></span>
<span data-ttu-id="13962-223">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13962-223">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13962-224">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13962-224">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13962-225">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13962-225">INPUTS</span></span>

### <span data-ttu-id="13962-226">System. String</span><span class="sxs-lookup"><span data-stu-id="13962-226">System.String</span></span>

### <span data-ttu-id="13962-227">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="13962-227">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="13962-228">Parametry: Zone (ByValue)</span><span class="sxs-lookup"><span data-stu-id="13962-228">Parameters: Zone (ByValue)</span></span>

### <span data-ttu-id="13962-229">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="13962-229">System.UInt32</span></span>

### <span data-ttu-id="13962-230">Microsoft. Azure. Management. DNS. MODELES. recordType</span><span class="sxs-lookup"><span data-stu-id="13962-230">Microsoft.Azure.Management.Dns.Models.RecordType</span></span>

### <span data-ttu-id="13962-231">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="13962-231">System.Collections.Hashtable</span></span>

### <span data-ttu-id="13962-232">Microsoft. Azure. Commands. DNS. DnsRecordBase []</span><span class="sxs-lookup"><span data-stu-id="13962-232">Microsoft.Azure.Commands.Dns.DnsRecordBase[]</span></span>
<span data-ttu-id="13962-233">Parametry: DnsRecords (ByValue)</span><span class="sxs-lookup"><span data-stu-id="13962-233">Parameters: DnsRecords (ByValue)</span></span>

## <span data-ttu-id="13962-234">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="13962-234">OUTPUTS</span></span>

### <span data-ttu-id="13962-235">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="13962-235">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="13962-236">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="13962-236">NOTES</span></span>
<span data-ttu-id="13962-237">Za pomocą parametru *Confirm* można kontrolować, czy to polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="13962-237">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="13962-238">Domyślnie polecenie cmdlet monituje o potwierdzenie, jeśli zmienna $ConfirmPreference Windows PowerShell ma wartość średnią lub niższą.</span><span class="sxs-lookup"><span data-stu-id="13962-238">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="13962-239">Jeśli określisz pozycję *Potwierdź* lub *Potwierdź: $true* , to polecenie cmdlet wyświetli monit o potwierdzenie przed jego uruchomieniem.</span><span class="sxs-lookup"><span data-stu-id="13962-239">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="13962-240">Jeśli określisz pozycję *Confirm (Potwierdź): $false* , polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="13962-240">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="13962-241">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13962-241">RELATED LINKS</span></span>

[<span data-ttu-id="13962-242">Dodaj-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="13962-242">Add-AzureRmDnsRecordConfig</span></span>](./Add-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="13962-243">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="13962-243">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="13962-244">Nowe — AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="13962-244">New-AzureRmDnsRecordConfig</span></span>](./New-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="13962-245">Remove-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="13962-245">Remove-AzureRmDnsRecordSet</span></span>](./Remove-AzureRmDnsRecordSet.md)

[<span data-ttu-id="13962-246">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="13962-246">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)
