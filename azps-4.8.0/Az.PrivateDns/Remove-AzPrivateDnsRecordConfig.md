---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: 1e3362850880f02c648fb3318db226515fc95eef
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219990"
---
# <span data-ttu-id="f730b-101">Remove-AzPrivateDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="f730b-101">Remove-AzPrivateDnsRecordConfig</span></span>

## <span data-ttu-id="f730b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f730b-102">SYNOPSIS</span></span>
<span data-ttu-id="f730b-103">Usuwa prywatny rekord DNS z lokalnego obiektu zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="f730b-103">Removes a Private DNS record from a local record set object.</span></span>

## <span data-ttu-id="f730b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f730b-104">SYNTAX</span></span>

### <span data-ttu-id="f730b-105">A (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="f730b-105">A (Default)</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv4Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f730b-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="f730b-106">AAAA</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ipv6Address <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f730b-107">MX</span><span class="sxs-lookup"><span data-stu-id="f730b-107">MX</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Exchange <String> -Preference <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f730b-108">SYSTEMU</span><span class="sxs-lookup"><span data-stu-id="f730b-108">PTR</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Ptrdname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f730b-109">ROZSZERZENIEM</span><span class="sxs-lookup"><span data-stu-id="f730b-109">TXT</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Value <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f730b-110">SRV</span><span class="sxs-lookup"><span data-stu-id="f730b-110">SRV</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Priority <UInt16> -Target <String>
 -Port <UInt16> -Weight <UInt16> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f730b-111">REKORD</span><span class="sxs-lookup"><span data-stu-id="f730b-111">CNAME</span></span>
```
Remove-AzPrivateDnsRecordConfig -RecordSet <PSPrivateDnsRecordSet> -Cname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f730b-112">Opis</span><span class="sxs-lookup"><span data-stu-id="f730b-112">DESCRIPTION</span></span>
<span data-ttu-id="f730b-113">Polecenie cmdlet Remove-AzPrivateDnsRecordConfig powoduje usunięcie prywatnego rekordu DNS (Domain Name System) z zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="f730b-113">The Remove-AzPrivateDnsRecordConfig cmdlet removes a Private Domain Name System (DNS) record from a record set.</span></span> <span data-ttu-id="f730b-114">Obiekt RecordSet jest obiektem w trybie offline, a zmiany w nim nie zmieniają prywatnych odpowiedzi DNS, dopóki nie zostanie uruchomione polecenie cmdlet Set-AzPrivateDnsRecordSet w celu utrzymania zmiany w usłudze DNS Microsoft Azure Private.</span><span class="sxs-lookup"><span data-stu-id="f730b-114">The RecordSet object is an offline object, and changes to it do not change the Private DNS responses until after you run the Set-AzPrivateDnsRecordSet cmdlet to persist the change to the Microsoft Azure Private DNS service.</span></span> <span data-ttu-id="f730b-115">Aby usunąć rekord, wszystkie pola tego typu muszą odpowiadać dokładnie.</span><span class="sxs-lookup"><span data-stu-id="f730b-115">To remove a record, all the fields for that record type must match exactly.</span></span> <span data-ttu-id="f730b-116">Nie można dodawać ani usuwać rekordów SOA.</span><span class="sxs-lookup"><span data-stu-id="f730b-116">You cannot add or remove SOA records.</span></span> <span data-ttu-id="f730b-117">Rekordy SOA są tworzone automatycznie, gdy prywatna strefa DNS jest tworzona i automatycznie usuwana po usunięciu prywatnej strefy DNS.</span><span class="sxs-lookup"><span data-stu-id="f730b-117">SOA records are automatically created when a Private DNS zone is created and automatically deleted when the Private DNS zone is deleted.</span></span> <span data-ttu-id="f730b-118">Obiekt RecordSet można przekazać do tego polecenia cmdlet jako parametru lub za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="f730b-118">You can pass the RecordSet object to this cmdlet as a parameter or by using the pipeline operator.</span></span>

## <span data-ttu-id="f730b-119">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f730b-119">EXAMPLES</span></span>

### <span data-ttu-id="f730b-120">Przykład 1: Usuwanie rekordu z zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="f730b-120">Example 1: Remove an A record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 1.2.3.4
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Ipv4Address 1.2.3.4 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="f730b-121">W tym przykładzie usunięto rekord z istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="f730b-121">This example removes an A record from an existing record set.</span></span> <span data-ttu-id="f730b-122">Jeśli jest to jedyny rekord w zestawie rekordów, wynik będzie pustym zestawem rekordów.</span><span class="sxs-lookup"><span data-stu-id="f730b-122">If this is the only record in the record set, the result will be an empty record set.</span></span> <span data-ttu-id="f730b-123">Aby całkowicie usunąć zestaw rekordów, zobacz Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="f730b-123">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="f730b-124">Przykład 2: Usuwanie rekordu AAAA z zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="f730b-124">Example 2: Remove an AAAA record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Ipv6Address 2001:DB80:4009:1803::1005
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Ipv6Address 2001:DB80:4009:1803::1005 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="f730b-125">W tym przykładzie usunięto rekord AAAA z istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="f730b-125">This example removes an AAAA record from an existing record set.</span></span> <span data-ttu-id="f730b-126">Jeśli jest to jedyny rekord w zestawie rekordów, wynik będzie pustym zestawem rekordów.</span><span class="sxs-lookup"><span data-stu-id="f730b-126">If this is the only record in the record set, the result will be an empty record set.</span></span> <span data-ttu-id="f730b-127">Aby całkowicie usunąć zestaw rekordów, zobacz Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="f730b-127">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="f730b-128">Przykład 3: Usuwanie rekordu CNAME z zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="f730b-128">Example 3: Remove a CNAME record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Cname contoso.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Cname contoso.com | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/CNAME/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : CNAME
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="f730b-129">W tym przykładzie usunięto rekord CNAME z istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="f730b-129">This example removes a CNAME record from an existing record set.</span></span> <span data-ttu-id="f730b-130">Ponieważ zestaw rekordów CNAME może zawierać co najwyżej pojedynczy rekord, wynik jest pustym zestawem rekordów.</span><span class="sxs-lookup"><span data-stu-id="f730b-130">Because a CNAME record set can contain at most one record, the result is an empty record set.</span></span>

### <span data-ttu-id="f730b-131">Przykład 4: Usuwanie rekordu MX z zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="f730b-131">Example 4: Remove a MX record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "@" -RecordType MX -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "@" -RecordType MX -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Exchange mail.microsoft.com -Preference 5 | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/MX/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : MX
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="f730b-132">W tym przykładzie usunięto rekord MX z istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="f730b-132">This example removes an MX record from an existing record set.</span></span> <span data-ttu-id="f730b-133">Nazwa rekordu "@" wskazuje zestaw rekordów znajdujący się na wierzchołku strefy.</span><span class="sxs-lookup"><span data-stu-id="f730b-133">The record name "@" indicates a record set at the zone apex.</span></span> <span data-ttu-id="f730b-134">Jeśli jest to jedyny rekord w zestawie rekordów, wynik jest pustym zestawem rekordów.</span><span class="sxs-lookup"><span data-stu-id="f730b-134">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="f730b-135">Aby całkowicie usunąć zestaw rekordów, zobacz Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="f730b-135">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="f730b-136">Przykład 5: Usuwanie rekordu PTR z zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="f730b-136">Example 5: Remove a PTR record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -ZoneName 3.2.1.in-addr.arpa
PS C:\> Remove-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com -RecordSet $RecordSet
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -ZoneName "3.2.1.in-addr.arpa" | Remove-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/3.2.1.in-addr.arpa/PTR/4
Name              : 4
ZoneName          : 3.2.1.in-addr.arpa
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : PTR
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="f730b-137">W tym przykładzie usunięto rekord PTR z istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="f730b-137">This example removes a PTR record from an existing record set.</span></span> <span data-ttu-id="f730b-138">Jeśli jest to jedyny rekord w zestawie rekordów, wynik jest pustym zestawem rekordów.</span><span class="sxs-lookup"><span data-stu-id="f730b-138">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="f730b-139">Aby całkowicie usunąć zestaw rekordów, zobacz Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="f730b-139">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="f730b-140">Przykład 6: Usuwanie rekordu SRV z zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="f730b-140">Example 6: Remove a SRV record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Priority 0 -Weight 5 -Port 8080 -Target target.example.com
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target target.example.com  | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/SRV/_sip._tcp
Name              : _sip._tcp
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : SRV
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="f730b-141">W tym przykładzie usunięto rekord SRV z istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="f730b-141">This example removes an SRV record from an existing record set.</span></span> <span data-ttu-id="f730b-142">Jeśli jest to jedyny rekord w zestawie rekordów, wynik jest pustym zestawem rekordów.</span><span class="sxs-lookup"><span data-stu-id="f730b-142">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="f730b-143">Aby całkowicie usunąć zestaw rekordów, zobacz Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="f730b-143">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

### <span data-ttu-id="f730b-144">Przykład 7: Usuwanie rekordu TXT z zestawu rekordów</span><span class="sxs-lookup"><span data-stu-id="f730b-144">Example 7: Remove a TXT record from a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordConfig -RecordSet $RecordSet -Value "This is a TXT Record"
PS C:\> Set-AzPrivateDnsRecordSet -RecordSet $RecordSet

# The above sequence can also be piped:

PS C:\> Get-AzPrivateDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" | Remove-AzPrivateDnsRecordConfig -Value "This is a TXT Record"  | Set-AzPrivateDnsRecordSet

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/TXT/text
Name              : text
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : TXT
Records           : {}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="f730b-145">W tym przykładzie usunięto rekord TXT z istniejącego zestawu rekordów.</span><span class="sxs-lookup"><span data-stu-id="f730b-145">This example removes a TXT record from an existing record set.</span></span> <span data-ttu-id="f730b-146">Jeśli jest to jedyny rekord w zestawie rekordów, wynik jest pustym zestawem rekordów.</span><span class="sxs-lookup"><span data-stu-id="f730b-146">If this is the only record in the record set, the result is an empty record set.</span></span> <span data-ttu-id="f730b-147">Aby całkowicie usunąć zestaw rekordów, zobacz Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="f730b-147">To remove a record set entirely, see Remove-AzPrivateDnsRecordSet.</span></span>

## <span data-ttu-id="f730b-148">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f730b-148">PARAMETERS</span></span>

### <span data-ttu-id="f730b-149">-CNAME</span><span class="sxs-lookup"><span data-stu-id="f730b-149">-Cname</span></span>
<span data-ttu-id="f730b-150">Nazwa kanoniczna rekordu CNAME do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="f730b-150">The canonical name of the CNAME record to remove.</span></span>
<span data-ttu-id="f730b-151">Nie może być względem nazwy strefy.</span><span class="sxs-lookup"><span data-stu-id="f730b-151">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="f730b-152">Nie może mieć kropki kończącej się</span><span class="sxs-lookup"><span data-stu-id="f730b-152">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="f730b-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f730b-153">-DefaultProfile</span></span>
<span data-ttu-id="f730b-154">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f730b-154">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f730b-155">-Exchange</span><span class="sxs-lookup"><span data-stu-id="f730b-155">-Exchange</span></span>
<span data-ttu-id="f730b-156">Host programu Exchange mail rekordu MX do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="f730b-156">The mail exchange host of the MX record to remove.</span></span>
<span data-ttu-id="f730b-157">Nie może być względem nazwy strefy.</span><span class="sxs-lookup"><span data-stu-id="f730b-157">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="f730b-158">Nie może mieć kropki kończącej się</span><span class="sxs-lookup"><span data-stu-id="f730b-158">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="f730b-159">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="f730b-159">-Ipv4Address</span></span>
<span data-ttu-id="f730b-160">Adres IPv4 rekordu, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="f730b-160">The IPv4 address of the A record to remove.</span></span>

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

### <span data-ttu-id="f730b-161">-Adres_ipv6</span><span class="sxs-lookup"><span data-stu-id="f730b-161">-Ipv6Address</span></span>
<span data-ttu-id="f730b-162">Adres IPv6 rekordu AAAA do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="f730b-162">The IPv6 address of the AAAA record to remove.</span></span>

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

### <span data-ttu-id="f730b-163">-Port</span><span class="sxs-lookup"><span data-stu-id="f730b-163">-Port</span></span>
<span data-ttu-id="f730b-164">Numer portu rekordu SRV do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="f730b-164">The port number of the SRV record to remove.</span></span>

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

### <span data-ttu-id="f730b-165">-Preferencja</span><span class="sxs-lookup"><span data-stu-id="f730b-165">-Preference</span></span>
<span data-ttu-id="f730b-166">Wartość preferencji rekordu MX do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="f730b-166">The preference value of the MX record to remove.</span></span>

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

### <span data-ttu-id="f730b-167">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="f730b-167">-Priority</span></span>
<span data-ttu-id="f730b-168">Wartość priorytetu rekordu SRV do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="f730b-168">The priority value of the SRV record to remove.</span></span>

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

### <span data-ttu-id="f730b-169">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="f730b-169">-Ptrdname</span></span>
<span data-ttu-id="f730b-170">Host docelowy rekordu PTR do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="f730b-170">The target host of the PTR record to remove.</span></span>
<span data-ttu-id="f730b-171">Nie może być względem nazwy strefy.</span><span class="sxs-lookup"><span data-stu-id="f730b-171">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="f730b-172">Nie może mieć kropki kończącej się</span><span class="sxs-lookup"><span data-stu-id="f730b-172">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="f730b-173">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="f730b-173">-RecordSet</span></span>
<span data-ttu-id="f730b-174">Zestaw rekordów, z którego ma zostać usunięty rekord.</span><span class="sxs-lookup"><span data-stu-id="f730b-174">The record set from which to remove the record.</span></span>

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

### <span data-ttu-id="f730b-175">-Target</span><span class="sxs-lookup"><span data-stu-id="f730b-175">-Target</span></span>
<span data-ttu-id="f730b-176">Host docelowy rekordu SRV do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="f730b-176">The target host of the SRV record to remove.</span></span>
<span data-ttu-id="f730b-177">Nie może być względem nazwy strefy.</span><span class="sxs-lookup"><span data-stu-id="f730b-177">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="f730b-178">Nie może mieć kropki kończącej się</span><span class="sxs-lookup"><span data-stu-id="f730b-178">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="f730b-179">-Value</span><span class="sxs-lookup"><span data-stu-id="f730b-179">-Value</span></span>
<span data-ttu-id="f730b-180">Wartość tekstowa rekordu TXT do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="f730b-180">The text value of the TXT record to remove.</span></span>

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

### <span data-ttu-id="f730b-181">-Waga</span><span class="sxs-lookup"><span data-stu-id="f730b-181">-Weight</span></span>
<span data-ttu-id="f730b-182">Wartość wagi rekordu SRV do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="f730b-182">The weight value of the SRV record to remove.</span></span>

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

### <span data-ttu-id="f730b-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f730b-183">CommonParameters</span></span>
<span data-ttu-id="f730b-184">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f730b-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f730b-185">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f730b-185">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f730b-186">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f730b-186">INPUTS</span></span>

### <span data-ttu-id="f730b-187">Microsoft. Azure. Commands. PrivateDns. models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f730b-187">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="f730b-188">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f730b-188">OUTPUTS</span></span>

### <span data-ttu-id="f730b-189">Microsoft. Azure. Commands. PrivateDns. models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f730b-189">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="f730b-190">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f730b-190">NOTES</span></span>

## <span data-ttu-id="f730b-191">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f730b-191">RELATED LINKS</span></span>
