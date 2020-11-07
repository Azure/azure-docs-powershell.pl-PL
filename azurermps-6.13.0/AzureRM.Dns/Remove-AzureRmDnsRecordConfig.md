---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: D1A2326C-CD41-45A6-B37A-FC6176193B01
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/remove-azurermdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsRecordConfig.md
ms.openlocfilehash: f4521b50d338d18eaa3c811ee64c5cff20dcf54a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546648"
---
# <span data-ttu-id="95fc3-101">Remove-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="95fc3-101">Remove-AzureRmDnsRecordConfig</span></span>

## <span data-ttu-id="95fc3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="95fc3-102">SYNOPSIS</span></span>
<span data-ttu-id="95fc3-103">Usuwa rekord DNS z lokalnego obiektu zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="95fc3-103">Removes a DNS record from a local record set object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95fc3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="95fc3-104">SYNTAX</span></span>

### <span data-ttu-id="95fc3-105">Sieci</span><span class="sxs-lookup"><span data-stu-id="95fc3-105">A</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95fc3-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="95fc3-106">AAAA</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95fc3-107">REKORDU</span><span class="sxs-lookup"><span data-stu-id="95fc3-107">NS</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Nsdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95fc3-108">MX</span><span class="sxs-lookup"><span data-stu-id="95fc3-108">MX</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95fc3-109">SYSTEMU</span><span class="sxs-lookup"><span data-stu-id="95fc3-109">PTR</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95fc3-110">ROZSZERZENIEM</span><span class="sxs-lookup"><span data-stu-id="95fc3-110">TXT</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Value <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95fc3-111">SRV</span><span class="sxs-lookup"><span data-stu-id="95fc3-111">SRV</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Priority <UInt16> -Target <String> -Port <UInt16>
 -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95fc3-112">REKORD</span><span class="sxs-lookup"><span data-stu-id="95fc3-112">CNAME</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -Cname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95fc3-113">Caa</span><span class="sxs-lookup"><span data-stu-id="95fc3-113">Caa</span></span>
```
Remove-AzureRmDnsRecordConfig -RecordSet <DnsRecordSet> -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95fc3-114">Opis</span><span class="sxs-lookup"><span data-stu-id="95fc3-114">DESCRIPTION</span></span>
<span data-ttu-id="95fc3-115">Polecenie cmdlet **Remove-AzureRmDnsRecordConfig** usuwa rekord DNS (Domain Name System) z zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="95fc3-115">The **Remove-AzureRmDnsRecordConfig** cmdlet removes a Domain Name System (DNS) record from a record set.</span></span>
<span data-ttu-id="95fc3-116">Obiekt **Recordset** jest obiektem w trybie offline, a wprowadzone w nim zmiany nie zmieniają odpowiedzi DNS, dopóki nie zostanie uruchomione polecenie cmdlet Set-AzureRmDnsRecordSet w celu utrzymania zmiany w usłudze DNS Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="95fc3-116">The **RecordSet** object is an offline object, and changes to it do not change the DNS responses until after you run the Set-AzureRmDnsRecordSet cmdlet to persist the change to the Microsoft Azure DNS service.</span></span>
<span data-ttu-id="95fc3-117">Aby usunąć rekord, wszystkie pola tego typu muszą odpowiadać dokładnie.</span><span class="sxs-lookup"><span data-stu-id="95fc3-117">To remove a record, all the fields for that record type must match exactly.</span></span>
<span data-ttu-id="95fc3-118">Nie można dodawać ani usuwać rekordów SOA.</span><span class="sxs-lookup"><span data-stu-id="95fc3-118">You cannot add or remove SOA records.</span></span>
<span data-ttu-id="95fc3-119">Rekordy SOA są tworzone automatycznie podczas tworzenia i automatycznego usuwania strefy DNS po usunięciu strefy DNS.</span><span class="sxs-lookup"><span data-stu-id="95fc3-119">SOA records are automatically created when a DNS zone is created and automatically deleted when the DNS zone is deleted.</span></span>
<span data-ttu-id="95fc3-120">Obiekt **Recordset** można przekazać do tego polecenia cmdlet jako parametru lub za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="95fc3-120">You can pass the **RecordSet** object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="95fc3-121">Przykłady</span><span class="sxs-lookup"><span data-stu-id="95fc3-121">EXAMPLES</span></span>

### <span data-ttu-id="95fc3-122">Przykład 1: Usuwanie rekordu z zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="95fc3-122">Example 1: Remove an A record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "www" -RecordType A -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="95fc3-123">W tym przykładzie usunięto rekord z istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="95fc3-123">This example removes an A record from an existing record set.</span></span>
<span data-ttu-id="95fc3-124">Jeśli jest to jedyny rekord w zestawie rekordów, wynik będzie pustym zestawem rekordów.</span><span class="sxs-lookup"><span data-stu-id="95fc3-124">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="95fc3-125">Aby całkowicie usunąć zestaw rekordów, zobacz Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="95fc3-125">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="95fc3-126">Przykład 2: Usuwanie rekordu AAAA z zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="95fc3-126">Example 2: Remove an AAAA record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="95fc3-127">W tym przykładzie usunięto rekord AAAA z istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="95fc3-127">This example removes an AAAA record from an existing record set.</span></span>
<span data-ttu-id="95fc3-128">Jeśli jest to jedyny rekord w zestawie rekordów, wynik będzie pustym zestawem rekordów.</span><span class="sxs-lookup"><span data-stu-id="95fc3-128">If this is the only record in the record set, the result will be an empty record set.</span></span>
<span data-ttu-id="95fc3-129">Aby całkowicie usunąć zestaw rekordów, zobacz Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="95fc3-129">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="95fc3-130">Przykład 3: Usuwanie rekordu CNAME z zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="95fc3-130">Example 3: Remove a CNAME record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Cname contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="95fc3-131">W tym przykładzie usunięto rekord CNAME z istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="95fc3-131">This example removes a CNAME record from an existing record set.</span></span>
<span data-ttu-id="95fc3-132">Ponieważ zestaw rekordów CNAME może zawierać co najwyżej pojedynczy rekord, wynik jest pustym zestawem rekordów.</span><span class="sxs-lookup"><span data-stu-id="95fc3-132">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="95fc3-133">Przykład 4: Usuwanie rekordu MX z zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="95fc3-133">Example 4: Remove an MX record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "@" -RecordType MX -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="95fc3-134">W tym przykładzie usunięto rekord MX z istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="95fc3-134">This example removes an MX record from an existing record set.</span></span>
<span data-ttu-id="95fc3-135">Nazwa rekordu "@" wskazuje zestaw rekordów znajdujący się na wierzchołku strefy.</span><span class="sxs-lookup"><span data-stu-id="95fc3-135">The record name "@" indicates a record set at the zone apex.</span></span>
<span data-ttu-id="95fc3-136">Jeśli jest to jedyny rekord w zestawie rekordów, wynik jest pustym zestawem rekordów.</span><span class="sxs-lookup"><span data-stu-id="95fc3-136">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="95fc3-137">Aby całkowicie usunąć zestaw rekordów, zobacz Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="95fc3-137">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="95fc3-138">Przykład 5: Usuwanie rekordu NS z zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="95fc3-138">Example 5: Remove an NS record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -Nsdname ns1.myzone.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "abc" -RecordType NS -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Nsdname "ns1.myzone.com" | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="95fc3-139">W tym przykładzie usunięto rekord NS z istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="95fc3-139">This example removes an NS record from an existing record set.</span></span>
<span data-ttu-id="95fc3-140">Jeśli jest to jedyny rekord w zestawie rekordów, wynik jest pustym zestawem rekordów.</span><span class="sxs-lookup"><span data-stu-id="95fc3-140">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="95fc3-141">Aby całkowicie usunąć zestaw rekordów, zobacz Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="95fc3-141">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="95fc3-142">Przykład 6: Usuwanie rekordu PTR z zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="95fc3-142">Example 6: Remove a PTR record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzureRmDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResouceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzureRmDnsRecordConfig -Ptrdname www.contoso.com | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="95fc3-143">W tym przykładzie usunięto rekord PTR z istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="95fc3-143">This example removes a PTR record from an existing record set.</span></span>
<span data-ttu-id="95fc3-144">Jeśli jest to jedyny rekord w zestawie rekordów, wynik jest pustym zestawem rekordów.</span><span class="sxs-lookup"><span data-stu-id="95fc3-144">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="95fc3-145">Aby całkowicie usunąć zestaw rekordów, zobacz Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="95fc3-145">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="95fc3-146">Przykład 7: Usuwanie rekordu SRV z zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="95fc3-146">Example 7: Remove an SRV record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="95fc3-147">W tym przykładzie usunięto rekord SRV z istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="95fc3-147">This example removes an SRV record from an existing record set.</span></span>
<span data-ttu-id="95fc3-148">Jeśli jest to jedyny rekord w zestawie rekordów, wynik jest pustym zestawem rekordów.</span><span class="sxs-lookup"><span data-stu-id="95fc3-148">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="95fc3-149">Aby całkowicie usunąć zestaw rekordów, zobacz Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="95fc3-149">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

### <span data-ttu-id="95fc3-150">Przykład 8: Usuwanie rekordu TXT z zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="95fc3-150">Example 8: Remove a TXT record from a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResouceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzureRmDnsRecordConfig -Value "This is a TXT Record"  | Set-AzureRmDnsRecordSet
```

<span data-ttu-id="95fc3-151">W tym przykładzie usunięto rekord TXT z istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="95fc3-151">This example removes a TXT record from an existing record set.</span></span>
<span data-ttu-id="95fc3-152">Jeśli jest to jedyny rekord w zestawie rekordów, wynik jest pustym zestawem rekordów.</span><span class="sxs-lookup"><span data-stu-id="95fc3-152">If this is the only record in the record set, the result is an empty record set.</span></span>
<span data-ttu-id="95fc3-153">Aby całkowicie usunąć zestaw rekordów, zobacz Remove-AzureRmDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="95fc3-153">To remove a record set entirely, see Remove-AzureRmDnsRecordSet.</span></span>

## <span data-ttu-id="95fc3-154">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="95fc3-154">PARAMETERS</span></span>

### <span data-ttu-id="95fc3-155">-CaaFlags</span><span class="sxs-lookup"><span data-stu-id="95fc3-155">-CaaFlags</span></span>
<span data-ttu-id="95fc3-156">Flagi rekordu CAA, które mają zostać dodane.</span><span class="sxs-lookup"><span data-stu-id="95fc3-156">The flags for the CAA record to add.</span></span> <span data-ttu-id="95fc3-157">Musi być liczbą z przedziału od 0 do 255.</span><span class="sxs-lookup"><span data-stu-id="95fc3-157">Must be a number between 0 and 255.</span></span>

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

### <span data-ttu-id="95fc3-158">-CaaTag</span><span class="sxs-lookup"><span data-stu-id="95fc3-158">-CaaTag</span></span>
<span data-ttu-id="95fc3-159">Pole tag w rekordzie CAA, które ma zostać dodane.</span><span class="sxs-lookup"><span data-stu-id="95fc3-159">The tag field of the CAA record to add.</span></span>

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

### <span data-ttu-id="95fc3-160">-CaaValue</span><span class="sxs-lookup"><span data-stu-id="95fc3-160">-CaaValue</span></span>
<span data-ttu-id="95fc3-161">Pole wartości dla rekordu CAA, który ma zostać dodany.</span><span class="sxs-lookup"><span data-stu-id="95fc3-161">The value field for the CAA record to add.</span></span>

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

### <span data-ttu-id="95fc3-162">-CNAME</span><span class="sxs-lookup"><span data-stu-id="95fc3-162">-Cname</span></span>
<span data-ttu-id="95fc3-163">Określa nazwę domeny dla rekordu kanonicznego (CNAME).</span><span class="sxs-lookup"><span data-stu-id="95fc3-163">Specifies the domain name for a canonical name (CNAME) record.</span></span>

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

### <span data-ttu-id="95fc3-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95fc3-164">-DefaultProfile</span></span>
<span data-ttu-id="95fc3-165">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="95fc3-165">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95fc3-166">-Exchange</span><span class="sxs-lookup"><span data-stu-id="95fc3-166">-Exchange</span></span>
<span data-ttu-id="95fc3-167">Określa nazwę serwera Exchange mail dla rekordu wymiany poczty (MX).</span><span class="sxs-lookup"><span data-stu-id="95fc3-167">Specifies the mail exchange server name for a mail exchange (MX) record.</span></span>

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

### <span data-ttu-id="95fc3-168">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="95fc3-168">-Ipv4Address</span></span>
<span data-ttu-id="95fc3-169">Określa adres IPv4 rekordu A.</span><span class="sxs-lookup"><span data-stu-id="95fc3-169">Specifies an IPv4 address for an A record.</span></span>

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

### <span data-ttu-id="95fc3-170">-Adres_ipv6</span><span class="sxs-lookup"><span data-stu-id="95fc3-170">-Ipv6Address</span></span>
<span data-ttu-id="95fc3-171">Określa adres IPv6 rekordu AAAA.</span><span class="sxs-lookup"><span data-stu-id="95fc3-171">Specifies an IPv6 address for an AAAA record.</span></span>

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

### <span data-ttu-id="95fc3-172">-Nsdname</span><span class="sxs-lookup"><span data-stu-id="95fc3-172">-Nsdname</span></span>
<span data-ttu-id="95fc3-173">Określa serwer nazw dla rekordu serwera nazw (NS).</span><span class="sxs-lookup"><span data-stu-id="95fc3-173">Specifies the name server for a name server (NS) record.</span></span>

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

### <span data-ttu-id="95fc3-174">-Port</span><span class="sxs-lookup"><span data-stu-id="95fc3-174">-Port</span></span>
<span data-ttu-id="95fc3-175">Określa port dla rekordu usługi (SRV).</span><span class="sxs-lookup"><span data-stu-id="95fc3-175">Specifies the port for a service (SRV) record.</span></span>

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

### <span data-ttu-id="95fc3-176">-Preferencja</span><span class="sxs-lookup"><span data-stu-id="95fc3-176">-Preference</span></span>
<span data-ttu-id="95fc3-177">Określa preferencję dla rekordu MX.</span><span class="sxs-lookup"><span data-stu-id="95fc3-177">Specifies the preference for an MX record.</span></span>

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

### <span data-ttu-id="95fc3-178">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="95fc3-178">-Priority</span></span>
<span data-ttu-id="95fc3-179">Określa priorytet rekordu SRV.</span><span class="sxs-lookup"><span data-stu-id="95fc3-179">Specifies the priority for an SRV record.</span></span>

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

### <span data-ttu-id="95fc3-180">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="95fc3-180">-Ptrdname</span></span>
<span data-ttu-id="95fc3-181">Określa nazwę domeny docelowej rekordu wskaźnika (PTR).</span><span class="sxs-lookup"><span data-stu-id="95fc3-181">Specifies the target domain name of a pointer (PTR) record.</span></span>

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

### <span data-ttu-id="95fc3-182">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="95fc3-182">-RecordSet</span></span>
<span data-ttu-id="95fc3-183">Określa obiekt **Recordset** , który zawiera rekord do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="95fc3-183">Specifies the **RecordSet** object that contains the record to remove.</span></span>

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

### <span data-ttu-id="95fc3-184">-Target</span><span class="sxs-lookup"><span data-stu-id="95fc3-184">-Target</span></span>
<span data-ttu-id="95fc3-185">Określa cel dla rekordu SRV.</span><span class="sxs-lookup"><span data-stu-id="95fc3-185">Specifies the target for an SRV record.</span></span>

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

### <span data-ttu-id="95fc3-186">-Value</span><span class="sxs-lookup"><span data-stu-id="95fc3-186">-Value</span></span>
<span data-ttu-id="95fc3-187">Określa wartość rekordu TXT.</span><span class="sxs-lookup"><span data-stu-id="95fc3-187">Specifies the value for a TXT record.</span></span>

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

### <span data-ttu-id="95fc3-188">-Waga</span><span class="sxs-lookup"><span data-stu-id="95fc3-188">-Weight</span></span>
<span data-ttu-id="95fc3-189">Określa wagę rekordu SRV.</span><span class="sxs-lookup"><span data-stu-id="95fc3-189">Specifies the weight for an SRV record.</span></span>

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

### <span data-ttu-id="95fc3-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95fc3-190">CommonParameters</span></span>
<span data-ttu-id="95fc3-191">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95fc3-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95fc3-192">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95fc3-192">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95fc3-193">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="95fc3-193">INPUTS</span></span>

### <span data-ttu-id="95fc3-194">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="95fc3-194">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="95fc3-195">Parametry: zestaw rekordów (ByValue)</span><span class="sxs-lookup"><span data-stu-id="95fc3-195">Parameters: RecordSet (ByValue)</span></span>

### <span data-ttu-id="95fc3-196">System. String</span><span class="sxs-lookup"><span data-stu-id="95fc3-196">System.String</span></span>

### <span data-ttu-id="95fc3-197">System. UInt16</span><span class="sxs-lookup"><span data-stu-id="95fc3-197">System.UInt16</span></span>

### <span data-ttu-id="95fc3-198">System. Byte</span><span class="sxs-lookup"><span data-stu-id="95fc3-198">System.Byte</span></span>

## <span data-ttu-id="95fc3-199">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="95fc3-199">OUTPUTS</span></span>

### <span data-ttu-id="95fc3-200">Microsoft. Azure. Commands. DNS. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="95fc3-200">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="95fc3-201">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="95fc3-201">NOTES</span></span>

## <span data-ttu-id="95fc3-202">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="95fc3-202">RELATED LINKS</span></span>

[<span data-ttu-id="95fc3-203">Dodaj-AzureRmDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="95fc3-203">Add-AzureRmDnsRecordConfig</span></span>](./Add-AzureRmDnsRecordConfig.md)

[<span data-ttu-id="95fc3-204">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="95fc3-204">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="95fc3-205">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="95fc3-205">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)