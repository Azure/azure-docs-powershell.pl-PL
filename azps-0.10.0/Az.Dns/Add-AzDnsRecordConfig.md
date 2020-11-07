---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: CD119EBE-E1A4-4E9D-B3BA-FDAF89BF0DDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/add-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Add-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Add-AzDnsRecordConfig.md
ms.openlocfilehash: a5f3871f0ab63d875c2a0389c5585f0871fb0cb9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891545"
---
# <span data-ttu-id="1661b-101">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="1661b-101">Add-AzDnsRecordConfig</span></span>

## <span data-ttu-id="1661b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1661b-102">SYNOPSIS</span></span>
<span data-ttu-id="1661b-103">Dodaje rekord DNS do lokalnego obiektu zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="1661b-103">Adds a DNS record to a local record set object.</span></span>

## <span data-ttu-id="1661b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1661b-104">SYNTAX</span></span>

### <span data-ttu-id="1661b-105">Sieci</span><span class="sxs-lookup"><span data-stu-id="1661b-105">A</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String> [<CommonParameters>]
```

### <span data-ttu-id="1661b-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="1661b-106">AAAA</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String> [<CommonParameters>]
```

### <span data-ttu-id="1661b-107">REKORDU</span><span class="sxs-lookup"><span data-stu-id="1661b-107">NS</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [<CommonParameters>]
```

### <span data-ttu-id="1661b-108">MX</span><span class="sxs-lookup"><span data-stu-id="1661b-108">MX</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [<CommonParameters>]
```

### <span data-ttu-id="1661b-109">SYSTEMU</span><span class="sxs-lookup"><span data-stu-id="1661b-109">PTR</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String> [<CommonParameters>]
```

### <span data-ttu-id="1661b-110">ROZSZERZENIEM</span><span class="sxs-lookup"><span data-stu-id="1661b-110">TXT</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [<CommonParameters>]
```

### <span data-ttu-id="1661b-111">SRV</span><span class="sxs-lookup"><span data-stu-id="1661b-111">SRV</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [<CommonParameters>]
```

### <span data-ttu-id="1661b-112">REKORD</span><span class="sxs-lookup"><span data-stu-id="1661b-112">CNAME</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [<CommonParameters>]
```

## <span data-ttu-id="1661b-113">Opis</span><span class="sxs-lookup"><span data-stu-id="1661b-113">DESCRIPTION</span></span>
<span data-ttu-id="1661b-114">Polecenie cmdlet **Add-AzDnsRecordConfig** powoduje dodanie rekordu DNS (Domain Name System) do obiektu **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="1661b-114">The **Add-AzDnsRecordConfig** cmdlet adds a Domain Name System (DNS) record to a **RecordSet** object.</span></span>
<span data-ttu-id="1661b-115">Obiekt **Recordset** jest obiektem w trybie offline, a wprowadzone w nim zmiany nie zmieniają odpowiedzi DNS, dopóki nie zostanie uruchomione polecenie cmdlet Set-AzDnsRecordSet w celu utrzymania zmiany w usłudze DNS Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1661b-115">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>

<span data-ttu-id="1661b-116">Rekordy SOA są tworzone podczas tworzenia strefy DNS i są usuwane po usunięciu strefy DNS.</span><span class="sxs-lookup"><span data-stu-id="1661b-116">SOA records are created when a DNS zone is created, and are removed when the DNS zone is deleted.</span></span>
<span data-ttu-id="1661b-117">Nie można dodawać ani usuwać rekordów SOA, ale można je edytować.</span><span class="sxs-lookup"><span data-stu-id="1661b-117">You cannot add or remove SOA records, but you can edit them.</span></span>

<span data-ttu-id="1661b-118">Obiekt **Recordset** można przekazać do tego polecenia cmdlet jako parametru lub za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="1661b-118">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="1661b-119">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1661b-119">EXAMPLES</span></span>

### <span data-ttu-id="1661b-120">Przykład 1. Dodawanie rekordu A do zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="1661b-120">Example 1: Add an A record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

<span data-ttu-id="1661b-121">W tym przykładzie dodano rekord do istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="1661b-121">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="1661b-122">Przykład 2: Dodawanie rekordu AAAA do zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="1661b-122">Example 2: Add an AAAA record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

<span data-ttu-id="1661b-123">W tym przykładzie dodano rekord AAAA do istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="1661b-123">This example adds an AAAA record to an existing record set.</span></span>

### <span data-ttu-id="1661b-124">Przykład 3: Dodawanie rekordu CNAME do zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="1661b-124">Example 3: Add a CNAME record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="1661b-125">W tym przykładzie dodano rekord CNAME do istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="1661b-125">This example adds a CNAME record to an existing record set.</span></span>
<span data-ttu-id="1661b-126">Ponieważ zestaw rekordów CNAME może zawierać co najwyżej pojedynczy rekord, musi być on początkowo pustym zestawem rekordów lub istniejące rekordy muszą zostać usunięte przy użyciu polecenia Remove-AzDnsRecordConfig.</span><span class="sxs-lookup"><span data-stu-id="1661b-126">Because a CNAME record set can contain at most one record, it must initially be an empty record set, or existing records must be removed using Remove-AzDnsRecordConfig.</span></span>

### <span data-ttu-id="1661b-127">Przykład 4: Dodawanie rekordu MX do zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="1661b-127">Example 4: Add an MX record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

<span data-ttu-id="1661b-128">W tym przykładzie dodano rekord MX do istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="1661b-128">This example adds an MX record to an existing record set.</span></span>
<span data-ttu-id="1661b-129">Nazwa rekordu "@" wskazuje zestaw rekordów znajdujący się na wierzchołku strefy.</span><span class="sxs-lookup"><span data-stu-id="1661b-129">The record name "@" indicates a record set at the zone apex.</span></span>

### <span data-ttu-id="1661b-130">Przykład 5: Dodawanie rekordu NS do zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="1661b-130">Example 5: Add an NS record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Nsdname ns1.myzone.com | Set-AzDnsRecordSet
```

<span data-ttu-id="1661b-131">W tym przykładzie dodano rekord NS do istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="1661b-131">This example adds an NS record to an existing record set.</span></span>

### <span data-ttu-id="1661b-132">Przykład 6: Dodawanie rekordu PTR do zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="1661b-132">Example 6: Add a PTR record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="1661b-133">W tym przykładzie do istniejącego zestawu rekordów jest dodawany rekord PTR.</span><span class="sxs-lookup"><span data-stu-id="1661b-133">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="1661b-134">Przykład 7: Dodawanie rekordu SRV do zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="1661b-134">Example 7: Add an SRV record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

<span data-ttu-id="1661b-135">W tym przykładzie dodano rekord SRV do istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="1661b-135">This example adds an SRV record to an existing record set.</span></span>

### <span data-ttu-id="1661b-136">Przykład 8: Dodawanie rekordu TXT do zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="1661b-136">Example 8: Add a TXT record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Value "This is a TXT Record" | Set-AzDnsRecordSet
```

<span data-ttu-id="1661b-137">W tym przykładzie dodano rekord TXT do istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="1661b-137">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="1661b-138">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1661b-138">PARAMETERS</span></span>

### <span data-ttu-id="1661b-139">-CNAME</span><span class="sxs-lookup"><span data-stu-id="1661b-139">-Cname</span></span>
<span data-ttu-id="1661b-140">Określa nazwę domeny dla rekordu kanonicznego (CNAME).</span><span class="sxs-lookup"><span data-stu-id="1661b-140">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="1661b-141">-Exchange</span><span class="sxs-lookup"><span data-stu-id="1661b-141">-Exchange</span></span>
<span data-ttu-id="1661b-142">Określa nazwę serwera Exchange mail dla rekordu wymiany poczty (MX).</span><span class="sxs-lookup"><span data-stu-id="1661b-142">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="1661b-143">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="1661b-143">-Ipv4Address</span></span>
<span data-ttu-id="1661b-144">Określa adres IPv4 rekordu A.</span><span class="sxs-lookup"><span data-stu-id="1661b-144">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="1661b-145">-Adres_ipv6</span><span class="sxs-lookup"><span data-stu-id="1661b-145">-Ipv6Address</span></span>
<span data-ttu-id="1661b-146">Określa adres IPv6 rekordu AAAA.</span><span class="sxs-lookup"><span data-stu-id="1661b-146">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="1661b-147">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="1661b-147">-Nsdname</span></span>
<span data-ttu-id="1661b-148">Określa nazwę serwera nazw dla rekordu serwera nazw (NS).</span><span class="sxs-lookup"><span data-stu-id="1661b-148">Specifies the name server name for a name server (NS) record.</span></span>

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

### <span data-ttu-id="1661b-149">-Port</span><span class="sxs-lookup"><span data-stu-id="1661b-149">-Port</span></span>
<span data-ttu-id="1661b-150">Określa port dla rekordu usługi (SRV).</span><span class="sxs-lookup"><span data-stu-id="1661b-150">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="1661b-151">-Preferencja</span><span class="sxs-lookup"><span data-stu-id="1661b-151">-Preference</span></span>
<span data-ttu-id="1661b-152">Określa preferencję dla rekordu MX.</span><span class="sxs-lookup"><span data-stu-id="1661b-152">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="1661b-153">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="1661b-153">-Priority</span></span>
<span data-ttu-id="1661b-154">Określa priorytet rekordu SRV.</span><span class="sxs-lookup"><span data-stu-id="1661b-154">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="1661b-155">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="1661b-155">-Ptrdname</span></span>
<span data-ttu-id="1661b-156">Określa nazwę domeny docelowej rekordu zasobu wskaźnika (PTR).</span><span class="sxs-lookup"><span data-stu-id="1661b-156">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

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

### <span data-ttu-id="1661b-157">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="1661b-157">-RecordSet</span></span>
<span data-ttu-id="1661b-158">Określa obiekt **zestawu rekordów** do edycji.</span><span class="sxs-lookup"><span data-stu-id="1661b-158">Specifies the **RecordSet** object to edit.</span></span>

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

### <span data-ttu-id="1661b-159">-Target</span><span class="sxs-lookup"><span data-stu-id="1661b-159">-Target</span></span>
<span data-ttu-id="1661b-160">Określa cel dla rekordu SRV.</span><span class="sxs-lookup"><span data-stu-id="1661b-160">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="1661b-161">-Value</span><span class="sxs-lookup"><span data-stu-id="1661b-161">-Value</span></span>
<span data-ttu-id="1661b-162">Określa wartość rekordu TXT.</span><span class="sxs-lookup"><span data-stu-id="1661b-162">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="1661b-163">-Waga</span><span class="sxs-lookup"><span data-stu-id="1661b-163">-Weight</span></span>
<span data-ttu-id="1661b-164">Określa wagę rekordu SRV.</span><span class="sxs-lookup"><span data-stu-id="1661b-164">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="1661b-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1661b-165">CommonParameters</span></span>
<span data-ttu-id="1661b-166">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1661b-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1661b-167">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1661b-167">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1661b-168">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1661b-168">INPUTS</span></span>

### <span data-ttu-id="1661b-169">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="1661b-169">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="1661b-170">Do tego polecenia cmdlet można przetworzyć obiekt **zestawu rekordów** .</span><span class="sxs-lookup"><span data-stu-id="1661b-170">You can pipe a **RecordSet** object to this cmdlet.</span></span>
<span data-ttu-id="1661b-171">Jest to reprezentacja **zestawu rekordów** w trybie offline, a zmiana nie powoduje zmiany odpowiedzi DNS, dopóki nie zostanie uruchomione polecenie cmdlet Set-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="1661b-171">This is an offline representation of the **RecordSet** , and changes to it do not change DNS responses until after you run the Set-AzDnsRecordSet cmdlet.</span></span>

## <span data-ttu-id="1661b-172">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1661b-172">OUTPUTS</span></span>

### <span data-ttu-id="1661b-173">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="1661b-173">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="1661b-174">To polecenie cmdlet zwraca zmodyfikowany obiekt **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="1661b-174">This cmdlet returns the modified **RecordSet** object.</span></span>
<span data-ttu-id="1661b-175">Ponadto przekazana obiekt jest modyfikowany bezpośrednio.</span><span class="sxs-lookup"><span data-stu-id="1661b-175">In addition, the object passed in is modified directly.</span></span>

## <span data-ttu-id="1661b-176">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1661b-176">NOTES</span></span>

## <span data-ttu-id="1661b-177">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1661b-177">RELATED LINKS</span></span>

[<span data-ttu-id="1661b-178">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="1661b-178">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="1661b-179">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="1661b-179">Remove-AzDnsRecordConfig</span></span>](./Remove-AzDnsRecordConfig.md)

[<span data-ttu-id="1661b-180">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="1661b-180">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
