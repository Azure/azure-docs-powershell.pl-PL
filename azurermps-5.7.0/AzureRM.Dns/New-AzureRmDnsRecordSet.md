---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/new-azurermdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsRecordSet.md
ms.openlocfilehash: 9896a8e1cfd2e3c0dc3887513d93e902260b82c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718501"
---
# <span data-ttu-id="690a0-101">New-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="690a0-101">New-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="690a0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="690a0-102">SYNOPSIS</span></span>
<span data-ttu-id="690a0-103">Tworzy zestaw rekordów DNS.</span><span class="sxs-lookup"><span data-stu-id="690a0-103">Creates a DNS record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="690a0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="690a0-104">SYNTAX</span></span>

### <span data-ttu-id="690a0-105">Field</span><span class="sxs-lookup"><span data-stu-id="690a0-105">Fields</span></span>
```
New-AzureRmDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="690a0-106">Stream</span><span class="sxs-lookup"><span data-stu-id="690a0-106">Object</span></span>
```
New-AzureRmDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="690a0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="690a0-107">DESCRIPTION</span></span>
<span data-ttu-id="690a0-108">Polecenie cmdlet **New-AzureRmDnsRecordSet** tworzy nowy zestaw rekordów DNS (Domain Name System) o określonej nazwie i wpisz w określonej strefie.</span><span class="sxs-lookup"><span data-stu-id="690a0-108">The **New-AzureRmDnsRecordSet** cmdlet creates a new Domain Name System (DNS) record set with the specified name and type in the specified zone.</span></span>
<span data-ttu-id="690a0-109">Obiekt **Recordset** to zestaw rekordów DNS o tej samej nazwie i typie.</span><span class="sxs-lookup"><span data-stu-id="690a0-109">A **RecordSet** object is a set of DNS records with the same name and type.</span></span>
<span data-ttu-id="690a0-110">Zauważ, że nazwa jest względna względem strefy, a nie w pełni kwalifikowanej nazwy.</span><span class="sxs-lookup"><span data-stu-id="690a0-110">Note that the name is relative to the zone and not the fully qualified name.</span></span>

<span data-ttu-id="690a0-111">Parametr *DnsRecords* określa rekordy w zestawie rekordów.</span><span class="sxs-lookup"><span data-stu-id="690a0-111">The *DnsRecords* parameter specifies the records in the record set.</span></span>
<span data-ttu-id="690a0-112">Ten parametr pobiera tablicę rekordów DNS konstruowaną przy użyciu funkcji New-AzureRmDnsRecordConfig.</span><span class="sxs-lookup"><span data-stu-id="690a0-112">This parameter takes an array of DNS records, constructed using New-AzureRmDnsRecordConfig.</span></span>

<span data-ttu-id="690a0-113">Za pomocą operatora potoku można przekazać obiekt **dnsZone** do tego polecenia cmdlet lub przekazać obiekt **dnsZone** jako parametr *Zone* lub można też określić nazwę strefy według nazwy.</span><span class="sxs-lookup"><span data-stu-id="690a0-113">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone by name.</span></span>

<span data-ttu-id="690a0-114">Za pomocą zmiennej *Confirm* i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="690a0-114">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="690a0-115">Jeśli pasujący **zestaw rekordów** już istnieje (ta sama nazwa i typ rekordu), należy określić parametr *zastępowania* , w przeciwnym razie polecenie cmdlet nie spowoduje utworzenia nowego **zestawu rekordów** .</span><span class="sxs-lookup"><span data-stu-id="690a0-115">If a matching **RecordSet** already exists (same name and record type), you must specify the *Overwrite* parameter, otherwise the cmdlet will not create a new **RecordSet** .</span></span>

## <span data-ttu-id="690a0-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="690a0-116">EXAMPLES</span></span>

### <span data-ttu-id="690a0-117">Przykład 1. Tworzenie zestawu rekordów typu A</span><span class="sxs-lookup"><span data-stu-id="690a0-117">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="690a0-118">W tym przykładzie przedstawiono tworzenie **zestawu rekordów** o nazwie www w strefie MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="690a0-118">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="690a0-119">Zestaw rekordów jest typu A i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="690a0-119">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="690a0-120">Zawiera jeden rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="690a0-120">It contains a single DNS record.</span></span>

### <span data-ttu-id="690a0-121">Przykład 2: Tworzenie zestawu rekordów typu AAAA</span><span class="sxs-lookup"><span data-stu-id="690a0-121">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="690a0-122">W tym przykładzie przedstawiono tworzenie **zestawu rekordów** o nazwie www w strefie MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="690a0-122">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="690a0-123">Zestaw rekordów jest typu AAAA i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="690a0-123">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="690a0-124">Zawiera jeden rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="690a0-124">It contains a single DNS record.</span></span>

<span data-ttu-id="690a0-125">Aby utworzyć **zestaw rekordów** przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="690a0-125">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="690a0-126">Przykład 3: Tworzenie zestawu rekordów typu CNAME</span><span class="sxs-lookup"><span data-stu-id="690a0-126">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="690a0-127">W tym przykładzie przedstawiono tworzenie **zestawu rekordów** o nazwie www w strefie MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="690a0-127">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="690a0-128">Zestaw rekordów jest typu CNAME i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="690a0-128">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="690a0-129">Zawiera jeden rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="690a0-129">It contains a single DNS record.</span></span>

<span data-ttu-id="690a0-130">Aby utworzyć **zestaw rekordów** przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="690a0-130">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="690a0-131">Przykład 4: Tworzenie zestawu rekordów typu MX</span><span class="sxs-lookup"><span data-stu-id="690a0-131">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="690a0-132">To polecenie tworzy **zestaw rekordów** o nazwie www w strefie MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="690a0-132">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="690a0-133">Zestaw rekordów jest typu MX i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="690a0-133">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="690a0-134">Zawiera jeden rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="690a0-134">It contains a single DNS record.</span></span>

<span data-ttu-id="690a0-135">Aby utworzyć **zestaw rekordów** przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="690a0-135">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="690a0-136">Przykład 5: Tworzenie zestawu rekordów typu NS</span><span class="sxs-lookup"><span data-stu-id="690a0-136">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="690a0-137">To polecenie tworzy **zestaw rekordów** o nazwie ns1 w strefie MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="690a0-137">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="690a0-138">Zestaw rekordów jest typu NS i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="690a0-138">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="690a0-139">Zawiera jeden rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="690a0-139">It contains a single DNS record.</span></span>

<span data-ttu-id="690a0-140">Aby utworzyć **zestaw rekordów** przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="690a0-140">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="690a0-141">Przykład 6: Tworzenie zestawu rekordów typu PTR</span><span class="sxs-lookup"><span data-stu-id="690a0-141">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="690a0-142">To polecenie tworzy **zestaw rekordów** o nazwie 4 w strefie 3.2.1.in-addr. arpa.</span><span class="sxs-lookup"><span data-stu-id="690a0-142">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="690a0-143">Zestaw rekordów jest typu PTR i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="690a0-143">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="690a0-144">Zawiera jeden rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="690a0-144">It contains a single DNS record.</span></span>

<span data-ttu-id="690a0-145">Aby utworzyć **zestaw rekordów** przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="690a0-145">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="690a0-146">Przykład 7: Tworzenie zestawu rekordów typu SRV</span><span class="sxs-lookup"><span data-stu-id="690a0-146">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="690a0-147">To polecenie tworzy **zestaw rekordów** o nazwie _sip. _tcp w strefie MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="690a0-147">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="690a0-148">Zestaw rekordów jest typu SRV i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="690a0-148">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="690a0-149">Zawiera jeden rekord DNS wskazujący adres IP 2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="690a0-149">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>

<span data-ttu-id="690a0-150">Usługa (SIP) i protokół (TCP) są określone jako część nazwy zestawu rekordów, a nie jako część danych rekordu.</span><span class="sxs-lookup"><span data-stu-id="690a0-150">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>

<span data-ttu-id="690a0-151">Aby utworzyć **zestaw rekordów** przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="690a0-151">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="690a0-152">Przykład 8: Tworzenie zestawu rekordów typu TXT</span><span class="sxs-lookup"><span data-stu-id="690a0-152">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="690a0-153">To polecenie tworzy **zestaw rekordów** o nazwie tekst w strefie MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="690a0-153">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="690a0-154">Zestaw rekordów jest typu TXT i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="690a0-154">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="690a0-155">Zawiera jeden rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="690a0-155">It contains a single DNS record.</span></span>

<span data-ttu-id="690a0-156">Aby utworzyć **zestaw rekordów** przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="690a0-156">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="690a0-157">Przykład 9: Tworzenie zestawu rekordów w strefie Apex</span><span class="sxs-lookup"><span data-stu-id="690a0-157">Example 9: Create a RecordSet at the zone apex</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="690a0-158">To polecenie tworzy **zestaw rekordów** według wierzchołka (lub głównego) strefy MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="690a0-158">This command creates a **RecordSet** at the apex (or root) of the zone myzone.com.</span></span>
<span data-ttu-id="690a0-159">W tym celu nazwa zestawu rekordów jest określana jako "@" (łącznie z cudzysłowami podwójnymi).</span><span class="sxs-lookup"><span data-stu-id="690a0-159">To do this, the record set name is specified as "@" (including the double-quotes).</span></span>

<span data-ttu-id="690a0-160">Nie można utworzyć rekordów CNAME na wierzchołku strefy.</span><span class="sxs-lookup"><span data-stu-id="690a0-160">You cannot create CNAME records at the apex of a zone.</span></span>
<span data-ttu-id="690a0-161">Jest to ograniczenie standardów DNS. nie jest to ograniczenie dotyczące usługi Azure DNS.</span><span class="sxs-lookup"><span data-stu-id="690a0-161">This is a constraint of the DNS standards; it is not a limitation of Azure DNS.</span></span>

<span data-ttu-id="690a0-162">Aby utworzyć **zestaw rekordów** przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="690a0-162">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="690a0-163">Przykład 10: Tworzenie zestawu rekordów symboli wieloznacznych</span><span class="sxs-lookup"><span data-stu-id="690a0-163">Example 10: Create a wildcard Record Set</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="690a0-164">To polecenie tworzy **zestaw rekordów** o nazwie \* w strefie MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="690a0-164">This command creates a **RecordSet** named \* in the zone myzone.com.</span></span>
<span data-ttu-id="690a0-165">To jest zestaw rekordów z symbolami wieloznacznymi.</span><span class="sxs-lookup"><span data-stu-id="690a0-165">This is a wildcard record set.</span></span>

<span data-ttu-id="690a0-166">Aby utworzyć **zestaw rekordów** przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="690a0-166">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="690a0-167">Przykład 11: Tworzenie pustego zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="690a0-167">Example 11: Create an empty record set</span></span>
```
PS C:\>$RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

<span data-ttu-id="690a0-168">To polecenie tworzy **zestaw rekordów** o nazwie www w strefie MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="690a0-168">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="690a0-169">Zestaw rekordów jest typu A i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="690a0-169">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="690a0-170">To jest pusty zestaw rekordów, który działa jako symbol zastępczy, do którego można później dodawać rekordy.</span><span class="sxs-lookup"><span data-stu-id="690a0-170">This is an empty record set, which acts as a placeholder to which you can later add records.</span></span>

### <span data-ttu-id="690a0-171">Przykład 12: Tworzenie zestawu rekordów i pomijanie wszystkich potwierdzeń</span><span class="sxs-lookup"><span data-stu-id="690a0-171">Example 12: Create a record set and suppress all confirmation</span></span>
```
PS C:\>$RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

<span data-ttu-id="690a0-172">To polecenie tworzy **zestaw rekordów**.</span><span class="sxs-lookup"><span data-stu-id="690a0-172">This command creates a **RecordSet**.</span></span>
<span data-ttu-id="690a0-173">Parametr *overwrite* zapewnia, że ten zestaw rekordów zastępuje dowolny już istniejący zestaw rekordów o tej samej nazwie i typie (istniejące rekordy w tym zestawie rekordów zostaną utracone).</span><span class="sxs-lookup"><span data-stu-id="690a0-173">The *Overwrite* parameter ensures that this record set overwrites any pre-existing record set with the same name and type (existing records in that record set are lost).</span></span>
<span data-ttu-id="690a0-174">Parametr *Confirm* z wartością $false powoduje pominięcie monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="690a0-174">The *Confirm* parameter with a value of $False suppresses the confirmation prompt.</span></span>

## <span data-ttu-id="690a0-175">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="690a0-175">PARAMETERS</span></span>

### <span data-ttu-id="690a0-176">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="690a0-176">-DefaultProfile</span></span>
<span data-ttu-id="690a0-177">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="690a0-177">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="690a0-178">-DnsRecords</span><span class="sxs-lookup"><span data-stu-id="690a0-178">-DnsRecords</span></span>
<span data-ttu-id="690a0-179">Określa tablicę rekordów DNS, które mają zostać uwzględnione w zestawie rekordów.</span><span class="sxs-lookup"><span data-stu-id="690a0-179">Specifies the array of DNS records to include in the record set.</span></span>
<span data-ttu-id="690a0-180">Za pomocą polecenia cmdlet New-AzureRmDnsRecordConfig możesz tworzyć obiekty rekordów DNS.</span><span class="sxs-lookup"><span data-stu-id="690a0-180">You can use the New-AzureRmDnsRecordConfig cmdlet to create DNS record objects.</span></span>
<span data-ttu-id="690a0-181">Zobacz przykłady, aby uzyskać więcej informacji.</span><span class="sxs-lookup"><span data-stu-id="690a0-181">See the examples for more information.</span></span>

```yaml
Type: DnsRecordBase[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="690a0-182">-Force</span><span class="sxs-lookup"><span data-stu-id="690a0-182">-Force</span></span>
<span data-ttu-id="690a0-183">Ten parametr jest przestarzały dla tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="690a0-183">This parameter is deprecated for this cmdlet.</span></span>
<span data-ttu-id="690a0-184">Zostanie on usunięty w przyszłym wydaniu.</span><span class="sxs-lookup"><span data-stu-id="690a0-184">It will be removed in a future release.</span></span>

<span data-ttu-id="690a0-185">Aby określić, czy to polecenie cmdlet monituje o comfirmation, użyj parametru *Confirm* .</span><span class="sxs-lookup"><span data-stu-id="690a0-185">To control whether this cmdlet prompts you for comfirmation, use the *Confirm* parameter.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="690a0-186">-Metadata</span><span class="sxs-lookup"><span data-stu-id="690a0-186">-Metadata</span></span>
<span data-ttu-id="690a0-187">Określa tablicę metadanych, które należy skojarzyć z zestawem rekordów.</span><span class="sxs-lookup"><span data-stu-id="690a0-187">Specifies an array of metadata to associate with the RecordSet.</span></span>
<span data-ttu-id="690a0-188">Metadane są określane za pomocą par nazwa-wartość, które są reprezentowane jako tabele skrótów, na przykład @ (@ {"name" = "Dept"; "Wartość" = "zakupy"}, @ {"nazwa" = "ENV"; "Wartość" = "produkcja"}).</span><span class="sxs-lookup"><span data-stu-id="690a0-188">Metadata is specified using name-value pairs that are represented as hash tables, for example @(@{"Name"="dept"; "Value"="shopping"}, @{"Name"="env"; "Value"="production"}).</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="690a0-189">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="690a0-189">-Name</span></span>
<span data-ttu-id="690a0-190">Określa nazwę **zestawu rekordów** , który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="690a0-190">Specifies the name of the **RecordSet** to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="690a0-191">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="690a0-191">-Overwrite</span></span>
<span data-ttu-id="690a0-192">Wskazuje, że to polecenie cmdlet zastąpi określony **zestaw rekordów** , jeśli już istnieje.</span><span class="sxs-lookup"><span data-stu-id="690a0-192">Indicates that this cmdlet overwrites the specified **RecordSet** if it already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="690a0-193">-Records</span><span class="sxs-lookup"><span data-stu-id="690a0-193">-RecordType</span></span>
<span data-ttu-id="690a0-194">Określa typ rekordu DNS, który ma zostać utworzony.</span><span class="sxs-lookup"><span data-stu-id="690a0-194">Specifies the type of DNS record to create.</span></span>

<span data-ttu-id="690a0-195">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="690a0-195">Valid values are:</span></span>

- <span data-ttu-id="690a0-196">Sieci</span><span class="sxs-lookup"><span data-stu-id="690a0-196">A</span></span>
- <span data-ttu-id="690a0-197">AAAA</span><span class="sxs-lookup"><span data-stu-id="690a0-197">AAAA</span></span>
- <span data-ttu-id="690a0-198">REKORD</span><span class="sxs-lookup"><span data-stu-id="690a0-198">CNAME</span></span>
- <span data-ttu-id="690a0-199">MX</span><span class="sxs-lookup"><span data-stu-id="690a0-199">MX</span></span>
- <span data-ttu-id="690a0-200">REKORDU</span><span class="sxs-lookup"><span data-stu-id="690a0-200">NS</span></span>
- <span data-ttu-id="690a0-201">SYSTEMU</span><span class="sxs-lookup"><span data-stu-id="690a0-201">PTR</span></span>
- <span data-ttu-id="690a0-202">SRV</span><span class="sxs-lookup"><span data-stu-id="690a0-202">SRV</span></span>
- <span data-ttu-id="690a0-203">ROZSZERZENIEM</span><span class="sxs-lookup"><span data-stu-id="690a0-203">TXT</span></span>

<span data-ttu-id="690a0-204">Rekordy SOA są tworzone automatycznie podczas tworzenia strefy i nie można ich tworzyć ręcznie.</span><span class="sxs-lookup"><span data-stu-id="690a0-204">SOA records are created automatically when the zone is created and cannot be created manually.</span></span>

```yaml
Type: RecordType
Parameter Sets: (All)
Aliases: 
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="690a0-205">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="690a0-205">-ResourceGroupName</span></span>
<span data-ttu-id="690a0-206">Określa grupę zasobów zawierającą strefę DNS.</span><span class="sxs-lookup"><span data-stu-id="690a0-206">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="690a0-207">Aby określić nazwę strefy, należy również określić parametr *zonename* .</span><span class="sxs-lookup"><span data-stu-id="690a0-207">You must also specify the *ZoneName* parameter to specify the zone name.</span></span>

<span data-ttu-id="690a0-208">Możesz też określić strefę i grupę zasobów, przechodząc do obiektu strefy DNS przy użyciu parametru *Zone* .</span><span class="sxs-lookup"><span data-stu-id="690a0-208">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="690a0-209">-TTL</span><span class="sxs-lookup"><span data-stu-id="690a0-209">-Ttl</span></span>
<span data-ttu-id="690a0-210">Określa czas wygaśnięcia zestawu rekordów DNS (TTL).</span><span class="sxs-lookup"><span data-stu-id="690a0-210">Specifies the Time to Live (TTL) for the DNS RecordSet.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="690a0-211">-Zone</span><span class="sxs-lookup"><span data-stu-id="690a0-211">-Zone</span></span>
<span data-ttu-id="690a0-212">Określa DnsZone, w którym ma zostać utworzony **zestaw rekordów**.</span><span class="sxs-lookup"><span data-stu-id="690a0-212">Specifies the DnsZone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="690a0-213">Możesz też określić strefę przy użyciu parametrów *zonename* i *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="690a0-213">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="690a0-214">-Nazwa_strefy</span><span class="sxs-lookup"><span data-stu-id="690a0-214">-ZoneName</span></span>
<span data-ttu-id="690a0-215">Określa nazwę strefy, w której ma zostać utworzony **zestaw rekordów**.</span><span class="sxs-lookup"><span data-stu-id="690a0-215">Specifies the name of the zone in which to create the **RecordSet**.</span></span>
<span data-ttu-id="690a0-216">Należy także określić grupę zasobów zawierającą strefę za pomocą parametru *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="690a0-216">You must also specify the resource group containing the zone using the *ResourceGroupName* parameter.</span></span>

<span data-ttu-id="690a0-217">Możesz też określić strefę i grupę zasobów, przechodząc do obiektu strefy DNS przy użyciu parametru *Zone* .</span><span class="sxs-lookup"><span data-stu-id="690a0-217">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="690a0-218">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="690a0-218">-Confirm</span></span>
<span data-ttu-id="690a0-219">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="690a0-219">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="690a0-220">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="690a0-220">-WhatIf</span></span>
<span data-ttu-id="690a0-221">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="690a0-221">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="690a0-222">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="690a0-222">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="690a0-223">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="690a0-223">CommonParameters</span></span>
<span data-ttu-id="690a0-224">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="690a0-224">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="690a0-225">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="690a0-225">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="690a0-226">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="690a0-226">INPUTS</span></span>

### <span data-ttu-id="690a0-227">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="690a0-227">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="690a0-228">Do tego polecenia cmdlet można nawiązać obiekt DnsZone.</span><span class="sxs-lookup"><span data-stu-id="690a0-228">You can pipe a DnsZone object to this cmdlet.</span></span>

## <span data-ttu-id="690a0-229">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="690a0-229">OUTPUTS</span></span>

### <span data-ttu-id="690a0-230">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="690a0-230">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="690a0-231">To polecenie cmdlet zwraca obiekt **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="690a0-231">This cmdlet returns a **RecordSet** object.</span></span>

## <span data-ttu-id="690a0-232">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="690a0-232">NOTES</span></span>
<span data-ttu-id="690a0-233">Za pomocą parametru *Confirm* można kontrolować, czy to polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="690a0-233">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="690a0-234">Domyślnie polecenie cmdlet monituje o potwierdzenie, jeśli zmienna $ConfirmPreference Windows PowerShell ma wartość średnią lub niższą.</span><span class="sxs-lookup"><span data-stu-id="690a0-234">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="690a0-235">Jeśli określisz pozycję *Potwierdź* lub *Potwierdź: $true* , to polecenie cmdlet wyświetli monit o potwierdzenie przed jego uruchomieniem.</span><span class="sxs-lookup"><span data-stu-id="690a0-235">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="690a0-236">Jeśli określisz pozycję *Confirm (Potwierdź): $false* , polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="690a0-236">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="690a0-237">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="690a0-237">RELATED LINKS</span></span>

[<span data-ttu-id="690a0-238">Dodaj-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="690a0-238">Add-AzureRmDnsRecordConfig</span></span>](./Add-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="690a0-239">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="690a0-239">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="690a0-240">Nowe — AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="690a0-240">New-AzureRmDnsRecordConfig</span></span>](./New-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="690a0-241">Remove-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="690a0-241">Remove-AzureRmDnsRecordSet</span></span>](./Remove-AzureRmDnsRecordSet.md)

[<span data-ttu-id="690a0-242">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="690a0-242">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)
