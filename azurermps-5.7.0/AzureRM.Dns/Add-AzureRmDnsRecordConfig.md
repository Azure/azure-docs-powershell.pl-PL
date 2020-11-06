---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: CD119EBE-E1A4-4E9D-B3BA-FDAF89BF0DDB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/add-azurermdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Add-AzureRmDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Add-AzureRmDnsRecordConfig.md
ms.openlocfilehash: c9e824160b04b183414c6b99fce4b09b6d70766a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528146"
---
# <span data-ttu-id="b7124-101">Add-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="b7124-101">Add-AzureRmDnsRecordConfig</span></span>

## <span data-ttu-id="b7124-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b7124-102">SYNOPSIS</span></span>
<span data-ttu-id="b7124-103">Dodaje rekord DNS do lokalnego obiektu zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="b7124-103">Adds a DNS record to a local record set object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7124-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b7124-104">SYNTAX</span></span>

### <span data-ttu-id="b7124-105">Sieci</span><span class="sxs-lookup"><span data-stu-id="b7124-105">A</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7124-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="b7124-106">AAAA</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7124-107">REKORDU</span><span class="sxs-lookup"><span data-stu-id="b7124-107">NS</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7124-108">MX</span><span class="sxs-lookup"><span data-stu-id="b7124-108">MX</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7124-109">SYSTEMU</span><span class="sxs-lookup"><span data-stu-id="b7124-109">PTR</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7124-110">ROZSZERZENIEM</span><span class="sxs-lookup"><span data-stu-id="b7124-110">TXT</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b7124-111">SRV</span><span class="sxs-lookup"><span data-stu-id="b7124-111">SRV</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7124-112">REKORD</span><span class="sxs-lookup"><span data-stu-id="b7124-112">CNAME</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b7124-113">Caa</span><span class="sxs-lookup"><span data-stu-id="b7124-113">Caa</span></span>
```
Add-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7124-114">Opis</span><span class="sxs-lookup"><span data-stu-id="b7124-114">DESCRIPTION</span></span>
<span data-ttu-id="b7124-115">Polecenie cmdlet **Add-AzureRmDnsRecordConfig** powoduje dodanie rekordu DNS (Domain Name System) do obiektu **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="b7124-115">The **Add-AzureRmDnsRecordConfig** cmdlet adds a Domain Name System (DNS) record to a **RecordSet** object.</span></span>
<span data-ttu-id="b7124-116">Obiekt **Recordset** jest obiektem w trybie offline, a wprowadzone w nim zmiany nie zmieniają odpowiedzi DNS, dopóki nie zostanie uruchomione polecenie cmdlet Set-AzureRmDnsRecordSet w celu utrzymania zmiany w usłudze DNS Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b7124-116">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzureRmDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>

<span data-ttu-id="b7124-117">Rekordy SOA są tworzone podczas tworzenia strefy DNS i są usuwane po usunięciu strefy DNS.</span><span class="sxs-lookup"><span data-stu-id="b7124-117">SOA records are created when a DNS zone is created, and are removed when the DNS zone is deleted.</span></span>
<span data-ttu-id="b7124-118">Nie można dodawać ani usuwać rekordów SOA, ale można je edytować.</span><span class="sxs-lookup"><span data-stu-id="b7124-118">You cannot add or remove SOA records, but you can edit them.</span></span>

<span data-ttu-id="b7124-119">Obiekt **Recordset** można przekazać do tego polecenia cmdlet jako parametru lub za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="b7124-119">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="b7124-120">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b7124-120">EXAMPLES</span></span>

### <span data-ttu-id="b7124-121">Przykład 1. Dodawanie rekordu A do zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="b7124-121">Example 1: Add an A record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="b7124-122">W tym przykładzie dodano rekord do istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="b7124-122">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="b7124-123">Przykład 2: Dodawanie rekordu AAAA do zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="b7124-123">Example 2: Add an AAAA record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="b7124-124">W tym przykładzie dodano rekord AAAA do istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="b7124-124">This example adds an AAAA record to an existing record set.</span></span>

### <span data-ttu-id="b7124-125">Przykład 3: Dodawanie rekordu CNAME do zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="b7124-125">Example 3: Add a CNAME record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Cname contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="b7124-126">W tym przykładzie dodano rekord CNAME do istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="b7124-126">This example adds a CNAME record to an existing record set.</span></span>
<span data-ttu-id="b7124-127">Ponieważ zestaw rekordów CNAME może zawierać co najwyżej pojedynczy rekord, musi być on początkowo pustym zestawem rekordów lub istniejące rekordy muszą zostać usunięte przy użyciu polecenia Remove-AzureRmDnsRecordConfig.</span><span class="sxs-lookup"><span data-stu-id="b7124-127">Because a CNAME record set can contain at most one record, it must initially be an empty record set, or existing records must be removed using Remove-AzureRmDnsRecordConfig.</span></span>

### <span data-ttu-id="b7124-128">Przykład 4: Dodawanie rekordu MX do zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="b7124-128">Example 4: Add an MX record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="b7124-129">W tym przykładzie dodano rekord MX do istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="b7124-129">This example adds an MX record to an existing record set.</span></span>
<span data-ttu-id="b7124-130">Nazwa rekordu "@" wskazuje zestaw rekordów znajdujący się na wierzchołku strefy.</span><span class="sxs-lookup"><span data-stu-id="b7124-130">The record name "@" indicates a record set at the zone apex.</span></span>

### <span data-ttu-id="b7124-131">Przykład 5: Dodawanie rekordu NS do zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="b7124-131">Example 5: Add an NS record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzureRmDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Nsdname ns1.myzone.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="b7124-132">W tym przykładzie dodano rekord NS do istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="b7124-132">This example adds an NS record to an existing record set.</span></span>

### <span data-ttu-id="b7124-133">Przykład 6: Dodawanie rekordu PTR do zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="b7124-133">Example 6: Add a PTR record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzureRmDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzureRmDnsRecordConfig -Ptrdname www.contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="b7124-134">W tym przykładzie do istniejącego zestawu rekordów jest dodawany rekord PTR.</span><span class="sxs-lookup"><span data-stu-id="b7124-134">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="b7124-135">Przykład 7: Dodawanie rekordu SRV do zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="b7124-135">Example 7: Add an SRV record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="b7124-136">W tym przykładzie dodano rekord SRV do istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="b7124-136">This example adds an SRV record to an existing record set.</span></span>

### <span data-ttu-id="b7124-137">Przykład 8: Dodawanie rekordu TXT do zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="b7124-137">Example 8: Add a TXT record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzureRmDnsRecordConfig -Value "This is a TXT Record" | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="b7124-138">W tym przykładzie dodano rekord TXT do istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="b7124-138">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="b7124-139">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b7124-139">PARAMETERS</span></span>

### <span data-ttu-id="b7124-140">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="b7124-140">-CaaFlags</span></span>
<span data-ttu-id="b7124-141">Flagi rekordu CAA, które mają zostać dodane.</span><span class="sxs-lookup"><span data-stu-id="b7124-141">The flags for the CAA record to add.</span></span> <span data-ttu-id="b7124-142">Musi być liczbą z przedziału od 0 do 255.</span><span class="sxs-lookup"><span data-stu-id="b7124-142">Must be a number between 0 and 255.</span></span>

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

### <span data-ttu-id="b7124-143">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="b7124-143">-CaaTag</span></span>
<span data-ttu-id="b7124-144">Pole tag w rekordzie CAA, które ma zostać dodane.</span><span class="sxs-lookup"><span data-stu-id="b7124-144">The tag field of the CAA record to add.</span></span>

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

### <span data-ttu-id="b7124-145">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="b7124-145">-CaaValue</span></span>
<span data-ttu-id="b7124-146">Pole wartości dla rekordu CAA, który ma zostać dodany.</span><span class="sxs-lookup"><span data-stu-id="b7124-146">The value field for the CAA record to add.</span></span>

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

### <span data-ttu-id="b7124-147">-CNAME</span><span class="sxs-lookup"><span data-stu-id="b7124-147">-Cname</span></span>
<span data-ttu-id="b7124-148">Określa nazwę domeny dla rekordu kanonicznego (CNAME).</span><span class="sxs-lookup"><span data-stu-id="b7124-148">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="b7124-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7124-149">-DefaultProfile</span></span>
<span data-ttu-id="b7124-150">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b7124-150">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7124-151">-Exchange</span><span class="sxs-lookup"><span data-stu-id="b7124-151">-Exchange</span></span>
<span data-ttu-id="b7124-152">Określa nazwę serwera Exchange mail dla rekordu wymiany poczty (MX).</span><span class="sxs-lookup"><span data-stu-id="b7124-152">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="b7124-153">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="b7124-153">-Ipv4Address</span></span>
<span data-ttu-id="b7124-154">Określa adres IPv4 rekordu A.</span><span class="sxs-lookup"><span data-stu-id="b7124-154">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="b7124-155">-Adres_ipv6</span><span class="sxs-lookup"><span data-stu-id="b7124-155">-Ipv6Address</span></span>
<span data-ttu-id="b7124-156">Określa adres IPv6 rekordu AAAA.</span><span class="sxs-lookup"><span data-stu-id="b7124-156">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="b7124-157">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="b7124-157">-Nsdname</span></span>
<span data-ttu-id="b7124-158">Określa nazwę serwera nazw dla rekordu serwera nazw (NS).</span><span class="sxs-lookup"><span data-stu-id="b7124-158">Specifies the name server name for a name server (NS) record.</span></span>

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

### <span data-ttu-id="b7124-159">-Port</span><span class="sxs-lookup"><span data-stu-id="b7124-159">-Port</span></span>
<span data-ttu-id="b7124-160">Określa port dla rekordu usługi (SRV).</span><span class="sxs-lookup"><span data-stu-id="b7124-160">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="b7124-161">-Preferencja</span><span class="sxs-lookup"><span data-stu-id="b7124-161">-Preference</span></span>
<span data-ttu-id="b7124-162">Określa preferencję dla rekordu MX.</span><span class="sxs-lookup"><span data-stu-id="b7124-162">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="b7124-163">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="b7124-163">-Priority</span></span>
<span data-ttu-id="b7124-164">Określa priorytet rekordu SRV.</span><span class="sxs-lookup"><span data-stu-id="b7124-164">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="b7124-165">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="b7124-165">-Ptrdname</span></span>
<span data-ttu-id="b7124-166">Określa nazwę domeny docelowej rekordu zasobu wskaźnika (PTR).</span><span class="sxs-lookup"><span data-stu-id="b7124-166">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

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

### <span data-ttu-id="b7124-167">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="b7124-167">-RecordSet</span></span>
<span data-ttu-id="b7124-168">Określa obiekt **zestawu rekordów** do edycji.</span><span class="sxs-lookup"><span data-stu-id="b7124-168">Specifies the **RecordSet** object to edit.</span></span>

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

### <span data-ttu-id="b7124-169">-Target</span><span class="sxs-lookup"><span data-stu-id="b7124-169">-Target</span></span>
<span data-ttu-id="b7124-170">Określa cel dla rekordu SRV.</span><span class="sxs-lookup"><span data-stu-id="b7124-170">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="b7124-171">-Value</span><span class="sxs-lookup"><span data-stu-id="b7124-171">-Value</span></span>
<span data-ttu-id="b7124-172">Określa wartość rekordu TXT.</span><span class="sxs-lookup"><span data-stu-id="b7124-172">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="b7124-173">-Waga</span><span class="sxs-lookup"><span data-stu-id="b7124-173">-Weight</span></span>
<span data-ttu-id="b7124-174">Określa wagę rekordu SRV.</span><span class="sxs-lookup"><span data-stu-id="b7124-174">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="b7124-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7124-175">CommonParameters</span></span>
<span data-ttu-id="b7124-176">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7124-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7124-177">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7124-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7124-178">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b7124-178">INPUTS</span></span>

### <span data-ttu-id="b7124-179">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b7124-179">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="b7124-180">Do tego polecenia cmdlet można przetworzyć obiekt **zestawu rekordów** .</span><span class="sxs-lookup"><span data-stu-id="b7124-180">You can pipe a **RecordSet** object to this cmdlet.</span></span>
<span data-ttu-id="b7124-181">Jest to reprezentacja **zestawu rekordów** w trybie offline, a zmiana nie powoduje zmiany odpowiedzi DNS, dopóki nie zostanie uruchomione polecenie cmdlet Set-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="b7124-181">This is an offline representation of the **RecordSet** , and changes to it do not change DNS responses until after you run the Set-AzureRmDnsRecordSet cmdlet.</span></span>

## <span data-ttu-id="b7124-182">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b7124-182">OUTPUTS</span></span>

### <span data-ttu-id="b7124-183">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b7124-183">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="b7124-184">To polecenie cmdlet zwraca zmodyfikowany obiekt **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="b7124-184">This cmdlet returns the modified **RecordSet** object.</span></span>
<span data-ttu-id="b7124-185">Ponadto przekazana obiekt jest modyfikowany bezpośrednio.</span><span class="sxs-lookup"><span data-stu-id="b7124-185">In addition, the object passed in is modified directly.</span></span>

## <span data-ttu-id="b7124-186">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b7124-186">NOTES</span></span>

## <span data-ttu-id="b7124-187">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b7124-187">RELATED LINKS</span></span>

[<span data-ttu-id="b7124-188">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b7124-188">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="b7124-189">Remove-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="b7124-189">Remove-AzureRmDnsRecordConfig</span></span>](./Remove-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="b7124-190">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="b7124-190">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)
