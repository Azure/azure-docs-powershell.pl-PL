---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: CD119EBE-E1A4-4E9D-B3BA-FDAF89BF0DDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/add-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Add-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Add-AzDnsRecordConfig.md
ms.openlocfilehash: c9390514ad7680a047ca145c8fe71feda0ab1b51
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196362"
---
# <span data-ttu-id="fe2fc-101">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="fe2fc-101">Add-AzDnsRecordConfig</span></span>

## <span data-ttu-id="fe2fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe2fc-102">SYNOPSIS</span></span>
<span data-ttu-id="fe2fc-103">Dodaje rekord DNS do obiektu lokalnego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="fe2fc-103">Adds a DNS record to a local record set object.</span></span>

## <span data-ttu-id="fe2fc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fe2fc-104">SYNTAX</span></span>

### <span data-ttu-id="fe2fc-105">A</span><span class="sxs-lookup"><span data-stu-id="fe2fc-105">A</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe2fc-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="fe2fc-106">AAAA</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe2fc-107">NS</span><span class="sxs-lookup"><span data-stu-id="fe2fc-107">NS</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fe2fc-108">MX</span><span class="sxs-lookup"><span data-stu-id="fe2fc-108">MX</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe2fc-109">PTR</span><span class="sxs-lookup"><span data-stu-id="fe2fc-109">PTR</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fe2fc-110">TXT</span><span class="sxs-lookup"><span data-stu-id="fe2fc-110">TXT</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fe2fc-111">SRV</span><span class="sxs-lookup"><span data-stu-id="fe2fc-111">SRV</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe2fc-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="fe2fc-112">CNAME</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fe2fc-113">Caa</span><span class="sxs-lookup"><span data-stu-id="fe2fc-113">Caa</span></span>
```
Add-AzDnsRecordConfig -RecordSet <DnsRecordSet> -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe2fc-114">OPIS</span><span class="sxs-lookup"><span data-stu-id="fe2fc-114">DESCRIPTION</span></span>
<span data-ttu-id="fe2fc-115">Polecenie **cmdlet Add-AzDnsRecordConfig** dodaje rekord DNS (Domain Name System) do **obiektu RecordSet.**</span><span class="sxs-lookup"><span data-stu-id="fe2fc-115">The **Add-AzDnsRecordConfig** cmdlet adds a Domain Name System (DNS) record to a **RecordSet** object.</span></span>
<span data-ttu-id="fe2fc-116">Obiekt **RecordSet** jest obiektem offline i zmiany w nim nie zmieniają odpowiedzi DNS dopiero po uruchomieniu polecenia cmdlet Set-AzDnsRecordSet w celu utrwalenia zmiany w usłudze DNS platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fe2fc-116">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>
<span data-ttu-id="fe2fc-117">Rekordy SOA są tworzone po utworzeniu strefy DNS i usuwane po jej usunięciu.</span><span class="sxs-lookup"><span data-stu-id="fe2fc-117">SOA records are created when a DNS zone is created, and are removed when the DNS zone is deleted.</span></span>
<span data-ttu-id="fe2fc-118">Nie można dodawać ani usuwać rekordów SOA, ale można je edytować.</span><span class="sxs-lookup"><span data-stu-id="fe2fc-118">You cannot add or remove SOA records, but you can edit them.</span></span>
<span data-ttu-id="fe2fc-119">Obiekt **RecordSet** można przekazać do tego polecenia cmdlet jako parametr lub za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="fe2fc-119">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="fe2fc-120">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fe2fc-120">EXAMPLES</span></span>

### <span data-ttu-id="fe2fc-121">Przykład 1. Dodawanie rekordu A do zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="fe2fc-121">Example 1: Add an A record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType A -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

<span data-ttu-id="fe2fc-122">W tym przykładzie do istniejącego zestawu rekordów został dodano rekord A.</span><span class="sxs-lookup"><span data-stu-id="fe2fc-122">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="fe2fc-123">Przykład 2. Dodawanie rekordu AAAA do zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="fe2fc-123">Example 2: Add an AAAA record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType AAAA -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

<span data-ttu-id="fe2fc-124">W tym przykładzie do istniejącego zestawu rekordów został dodano rekord AAAA.</span><span class="sxs-lookup"><span data-stu-id="fe2fc-124">This example adds an AAAA record to an existing record set.</span></span>

### <span data-ttu-id="fe2fc-125">Przykład 3. Dodawanie rekordu CNAME do zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="fe2fc-125">Example 3: Add a CNAME record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name www -RecordType CNAME -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="fe2fc-126">W tym przykładzie do istniejącego zestawu rekordów został dodano rekord CNAME.</span><span class="sxs-lookup"><span data-stu-id="fe2fc-126">This example adds a CNAME record to an existing record set.</span></span>
<span data-ttu-id="fe2fc-127">Ponieważ zestaw rekordów CNAME może zawierać co najwyżej jeden rekord, początkowo musi być pustym zestawem rekordów lub istniejący rekord musi zostać usunięty za pomocą narzędzia Remove-AzDnsRecordConfig.</span><span class="sxs-lookup"><span data-stu-id="fe2fc-127">Because a CNAME record set can contain at most one record, it must initially be an empty record set, or existing records must be removed using Remove-AzDnsRecordConfig.</span></span>

### <span data-ttu-id="fe2fc-128">Przykład 4. Dodawanie rekordu MX do zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="fe2fc-128">Example 4: Add an MX record to a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

<span data-ttu-id="fe2fc-129">W tym przykładzie do istniejącego zestawu rekordów został dodano rekord MX.</span><span class="sxs-lookup"><span data-stu-id="fe2fc-129">This example adds an MX record to an existing record set.</span></span>
<span data-ttu-id="fe2fc-130">Nazwa rekordu "@" oznacza zestaw rekordów w wierzchołku strefy.</span><span class="sxs-lookup"><span data-stu-id="fe2fc-130">The record name "@" indicates a record set at the zone apex.</span></span>

### <span data-ttu-id="fe2fc-131">Przykład 5. Dodawanie rekordu NS do zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="fe2fc-131">Example 5: Add an NS record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzDnsRecordSet -Name abc -RecordType NS -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Nsdname ns1.myzone.com | Set-AzDnsRecordSet
```

<span data-ttu-id="fe2fc-132">Ten przykład powoduje dodanie rekordu NS do istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="fe2fc-132">This example adds an NS record to an existing record set.</span></span>

### <span data-ttu-id="fe2fc-133">Przykład 6. Dodawanie rekordu PTR do zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="fe2fc-133">Example 6: Add a PTR record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name 4 -RecordType PTR -ResouceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="fe2fc-134">W tym przykładzie do istniejącego zestawu rekordów został dodano rekord PTR.</span><span class="sxs-lookup"><span data-stu-id="fe2fc-134">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="fe2fc-135">Przykład 7. Dodawanie rekordu SRV do zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="fe2fc-135">Example 7: Add an SRV record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name _sip._tcp -RecordType SRV -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

<span data-ttu-id="fe2fc-136">W tym przykładzie do istniejącego zestawu rekordów został dodano rekord SRV.</span><span class="sxs-lookup"><span data-stu-id="fe2fc-136">This example adds an SRV record to an existing record set.</span></span>

### <span data-ttu-id="fe2fc-137">Przykład 8. Dodawanie rekordu TXT do zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="fe2fc-137">Example 8: Add a TXT record to a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name text -RecordType TXT -ResouceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzDnsRecordConfig -Value "This is a TXT Record" | Set-AzDnsRecordSet
```

<span data-ttu-id="fe2fc-138">W tym przykładzie do istniejącego zestawu rekordów został dodano rekord TXT.</span><span class="sxs-lookup"><span data-stu-id="fe2fc-138">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="fe2fc-139">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe2fc-139">PARAMETERS</span></span>

### <span data-ttu-id="fe2fc-140">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="fe2fc-140">-CaaFlags</span></span>
<span data-ttu-id="fe2fc-141">Flagi dla rekordu CAA do dodania.</span><span class="sxs-lookup"><span data-stu-id="fe2fc-141">The flags for the CAA record to add.</span></span> <span data-ttu-id="fe2fc-142">Musi to być liczba z wartości od 0 do 255.</span><span class="sxs-lookup"><span data-stu-id="fe2fc-142">Must be a number between 0 and 255.</span></span>

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

### <span data-ttu-id="fe2fc-143">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="fe2fc-143">-CaaTag</span></span>
<span data-ttu-id="fe2fc-144">Pole tagu rekordu CAA do dodania.</span><span class="sxs-lookup"><span data-stu-id="fe2fc-144">The tag field of the CAA record to add.</span></span>

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

### <span data-ttu-id="fe2fc-145">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="fe2fc-145">-CaaValue</span></span>
<span data-ttu-id="fe2fc-146">Pole wartości rekordu CAA do dodania.</span><span class="sxs-lookup"><span data-stu-id="fe2fc-146">The value field for the CAA record to add.</span></span>

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

### <span data-ttu-id="fe2fc-147">- Cname</span><span class="sxs-lookup"><span data-stu-id="fe2fc-147">-Cname</span></span>
<span data-ttu-id="fe2fc-148">Określa nazwę domeny dla rekordu nazwa kanoniczna (CNAME).</span><span class="sxs-lookup"><span data-stu-id="fe2fc-148">Specifies the domain name for a canonical name (CNAME) record.</span></span>

```yaml
Type: System.String
Parameter Sets: CNAME
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe2fc-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe2fc-149">-DefaultProfile</span></span>
<span data-ttu-id="fe2fc-150">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="fe2fc-150">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe2fc-151">— Exchange</span><span class="sxs-lookup"><span data-stu-id="fe2fc-151">-Exchange</span></span>
<span data-ttu-id="fe2fc-152">Określa nazwę serwera wymiany poczty dla rekordu wymiany poczty (MX).</span><span class="sxs-lookup"><span data-stu-id="fe2fc-152">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

```yaml
Type: System.String
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe2fc-153">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="fe2fc-153">-Ipv4Address</span></span>
<span data-ttu-id="fe2fc-154">Określa adres IPv4 rekordu A.</span><span class="sxs-lookup"><span data-stu-id="fe2fc-154">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="fe2fc-155">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="fe2fc-155">-Ipv6Address</span></span>
<span data-ttu-id="fe2fc-156">Określa adres IPv6 dla rekordu AAAA.</span><span class="sxs-lookup"><span data-stu-id="fe2fc-156">Specifies an IPv6 address for an AAAA record.</span></span>

```yaml
Type: System.String
Parameter Sets: AAAA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe2fc-157">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="fe2fc-157">-Nsdname</span></span>
<span data-ttu-id="fe2fc-158">Określa nazwę serwera nazw dla rekordu serwera nazw.</span><span class="sxs-lookup"><span data-stu-id="fe2fc-158">Specifies the name server name for a name server (NS) record.</span></span>

```yaml
Type: System.String
Parameter Sets: NS
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe2fc-159">— Port</span><span class="sxs-lookup"><span data-stu-id="fe2fc-159">-Port</span></span>
<span data-ttu-id="fe2fc-160">Określa port rekordu usługi (SRV).</span><span class="sxs-lookup"><span data-stu-id="fe2fc-160">Specifies the port for a service (SRV) record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe2fc-161">—Preference (Preferencja)</span><span class="sxs-lookup"><span data-stu-id="fe2fc-161">-Preference</span></span>
<span data-ttu-id="fe2fc-162">Określa preferencje rekordu MX.</span><span class="sxs-lookup"><span data-stu-id="fe2fc-162">Specifies the preference for an MX record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe2fc-163">— Priority (Priorytet)</span><span class="sxs-lookup"><span data-stu-id="fe2fc-163">-Priority</span></span>
<span data-ttu-id="fe2fc-164">Określa priorytet rekordu SRV.</span><span class="sxs-lookup"><span data-stu-id="fe2fc-164">Specifies the priority for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe2fc-165">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="fe2fc-165">-Ptrdname</span></span>
<span data-ttu-id="fe2fc-166">Określa nazwę domeny docelowej rekordu zasobu wskaźnika (PTR).</span><span class="sxs-lookup"><span data-stu-id="fe2fc-166">Specifies the target domain name of a pointer resource (PTR) record.</span></span>

```yaml
Type: System.String
Parameter Sets: PTR
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe2fc-167">- RecordSet</span><span class="sxs-lookup"><span data-stu-id="fe2fc-167">-RecordSet</span></span>
<span data-ttu-id="fe2fc-168">Określa obiekt **RecordSet,** który ma być edytowany.</span><span class="sxs-lookup"><span data-stu-id="fe2fc-168">Specifies the **RecordSet** object to edit.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe2fc-169">— element docelowy</span><span class="sxs-lookup"><span data-stu-id="fe2fc-169">-Target</span></span>
<span data-ttu-id="fe2fc-170">Określa wartość docelową rekordu SRV.</span><span class="sxs-lookup"><span data-stu-id="fe2fc-170">Specifies the target for an SRV record.</span></span>

```yaml
Type: System.String
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe2fc-171">— Wartość</span><span class="sxs-lookup"><span data-stu-id="fe2fc-171">-Value</span></span>
<span data-ttu-id="fe2fc-172">Określa wartość rekordu TXT.</span><span class="sxs-lookup"><span data-stu-id="fe2fc-172">Specifies the value for a TXT record.</span></span>

```yaml
Type: System.String
Parameter Sets: TXT
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe2fc-173">— Waga</span><span class="sxs-lookup"><span data-stu-id="fe2fc-173">-Weight</span></span>
<span data-ttu-id="fe2fc-174">Określa wagę rekordu SRV.</span><span class="sxs-lookup"><span data-stu-id="fe2fc-174">Specifies the weight for an SRV record.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe2fc-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe2fc-175">CommonParameters</span></span>
<span data-ttu-id="fe2fc-176">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe2fc-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe2fc-177">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe2fc-177">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe2fc-178">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe2fc-178">INPUTS</span></span>

### <span data-ttu-id="fe2fc-179">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="fe2fc-179">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

### <span data-ttu-id="fe2fc-180">System.String</span><span class="sxs-lookup"><span data-stu-id="fe2fc-180">System.String</span></span>

### <span data-ttu-id="fe2fc-181">System.UInt16</span><span class="sxs-lookup"><span data-stu-id="fe2fc-181">System.UInt16</span></span>

### <span data-ttu-id="fe2fc-182">System.Byte</span><span class="sxs-lookup"><span data-stu-id="fe2fc-182">System.Byte</span></span>

## <span data-ttu-id="fe2fc-183">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe2fc-183">OUTPUTS</span></span>

### <span data-ttu-id="fe2fc-184">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="fe2fc-184">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="fe2fc-185">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fe2fc-185">NOTES</span></span>

## <span data-ttu-id="fe2fc-186">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fe2fc-186">RELATED LINKS</span></span>

[<span data-ttu-id="fe2fc-187">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="fe2fc-187">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="fe2fc-188">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="fe2fc-188">Remove-AzDnsRecordConfig</span></span>](./Remove-AzDnsRecordConfig.md)

[<span data-ttu-id="fe2fc-189">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="fe2fc-189">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
