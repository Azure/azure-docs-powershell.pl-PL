---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: AD97BCAF-69BA-4C16-8B57-AB243D796B71
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/new-azurermdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsRecordConfig.md
ms.openlocfilehash: f44472ac83c1d92baab5d4c7c3b4c8d325e3dfbe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549767"
---
# <span data-ttu-id="30484-101">New-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="30484-101">New-AzureRmDnsRecordConfig</span></span>

## <span data-ttu-id="30484-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="30484-102">SYNOPSIS</span></span>
<span data-ttu-id="30484-103">Tworzy nowy obiekt lokalny rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="30484-103">Creates a new DNS record local object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30484-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="30484-104">SYNTAX</span></span>

### <span data-ttu-id="30484-105">Sieci</span><span class="sxs-lookup"><span data-stu-id="30484-105">A</span></span>
```
New-AzureRmDnsRecordConfig -Ipv4Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="30484-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="30484-106">Aaaa</span></span>
```
New-AzureRmDnsRecordConfig -Ipv6Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="30484-107">Rekordu</span><span class="sxs-lookup"><span data-stu-id="30484-107">Ns</span></span>
```
New-AzureRmDnsRecordConfig -Nsdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30484-108">MX</span><span class="sxs-lookup"><span data-stu-id="30484-108">Mx</span></span>
```
New-AzureRmDnsRecordConfig -Exchange <String> -Preference <UInt16> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="30484-109">Systemu</span><span class="sxs-lookup"><span data-stu-id="30484-109">Ptr</span></span>
```
New-AzureRmDnsRecordConfig -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30484-110">Rozszerzeniem</span><span class="sxs-lookup"><span data-stu-id="30484-110">Txt</span></span>
```
New-AzureRmDnsRecordConfig -Value <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30484-111">SRV</span><span class="sxs-lookup"><span data-stu-id="30484-111">Srv</span></span>
```
New-AzureRmDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30484-112">Rekord</span><span class="sxs-lookup"><span data-stu-id="30484-112">CName</span></span>
```
New-AzureRmDnsRecordConfig -Cname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30484-113">Caa</span><span class="sxs-lookup"><span data-stu-id="30484-113">Caa</span></span>
```
New-AzureRmDnsRecordConfig -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30484-114">Opis</span><span class="sxs-lookup"><span data-stu-id="30484-114">DESCRIPTION</span></span>
<span data-ttu-id="30484-115">Polecenie cmdlet **New-AzureRmDnsRecordConfig** tworzy lokalny obiekt **DnsRecord** .</span><span class="sxs-lookup"><span data-stu-id="30484-115">The **New-AzureRmDnsRecordConfig** cmdlet creates a local **DnsRecord** object.</span></span>
<span data-ttu-id="30484-116">Tablica tych obiektów jest przekazywana do polecenia cmdlet New-AzureRmDnsRecordSet za pomocą parametru *DnsRecords* w celu określenia rekordów, które mają zostać utworzone w zestawie rekordów.</span><span class="sxs-lookup"><span data-stu-id="30484-116">An array of these objects is passed to the New-AzureRmDnsRecordSet cmdlet using the *DnsRecords* parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="30484-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="30484-117">EXAMPLES</span></span>

### <span data-ttu-id="30484-118">Przykład 1. Tworzenie zestawu rekordów typu A</span><span class="sxs-lookup"><span data-stu-id="30484-118">Example 1: Create a RecordSet of type A</span></span>
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

<span data-ttu-id="30484-119">W tym przykładzie przedstawiono tworzenie **zestawu rekordów** o nazwie www w strefie MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="30484-119">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="30484-120">Zestaw rekordów jest typu A i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="30484-120">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="30484-121">Zawiera jeden rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="30484-121">It contains a single DNS record.</span></span>

### <span data-ttu-id="30484-122">Przykład 2: Tworzenie zestawu rekordów typu AAAA</span><span class="sxs-lookup"><span data-stu-id="30484-122">Example 2: Create a RecordSet of type AAAA</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="30484-123">W tym przykładzie przedstawiono tworzenie **zestawu rekordów** o nazwie www w strefie MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="30484-123">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="30484-124">Zestaw rekordów jest typu AAAA i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="30484-124">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="30484-125">Zawiera jeden rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="30484-125">It contains a single DNS record.</span></span>

<span data-ttu-id="30484-126">Aby utworzyć **zestaw rekordów** przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="30484-126">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="30484-127">Przykład 3: Tworzenie zestawu rekordów typu CNAME</span><span class="sxs-lookup"><span data-stu-id="30484-127">Example 3: Create a RecordSet of type CNAME</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="30484-128">W tym przykładzie przedstawiono tworzenie **zestawu rekordów** o nazwie www w strefie MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="30484-128">This example creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="30484-129">Zestaw rekordów jest typu CNAME i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="30484-129">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="30484-130">Zawiera jeden rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="30484-130">It contains a single DNS record.</span></span>

<span data-ttu-id="30484-131">Aby utworzyć **zestaw rekordów** przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="30484-131">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="30484-132">Przykład 4: Tworzenie zestawu rekordów typu MX</span><span class="sxs-lookup"><span data-stu-id="30484-132">Example 4: Create a RecordSet of type MX</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="30484-133">To polecenie tworzy **zestaw rekordów** o nazwie www w strefie MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="30484-133">This command creates a **RecordSet** named www in the zone myzone.com.</span></span>
<span data-ttu-id="30484-134">Zestaw rekordów jest typu MX i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="30484-134">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="30484-135">Zawiera jeden rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="30484-135">It contains a single DNS record.</span></span>

<span data-ttu-id="30484-136">Aby utworzyć **zestaw rekordów** przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="30484-136">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="30484-137">Przykład 5: Tworzenie zestawu rekordów typu NS</span><span class="sxs-lookup"><span data-stu-id="30484-137">Example 5: Create a RecordSet of type NS</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="30484-138">To polecenie tworzy **zestaw rekordów** o nazwie ns1 w strefie MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="30484-138">This command creates a **RecordSet** named ns1 in the zone myzone.com.</span></span>
<span data-ttu-id="30484-139">Zestaw rekordów jest typu NS i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="30484-139">The record set is of type NS and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="30484-140">Zawiera jeden rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="30484-140">It contains a single DNS record.</span></span>

<span data-ttu-id="30484-141">Aby utworzyć **zestaw rekordów** przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="30484-141">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="30484-142">Przykład 6: Tworzenie zestawu rekordów typu PTR</span><span class="sxs-lookup"><span data-stu-id="30484-142">Example 6: Create a RecordSet of type PTR</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

<span data-ttu-id="30484-143">To polecenie tworzy **zestaw rekordów** o nazwie 4 w strefie 3.2.1.in-addr. arpa.</span><span class="sxs-lookup"><span data-stu-id="30484-143">This command creates a **RecordSet** named 4 in the zone 3.2.1.in-addr.arpa.</span></span>
<span data-ttu-id="30484-144">Zestaw rekordów jest typu PTR i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="30484-144">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="30484-145">Zawiera jeden rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="30484-145">It contains a single DNS record.</span></span>

<span data-ttu-id="30484-146">Aby utworzyć **zestaw rekordów** przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="30484-146">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="30484-147">Przykład 7: Tworzenie zestawu rekordów typu SRV</span><span class="sxs-lookup"><span data-stu-id="30484-147">Example 7: Create a RecordSet of type SRV</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="30484-148">To polecenie tworzy **zestaw rekordów** o nazwie _sip. _tcp w strefie MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="30484-148">This command creates a **RecordSet** named _sip._tcp in the zone myzone.com.</span></span>
<span data-ttu-id="30484-149">Zestaw rekordów jest typu SRV i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="30484-149">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="30484-150">Zawiera jeden rekord DNS wskazujący adres IP 2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="30484-150">It contains a single DNS record, pointing to the IP address 2001.2.3.4.</span></span>

<span data-ttu-id="30484-151">Usługa (SIP) i protokół (TCP) są określone jako część nazwy zestawu rekordów, a nie jako część danych rekordu.</span><span class="sxs-lookup"><span data-stu-id="30484-151">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span>

<span data-ttu-id="30484-152">Aby utworzyć **zestaw rekordów** przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="30484-152">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="30484-153">Przykład 8: Tworzenie zestawu rekordów typu TXT</span><span class="sxs-lookup"><span data-stu-id="30484-153">Example 8: Create a RecordSet of type TXT</span></span>
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

<span data-ttu-id="30484-154">To polecenie tworzy **zestaw rekordów** o nazwie tekst w strefie MyZone.com.</span><span class="sxs-lookup"><span data-stu-id="30484-154">This command creates a **RecordSet** named text in the zone myzone.com.</span></span>
<span data-ttu-id="30484-155">Zestaw rekordów jest typu TXT i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="30484-155">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span>
<span data-ttu-id="30484-156">Zawiera jeden rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="30484-156">It contains a single DNS record.</span></span>

<span data-ttu-id="30484-157">Aby utworzyć **zestaw rekordów** przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="30484-157">To create a **RecordSet** using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="30484-158">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="30484-158">PARAMETERS</span></span>

### <span data-ttu-id="30484-159">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="30484-159">-CaaFlags</span></span>
<span data-ttu-id="30484-160">Flagi rekordu CAA, które mają zostać dodane.</span><span class="sxs-lookup"><span data-stu-id="30484-160">The flags for the CAA record to add.</span></span> <span data-ttu-id="30484-161">Musi być liczbą z przedziału od 0 do 255.</span><span class="sxs-lookup"><span data-stu-id="30484-161">Must be a number between 0 and 255.</span></span>

```yaml
Type: Byte
Parameter Sets: Caa
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30484-162">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="30484-162">-CaaTag</span></span>
<span data-ttu-id="30484-163">Pole tag w rekordzie CAA, które ma zostać dodane.</span><span class="sxs-lookup"><span data-stu-id="30484-163">The tag field of the CAA record to add.</span></span>

```yaml
Type: String
Parameter Sets: Caa
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30484-164">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="30484-164">-CaaValue</span></span>
<span data-ttu-id="30484-165">Pole wartości dla rekordu CAA, który ma zostać dodany.</span><span class="sxs-lookup"><span data-stu-id="30484-165">The value field for the CAA record to add.</span></span>

```yaml
Type: String
Parameter Sets: Caa
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30484-166">-CNAME</span><span class="sxs-lookup"><span data-stu-id="30484-166">-Cname</span></span>
<span data-ttu-id="30484-167">Określa nazwę domeny dla rekordu kanonicznego (CNAME).</span><span class="sxs-lookup"><span data-stu-id="30484-167">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="30484-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30484-168">-DefaultProfile</span></span>
<span data-ttu-id="30484-169">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="30484-169">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30484-170">-Exchange</span><span class="sxs-lookup"><span data-stu-id="30484-170">-Exchange</span></span>
<span data-ttu-id="30484-171">Określa nazwę serwera Exchange mail dla rekordu wymiany poczty (MX).</span><span class="sxs-lookup"><span data-stu-id="30484-171">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="30484-172">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="30484-172">-Ipv4Address</span></span>
<span data-ttu-id="30484-173">Określa adres IPv4 rekordu A.</span><span class="sxs-lookup"><span data-stu-id="30484-173">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="30484-174">-Adres_ipv6</span><span class="sxs-lookup"><span data-stu-id="30484-174">-Ipv6Address</span></span>
<span data-ttu-id="30484-175">Określa adres IPv6 rekordu AAAA.</span><span class="sxs-lookup"><span data-stu-id="30484-175">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="30484-176">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="30484-176">-Nsdname</span></span>
<span data-ttu-id="30484-177">Określa nazwę serwera nazw dla rekordu serwera nazw (NS).</span><span class="sxs-lookup"><span data-stu-id="30484-177">Specifies the name server name for a name server (NS) record.</span></span>

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

### <span data-ttu-id="30484-178">-Port</span><span class="sxs-lookup"><span data-stu-id="30484-178">-Port</span></span>
<span data-ttu-id="30484-179">Określa port dla rekordu usługi (SRV).</span><span class="sxs-lookup"><span data-stu-id="30484-179">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="30484-180">-Preferencja</span><span class="sxs-lookup"><span data-stu-id="30484-180">-Preference</span></span>
<span data-ttu-id="30484-181">Określa preferencję dla rekordu MX.</span><span class="sxs-lookup"><span data-stu-id="30484-181">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="30484-182">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="30484-182">-Priority</span></span>
<span data-ttu-id="30484-183">Określa priorytet rekordu SRV.</span><span class="sxs-lookup"><span data-stu-id="30484-183">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="30484-184">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="30484-184">-Ptrdname</span></span>
<span data-ttu-id="30484-185">Określa nazwę domeny docelowej rekordu zasobu wskaźnika (PTR).</span><span class="sxs-lookup"><span data-stu-id="30484-185">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

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

### <span data-ttu-id="30484-186">-Target</span><span class="sxs-lookup"><span data-stu-id="30484-186">-Target</span></span>
<span data-ttu-id="30484-187">Określa cel dla rekordu SRV.</span><span class="sxs-lookup"><span data-stu-id="30484-187">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="30484-188">-Value</span><span class="sxs-lookup"><span data-stu-id="30484-188">-Value</span></span>
<span data-ttu-id="30484-189">Określa wartość rekordu TXT.</span><span class="sxs-lookup"><span data-stu-id="30484-189">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="30484-190">-Waga</span><span class="sxs-lookup"><span data-stu-id="30484-190">-Weight</span></span>
<span data-ttu-id="30484-191">Określa wagę rekordu SRV.</span><span class="sxs-lookup"><span data-stu-id="30484-191">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="30484-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30484-192">CommonParameters</span></span>
<span data-ttu-id="30484-193">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30484-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30484-194">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30484-194">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30484-195">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="30484-195">INPUTS</span></span>

### <span data-ttu-id="30484-196">Znaleziono.</span><span class="sxs-lookup"><span data-stu-id="30484-196">None.</span></span>

## <span data-ttu-id="30484-197">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="30484-197">OUTPUTS</span></span>

### <span data-ttu-id="30484-198">Microsoft. Azure. Commands. DNS. DnsRecordBase</span><span class="sxs-lookup"><span data-stu-id="30484-198">Microsoft.Azure.Commands.Dns.DnsRecordBase</span></span>

## <span data-ttu-id="30484-199">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="30484-199">NOTES</span></span>

## <span data-ttu-id="30484-200">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="30484-200">RELATED LINKS</span></span>

[<span data-ttu-id="30484-201">Dodaj-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="30484-201">Add-AzureRmDnsRecordConfig</span></span>](./Add-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="30484-202">Nowe — AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="30484-202">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="30484-203">Remove-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="30484-203">Remove-AzureRmDnsRecordConfig</span></span>](./Remove-AzureRmDnsRecordConfig.md)