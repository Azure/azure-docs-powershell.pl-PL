---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/new-azprivatednsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/New-AzPrivateDnsRecordConfig.md
ms.openlocfilehash: fc5686e22167613550b236bd234c649317ba8cca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708750"
---
# <span data-ttu-id="78c9a-101">New-AzPrivateDnsRecordConfig</span><span class="sxs-lookup"><span data-stu-id="78c9a-101">New-AzPrivateDnsRecordConfig</span></span>

## <span data-ttu-id="78c9a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="78c9a-102">SYNOPSIS</span></span>
<span data-ttu-id="78c9a-103">Tworzy nowy prywatny obiekt lokalny rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="78c9a-103">Creates a new Private DNS record local object.</span></span>

## <span data-ttu-id="78c9a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="78c9a-104">SYNTAX</span></span>

### <span data-ttu-id="78c9a-105">A (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="78c9a-105">A (Default)</span></span>
```
New-AzPrivateDnsRecordConfig -Ipv4Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="78c9a-106">AAAA</span><span class="sxs-lookup"><span data-stu-id="78c9a-106">AAAA</span></span>
```
New-AzPrivateDnsRecordConfig -Ipv6Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="78c9a-107">MX</span><span class="sxs-lookup"><span data-stu-id="78c9a-107">MX</span></span>
```
New-AzPrivateDnsRecordConfig -Exchange <String> -Preference <UInt16> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="78c9a-108">SYSTEMU</span><span class="sxs-lookup"><span data-stu-id="78c9a-108">PTR</span></span>
```
New-AzPrivateDnsRecordConfig -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78c9a-109">ROZSZERZENIEM</span><span class="sxs-lookup"><span data-stu-id="78c9a-109">TXT</span></span>
```
New-AzPrivateDnsRecordConfig -Value <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78c9a-110">SRV</span><span class="sxs-lookup"><span data-stu-id="78c9a-110">SRV</span></span>
```
New-AzPrivateDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78c9a-111">REKORD</span><span class="sxs-lookup"><span data-stu-id="78c9a-111">CNAME</span></span>
```
New-AzPrivateDnsRecordConfig -Cname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78c9a-112">Opis</span><span class="sxs-lookup"><span data-stu-id="78c9a-112">DESCRIPTION</span></span>
<span data-ttu-id="78c9a-113">Polecenie cmdlet New-AzPrivateDnsRecordConfig tworzy lokalny obiekt PSPrivateDnsRecord.</span><span class="sxs-lookup"><span data-stu-id="78c9a-113">The New-AzPrivateDnsRecordConfig cmdlet creates a local PSPrivateDnsRecord object.</span></span> <span data-ttu-id="78c9a-114">Tablica tych obiektów jest przekazywana do polecenia cmdlet New-AzPrivateDnsRecordSet za pomocą parametru PrivateDnsRecord w celu określenia rekordów, które mają zostać utworzone w zestawie rekordów.</span><span class="sxs-lookup"><span data-stu-id="78c9a-114">An array of these objects is passed to the New-AzPrivateDnsRecordSet cmdlet using the PrivateDnsRecord parameter to specify the records to create in the record set.</span></span>

## <span data-ttu-id="78c9a-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="78c9a-115">EXAMPLES</span></span>

### <span data-ttu-id="78c9a-116">Przykład 1. Tworzenie zestawu rekordów typu A</span><span class="sxs-lookup"><span data-stu-id="78c9a-116">Example 1: Create a RecordSet of type A</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords (New-AzPrivateDnsRecordConfig -IPv4Address 1.2.3.4)

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Netwo
                    rk/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4}
Metadata          :
IsAutoRegistered  :


# To create a record set containing multiple records, use New-AzPrivateDnsRecordConfig to add each record to the $Records array,
# then call New-AzPrivateDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzPrivateDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.Netwo
                    rk/privateDnsZones/myzone.com/A/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : A
Records           : {1.2.3.4, 5.6.7.8}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="78c9a-117">W tym przykładzie przedstawiono tworzenie zestawu rekordów o nazwie www w strefie prywatnej myzone.com.</span><span class="sxs-lookup"><span data-stu-id="78c9a-117">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="78c9a-118">Zestaw rekordów jest typu A i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="78c9a-118">The record set is of type A and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="78c9a-119">Zawiera jeden prywatny rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="78c9a-119">It contains a single Private DNS record.</span></span>

### <span data-ttu-id="78c9a-120">Przykład 2: Tworzenie zestawu rekordów typu AAAA</span><span class="sxs-lookup"><span data-stu-id="78c9a-120">Example 2: Create a RecordSet of type AAAA</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

Id                : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Micros
                    oft.Network/privateDnsZones/myzone.com/AAAA/www
Name              : www
ZoneName          : myzone.com
ResourceGroupName : MyResourceGroup
Ttl               : 3600
Etag              : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
RecordType        : AAAA
Records           : {2001:db8::1}
Metadata          :
IsAutoRegistered  :
```

<span data-ttu-id="78c9a-121">W tym przykładzie przedstawiono tworzenie zestawu rekordów o nazwie www w strefie prywatnej myzone.com.</span><span class="sxs-lookup"><span data-stu-id="78c9a-121">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="78c9a-122">Zestaw rekordów jest typu AAAA i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="78c9a-122">The record set is of type AAAA and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="78c9a-123">Zawiera jeden prywatny rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="78c9a-123">It contains a single Private DNS record.</span></span> <span data-ttu-id="78c9a-124">Aby utworzyć zestaw rekordów przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="78c9a-124">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="78c9a-125">Przykład 3: Tworzenie zestawu rekordów typu CNAME</span><span class="sxs-lookup"><span data-stu-id="78c9a-125">Example 3: Create a RecordSet of type CNAME</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

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

<span data-ttu-id="78c9a-126">W tym przykładzie przedstawiono tworzenie zestawu rekordów o nazwie www w strefie prywatnej myzone.com.</span><span class="sxs-lookup"><span data-stu-id="78c9a-126">This example creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="78c9a-127">Zestaw rekordów jest typu CNAME i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="78c9a-127">The record set is of type CNAME and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="78c9a-128">Zawiera jeden prywatny rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="78c9a-128">It contains a single Private DNS record.</span></span> <span data-ttu-id="78c9a-129">Aby utworzyć zestaw rekordów przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="78c9a-129">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="78c9a-130">Przykład 4: Tworzenie zestawu rekordów typu MX</span><span class="sxs-lookup"><span data-stu-id="78c9a-130">Example 4: Create a RecordSet of type MX</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

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

<span data-ttu-id="78c9a-131">To polecenie tworzy zestaw rekordów o nazwie www w strefie prywatnej myzone.com.</span><span class="sxs-lookup"><span data-stu-id="78c9a-131">This command creates a RecordSet named www in the private zone myzone.com.</span></span> <span data-ttu-id="78c9a-132">Zestaw rekordów jest typu MX i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="78c9a-132">The record set is of type MX and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="78c9a-133">Zawiera jeden prywatny rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="78c9a-133">It contains a single Private DNS record.</span></span> <span data-ttu-id="78c9a-134">Aby utworzyć zestaw rekordów przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="78c9a-134">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="78c9a-135">Przykład 5: Tworzenie zestawu rekordów typu PTR</span><span class="sxs-lookup"><span data-stu-id="78c9a-135">Example 5: Create a RecordSet of type PTR</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -PrivateDnsRecords $Records

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

<span data-ttu-id="78c9a-136">To polecenie tworzy zestaw rekordów o nazwie 4 w strefie prywatnej 3.2.1.in-addr. arpa.</span><span class="sxs-lookup"><span data-stu-id="78c9a-136">This command creates a RecordSet named 4 in the private zone 3.2.1.in-addr.arpa.</span></span> <span data-ttu-id="78c9a-137">Zestaw rekordów jest typu PTR i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="78c9a-137">The record set is of type PTR and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="78c9a-138">Zawiera jeden prywatny rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="78c9a-138">It contains a single Private DNS record.</span></span> <span data-ttu-id="78c9a-139">Aby utworzyć zestaw rekordów przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="78c9a-139">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="78c9a-140">Przykład 6: Tworzenie zestawu rekordów typu SRV</span><span class="sxs-lookup"><span data-stu-id="78c9a-140">Example 6: Create a RecordSet of type SRV</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

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

<span data-ttu-id="78c9a-141">To polecenie tworzy zestaw rekordów o nazwie _sip. _tcp w strefie prywatnej myzone.com.</span><span class="sxs-lookup"><span data-stu-id="78c9a-141">This command creates a RecordSet named _sip._tcp in the private zone myzone.com.</span></span> <span data-ttu-id="78c9a-142">Zestaw rekordów jest typu SRV i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="78c9a-142">The record set is of type SRV and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="78c9a-143">Zawiera pojedynczy prywatny rekord DNS, wskazujący adres IP 2001.2.3.4.</span><span class="sxs-lookup"><span data-stu-id="78c9a-143">It contains a single Private DNS record, pointing to the IP address 2001.2.3.4.</span></span> <span data-ttu-id="78c9a-144">Usługa (SIP) i protokół (TCP) są określone jako część nazwy zestawu rekordów, a nie jako część danych rekordu.</span><span class="sxs-lookup"><span data-stu-id="78c9a-144">The service (sip) and the protocol (tcp) are specified as part of the record set name, not as part of the record data.</span></span> <span data-ttu-id="78c9a-145">Aby utworzyć zestaw rekordów przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="78c9a-145">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

### <span data-ttu-id="78c9a-146">Przykład 7: Tworzenie zestawu rekordów typu TXT</span><span class="sxs-lookup"><span data-stu-id="78c9a-146">Example 7: Create a RecordSet of type TXT</span></span>
```powershell
PS C:\> $Records = @()
PS C:\> $Records += New-AzPrivateDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzPrivateDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -PrivateDnsRecords $Records

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

<span data-ttu-id="78c9a-147">To polecenie tworzy zestaw rekordów o nazwie tekst w strefie prywatnej myzone.com.</span><span class="sxs-lookup"><span data-stu-id="78c9a-147">This command creates a RecordSet named text in the private zone myzone.com.</span></span> <span data-ttu-id="78c9a-148">Zestaw rekordów jest typu TXT i ma wartość TTL równą 1 godzinie (3600 sekund).</span><span class="sxs-lookup"><span data-stu-id="78c9a-148">The record set is of type TXT and has a TTL of 1 hour (3600 seconds).</span></span> <span data-ttu-id="78c9a-149">Zawiera jeden prywatny rekord DNS.</span><span class="sxs-lookup"><span data-stu-id="78c9a-149">It contains a single Private DNS record.</span></span> <span data-ttu-id="78c9a-150">Aby utworzyć zestaw rekordów przy użyciu tylko jednego wiersza pn_PowerShell_short lub aby utworzyć zestaw rekordów z wieloma rekordami, zobacz przykład 1.</span><span class="sxs-lookup"><span data-stu-id="78c9a-150">To create a RecordSet using only one line of pn_PowerShell_short, or to create a record set with multiple records, see Example 1.</span></span>

## <span data-ttu-id="78c9a-151">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="78c9a-151">PARAMETERS</span></span>

### <span data-ttu-id="78c9a-152">-CNAME</span><span class="sxs-lookup"><span data-stu-id="78c9a-152">-Cname</span></span>
<span data-ttu-id="78c9a-153">Nazwa kanoniczna rekordu CNAME do dodania.</span><span class="sxs-lookup"><span data-stu-id="78c9a-153">The canonical name for the CNAME record to add.</span></span>
<span data-ttu-id="78c9a-154">Nie może być względem nazwy strefy.</span><span class="sxs-lookup"><span data-stu-id="78c9a-154">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="78c9a-155">Nie może mieć kropki kończącej się</span><span class="sxs-lookup"><span data-stu-id="78c9a-155">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="78c9a-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78c9a-156">-DefaultProfile</span></span>
<span data-ttu-id="78c9a-157">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="78c9a-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78c9a-158">-Exchange</span><span class="sxs-lookup"><span data-stu-id="78c9a-158">-Exchange</span></span>
<span data-ttu-id="78c9a-159">Host programu Exchange mail, który ma zostać dodany do rekordu MX.</span><span class="sxs-lookup"><span data-stu-id="78c9a-159">The mail exchange host for the MX record to add.</span></span>
<span data-ttu-id="78c9a-160">Nie może być względem nazwy strefy.</span><span class="sxs-lookup"><span data-stu-id="78c9a-160">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="78c9a-161">Nie może mieć kropki kończącej się</span><span class="sxs-lookup"><span data-stu-id="78c9a-161">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="78c9a-162">-Ipv4Address</span><span class="sxs-lookup"><span data-stu-id="78c9a-162">-Ipv4Address</span></span>
<span data-ttu-id="78c9a-163">Adres IPv4 rekordu, który ma zostać dodany.</span><span class="sxs-lookup"><span data-stu-id="78c9a-163">The IPv4 address for the A record to add.</span></span>

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

### <span data-ttu-id="78c9a-164">-Adres_ipv6</span><span class="sxs-lookup"><span data-stu-id="78c9a-164">-Ipv6Address</span></span>
<span data-ttu-id="78c9a-165">Adres IPv6 rekordu AAAA, który ma zostać dodany.</span><span class="sxs-lookup"><span data-stu-id="78c9a-165">The IPv6 address for the AAAA record to add.</span></span>

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

### <span data-ttu-id="78c9a-166">-Port</span><span class="sxs-lookup"><span data-stu-id="78c9a-166">-Port</span></span>
<span data-ttu-id="78c9a-167">Numer portu rekordu SRV do dodania.</span><span class="sxs-lookup"><span data-stu-id="78c9a-167">The port number for the SRV record to add.</span></span>

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

### <span data-ttu-id="78c9a-168">-Preferencja</span><span class="sxs-lookup"><span data-stu-id="78c9a-168">-Preference</span></span>
<span data-ttu-id="78c9a-169">Wartość preferencji dla rekordu MX do dodania.</span><span class="sxs-lookup"><span data-stu-id="78c9a-169">The preference value for the MX record to add.</span></span>

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

### <span data-ttu-id="78c9a-170">-Priority (priorytet)</span><span class="sxs-lookup"><span data-stu-id="78c9a-170">-Priority</span></span>
<span data-ttu-id="78c9a-171">Rekord SRV wartości priorytetu do dodania.</span><span class="sxs-lookup"><span data-stu-id="78c9a-171">The priority value SRV record to add.</span></span>

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

### <span data-ttu-id="78c9a-172">-Ptrdname</span><span class="sxs-lookup"><span data-stu-id="78c9a-172">-Ptrdname</span></span>
<span data-ttu-id="78c9a-173">Host docelowy rekordu PTR do dodania.</span><span class="sxs-lookup"><span data-stu-id="78c9a-173">The target host for the PTR record to add.</span></span>
<span data-ttu-id="78c9a-174">Nie może być względem nazwy strefy.</span><span class="sxs-lookup"><span data-stu-id="78c9a-174">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="78c9a-175">Nie może mieć kropki kończącej się</span><span class="sxs-lookup"><span data-stu-id="78c9a-175">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="78c9a-176">-Target</span><span class="sxs-lookup"><span data-stu-id="78c9a-176">-Target</span></span>
<span data-ttu-id="78c9a-177">Host docelowy rekordu SRV do dodania.</span><span class="sxs-lookup"><span data-stu-id="78c9a-177">The target host for the SRV record to add.</span></span>
<span data-ttu-id="78c9a-178">Nie może być względem nazwy strefy.</span><span class="sxs-lookup"><span data-stu-id="78c9a-178">Must not be relative to the name of the zone.</span></span>
<span data-ttu-id="78c9a-179">Nie może mieć kropki kończącej się</span><span class="sxs-lookup"><span data-stu-id="78c9a-179">Must not have a terminating dot</span></span>

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

### <span data-ttu-id="78c9a-180">-Value</span><span class="sxs-lookup"><span data-stu-id="78c9a-180">-Value</span></span>
<span data-ttu-id="78c9a-181">Wartość tekstowa rekordu TXT do dodania.</span><span class="sxs-lookup"><span data-stu-id="78c9a-181">The text value for the TXT record to add.</span></span>

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

### <span data-ttu-id="78c9a-182">-Waga</span><span class="sxs-lookup"><span data-stu-id="78c9a-182">-Weight</span></span>
<span data-ttu-id="78c9a-183">Wartość wagi rekordu SRV do dodania.</span><span class="sxs-lookup"><span data-stu-id="78c9a-183">The weight value for the SRV record to add.</span></span>

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

### <span data-ttu-id="78c9a-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78c9a-184">CommonParameters</span></span>
<span data-ttu-id="78c9a-185">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78c9a-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78c9a-186">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78c9a-186">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78c9a-187">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78c9a-187">INPUTS</span></span>

### <span data-ttu-id="78c9a-188">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="78c9a-188">None</span></span>

## <span data-ttu-id="78c9a-189">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="78c9a-189">OUTPUTS</span></span>

### <span data-ttu-id="78c9a-190">Microsoft. Azure. Commands. PrivateDns. models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="78c9a-190">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

## <span data-ttu-id="78c9a-191">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="78c9a-191">NOTES</span></span>

## <span data-ttu-id="78c9a-192">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="78c9a-192">RELATED LINKS</span></span>