---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: D1A2326C-CD41-45A6-B37A-FC6176193B01
online version: https://docs.microsoft.com/powershell/module/az.dns/remove-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
ms.openlocfilehash: 07af143e1a1582670d15a15c356f673fef1f7590
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984782"
---
# <span data-ttu-id="ba585-101">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="ba585-101">Remove-AzDnsRecordConfig</span></span>

## <span data-ttu-id="ba585-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba585-102">SYNOPSIS</span></span>
<span data-ttu-id="ba585-103">Usuwa rekord DNS z obiektu lokalnego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="ba585-103">Removes a DNS record from a local record set object.</span></span>

## <span data-ttu-id="ba585-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ba585-104">SYNTAX</span></span>

### <span data-ttu-id="ba585-105">A</span><span class="sxs-lookup"><span data-stu-id="ba585-105">A</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba585-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="ba585-106">AAAA</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba585-107">NS</span><span class="sxs-lookup"><span data-stu-id="ba585-107">NS</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ba585-108">MX</span><span class="sxs-lookup"><span data-stu-id="ba585-108">MX</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba585-109">PTR</span><span class="sxs-lookup"><span data-stu-id="ba585-109">PTR</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba585-110">TXT</span><span class="sxs-lookup"><span data-stu-id="ba585-110">TXT</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ba585-111">SRV</span><span class="sxs-lookup"><span data-stu-id="ba585-111">SRV</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba585-112">CNAME</span><span class="sxs-lookup"><span data-stu-id="ba585-112">CNAME</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ba585-113">Caa</span><span class="sxs-lookup"><span data-stu-id="ba585-113">Caa</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba585-114">OPIS</span><span class="sxs-lookup"><span data-stu-id="ba585-114">DESCRIPTION</span></span>
<span data-ttu-id="ba585-115">Polecenie **cmdlet Remove-AzDnsRecordConfig** usuwa rekord DNS (Domain Name System) z zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="ba585-115">The **Remove-AzDnsRecordConfig** cmdlet removes a Domain Name System (DNS) record from a record set.</span></span>
<span data-ttu-id="ba585-116">Obiekt **RecordSet** jest obiektem offline i zmiany w nim nie zmieniają odpowiedzi DNS do momentu uruchomienia polecenia cmdlet Set-AzDnsRecordSet w celu utrwalenia zmiany w usłudze DNS platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ba585-116">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>
<span data-ttu-id="ba585-117">Aby można było usunąć rekord, wszystkie pola tego typu muszą być dokładnie zgodne.</span><span class="sxs-lookup"><span data-stu-id="ba585-117">To remove a record, all the fields for that record type must match exactly.</span></span>
<span data-ttu-id="ba585-118">Nie można dodawać ani usuwać rekordów SOA.</span><span class="sxs-lookup"><span data-stu-id="ba585-118">You cannot add or remove SOA records.</span></span>
<span data-ttu-id="ba585-119">Rekordy SOA są tworzone automatycznie po utworzeniu strefy DNS i automatyczne usunięciu jej po jej usunięciu.</span><span class="sxs-lookup"><span data-stu-id="ba585-119">SOA records are automatically created when a DNS zone is created and automatically deleted when the DNS zone is deleted.</span></span>
<span data-ttu-id="ba585-120">Obiekt **RecordSet** można przekazać do tego polecenia cmdlet jako parametr lub za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="ba585-120">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="ba585-121">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ba585-121">EXAMPLES</span></span>

### <span data-ttu-id="ba585-122">Przykład 1. Usuwanie rekordu A ze zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="ba585-122">Example 1: Remove an A record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

<span data-ttu-id="ba585-123">W tym przykładzie jest usuwany rekord A z istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="ba585-123">This example removes an A record from an existing record set.</span></span>
<span data-ttu-id="ba585-124">Jeśli jest to jedyny rekord w zestawie rekordów, wynikiem będzie pusty zestaw rekordów.</span><span class="sxs-lookup"><span data-stu-id="ba585-124">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="ba585-125">Aby całkowicie usunąć zestaw rekordów, zobacz Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="ba585-125">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="ba585-126">Przykład 2. Usuwanie rekordu AAAA ze zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="ba585-126">Example 2: Remove an AAAA record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

<span data-ttu-id="ba585-127">W tym przykładzie jest usuwany rekord AAAA z istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="ba585-127">This example removes an AAAA record from an existing record set.</span></span>
<span data-ttu-id="ba585-128">Jeśli jest to jedyny rekord w zestawie rekordów, wynikiem będzie pusty zestaw rekordów.</span><span class="sxs-lookup"><span data-stu-id="ba585-128">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="ba585-129">Aby całkowicie usunąć zestaw rekordów, zobacz Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="ba585-129">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="ba585-130">Przykład 3. Usuwanie rekordu CNAME z zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="ba585-130">Example 3: Remove a CNAME record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="ba585-131">W tym przykładzie jest usuwany rekord CNAME z istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="ba585-131">This example removes a CNAME record from an existing record set.</span></span>
<span data-ttu-id="ba585-132">Ponieważ zestaw rekordów CNAME może zawierać co najwyżej jeden rekord, wynikiem jest pusty zestaw rekordów.</span><span class="sxs-lookup"><span data-stu-id="ba585-132">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="ba585-133">Przykład 4. Usuwanie rekordu MX ze zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="ba585-133">Example 4: Remove an MX record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

<span data-ttu-id="ba585-134">W tym przykładzie jest usuwany rekord MX z istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="ba585-134">This example removes an MX record from an existing record set.</span></span>
<span data-ttu-id="ba585-135">Nazwa rekordu "@" oznacza zestaw rekordów w wierzchołku strefy.</span><span class="sxs-lookup"><span data-stu-id="ba585-135">The record name "@" indicates a record set at the zone apex.</span></span>
<span data-ttu-id="ba585-136">Jeśli jest to jedyny rekord w zestawie rekordów, wynikiem jest pusty zestaw rekordów.</span><span class="sxs-lookup"><span data-stu-id="ba585-136">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="ba585-137">Aby całkowicie usunąć zestaw rekordów, zobacz Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="ba585-137">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="ba585-138">Przykład 5. Usuwanie rekordu NS ze zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="ba585-138">Example 5: Remove an NS record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Nsdname "ns1.myzone.com" | Set-AzDnsRecordSet
```

<span data-ttu-id="ba585-139">W tym przykładzie jest usuwany rekord NS z istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="ba585-139">This example removes an NS record from an existing record set.</span></span>
<span data-ttu-id="ba585-140">Jeśli jest to jedyny rekord w zestawie rekordów, wynikiem jest pusty zestaw rekordów.</span><span class="sxs-lookup"><span data-stu-id="ba585-140">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="ba585-141">Aby całkowicie usunąć zestaw rekordów, zobacz Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="ba585-141">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="ba585-142">Przykład 6. Usuwanie rekordu PTR ze zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="ba585-142">Example 6: Remove a PTR record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="ba585-143">W tym przykładzie jest usuwany rekord PTR z istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="ba585-143">This example removes a PTR record from an existing record set.</span></span>
<span data-ttu-id="ba585-144">Jeśli jest to jedyny rekord w zestawie rekordów, wynikiem jest pusty zestaw rekordów.</span><span class="sxs-lookup"><span data-stu-id="ba585-144">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="ba585-145">Aby całkowicie usunąć zestaw rekordów, zobacz Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="ba585-145">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="ba585-146">Przykład 7. Usuwanie rekordu SRV ze zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="ba585-146">Example 7: Remove an SRV record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

<span data-ttu-id="ba585-147">W tym przykładzie jest usuwany rekord SRV z istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="ba585-147">This example removes an SRV record from an existing record set.</span></span>
<span data-ttu-id="ba585-148">Jeśli jest to jedyny rekord w zestawie rekordów, wynikiem jest pusty zestaw rekordów.</span><span class="sxs-lookup"><span data-stu-id="ba585-148">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="ba585-149">Aby całkowicie usunąć zestaw rekordów, zobacz Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="ba585-149">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="ba585-150">Przykład 8. Usuwanie rekordu TXT ze zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="ba585-150">Example 8: Remove a TXT record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Value "This is a TXT Record"  | Set-AzDnsRecordSet
```

<span data-ttu-id="ba585-151">W tym przykładzie jest usuwany rekord TXT z istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="ba585-151">This example removes a TXT record from an existing record set.</span></span>
<span data-ttu-id="ba585-152">Jeśli jest to jedyny rekord w zestawie rekordów, wynikiem jest pusty zestaw rekordów.</span><span class="sxs-lookup"><span data-stu-id="ba585-152">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="ba585-153">Aby całkowicie usunąć zestaw rekordów, zobacz Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="ba585-153">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

## <span data-ttu-id="ba585-154">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba585-154">PARAMETERS</span></span>

### <span data-ttu-id="ba585-155">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="ba585-155">-CaaFlags</span></span>
<span data-ttu-id="ba585-156">Flagi dla rekordu CAA do dodania.</span><span class="sxs-lookup"><span data-stu-id="ba585-156">The flags for the CAA record to add.</span></span> <span data-ttu-id="ba585-157">Musi to być liczba z wartości od 0 do 255.</span><span class="sxs-lookup"><span data-stu-id="ba585-157">Must be a number between 0 and 255.</span></span>

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

### <span data-ttu-id="ba585-158">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="ba585-158">-CaaTag</span></span>
<span data-ttu-id="ba585-159">Pole tagu rekordu CAA do dodania.</span><span class="sxs-lookup"><span data-stu-id="ba585-159">The tag field of the CAA record to add.</span></span>

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

### <span data-ttu-id="ba585-160">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="ba585-160">-CaaValue</span></span>
<span data-ttu-id="ba585-161">Pole wartości rekordu CAA do dodania.</span><span class="sxs-lookup"><span data-stu-id="ba585-161">The value field for the CAA record to add.</span></span>

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

### <span data-ttu-id="ba585-162">- Cname</span><span class="sxs-lookup"><span data-stu-id="ba585-162">-Cname</span></span>
<span data-ttu-id="ba585-163">Określa nazwę domeny dla rekordu nazwa kanoniczna (CNAME).</span><span class="sxs-lookup"><span data-stu-id="ba585-163">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="ba585-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba585-164">-DefaultProfile</span></span>
<span data-ttu-id="ba585-165">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="ba585-165">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba585-166">— Exchange</span><span class="sxs-lookup"><span data-stu-id="ba585-166">-Exchange</span></span>
<span data-ttu-id="ba585-167">Określa nazwę serwera wymiany poczty dla rekordu wymiany poczty (MX).</span><span class="sxs-lookup"><span data-stu-id="ba585-167">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="ba585-168">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="ba585-168">-Ipv4Address</span></span>
<span data-ttu-id="ba585-169">Określa adres IPv4 rekordu A.</span><span class="sxs-lookup"><span data-stu-id="ba585-169">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="ba585-170">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="ba585-170">-Ipv6Address</span></span>
<span data-ttu-id="ba585-171">Określa adres IPv6 rekordu AAAA.</span><span class="sxs-lookup"><span data-stu-id="ba585-171">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="ba585-172">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="ba585-172">-Nsdname</span></span>
<span data-ttu-id="ba585-173">Określa serwer nazw dla rekordu serwera nazw.</span><span class="sxs-lookup"><span data-stu-id="ba585-173">Specifies the name server for a name server (NS) record.</span></span>

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

### <span data-ttu-id="ba585-174">— Port</span><span class="sxs-lookup"><span data-stu-id="ba585-174">-Port</span></span>
<span data-ttu-id="ba585-175">Określa port rekordu usługi (SRV).</span><span class="sxs-lookup"><span data-stu-id="ba585-175">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="ba585-176">—Preference (Preferencja)</span><span class="sxs-lookup"><span data-stu-id="ba585-176">-Preference</span></span>
<span data-ttu-id="ba585-177">Określa preferencje rekordu MX.</span><span class="sxs-lookup"><span data-stu-id="ba585-177">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="ba585-178">— Priority (Priorytet)</span><span class="sxs-lookup"><span data-stu-id="ba585-178">-Priority</span></span>
<span data-ttu-id="ba585-179">Określa priorytet rekordu SRV.</span><span class="sxs-lookup"><span data-stu-id="ba585-179">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="ba585-180">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="ba585-180">-Ptrdname</span></span>
<span data-ttu-id="ba585-181">Określa nazwę domeny docelowej rekordu wskaźnika (PTR).</span><span class="sxs-lookup"><span data-stu-id="ba585-181">Specifies the target domain name of a pointer (PTR) record.</span></span>

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

### <span data-ttu-id="ba585-182">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="ba585-182">-RecordSet</span></span>
<span data-ttu-id="ba585-183">Określa obiekt **RecordSet** zawierający rekord do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="ba585-183">Specifies the **RecordSet** object that contains the record to remove.</span></span>

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

### <span data-ttu-id="ba585-184">— element docelowy</span><span class="sxs-lookup"><span data-stu-id="ba585-184">-Target</span></span>
<span data-ttu-id="ba585-185">Określa wartość docelową rekordu SRV.</span><span class="sxs-lookup"><span data-stu-id="ba585-185">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="ba585-186">— Wartość</span><span class="sxs-lookup"><span data-stu-id="ba585-186">-Value</span></span>
<span data-ttu-id="ba585-187">Określa wartość rekordu TXT.</span><span class="sxs-lookup"><span data-stu-id="ba585-187">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="ba585-188">— Waga</span><span class="sxs-lookup"><span data-stu-id="ba585-188">-Weight</span></span>
<span data-ttu-id="ba585-189">Określa wagę rekordu SRV.</span><span class="sxs-lookup"><span data-stu-id="ba585-189">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="ba585-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba585-190">CommonParameters</span></span>
<span data-ttu-id="ba585-191">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba585-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba585-192">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba585-192">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba585-193">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ba585-193">INPUTS</span></span>

### <span data-ttu-id="ba585-194">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ba585-194">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

### <span data-ttu-id="ba585-195">System.String</span><span class="sxs-lookup"><span data-stu-id="ba585-195">System.String</span></span>

### <span data-ttu-id="ba585-196">System.UInt16</span><span class="sxs-lookup"><span data-stu-id="ba585-196">System.UInt16</span></span>

### <span data-ttu-id="ba585-197">System.Byte</span><span class="sxs-lookup"><span data-stu-id="ba585-197">System.Byte</span></span>

## <span data-ttu-id="ba585-198">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ba585-198">OUTPUTS</span></span>

### <span data-ttu-id="ba585-199">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ba585-199">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="ba585-200">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ba585-200">NOTES</span></span>

## <span data-ttu-id="ba585-201">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ba585-201">RELATED LINKS</span></span>

[<span data-ttu-id="ba585-202">Add-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="ba585-202">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="ba585-203">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ba585-203">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="ba585-204">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="ba585-204">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
