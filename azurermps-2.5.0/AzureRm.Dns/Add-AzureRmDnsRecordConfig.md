---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: CD119EBE-E1A4-4E9D-B3BA-FDAF89BF0DDB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f2ba0cb03b4819c444f43a59f5556cf2ec8c17a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898013"
---
# <span data-ttu-id="a14b6-101">Add-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="a14b6-101">Add-AzureRmDnsRecordConfig</span></span>

## <span data-ttu-id="a14b6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a14b6-102">SYNOPSIS</span></span>
<span data-ttu-id="a14b6-103">Dodaje rekord DNS do lokalnego obiektu zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="a14b6-103">Adds a DNS record to a local record set object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a14b6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a14b6-104">SYNTAX</span></span>

### <span data-ttu-id="a14b6-105">Sieci</span><span class="sxs-lookup"><span data-stu-id="a14b6-105">A</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String> [<CommonParameters>]
```

### <span data-ttu-id="a14b6-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="a14b6-106">AAAA</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String> [<CommonParameters>]
```

### <span data-ttu-id="a14b6-107">REKORDU</span><span class="sxs-lookup"><span data-stu-id="a14b6-107">NS</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [<CommonParameters>]
```

### <span data-ttu-id="a14b6-108">MX</span><span class="sxs-lookup"><span data-stu-id="a14b6-108">MX</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [<CommonParameters>]
```

### <span data-ttu-id="a14b6-109">SYSTEMU</span><span class="sxs-lookup"><span data-stu-id="a14b6-109">PTR</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String> [<CommonParameters>]
```

### <span data-ttu-id="a14b6-110">ROZSZERZENIEM</span><span class="sxs-lookup"><span data-stu-id="a14b6-110">TXT</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [<CommonParameters>]
```

### <span data-ttu-id="a14b6-111">SRV</span><span class="sxs-lookup"><span data-stu-id="a14b6-111">SRV</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [<CommonParameters>]
```

### <span data-ttu-id="a14b6-112">REKORD</span><span class="sxs-lookup"><span data-stu-id="a14b6-112">CNAME</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [<CommonParameters>]
```

## <span data-ttu-id="a14b6-113">Opis</span><span class="sxs-lookup"><span data-stu-id="a14b6-113">DESCRIPTION</span></span>
<span data-ttu-id="a14b6-114">Polecenie cmdlet **Add-AzureRmDnsRecordConfig** powoduje dodanie rekordu DNS (Domain Name System) do obiektu **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="a14b6-114">The **Add-AzureRmDnsRecordConfig** cmdlet adds a Domain Name System (DNS) record to a **RecordSet** object.</span></span>
<span data-ttu-id="a14b6-115">Obiekt **Recordset** jest obiektem w trybie offline, a wprowadzone w nim zmiany nie zmieniają odpowiedzi DNS, dopóki nie zostanie uruchomione polecenie cmdlet Set-AzureRmDnsRecordSet w celu utrzymania zmiany w usłudze DNS Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a14b6-115">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzureRmDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>

<span data-ttu-id="a14b6-116">Rekordy SOA są tworzone podczas tworzenia strefy DNS i są usuwane po usunięciu strefy DNS.</span><span class="sxs-lookup"><span data-stu-id="a14b6-116">SOA records are created when a DNS zone is created, and are removed when the DNS zone is deleted.</span></span>
<span data-ttu-id="a14b6-117">Nie można dodawać ani usuwać rekordów SOA, ale można je edytować.</span><span class="sxs-lookup"><span data-stu-id="a14b6-117">You cannot add or remove SOA records, but you can edit them.</span></span>

<span data-ttu-id="a14b6-118">Obiekt **Recordset** można przekazać do tego polecenia cmdlet jako parametru lub za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="a14b6-118">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="a14b6-119">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a14b6-119">EXAMPLES</span></span>

### <span data-ttu-id="a14b6-120">Przykład 1. Dodawanie rekordu A do zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="a14b6-120">Example 1: Add an A record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="a14b6-121">W tym przykładzie dodano rekord do istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="a14b6-121">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="a14b6-122">Przykład 2: Dodawanie rekordu AAAA do zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="a14b6-122">Example 2: Add an AAAA record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="a14b6-123">W tym przykładzie dodano rekord AAAA do istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="a14b6-123">This example adds an AAAA record to an existing record set.</span></span>

### <span data-ttu-id="a14b6-124">Przykład 3: Dodawanie rekordu CNAME do zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="a14b6-124">Example 3: Add a CNAME record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Cname contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="a14b6-125">W tym przykładzie dodano rekord CNAME do istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="a14b6-125">This example adds a CNAME record to an existing record set.</span></span>
<span data-ttu-id="a14b6-126">Ponieważ zestaw rekordów CNAME może zawierać co najwyżej pojedynczy rekord, musi być on początkowo pustym zestawem rekordów lub istniejące rekordy muszą zostać usunięte przy użyciu polecenia Remove-AzureRmDnsRecordConfig.</span><span class="sxs-lookup"><span data-stu-id="a14b6-126">Because a CNAME record set can contain at most one record, it must initially be an empty record set, or existing records must be removed using Remove-AzureRmDnsRecordConfig.</span></span>

### <span data-ttu-id="a14b6-127">Przykład 4: Dodawanie rekordu MX do zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="a14b6-127">Example 4: Add an MX record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="a14b6-128">W tym przykładzie dodano rekord MX do istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="a14b6-128">This example adds an MX record to an existing record set.</span></span>
<span data-ttu-id="a14b6-129">Nazwa rekordu "@" wskazuje zestaw rekordów znajdujący się na wierzchołku strefy.</span><span class="sxs-lookup"><span data-stu-id="a14b6-129">The record name "@" indicates a record set at the zone apex.</span></span>

### <span data-ttu-id="a14b6-130">Przykład 5: Dodawanie rekordu NS do zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="a14b6-130">Example 5: Add an NS record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Nsdname ns1.myzone.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="a14b6-131">W tym przykładzie dodano rekord NS do istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="a14b6-131">This example adds an NS record to an existing record set.</span></span>

### <span data-ttu-id="a14b6-132">Przykład 6: Dodawanie rekordu PTR do zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="a14b6-132">Example 6: Add a PTR record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzureRmDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzureRmDnsRecordConfig -Ptrdname www.contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="a14b6-133">W tym przykładzie do istniejącego zestawu rekordów jest dodawany rekord PTR.</span><span class="sxs-lookup"><span data-stu-id="a14b6-133">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="a14b6-134">Przykład 7: Dodawanie rekordu SRV do zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="a14b6-134">Example 7: Add an SRV record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="a14b6-135">W tym przykładzie dodano rekord SRV do istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="a14b6-135">This example adds an SRV record to an existing record set.</span></span>

### <span data-ttu-id="a14b6-136">Przykład 8: Dodawanie rekordu TXT do zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="a14b6-136">Example 8: Add a TXT record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Value "This is a TXT Record" | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="a14b6-137">W tym przykładzie dodano rekord TXT do istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="a14b6-137">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="a14b6-138">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a14b6-138">PARAMETERS</span></span>

### <span data-ttu-id="a14b6-139">-CNAME</span><span class="sxs-lookup"><span data-stu-id="a14b6-139">-Cname</span></span>
<span data-ttu-id="a14b6-140">Określa nazwę domeny dla rekordu kanonicznego (CNAME).</span><span class="sxs-lookup"><span data-stu-id="a14b6-140">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: String
Parameter Sets: CNAME
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a14b6-141">-Exchange</span><span class="sxs-lookup"><span data-stu-id="a14b6-141">-Exchange</span></span>
<span data-ttu-id="a14b6-142">Określa nazwę serwera Exchange mail dla rekordu wymiany poczty (MX).</span><span class="sxs-lookup"><span data-stu-id="a14b6-142">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: String
Parameter Sets: MX
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a14b6-143">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="a14b6-143">-Ipv4Address</span></span>
<span data-ttu-id="a14b6-144">Określa adres IPv4 rekordu A.</span><span class="sxs-lookup"><span data-stu-id="a14b6-144">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="a14b6-145">-Adres_ipv6</span><span class="sxs-lookup"><span data-stu-id="a14b6-145">-Ipv6Address</span></span>
<span data-ttu-id="a14b6-146">Określa adres IPv6 rekordu AAAA.</span><span class="sxs-lookup"><span data-stu-id="a14b6-146">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: String
Parameter Sets: AAAA
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a14b6-147">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="a14b6-147">-Nsdname</span></span>
<span data-ttu-id="a14b6-148">Określa nazwę serwera nazw dla rekordu serwera nazw (NS).</span><span class="sxs-lookup"><span data-stu-id="a14b6-148">Specifies the name server name for a name server (NS) record.</span></span>

```yaml
Type: String
Parameter Sets: NS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a14b6-149">-Port</span><span class="sxs-lookup"><span data-stu-id="a14b6-149">-Port</span></span>
<span data-ttu-id="a14b6-150">Określa port dla rekordu usługi (SRV).</span><span class="sxs-lookup"><span data-stu-id="a14b6-150">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a14b6-151">-Preferencja</span><span class="sxs-lookup"><span data-stu-id="a14b6-151">-Preference</span></span>
<span data-ttu-id="a14b6-152">Określa preferencję dla rekordu MX.</span><span class="sxs-lookup"><span data-stu-id="a14b6-152">Specifies the preference for an MX record.</span></span>

```yaml
Type: UInt16
Parameter Sets: MX
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a14b6-153">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="a14b6-153">-Priority</span></span>
<span data-ttu-id="a14b6-154">Określa priorytet rekordu SRV.</span><span class="sxs-lookup"><span data-stu-id="a14b6-154">Specifies the priority for an SRV record.</span></span>

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a14b6-155">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="a14b6-155">-Ptrdname</span></span>
<span data-ttu-id="a14b6-156">Określa nazwę domeny docelowej rekordu zasobu wskaźnika (PTR).</span><span class="sxs-lookup"><span data-stu-id="a14b6-156">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

```yaml
Type: String
Parameter Sets: PTR
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a14b6-157">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="a14b6-157">-RecordSet</span></span>
<span data-ttu-id="a14b6-158">Określa obiekt **zestawu rekordów** do edycji.</span><span class="sxs-lookup"><span data-stu-id="a14b6-158">Specifies the **RecordSet** object to edit.</span></span>

```yaml
Type: DnsRecordSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a14b6-159">-Target</span><span class="sxs-lookup"><span data-stu-id="a14b6-159">-Target</span></span>
<span data-ttu-id="a14b6-160">Określa cel dla rekordu SRV.</span><span class="sxs-lookup"><span data-stu-id="a14b6-160">Specifies the target for an SRV record.</span></span>

```yaml
Type: String
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a14b6-161">-Value</span><span class="sxs-lookup"><span data-stu-id="a14b6-161">-Value</span></span>
<span data-ttu-id="a14b6-162">Określa wartość rekordu TXT.</span><span class="sxs-lookup"><span data-stu-id="a14b6-162">Specifies the value for a TXT record.</span></span>

```yaml
Type: String
Parameter Sets: TXT
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a14b6-163">-Waga</span><span class="sxs-lookup"><span data-stu-id="a14b6-163">-Weight</span></span>
<span data-ttu-id="a14b6-164">Określa wagę rekordu SRV.</span><span class="sxs-lookup"><span data-stu-id="a14b6-164">Specifies the weight for an SRV record.</span></span>

```yaml
Type: UInt16
Parameter Sets: SRV
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a14b6-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a14b6-165">CommonParameters</span></span>
<span data-ttu-id="a14b6-166">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a14b6-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a14b6-167">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a14b6-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a14b6-168">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a14b6-168">INPUTS</span></span>

### <span data-ttu-id="a14b6-169">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a14b6-169">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="a14b6-170">Do tego polecenia cmdlet można przetworzyć obiekt **zestawu rekordów** .</span><span class="sxs-lookup"><span data-stu-id="a14b6-170">You can pipe a **RecordSet** object to this cmdlet.</span></span>
<span data-ttu-id="a14b6-171">Jest to reprezentacja **zestawu rekordów** w trybie offline, a zmiana nie powoduje zmiany odpowiedzi DNS, dopóki nie zostanie uruchomione polecenie cmdlet Set-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="a14b6-171">This is an offline representation of the **RecordSet** , and changes to it do not change DNS responses until after you run the Set-AzureRmDnsRecordSet cmdlet.</span></span>

## <span data-ttu-id="a14b6-172">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a14b6-172">OUTPUTS</span></span>

### <span data-ttu-id="a14b6-173">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a14b6-173">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="a14b6-174">To polecenie cmdlet zwraca zmodyfikowany obiekt **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="a14b6-174">This cmdlet returns the modified **RecordSet** object.</span></span>
<span data-ttu-id="a14b6-175">Ponadto przekazana obiekt jest modyfikowany bezpośrednio.</span><span class="sxs-lookup"><span data-stu-id="a14b6-175">In addition, the object passed in is modified directly.</span></span>

## <span data-ttu-id="a14b6-176">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a14b6-176">NOTES</span></span>

## <span data-ttu-id="a14b6-177">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a14b6-177">RELATED LINKS</span></span>

[<span data-ttu-id="a14b6-178">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a14b6-178">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="a14b6-179">Remove-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="a14b6-179">Remove-AzureRmDnsRecordConfig</span></span>](./Remove-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="a14b6-180">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="a14b6-180">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)
