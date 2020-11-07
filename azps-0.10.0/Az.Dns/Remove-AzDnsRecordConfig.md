---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: D1A2326C-CD41-45A6-B37A-FC6176193B01
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Remove-AzDnsRecordConfig.md
ms.openlocfilehash: e00b31783554b8ea70760809c36f23a6a62575ca
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893162"
---
# <span data-ttu-id="5e183-101">Remove-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="5e183-101">Remove-AzDnsRecordConfig</span></span>

## <span data-ttu-id="5e183-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5e183-102">SYNOPSIS</span></span>
<span data-ttu-id="5e183-103">Usuwa rekord DNS z lokalnego obiektu zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="5e183-103">Removes a DNS record from a local record set object.</span></span>

## <span data-ttu-id="5e183-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5e183-104">SYNTAX</span></span>

### <span data-ttu-id="5e183-105">Sieci</span><span class="sxs-lookup"><span data-stu-id="5e183-105">A</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String> [<CommonParameters>]
```

### <span data-ttu-id="5e183-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="5e183-106">AAAA</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String> [<CommonParameters>]
```

### <span data-ttu-id="5e183-107">REKORDU</span><span class="sxs-lookup"><span data-stu-id="5e183-107">NS</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String> [<CommonParameters>]
```

### <span data-ttu-id="5e183-108">MX</span><span class="sxs-lookup"><span data-stu-id="5e183-108">MX</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [<CommonParameters>]
```

### <span data-ttu-id="5e183-109">SYSTEMU</span><span class="sxs-lookup"><span data-stu-id="5e183-109">PTR</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String> [<CommonParameters>]
```

### <span data-ttu-id="5e183-110">ROZSZERZENIEM</span><span class="sxs-lookup"><span data-stu-id="5e183-110">TXT</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String> [<CommonParameters>]
```

### <span data-ttu-id="5e183-111">SRV</span><span class="sxs-lookup"><span data-stu-id="5e183-111">SRV</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [<CommonParameters>]
```

### <span data-ttu-id="5e183-112">REKORD</span><span class="sxs-lookup"><span data-stu-id="5e183-112">CNAME</span></span>
```
Remove-AzDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String> [<CommonParameters>]
```

## <span data-ttu-id="5e183-113">Opis</span><span class="sxs-lookup"><span data-stu-id="5e183-113">DESCRIPTION</span></span>
<span data-ttu-id="5e183-114">Polecenie cmdlet **Remove-AzDnsRecordConfig** usuwa rekord DNS (Domain Name System) z zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="5e183-114">The **Remove-AzDnsRecordConfig** cmdlet removes a Domain Name System (DNS) record from a record set.</span></span>
<span data-ttu-id="5e183-115">Obiekt **Recordset** jest obiektem w trybie offline, a wprowadzone w nim zmiany nie zmieniają odpowiedzi DNS, dopóki nie zostanie uruchomione polecenie cmdlet Set-AzDnsRecordSet w celu utrzymania zmiany w usłudze DNS Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5e183-115">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>

<span data-ttu-id="5e183-116">Aby usunąć rekord, wszystkie pola tego typu muszą odpowiadać dokładnie.</span><span class="sxs-lookup"><span data-stu-id="5e183-116">To remove a record, all the fields for that record type must match exactly.</span></span>
<span data-ttu-id="5e183-117">Nie można dodawać ani usuwać rekordów SOA.</span><span class="sxs-lookup"><span data-stu-id="5e183-117">You cannot add or remove SOA records.</span></span>
<span data-ttu-id="5e183-118">Rekordy SOA są tworzone automatycznie podczas tworzenia i automatycznego usuwania strefy DNS po usunięciu strefy DNS.</span><span class="sxs-lookup"><span data-stu-id="5e183-118">SOA records are automatically created when a DNS zone is created and automatically deleted when the DNS zone is deleted.</span></span>

<span data-ttu-id="5e183-119">Obiekt **Recordset** można przekazać do tego polecenia cmdlet jako parametru lub za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="5e183-119">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="5e183-120">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5e183-120">EXAMPLES</span></span>

### <span data-ttu-id="5e183-121">Przykład 1: Usuwanie rekordu z zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="5e183-121">Example 1: Remove an A record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzDnsRecordSet
```

<span data-ttu-id="5e183-122">W tym przykładzie usunięto rekord z istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="5e183-122">This example removes an A record from an existing record set.</span></span>
<span data-ttu-id="5e183-123">Jeśli jest to jedyny rekord w zestawie rekordów, wynik będzie pustym zestawem rekordów.</span><span class="sxs-lookup"><span data-stu-id="5e183-123">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="5e183-124">Aby całkowicie usunąć zestaw rekordów, zobacz Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="5e183-124">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="5e183-125">Przykład 2: Usuwanie rekordu AAAA z zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="5e183-125">Example 2: Remove an AAAA record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzDnsRecordSet
```

<span data-ttu-id="5e183-126">W tym przykładzie usunięto rekord AAAA z istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="5e183-126">This example removes an AAAA record from an existing record set.</span></span>
<span data-ttu-id="5e183-127">Jeśli jest to jedyny rekord w zestawie rekordów, wynik będzie pustym zestawem rekordów.</span><span class="sxs-lookup"><span data-stu-id="5e183-127">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="5e183-128">Aby całkowicie usunąć zestaw rekordów, zobacz Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="5e183-128">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="5e183-129">Przykład 3: Usuwanie rekordu CNAME z zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="5e183-129">Example 3: Remove a CNAME record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Cname contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="5e183-130">W tym przykładzie usunięto rekord CNAME z istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="5e183-130">This example removes a CNAME record from an existing record set.</span></span>
<span data-ttu-id="5e183-131">Ponieważ zestaw rekordów CNAME może zawierać co najwyżej pojedynczy rekord, wynik jest pustym zestawem rekordów.</span><span class="sxs-lookup"><span data-stu-id="5e183-131">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="5e183-132">Przykład 4: Usuwanie rekordu MX z zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="5e183-132">Example 4: Remove an MX record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzDnsRecordSet
```

<span data-ttu-id="5e183-133">W tym przykładzie usunięto rekord MX z istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="5e183-133">This example removes an MX record from an existing record set.</span></span>
<span data-ttu-id="5e183-134">Nazwa rekordu "@" wskazuje zestaw rekordów znajdujący się na wierzchołku strefy.</span><span class="sxs-lookup"><span data-stu-id="5e183-134">The record name "@" indicates a record set at the zone apex.</span></span>
<span data-ttu-id="5e183-135">Jeśli jest to jedyny rekord w zestawie rekordów, wynik jest pustym zestawem rekordów.</span><span class="sxs-lookup"><span data-stu-id="5e183-135">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="5e183-136">Aby całkowicie usunąć zestaw rekordów, zobacz Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="5e183-136">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="5e183-137">Przykład 5: Usuwanie rekordu NS z zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="5e183-137">Example 5: Remove an NS record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Nsdname "ns1.myzone.com" | Set-AzDnsRecordSet
```

<span data-ttu-id="5e183-138">W tym przykładzie usunięto rekord NS z istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="5e183-138">This example removes an NS record from an existing record set.</span></span>
<span data-ttu-id="5e183-139">Jeśli jest to jedyny rekord w zestawie rekordów, wynik jest pustym zestawem rekordów.</span><span class="sxs-lookup"><span data-stu-id="5e183-139">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="5e183-140">Aby całkowicie usunąć zestaw rekordów, zobacz Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="5e183-140">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="5e183-141">Przykład 6: Usuwanie rekordu PTR z zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="5e183-141">Example 6: Remove a PTR record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzDnsRecordConfig -Ptrdname www.contoso.com | Set-AzDnsRecordSet
```

<span data-ttu-id="5e183-142">W tym przykładzie usunięto rekord PTR z istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="5e183-142">This example removes a PTR record from an existing record set.</span></span>
<span data-ttu-id="5e183-143">Jeśli jest to jedyny rekord w zestawie rekordów, wynik jest pustym zestawem rekordów.</span><span class="sxs-lookup"><span data-stu-id="5e183-143">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="5e183-144">Aby całkowicie usunąć zestaw rekordów, zobacz Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="5e183-144">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="5e183-145">Przykład 7: Usuwanie rekordu SRV z zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="5e183-145">Example 7: Remove an SRV record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzDnsRecordSet
```

<span data-ttu-id="5e183-146">W tym przykładzie usunięto rekord SRV z istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="5e183-146">This example removes an SRV record from an existing record set.</span></span>
<span data-ttu-id="5e183-147">Jeśli jest to jedyny rekord w zestawie rekordów, wynik jest pustym zestawem rekordów.</span><span class="sxs-lookup"><span data-stu-id="5e183-147">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="5e183-148">Aby całkowicie usunąć zestaw rekordów, zobacz Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="5e183-148">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

### <span data-ttu-id="5e183-149">Przykład 8: Usuwanie rekordu TXT z zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="5e183-149">Example 8: Remove a TXT record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzDnsRecordConfig -Value "This is a TXT Record"  | Set-AzDnsRecordSet
```

<span data-ttu-id="5e183-150">W tym przykładzie usunięto rekord TXT z istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="5e183-150">This example removes a TXT record from an existing record set.</span></span>
<span data-ttu-id="5e183-151">Jeśli jest to jedyny rekord w zestawie rekordów, wynik jest pustym zestawem rekordów.</span><span class="sxs-lookup"><span data-stu-id="5e183-151">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="5e183-152">Aby całkowicie usunąć zestaw rekordów, zobacz Remove-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="5e183-152">To remove a record set entirely, see Remove-AzDnsRecordSet.</span></span>

## <span data-ttu-id="5e183-153">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5e183-153">PARAMETERS</span></span>

### <span data-ttu-id="5e183-154">-CNAME</span><span class="sxs-lookup"><span data-stu-id="5e183-154">-Cname</span></span>
<span data-ttu-id="5e183-155">Określa nazwę domeny dla rekordu kanonicznego (CNAME).</span><span class="sxs-lookup"><span data-stu-id="5e183-155">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="5e183-156">-Exchange</span><span class="sxs-lookup"><span data-stu-id="5e183-156">-Exchange</span></span>
<span data-ttu-id="5e183-157">Określa nazwę serwera Exchange mail dla rekordu wymiany poczty (MX).</span><span class="sxs-lookup"><span data-stu-id="5e183-157">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="5e183-158">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="5e183-158">-Ipv4Address</span></span>
<span data-ttu-id="5e183-159">Określa adres IPv4 rekordu A.</span><span class="sxs-lookup"><span data-stu-id="5e183-159">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="5e183-160">-Adres_ipv6</span><span class="sxs-lookup"><span data-stu-id="5e183-160">-Ipv6Address</span></span>
<span data-ttu-id="5e183-161">Określa adres IPv6 rekordu AAAA.</span><span class="sxs-lookup"><span data-stu-id="5e183-161">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="5e183-162">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="5e183-162">-Nsdname</span></span>
<span data-ttu-id="5e183-163">Określa serwer nazw dla rekordu serwera nazw (NS).</span><span class="sxs-lookup"><span data-stu-id="5e183-163">Specifies the name server for a name server (NS) record.</span></span>

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

### <span data-ttu-id="5e183-164">-Port</span><span class="sxs-lookup"><span data-stu-id="5e183-164">-Port</span></span>
<span data-ttu-id="5e183-165">Określa port dla rekordu usługi (SRV).</span><span class="sxs-lookup"><span data-stu-id="5e183-165">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="5e183-166">-Preferencja</span><span class="sxs-lookup"><span data-stu-id="5e183-166">-Preference</span></span>
<span data-ttu-id="5e183-167">Określa preferencję dla rekordu MX.</span><span class="sxs-lookup"><span data-stu-id="5e183-167">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="5e183-168">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="5e183-168">-Priority</span></span>
<span data-ttu-id="5e183-169">Określa priorytet rekordu SRV.</span><span class="sxs-lookup"><span data-stu-id="5e183-169">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="5e183-170">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="5e183-170">-Ptrdname</span></span>
<span data-ttu-id="5e183-171">Określa nazwę domeny docelowej rekordu wskaźnika (PTR).</span><span class="sxs-lookup"><span data-stu-id="5e183-171">Specifies the target domain name of a pointer (PTR) record.</span></span>

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

### <span data-ttu-id="5e183-172">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="5e183-172">-RecordSet</span></span>
<span data-ttu-id="5e183-173">Określa obiekt **Recordset** , który zawiera rekord do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="5e183-173">Specifies the **RecordSet** object that contains the record to remove.</span></span>

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

### <span data-ttu-id="5e183-174">-Target</span><span class="sxs-lookup"><span data-stu-id="5e183-174">-Target</span></span>
<span data-ttu-id="5e183-175">Określa cel dla rekordu SRV.</span><span class="sxs-lookup"><span data-stu-id="5e183-175">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="5e183-176">-Value</span><span class="sxs-lookup"><span data-stu-id="5e183-176">-Value</span></span>
<span data-ttu-id="5e183-177">Określa wartość rekordu TXT.</span><span class="sxs-lookup"><span data-stu-id="5e183-177">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="5e183-178">-Waga</span><span class="sxs-lookup"><span data-stu-id="5e183-178">-Weight</span></span>
<span data-ttu-id="5e183-179">Określa wagę rekordu SRV.</span><span class="sxs-lookup"><span data-stu-id="5e183-179">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="5e183-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e183-180">CommonParameters</span></span>
<span data-ttu-id="5e183-181">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e183-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e183-182">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e183-182">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e183-183">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5e183-183">INPUTS</span></span>

### <span data-ttu-id="5e183-184">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="5e183-184">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="5e183-185">Do tego polecenia cmdlet można nawiązać obiekt **DnsRecordSet** .</span><span class="sxs-lookup"><span data-stu-id="5e183-185">You can pipe a **DnsRecordSet** object to this cmdlet.</span></span>
<span data-ttu-id="5e183-186">Jest to reprezentacja zestawu rekordów w trybie offline i aktualizacje nie zmieniają odpowiedzi DNS, dopóki nie zostanie uruchomiony tryb Set-AzDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="5e183-186">This is an offline representation of the record set and updates to it do not change DNS responses until after you run Set-AzDnsRecordSet.</span></span>

## <span data-ttu-id="5e183-187">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5e183-187">OUTPUTS</span></span>

### <span data-ttu-id="5e183-188">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="5e183-188">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="5e183-189">To polecenie cmdlet zwraca zmodyfikowany obiekt **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="5e183-189">This cmdlet returns the modified **RecordSet** object.</span></span>

## <span data-ttu-id="5e183-190">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5e183-190">NOTES</span></span>

## <span data-ttu-id="5e183-191">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5e183-191">RELATED LINKS</span></span>

[<span data-ttu-id="5e183-192">Dodaj-AzDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="5e183-192">Add-AzDnsRecordConfig</span></span>](./Add-AzDnsRecordConfig.md)

[<span data-ttu-id="5e183-193">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="5e183-193">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="5e183-194">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="5e183-194">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)
