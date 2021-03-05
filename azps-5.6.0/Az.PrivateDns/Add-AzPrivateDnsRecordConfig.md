---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/powershell/module/az.privatedns/add-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Add-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Add-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: 63e42c7784fe34d726d6f9cb8db987db877c9248
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996052"
---
# <span data-ttu-id="385ee-101">Add-AzPrivateDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="385ee-101">Add-AzPrivateDnsRecordConfig</span></span>

## <span data-ttu-id="385ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="385ee-102">SYNOPSIS</span></span>
<span data-ttu-id="385ee-103">Dodaje prywatny rekord DNS do obiektu lokalnego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="385ee-103">Adds a Private DNS record to a local record set object.</span></span>

## <span data-ttu-id="385ee-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="385ee-104">SYNTAX</span></span>

### <span data-ttu-id="385ee-105">A (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="385ee-105">A (Default)</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="385ee-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="385ee-106">AAAA</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="385ee-107">MX</span><span class="sxs-lookup"><span data-stu-id="385ee-107">MX</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="385ee-108">PTR</span><span class="sxs-lookup"><span data-stu-id="385ee-108">PTR</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="385ee-109">TXT</span><span class="sxs-lookup"><span data-stu-id="385ee-109">TXT</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Value <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="385ee-110">SRV</span><span class="sxs-lookup"><span data-stu-id="385ee-110">SRV</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Priority <UInt16> -Target <String>
 -Port <UInt16> -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="385ee-111">CNAME</span><span class="sxs-lookup"><span data-stu-id="385ee-111">CNAME</span></span>
```
Add-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Cname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="385ee-112">OPIS</span><span class="sxs-lookup"><span data-stu-id="385ee-112">DESCRIPTION</span></span>
<span data-ttu-id="385ee-113">Polecenie Add-AzPrivateDnsRecordConfig cmdlet dodaje rekord DNS (Private Domain Name System) do obiektu RecordSet.</span><span class="sxs-lookup"><span data-stu-id="385ee-113">The Add-AzPrivateDnsRecordConfig cmdlet adds a Private Domain Name System (DNS) record to a RecordSet object.</span></span> <span data-ttu-id="385ee-114">Obiekt RecordSet jest obiektem w trybie offline i zmiany w nim nie zmieniają prywatnych odpowiedzi DNS do momentu uruchomienia polecenia cmdlet Set-AzPrivateDnsRecordSet w celu utrwalenia zmiany w prywatnej usłudze DNS platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="385ee-114">The RecordSet object is an offline object, and changes to it do not change the Private DNS responses until after you run the Set-AzPrivateDnsRecordSet cmdlet to persist the change to the Microsoft Azure Private DNS service.</span></span> <span data-ttu-id="385ee-115">Rekordy SOA są tworzone po utworzeniu prywatnej strefy DNS i usuwane po usunięciu prywatnej strefy DNS.</span><span class="sxs-lookup"><span data-stu-id="385ee-115">SOA records are created when a Private DNS zone is created, and are removed when the Private DNS zone is deleted.</span></span> <span data-ttu-id="385ee-116">Nie można dodawać ani usuwać rekordów SOA, ale można je edytować.</span><span class="sxs-lookup"><span data-stu-id="385ee-116">You cannot add or remove SOA records, but you can edit them.</span></span> <span data-ttu-id="385ee-117">Obiekt RecordSet można przekazać do tego polecenia cmdlet jako parametr lub za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="385ee-117">You can pass the RecordSet object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="385ee-118">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="385ee-118">EXAMPLES</span></span>

### <span data-ttu-id="385ee-119">Przykład 1. Dodawanie rekordu A do zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="385ee-119">Example 1: Add an A record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name www -RecordType A -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name www -RecordType A -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="385ee-120">W tym przykładzie do istniejącego zestawu rekordów został dodano rekord A.</span><span class="sxs-lookup"><span data-stu-id="385ee-120">This example adds an A record to an existing record set.</span></span>

### <span data-ttu-id="385ee-121">Przykład 2. Dodawanie rekordu AAAA do zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="385ee-121">Example 2: Add an AAAA record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name www -RecordType AAAAA -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name www -RecordType AAAAA -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:DB80:4009:1803::1005}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="385ee-122">Ten przykład powoduje dodanie rekordu AAAAA do istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="385ee-122">This example adds an AAAAA record to an existing record set.</span></span>

### <span data-ttu-id="385ee-123">Przykład 3. Dodawanie rekordu CNAME do zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="385ee-123">Example 3: Add a CNAME record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name www -RecordType CNAME -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name www -RecordType CNAME -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Cname contoso.com | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/CNAME/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : CNAME
Records           : {www.contoso.com}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="385ee-124">W tym przykładzie do istniejącego zestawu rekordów został dodano rekord CNAME.</span><span class="sxs-lookup"><span data-stu-id="385ee-124">This example adds a CNAME record to an existing record set.</span></span>

### <span data-ttu-id="385ee-125">Przykład 4. Dodawanie rekordu MX do zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="385ee-125">Example 4: Add a MX record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name @ -RecordType MX -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name "@" -RecordType MX -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/MX/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : MX
Records           : {[5,mail.microsoft.com]}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="385ee-126">Ten przykład powoduje dodanie rekordu MX do istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="385ee-126">This example adds a MX record to an existing record set.</span></span>

### <span data-ttu-id="385ee-127">Przykład 5. Dodawanie rekordu PTR do zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="385ee-127">Example 5: Add a PTR record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name 4 -RecordType PTR -ResourceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa
PS C:\> Add-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name 4 -RecordType PTR -ResourceGroupName MyResourceGroup -ZoneName 3.2.1.in-addr.arpa | Add-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/3.2.1.in-addr.arpa/PTR/4
Name              : 4
ZoneName          : 3.2.1.in-addr.arpa
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : PTR
Records           : {www.contoso.com}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="385ee-128">W tym przykładzie do istniejącego zestawu rekordów został dodano rekord PTR.</span><span class="sxs-lookup"><span data-stu-id="385ee-128">This example adds a PTR record to an existing record set.</span></span>

### <span data-ttu-id="385ee-129">Przykład 6. Dodawanie rekordu SRV do zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="385ee-129">Example 6: Add a SRV record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name _sip._tcp -RecordType SRV -ResourceGroupName MyResourceGroup-ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name _sip._tcp -RecordType SRV -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/SRV/_sip._tcp
Name              : _sip._tcp
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : SRV
Records           : {[0,5,8080,sipservice.contoso.com]}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="385ee-130">W tym przykładzie do istniejącego zestawu rekordów został dodano rekord SRV.</span><span class="sxs-lookup"><span data-stu-id="385ee-130">This example adds a SRV record to an existing record set.</span></span>

### <span data-ttu-id="385ee-131">Przykład 7. Dodawanie rekordu TXT do zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="385ee-131">Example 7: Add a TXT record to a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name text -RecordType TXT -ResourceGroupName MyResourceGroup -ZoneName myzone.com
PS C:\> Add-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# You can also pipe the above sequence:

PS C:\> Get-AzPrivateDnsRecordSet -Name text -RecordType TXT -ResourceGroupName MyResourceGroup -ZoneName myzone.com | Add-AzPrivateDnsRecordConfig -Value "This is a TXT Record" | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/TXT/text
Name              : text
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : TXT
Records           : {This is a TXT Record}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="385ee-132">W tym przykładzie do istniejącego zestawu rekordów został dodano rekord TXT.</span><span class="sxs-lookup"><span data-stu-id="385ee-132">This example adds a TXT record to an existing record set.</span></span>

## <span data-ttu-id="385ee-133">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="385ee-133">PARAMETERS</span></span>

### <span data-ttu-id="385ee-134">- Cname</span><span class="sxs-lookup"><span data-stu-id="385ee-134">-Cname</span></span>
<span data-ttu-id="385ee-135">Kanoniczna nazwa rekordu CNAME do dodania.</span><span class="sxs-lookup"><span data-stu-id="385ee-135">The canonical name for the CNAME record to add.</span></span>
<span data-ttu-id="385ee-136">Nie może być względna względem nazwy strefy.</span><span class="sxs-lookup"><span data-stu-id="385ee-136">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="385ee-137">Nie może zawierać kropki kończącej</span><span class="sxs-lookup"><span data-stu-id="385ee-137">Must not have a terminating dot</span></span>

```yaml
Type: System.String
Parameter Sets: CNAME
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="385ee-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="385ee-138">-DefaultProfile</span></span>
<span data-ttu-id="385ee-139">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="385ee-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="385ee-140">— Exchange</span><span class="sxs-lookup"><span data-stu-id="385ee-140">-Exchange</span></span>
<span data-ttu-id="385ee-141">Host wymiany poczty dla rekordu MX do dodania.</span><span class="sxs-lookup"><span data-stu-id="385ee-141">The mail exchange host for the MX record to add.</span></span>
<span data-ttu-id="385ee-142">Nie może być względna względem nazwy strefy.</span><span class="sxs-lookup"><span data-stu-id="385ee-142">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="385ee-143">Nie może zawierać kropki kończącej</span><span class="sxs-lookup"><span data-stu-id="385ee-143">Must not have a terminating dot</span></span>

```yaml
Type: System.String
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="385ee-144">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="385ee-144">-Ipv4Address</span></span>
<span data-ttu-id="385ee-145">Adres IPv4 rekordu A do dodania.</span><span class="sxs-lookup"><span data-stu-id="385ee-145">The IPv4 address for the A record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: A
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="385ee-146">-Ipv6Address</span><span class="sxs-lookup"><span data-stu-id="385ee-146">-Ipv6Address</span></span>
<span data-ttu-id="385ee-147">Adres IPv6 rekordu AAAA do dodania.</span><span class="sxs-lookup"><span data-stu-id="385ee-147">The IPv6 address for the AAAA record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: AAAA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="385ee-148">— Port</span><span class="sxs-lookup"><span data-stu-id="385ee-148">-Port</span></span>
<span data-ttu-id="385ee-149">Numer portu rekordu SRV do dodania.</span><span class="sxs-lookup"><span data-stu-id="385ee-149">The port number for the SRV record to add.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="385ee-150">—Preference (Preferencja)</span><span class="sxs-lookup"><span data-stu-id="385ee-150">-Preference</span></span>
<span data-ttu-id="385ee-151">Wartość preferencji dla rekordu MX do dodania.</span><span class="sxs-lookup"><span data-stu-id="385ee-151">The preference value for the MX record to add.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: MX
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="385ee-152">— Priority (Priorytet)</span><span class="sxs-lookup"><span data-stu-id="385ee-152">-Priority</span></span>
<span data-ttu-id="385ee-153">Rekord SRV o priorytecie, który należy dodać.</span><span class="sxs-lookup"><span data-stu-id="385ee-153">The priority value SRV record to add.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="385ee-154">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="385ee-154">-Ptrdname</span></span>
<span data-ttu-id="385ee-155">Host docelowy rekordu PTR do dodania.</span><span class="sxs-lookup"><span data-stu-id="385ee-155">The target host for the PTR record to add.</span></span>
<span data-ttu-id="385ee-156">Nie może być względna względem nazwy strefy.</span><span class="sxs-lookup"><span data-stu-id="385ee-156">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="385ee-157">Nie może zawierać kropki kończącej</span><span class="sxs-lookup"><span data-stu-id="385ee-157">Must not have a terminating dot</span></span>

```yaml
Type: System.String
Parameter Sets: PTR
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="385ee-158">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="385ee-158">-RecordSet</span></span>
<span data-ttu-id="385ee-159">Zestaw rekordów, w którym należy dodać rekord.</span><span class="sxs-lookup"><span data-stu-id="385ee-159">The record set in which to add the record.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="385ee-160">— element docelowy</span><span class="sxs-lookup"><span data-stu-id="385ee-160">-Target</span></span>
<span data-ttu-id="385ee-161">Host docelowy rekordu SRV do dodania.</span><span class="sxs-lookup"><span data-stu-id="385ee-161">The target host for the SRV record to add.</span></span>
<span data-ttu-id="385ee-162">Nie może być względna względem nazwy strefy.</span><span class="sxs-lookup"><span data-stu-id="385ee-162">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="385ee-163">Nie może zawierać kropki kończącej</span><span class="sxs-lookup"><span data-stu-id="385ee-163">Must not have a terminating dot</span></span>

```yaml
Type: System.String
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="385ee-164">— Wartość</span><span class="sxs-lookup"><span data-stu-id="385ee-164">-Value</span></span>
<span data-ttu-id="385ee-165">Wartość tekstowa rekordu TXT do dodania.</span><span class="sxs-lookup"><span data-stu-id="385ee-165">The text value for the TXT record to add.</span></span>

```yaml
Type: System.String
Parameter Sets: TXT
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="385ee-166">— Waga</span><span class="sxs-lookup"><span data-stu-id="385ee-166">-Weight</span></span>
<span data-ttu-id="385ee-167">Wartość wagi dla rekordu SRV do dodania.</span><span class="sxs-lookup"><span data-stu-id="385ee-167">The weight value for the SRV record to add.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: SRV
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="385ee-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="385ee-168">CommonParameters</span></span>
<span data-ttu-id="385ee-169">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="385ee-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="385ee-170">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="385ee-170">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="385ee-171">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="385ee-171">INPUTS</span></span>

### <span data-ttu-id="385ee-172">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="385ee-172">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="385ee-173">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="385ee-173">OUTPUTS</span></span>

### <span data-ttu-id="385ee-174">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="385ee-174">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="385ee-175">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="385ee-175">NOTES</span></span>

## <span data-ttu-id="385ee-176">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="385ee-176">RELATED LINKS</span></span>
