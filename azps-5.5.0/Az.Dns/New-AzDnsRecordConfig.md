---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: AD97BCAF-69BA-4C16-8B57-AB243D796B71
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordConfig.md
ms.openlocfilehash: cd503905cb36d14b0a0537978f02786da7189c33
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200371"
---
# <span data-ttu-id="c36d8-101">New-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="c36d8-101">New-AzDnsRecordConfig</span></span>

## <span data-ttu-id="c36d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c36d8-102">SYNOPSIS</span></span>
<span data-ttu-id="c36d8-103">Tworzy nowy obiekt lokalny rekordu DNS.</span><span class="sxs-lookup"><span data-stu-id="c36d8-103">Creates a new DNS record local object.</span></span>

## <span data-ttu-id="c36d8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c36d8-104">SYNTAX</span></span>

### <span data-ttu-id="c36d8-105">A</span><span class="sxs-lookup"><span data-stu-id="c36d8-105">A</span></span>
```
New-AzDnsRecordConfig -Ipv4Address <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c36d8-106">Aaaa</span><span class="sxs-lookup"><span data-stu-id="c36d8-106">Aaaa</span></span>
```
New-AzDnsRecordConfig -Ipv6Address <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c36d8-107">Ns</span><span class="sxs-lookup"><span data-stu-id="c36d8-107">Ns</span></span>
```
New-AzDnsRecordConfig -Nsdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c36d8-108">Mx</span><span class="sxs-lookup"><span data-stu-id="c36d8-108">Mx</span></span>
```
New-AzDnsRecordConfig -Exchange <String> -Preference <UInt16> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c36d8-109">Ptr</span><span class="sxs-lookup"><span data-stu-id="c36d8-109">Ptr</span></span>
```
New-AzDnsRecordConfig -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c36d8-110">Txt</span><span class="sxs-lookup"><span data-stu-id="c36d8-110">Txt</span></span>
```
New-AzDnsRecordConfig -Value <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c36d8-111">Srv</span><span class="sxs-lookup"><span data-stu-id="c36d8-111">Srv</span></span>
```
New-AzDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c36d8-112">CName</span><span class="sxs-lookup"><span data-stu-id="c36d8-112">CName</span></span>
```
New-AzDnsRecordConfig -Cname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c36d8-113">Caa</span><span class="sxs-lookup"><span data-stu-id="c36d8-113">Caa</span></span>
```
New-AzDnsRecordConfig -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c36d8-114">OPIS</span><span class="sxs-lookup"><span data-stu-id="c36d8-114">DESCRIPTION</span></span>
<span data-ttu-id="c36d8-115">Polecenie **cmdlet New-AzDnsRecordConfig** tworzy lokalny **obiekt DnsRecord.**</span><span class="sxs-lookup"><span data-stu-id="c36d8-115">The **New-AzDnsRecordConfig** cmdlet creates a local **DnsRecord** object.</span></span>
<span data-ttu-id="c36d8-116">Tablica tych obiektów jest przekazywana do polecenia cmdlet New-AzDnsRecordSet za pomocą parametru *DnsRecords* w celu określenia rekordów do utworzenia w zestawie rekordów.</span><span class="sxs-lookup"><span data-stu-id="c36d8-116">An array of these objects is passed to the New-AzDnsRecordSet cmdlet using the *DnsRecords* parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="c36d8-117">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c36d8-117">EXAMPLES</span></span>

### <span data-ttu-id="c36d8-118">Przykład 1. Tworzenie zestawu rekordów typu A</span><span class="sxs-lookup"><span data-stu-id="c36d8-118">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="c36d8-119">W tym przykładzie **jest owany zestaw rekordów** o nazwie www w strefie myzone.com.</span><span class="sxs-lookup"><span data-stu-id="c36d8-119">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="c36d8-120">Zestaw rekordów jest typu A i ma czas wygaśnięcia 1 godziny (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="c36d8-120">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="c36d8-121">Zawiera jeden rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="c36d8-121">It contains a single DNS record.</span></span>

### <span data-ttu-id="c36d8-122">Przykład 2. Tworzenie zestawu rekordów typu AAAA</span><span class="sxs-lookup"><span data-stu-id="c36d8-122">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="c36d8-123">W tym przykładzie **jest owany zestaw rekordów** o nazwie www w strefie myzone.com.</span><span class="sxs-lookup"><span data-stu-id="c36d8-123">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="c36d8-124">Zestaw rekordów jest typu AAAA i ma czas wygaśnięcia 1 godziny (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="c36d8-124">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="c36d8-125">Zawiera jeden rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="c36d8-125">It contains a single DNS record.</span></span>
<span data-ttu-id="c36d8-126">Aby utworzyć zestaw **rekordów tylko** przy użyciu jednego wiersza pn_PowerShell_short lub utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="c36d8-126">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="c36d8-127">Przykład 3. Tworzenie zestawu rekordów typu CNAME</span><span class="sxs-lookup"><span data-stu-id="c36d8-127">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="c36d8-128">W tym przykładzie **jest owany zestaw rekordów** o nazwie www w strefie myzone.com.</span><span class="sxs-lookup"><span data-stu-id="c36d8-128">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="c36d8-129">Zestaw rekordów jest typu CNAME i ma czas wygaśnięcia 1 godziny (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="c36d8-129">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="c36d8-130">Zawiera jeden rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="c36d8-130">It contains a single DNS record.</span></span>
<span data-ttu-id="c36d8-131">Aby utworzyć zestaw **rekordów tylko** przy użyciu jednego wiersza pn_PowerShell_short lub utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="c36d8-131">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="c36d8-132">Przykład 4. Tworzenie zestawu rekordów typu MX</span><span class="sxs-lookup"><span data-stu-id="c36d8-132">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="c36d8-133">To polecenie tworzy zestaw **rekordów o** nazwie www w strefie myzone.com.</span><span class="sxs-lookup"><span data-stu-id="c36d8-133">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="c36d8-134">Zestaw rekordów jest typu MX i ma czas wygaśnięcia 1 godziny (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="c36d8-134">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="c36d8-135">Zawiera jeden rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="c36d8-135">It contains a single DNS record.</span></span>
<span data-ttu-id="c36d8-136">Aby utworzyć zestaw **rekordów tylko** przy użyciu jednego wiersza pn_PowerShell_short lub utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="c36d8-136">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="c36d8-137">Przykład 5. Tworzenie zestawu rekordów typu NS</span><span class="sxs-lookup"><span data-stu-id="c36d8-137">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="c36d8-138">To polecenie tworzy **zestaw** rekordów o nazwie ns1 w strefie myzone.com.</span><span class="sxs-lookup"><span data-stu-id="c36d8-138">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="c36d8-139">Zestaw rekordów jest typu NS i ma czas wygaśnięcia 1 godziny (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="c36d8-139">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="c36d8-140">Zawiera jeden rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="c36d8-140">It contains a single DNS record.</span></span>
<span data-ttu-id="c36d8-141">Aby utworzyć zestaw **rekordów tylko** przy użyciu jednego wiersza pn_PowerShell_short lub utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="c36d8-141">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="c36d8-142">Przykład 6. Tworzenie zestawu rekordów typu PTR</span><span class="sxs-lookup"><span data-stu-id="c36d8-142">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="c36d8-143">To polecenie tworzy zestaw **rekordów o** nazwie 4 w strefie 3.2.1.in-addr.arpa.</span><span class="sxs-lookup"><span data-stu-id="c36d8-143">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="c36d8-144">Zestaw rekordów jest typu PTR i ma czas wygaśnięcia 1 godziny (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="c36d8-144">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="c36d8-145">Zawiera jeden rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="c36d8-145">It contains a single DNS record.</span></span>
<span data-ttu-id="c36d8-146">Aby utworzyć zestaw **rekordów tylko** przy użyciu jednego wiersza pn_PowerShell_short lub utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="c36d8-146">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="c36d8-147">Przykład 7. Tworzenie zestawu rekordów typu SRV</span><span class="sxs-lookup"><span data-stu-id="c36d8-147">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="c36d8-148">To polecenie tworzy **zestaw** rekordów o nazwie _sip._tcp w strefie myzone.com.</span><span class="sxs-lookup"><span data-stu-id="c36d8-148">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="c36d8-149">Zestaw rekordów jest typu SRV i ma czas wygaśnięcia 1 godziny (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="c36d8-149">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="c36d8-150">Zawiera ona jeden rekord DNS, który wskaże adres IP 2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="c36d8-150">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>
<span data-ttu-id="c36d8-151">Usługa (sip) i protokół (tcp) są określone jako część nazwy zestawu rekordów, a nie jako część danych rekordu.</span><span class="sxs-lookup"><span data-stu-id="c36d8-151">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>
<span data-ttu-id="c36d8-152">Aby utworzyć zestaw **rekordów tylko** przy użyciu jednego wiersza pn_PowerShell_short lub utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="c36d8-152">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="c36d8-153">Przykład 8. Tworzenie zestawu rekordów typu TXT</span><span class="sxs-lookup"><span data-stu-id="c36d8-153">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="c36d8-154">To polecenie tworzy **nazwany tekst zestawu** rekordów w strefie myzone.com.</span><span class="sxs-lookup"><span data-stu-id="c36d8-154">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="c36d8-155">Zestaw rekordów jest typu TXT i ma czas wygaśnięcia 1 godziny (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="c36d8-155">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="c36d8-156">Zawiera jeden rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="c36d8-156">It contains a single DNS record.</span></span>
<span data-ttu-id="c36d8-157">Aby utworzyć zestaw **rekordów tylko** przy użyciu jednego wiersza pn_PowerShell_short lub utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="c36d8-157">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="c36d8-158">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c36d8-158">PARAMETERS</span></span>

### <span data-ttu-id="c36d8-159">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="c36d8-159">-CaaFlags</span></span>
<span data-ttu-id="c36d8-160">Flagi dla rekordu CAA do dodania.</span><span class="sxs-lookup"><span data-stu-id="c36d8-160">The flags for the CAA record to add.</span></span> <span data-ttu-id="c36d8-161">Musi to być liczba z wartości od 0 do 255.</span><span class="sxs-lookup"><span data-stu-id="c36d8-161">Must be a number between 0 and 255.</span></span>

```yaml
Type: System.Byte
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c36d8-162">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="c36d8-162">-CaaTag</span></span>
<span data-ttu-id="c36d8-163">Pole tagu rekordu CAA do dodania.</span><span class="sxs-lookup"><span data-stu-id="c36d8-163">The tag field of the CAA record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c36d8-164">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="c36d8-164">-CaaValue</span></span>
<span data-ttu-id="c36d8-165">Pole wartości rekordu CAA do dodania.</span><span class="sxs-lookup"><span data-stu-id="c36d8-165">The value field for the CAA record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c36d8-166">- Cname</span><span class="sxs-lookup"><span data-stu-id="c36d8-166">-Cname</span></span>
<span data-ttu-id="c36d8-167">Określa nazwę domeny dla rekordu nazwa kanoniczna (CNAME).</span><span class="sxs-lookup"><span data-stu-id="c36d8-167">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: System.String
Parameter Sets: CName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c36d8-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c36d8-168">-DefaultProfile</span></span>
<span data-ttu-id="c36d8-169">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="c36d8-169">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c36d8-170">— Exchange</span><span class="sxs-lookup"><span data-stu-id="c36d8-170">-Exchange</span></span>
<span data-ttu-id="c36d8-171">Określa nazwę serwera wymiany poczty dla rekordu wymiany poczty (MX).</span><span class="sxs-lookup"><span data-stu-id="c36d8-171">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: System.String
Parameter Sets: Mx
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c36d8-172">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="c36d8-172">-Ipv4Address</span></span>
<span data-ttu-id="c36d8-173">Określa adres IPv4 rekordu A.</span><span class="sxs-lookup"><span data-stu-id="c36d8-173">Specifies an IPv4 address for an A record.</span></span>

```yaml
Type: System.String
Parameter Sets: A
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c36d8-174">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="c36d8-174">-Ipv6Address</span></span>
<span data-ttu-id="c36d8-175">Określa adres IPv6 rekordu AAAA.</span><span class="sxs-lookup"><span data-stu-id="c36d8-175">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: System.String
Parameter Sets: Aaaa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c36d8-176">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="c36d8-176">-Nsdname</span></span>
<span data-ttu-id="c36d8-177">Określa nazwę serwera nazw dla rekordu serwera nazw.</span><span class="sxs-lookup"><span data-stu-id="c36d8-177">Specifies the name server name for a name server (NS) record.</span></span>

```yaml
Type: System.String
Parameter Sets: Ns
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c36d8-178">— Port</span><span class="sxs-lookup"><span data-stu-id="c36d8-178">-Port</span></span>
<span data-ttu-id="c36d8-179">Określa port rekordu usługi (SRV).</span><span class="sxs-lookup"><span data-stu-id="c36d8-179">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c36d8-180">—Preference (Preferencja)</span><span class="sxs-lookup"><span data-stu-id="c36d8-180">-Preference</span></span>
<span data-ttu-id="c36d8-181">Określa preferencje rekordu MX.</span><span class="sxs-lookup"><span data-stu-id="c36d8-181">Specifies the preference for an MX record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Mx
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c36d8-182">— Priority (Priorytet)</span><span class="sxs-lookup"><span data-stu-id="c36d8-182">-Priority</span></span>
<span data-ttu-id="c36d8-183">Określa priorytet rekordu SRV.</span><span class="sxs-lookup"><span data-stu-id="c36d8-183">Specifies the priority for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c36d8-184">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="c36d8-184">-Ptrdname</span></span>
<span data-ttu-id="c36d8-185">Określa nazwę domeny docelowej rekordu zasobu wskaźnika (PTR).</span><span class="sxs-lookup"><span data-stu-id="c36d8-185">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

```yaml
Type: System.String
Parameter Sets: Ptr
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c36d8-186">— element docelowy</span><span class="sxs-lookup"><span data-stu-id="c36d8-186">-Target</span></span>
<span data-ttu-id="c36d8-187">Określa wartość docelową rekordu SRV.</span><span class="sxs-lookup"><span data-stu-id="c36d8-187">Specifies the target for an SRV record.</span></span>

```yaml
Type: System.String
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c36d8-188">— Wartość</span><span class="sxs-lookup"><span data-stu-id="c36d8-188">-Value</span></span>
<span data-ttu-id="c36d8-189">Określa wartość rekordu TXT.</span><span class="sxs-lookup"><span data-stu-id="c36d8-189">Specifies the value for a TXT record.</span></span>

```yaml
Type: System.String
Parameter Sets: Txt
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c36d8-190">— Waga</span><span class="sxs-lookup"><span data-stu-id="c36d8-190">-Weight</span></span>
<span data-ttu-id="c36d8-191">Określa wagę rekordu SRV.</span><span class="sxs-lookup"><span data-stu-id="c36d8-191">Specifies the weight for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c36d8-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c36d8-192">CommonParameters</span></span>
<span data-ttu-id="c36d8-193">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c36d8-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c36d8-194">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c36d8-194">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c36d8-195">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c36d8-195">INPUTS</span></span>

### <span data-ttu-id="c36d8-196">System.String</span><span class="sxs-lookup"><span data-stu-id="c36d8-196">System.String</span></span>

### <span data-ttu-id="c36d8-197">System.UInt16</span><span class="sxs-lookup"><span data-stu-id="c36d8-197">System.UInt16</span></span>

### <span data-ttu-id="c36d8-198">System.Byte</span><span class="sxs-lookup"><span data-stu-id="c36d8-198">System.Byte</span></span>

## <span data-ttu-id="c36d8-199">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c36d8-199">OUTPUTS</span></span>

### <span data-ttu-id="c36d8-200">Microsoft.Azure.Commands.Dns.DnsRecordBase</span><span class="sxs-lookup"><span data-stu-id="c36d8-200">Microsoft.Azure.Commands.Dns.DnsRecordBase</span></span>

## <span data-ttu-id="c36d8-201">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c36d8-201">NOTES</span></span>

## <span data-ttu-id="c36d8-202">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c36d8-202">RELATED LINKS</span></span>

[<span data-ttu-id="c36d8-203">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="c36d8-203">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="c36d8-204">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c36d8-204">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="c36d8-205">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="c36d8-205">Remove-AzDnsRecordConfig</span></span>](./Remove-AzDnsRecordConfig.md)
