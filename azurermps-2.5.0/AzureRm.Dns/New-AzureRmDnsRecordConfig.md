---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: AD97BCAF-69BA-4C16-8B57-AB243D796B71
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6368cffa168772a384deb99f5a8388aef84f85b2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898925"
---
# <span data-ttu-id="edbaa-101">New-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="edbaa-101">New-AzureRmDnsRecordConfig</span></span>

## <span data-ttu-id="edbaa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="edbaa-102">SYNOPSIS</span></span>
<span data-ttu-id="edbaa-103">Tworzy nowy obiekt lokalny rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="edbaa-103">Creates a new DNS record local object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="edbaa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="edbaa-104">SYNTAX</span></span>

### <span data-ttu-id="edbaa-105">Sieci</span><span class="sxs-lookup"><span data-stu-id="edbaa-105">A</span></span>
```
New-AzureRmDnsRecordConfig -Ipv4Address <String> [<CommonParameters>]
```

### <span data-ttu-id="edbaa-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="edbaa-106">Aaaa</span></span>
```
New-AzureRmDnsRecordConfig -Ipv6Address <String> [<CommonParameters>]
```

### <span data-ttu-id="edbaa-107">Rekordu</span><span class="sxs-lookup"><span data-stu-id="edbaa-107">Ns</span></span>
```
New-AzureRmDnsRecordConfig -Nsdname <String> [<CommonParameters>]
```

### <span data-ttu-id="edbaa-108">MX</span><span class="sxs-lookup"><span data-stu-id="edbaa-108">Mx</span></span>
```
New-AzureRmDnsRecordConfig -Exchange <String> -Preference <UInt16> [<CommonParameters>]
```

### <span data-ttu-id="edbaa-109">Systemu</span><span class="sxs-lookup"><span data-stu-id="edbaa-109">Ptr</span></span>
```
New-AzureRmDnsRecordConfig -Ptrdname <String> [<CommonParameters>]
```

### <span data-ttu-id="edbaa-110">Rozszerzeniem</span><span class="sxs-lookup"><span data-stu-id="edbaa-110">Txt</span></span>
```
New-AzureRmDnsRecordConfig -Value <String> [<CommonParameters>]
```

### <span data-ttu-id="edbaa-111">SRV</span><span class="sxs-lookup"><span data-stu-id="edbaa-111">Srv</span></span>
```
New-AzureRmDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [<CommonParameters>]
```

### <span data-ttu-id="edbaa-112">Rekord</span><span class="sxs-lookup"><span data-stu-id="edbaa-112">CName</span></span>
```
New-AzureRmDnsRecordConfig -Cname <String> [<CommonParameters>]
```

## <span data-ttu-id="edbaa-113">Opis</span><span class="sxs-lookup"><span data-stu-id="edbaa-113">DESCRIPTION</span></span>
<span data-ttu-id="edbaa-114">Polecenie cmdlet **New-AzureRmDnsRecordConfig** tworzy lokalny obiekt **DnsRecord** .</span><span class="sxs-lookup"><span data-stu-id="edbaa-114">The **New-AzureRmDnsRecordConfig** cmdlet creates a local **DnsRecord** object.</span></span>
<span data-ttu-id="edbaa-115">Tablica tych obiektów jest przekazywana do polecenia cmdlet New-AzureRmDnsRecordSet za pomocą parametru *DnsRecords* w celu określenia rekordów, które mają zostać utworzone w zestawie rekordów.</span><span class="sxs-lookup"><span data-stu-id="edbaa-115">An array of these objects is passed to the New-AzureRmDnsRecordSet cmdlet using the *DnsRecords* parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="edbaa-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="edbaa-116">EXAMPLES</span></span>

### <span data-ttu-id="edbaa-117">Przykład 1. Tworzenie zestawu rekordów typu A</span><span class="sxs-lookup"><span data-stu-id="edbaa-117">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="edbaa-118">W tym przykładzie przedstawiono tworzenie **zestawu rekordów** o nazwie www w strefie MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="edbaa-118">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="edbaa-119">Zestaw rekordów jest typu A i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="edbaa-119">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="edbaa-120">Zawiera jeden rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="edbaa-120">It contains a single DNS record.</span></span>

### <span data-ttu-id="edbaa-121">Przykład 2: Tworzenie zestawu rekordów typu AAAA</span><span class="sxs-lookup"><span data-stu-id="edbaa-121">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="edbaa-122">W tym przykładzie przedstawiono tworzenie **zestawu rekordów** o nazwie www w strefie MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="edbaa-122">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="edbaa-123">Zestaw rekordów jest typu AAAA i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="edbaa-123">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="edbaa-124">Zawiera jeden rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="edbaa-124">It contains a single DNS record.</span></span>

<span data-ttu-id="edbaa-125">Aby utworzyć **zestaw rekordów** przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="edbaa-125">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="edbaa-126">Przykład 3: Tworzenie zestawu rekordów typu CNAME</span><span class="sxs-lookup"><span data-stu-id="edbaa-126">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="edbaa-127">W tym przykładzie przedstawiono tworzenie **zestawu rekordów** o nazwie www w strefie MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="edbaa-127">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="edbaa-128">Zestaw rekordów jest typu CNAME i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="edbaa-128">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="edbaa-129">Zawiera jeden rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="edbaa-129">It contains a single DNS record.</span></span>

<span data-ttu-id="edbaa-130">Aby utworzyć **zestaw rekordów** przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="edbaa-130">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="edbaa-131">Przykład 4: Tworzenie zestawu rekordów typu MX</span><span class="sxs-lookup"><span data-stu-id="edbaa-131">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="edbaa-132">To polecenie tworzy **zestaw rekordów** o nazwie www w strefie MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="edbaa-132">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="edbaa-133">Zestaw rekordów jest typu MX i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="edbaa-133">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="edbaa-134">Zawiera jeden rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="edbaa-134">It contains a single DNS record.</span></span>

<span data-ttu-id="edbaa-135">Aby utworzyć **zestaw rekordów** przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="edbaa-135">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="edbaa-136">Przykład 5: Tworzenie zestawu rekordów typu NS</span><span class="sxs-lookup"><span data-stu-id="edbaa-136">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="edbaa-137">To polecenie tworzy **zestaw rekordów** o nazwie ns1 w strefie MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="edbaa-137">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="edbaa-138">Zestaw rekordów jest typu NS i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="edbaa-138">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="edbaa-139">Zawiera jeden rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="edbaa-139">It contains a single DNS record.</span></span>

<span data-ttu-id="edbaa-140">Aby utworzyć **zestaw rekordów** przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="edbaa-140">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="edbaa-141">Przykład 6: Tworzenie zestawu rekordów typu PTR</span><span class="sxs-lookup"><span data-stu-id="edbaa-141">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="edbaa-142">To polecenie tworzy **zestaw rekordów** o nazwie 4 w strefie 3.2.1.in-addr. arpa.</span><span class="sxs-lookup"><span data-stu-id="edbaa-142">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="edbaa-143">Zestaw rekordów jest typu PTR i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="edbaa-143">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="edbaa-144">Zawiera jeden rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="edbaa-144">It contains a single DNS record.</span></span>

<span data-ttu-id="edbaa-145">Aby utworzyć **zestaw rekordów** przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="edbaa-145">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="edbaa-146">Przykład 7: Tworzenie zestawu rekordów typu SRV</span><span class="sxs-lookup"><span data-stu-id="edbaa-146">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="edbaa-147">To polecenie tworzy **zestaw rekordów** o nazwie _sip. _tcp w strefie MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="edbaa-147">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="edbaa-148">Zestaw rekordów jest typu SRV i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="edbaa-148">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="edbaa-149">Zawiera jeden rekord DNS wskazujący adres IP 2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="edbaa-149">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>

<span data-ttu-id="edbaa-150">Usługa (SIP) i protokół (TCP) są określone jako część nazwy zestawu rekordów, a nie jako część danych rekordu.</span><span class="sxs-lookup"><span data-stu-id="edbaa-150">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>

<span data-ttu-id="edbaa-151">Aby utworzyć **zestaw rekordów** przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="edbaa-151">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="edbaa-152">Przykład 8: Tworzenie zestawu rekordów typu TXT</span><span class="sxs-lookup"><span data-stu-id="edbaa-152">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="edbaa-153">To polecenie tworzy **zestaw rekordów** o nazwie tekst w strefie MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="edbaa-153">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="edbaa-154">Zestaw rekordów jest typu TXT i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="edbaa-154">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="edbaa-155">Zawiera jeden rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="edbaa-155">It contains a single DNS record.</span></span>

<span data-ttu-id="edbaa-156">Aby utworzyć **zestaw rekordów** przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="edbaa-156">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="edbaa-157">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="edbaa-157">PARAMETERS</span></span>

### <span data-ttu-id="edbaa-158">-CNAME</span><span class="sxs-lookup"><span data-stu-id="edbaa-158">-Cname</span></span>
<span data-ttu-id="edbaa-159">Określa nazwę domeny dla rekordu kanonicznego (CNAME).</span><span class="sxs-lookup"><span data-stu-id="edbaa-159">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: String
Parameter Sets: CName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edbaa-160">-Exchange</span><span class="sxs-lookup"><span data-stu-id="edbaa-160">-Exchange</span></span>
<span data-ttu-id="edbaa-161">Określa nazwę serwera Exchange mail dla rekordu wymiany poczty (MX).</span><span class="sxs-lookup"><span data-stu-id="edbaa-161">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: String
Parameter Sets: Mx
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edbaa-162">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="edbaa-162">-Ipv4Address</span></span>
<span data-ttu-id="edbaa-163">Określa adres IPv4 rekordu A.</span><span class="sxs-lookup"><span data-stu-id="edbaa-163">Specifies an IPv4 address for an A record.</span></span>

```yaml
Type: String
Parameter Sets: A
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edbaa-164">-Adres_ipv6</span><span class="sxs-lookup"><span data-stu-id="edbaa-164">-Ipv6Address</span></span>
<span data-ttu-id="edbaa-165">Określa adres IPv6 rekordu AAAA.</span><span class="sxs-lookup"><span data-stu-id="edbaa-165">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: String
Parameter Sets: Aaaa
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edbaa-166">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="edbaa-166">-Nsdname</span></span>
<span data-ttu-id="edbaa-167">Określa nazwę serwera nazw dla rekordu serwera nazw (NS).</span><span class="sxs-lookup"><span data-stu-id="edbaa-167">Specifies the name server name for a name server (NS) record.</span></span>

```yaml
Type: String
Parameter Sets: Ns
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edbaa-168">-Port</span><span class="sxs-lookup"><span data-stu-id="edbaa-168">-Port</span></span>
<span data-ttu-id="edbaa-169">Określa port dla rekordu usługi (SRV).</span><span class="sxs-lookup"><span data-stu-id="edbaa-169">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: UInt16
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edbaa-170">-Preferencja</span><span class="sxs-lookup"><span data-stu-id="edbaa-170">-Preference</span></span>
<span data-ttu-id="edbaa-171">Określa preferencję dla rekordu MX.</span><span class="sxs-lookup"><span data-stu-id="edbaa-171">Specifies the preference for an MX record.</span></span>

```yaml
Type: UInt16
Parameter Sets: Mx
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edbaa-172">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="edbaa-172">-Priority</span></span>
<span data-ttu-id="edbaa-173">Określa priorytet rekordu SRV.</span><span class="sxs-lookup"><span data-stu-id="edbaa-173">Specifies the priority for an SRV record.</span></span>

```yaml
Type: UInt16
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edbaa-174">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="edbaa-174">-Ptrdname</span></span>
<span data-ttu-id="edbaa-175">Określa nazwę domeny docelowej rekordu zasobu wskaźnika (PTR).</span><span class="sxs-lookup"><span data-stu-id="edbaa-175">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

```yaml
Type: String
Parameter Sets: Ptr
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edbaa-176">-Target</span><span class="sxs-lookup"><span data-stu-id="edbaa-176">-Target</span></span>
<span data-ttu-id="edbaa-177">Określa cel dla rekordu SRV.</span><span class="sxs-lookup"><span data-stu-id="edbaa-177">Specifies the target for an SRV record.</span></span>

```yaml
Type: String
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edbaa-178">-Value</span><span class="sxs-lookup"><span data-stu-id="edbaa-178">-Value</span></span>
<span data-ttu-id="edbaa-179">Określa wartość rekordu TXT.</span><span class="sxs-lookup"><span data-stu-id="edbaa-179">Specifies the value for a TXT record.</span></span>

```yaml
Type: String
Parameter Sets: Txt
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edbaa-180">-Waga</span><span class="sxs-lookup"><span data-stu-id="edbaa-180">-Weight</span></span>
<span data-ttu-id="edbaa-181">Określa wagę rekordu SRV.</span><span class="sxs-lookup"><span data-stu-id="edbaa-181">Specifies the weight for an SRV record.</span></span>

```yaml
Type: UInt16
Parameter Sets: Srv
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edbaa-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edbaa-182">CommonParameters</span></span>
<span data-ttu-id="edbaa-183">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edbaa-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edbaa-184">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edbaa-184">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edbaa-185">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="edbaa-185">INPUTS</span></span>

### <span data-ttu-id="edbaa-186">Znaleziono.</span><span class="sxs-lookup"><span data-stu-id="edbaa-186">None.</span></span>

## <span data-ttu-id="edbaa-187">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="edbaa-187">OUTPUTS</span></span>

### <span data-ttu-id="edbaa-188">Microsoft. Azure. Commands. DNS. DnsRecordBase</span><span class="sxs-lookup"><span data-stu-id="edbaa-188">Microsoft.Azure.Commands.Dns.DnsRecordBase</span></span>

## <span data-ttu-id="edbaa-189">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="edbaa-189">NOTES</span></span>

## <span data-ttu-id="edbaa-190">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="edbaa-190">RELATED LINKS</span></span>

[<span data-ttu-id="edbaa-191">Dodaj-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="edbaa-191">Add-AzureRmDnsRecordConfig</span></span>](./Add-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="edbaa-192">Nowe — AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="edbaa-192">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="edbaa-193">Remove-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="edbaa-193">Remove-AzureRmDnsRecordConfig</span></span>](./Remove-AzureRmDnsRecordConfig.md)
