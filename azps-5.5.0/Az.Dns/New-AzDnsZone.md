---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
ms.openlocfilehash: dc110c8989951c6cf5a68e35fbc22c6545c84a1a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243682"
---
# <span data-ttu-id="03a45-101">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="03a45-101">New-AzDnsZone</span></span>

## <span data-ttu-id="03a45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03a45-102">SYNOPSIS</span></span>
<span data-ttu-id="03a45-103">Tworzy nową strefę DNS.</span><span class="sxs-lookup"><span data-stu-id="03a45-103">Creates a new DNS zone.</span></span>

## <span data-ttu-id="03a45-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="03a45-104">SYNTAX</span></span>

### <span data-ttu-id="03a45-105">Identyfikatory (domyślne)</span><span class="sxs-lookup"><span data-stu-id="03a45-105">Ids (Default)</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneId <String>]
 [-Tag <Hashtable>] [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03a45-106">Nazwy</span><span class="sxs-lookup"><span data-stu-id="03a45-106">Names</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneName <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03a45-107">Obiekty</span><span class="sxs-lookup"><span data-stu-id="03a45-107">Objects</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZone <DnsZone>]
 [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03a45-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="03a45-108">DESCRIPTION</span></span>
<span data-ttu-id="03a45-109">Polecenie **cmdlet New-AzDnsZone** tworzy nową strefę DNS (Domain Name System) w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="03a45-109">The **New-AzDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="03a45-110">Musisz określić unikatową nazwę strefy DNS dla *parametru Name* lub polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="03a45-110">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="03a45-111">Po utworzeniu strefy użyj polecenia cmdlet New-AzDnsRecordSet, aby utworzyć zestawy rekordów w strefie.</span><span class="sxs-lookup"><span data-stu-id="03a45-111">After the zone is created, use the New-AzDnsRecordSet cmdlet to create record sets in the zone.</span></span>
<span data-ttu-id="03a45-112">Za pomocą *parametru Confirm* i $ConfirmPreference programu Windows PowerShell możesz kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="03a45-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="03a45-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="03a45-113">EXAMPLES</span></span>

### <span data-ttu-id="03a45-114">Przykład 1. Tworzenie strefy DNS</span><span class="sxs-lookup"><span data-stu-id="03a45-114">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="03a45-115">To polecenie tworzy nową strefę DNS o nazwie myzone.com w określonej grupie zasobów, a następnie zapisuje ją w $Zone danych.</span><span class="sxs-lookup"><span data-stu-id="03a45-115">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="03a45-116">Przykład 2. Tworzenie prywatnej strefy DNS przez określenie identyfikatorów sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="03a45-116">Example 2: Create a Private DNS zone by specifying virtual network IDs</span></span>
```
PS C:\>$ResVirtualNetworkId = "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testresgroup/providers/Microsoft.Network/virtualNetworks/resvnet"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetworkId @($ResVirtualNetworkId)
```

<span data-ttu-id="03a45-117">To polecenie tworzy nową prywatną strefę DNS o nazwie myprivatezone.com w określonej grupie zasobów ze skojarzoną siecią wirtualną rozpoznawania (określającą jej identyfikator), a następnie przechowuje ją w $Zone sieci.</span><span class="sxs-lookup"><span data-stu-id="03a45-117">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (specifying its ID), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="03a45-118">Przykład 3. Tworzenie prywatnej strefy DNS przez określenie obiektów sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="03a45-118">Example 3: Create a Private DNS zone by specifying virtual network objects</span></span>
```
PS C:\>$ResVirtualNetwork = Get-AzVirtualNetwork -Name "resvnet" -ResourceGroupName "testresgroup"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetwork @($ResVirtualNetwork)
```

<span data-ttu-id="03a45-119">To polecenie tworzy nową prywatną strefę DNS o nazwie myprivatezone.com w określonej grupie zasobów ze skojarzoną siecią wirtualną rozpoznawania (określana przez zmienną $ResVirtualNetwork), a następnie zapisuje ją w $Zone sieciowej.</span><span class="sxs-lookup"><span data-stu-id="03a45-119">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (referred to by $ResVirtualNetwork variable), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="03a45-120">Przykład 4. Tworzenie strefy DNS z delegowaniem przez określenie nadrzędnej nazwy strefy</span><span class="sxs-lookup"><span data-stu-id="03a45-120">Example 4: Create a DNS zone with delegation by specifying parent zone name</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneName "zone.com"
```

<span data-ttu-id="03a45-121">To polecenie tworzy nową strefę DNS podrzędną o nazwie mychild.zone.com w określonej grupie zasobów i przechowuje w $Zone danych.</span><span class="sxs-lookup"><span data-stu-id="03a45-121">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="03a45-122">Powoduje również dodanie delegowania w nadrzędnej strefie DNS o nazwie zone.com w tej samej subskrypcji i w tej samej grupie zasobów, co strefa podrzędna.</span><span class="sxs-lookup"><span data-stu-id="03a45-122">It also adds delegation in the parent DNS zone named zone.com residing in the same subscription and resource group as child zone.</span></span>

### <span data-ttu-id="03a45-123">Przykład 5. Tworzenie strefy DNS z delegowaniem przez określenie nadrzędnego identyfikatora strefy</span><span class="sxs-lookup"><span data-stu-id="03a45-123">Example 5: Create a DNS zone with delegation by specifying parent zone id</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneId "/subscriptions/**67e2/resourceGroups/other-rg/providers/Microsoft.Network/dnszones/zone.com"
```

<span data-ttu-id="03a45-124">To polecenie tworzy nową strefę DNS podrzędną o nazwie mychild.zone.com w określonej grupie zasobów i przechowuje w $Zone danych.</span><span class="sxs-lookup"><span data-stu-id="03a45-124">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="03a45-125">Powoduje również dodanie delegowania w nadrzędnej strefie DNS o nazwie zone.com w grupie zasobów innej niż rg pod warunkiem, że subskrypcja jest taka sama jak utworzona strefa podrzędna.</span><span class="sxs-lookup"><span data-stu-id="03a45-125">It also adds delegation in the parent DNS zone named zone.com in resource group other-rg provided subscription is same as that of child zone created.</span></span>

### <span data-ttu-id="03a45-126">Przykład 6. Tworzenie strefy DNS z delegowaniem przez określenie nadrzędnego obiektu strefy</span><span class="sxs-lookup"><span data-stu-id="03a45-126">Example 6: Create a DNS zone with delegation by specifying parent zone object</span></span>
```
PS C:\>$PZone = New-AzDnsZone -Name "zone.com" -ResourceGroupName "MyResourceGroup" 
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZone @($PZone)
```

<span data-ttu-id="03a45-127">To polecenie tworzy nową strefę DNS podrzędną o nazwie mychild.zone.com w określonej grupie zasobów i przechowuje w $Zone danych.</span><span class="sxs-lookup"><span data-stu-id="03a45-127">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="03a45-128">Powoduje również dodanie delegowania w nadrzędnej strefie DNS zone.com przekazywanej w obiekcie ParentZone</span><span class="sxs-lookup"><span data-stu-id="03a45-128">It also adds delegation in the parent DNS zone named zone.com as passed in the ParentZone object</span></span>

## <span data-ttu-id="03a45-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03a45-129">PARAMETERS</span></span>

### <span data-ttu-id="03a45-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03a45-130">-DefaultProfile</span></span>
<span data-ttu-id="03a45-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="03a45-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="03a45-132">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="03a45-132">-Name</span></span>
<span data-ttu-id="03a45-133">Określa nazwę strefy DNS do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="03a45-133">Specifies the name of the DNS zone to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03a45-134">- ParentZone</span><span class="sxs-lookup"><span data-stu-id="03a45-134">-ParentZone</span></span>
<span data-ttu-id="03a45-135">Pełna nazwa strefy nadrzędnej w celu dodania delegowania (bez kropki kończącej).</span><span class="sxs-lookup"><span data-stu-id="03a45-135">The full name of the parent zone to add delegation (without a terminating dot).</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03a45-136">-ParentZoneId</span><span class="sxs-lookup"><span data-stu-id="03a45-136">-ParentZoneId</span></span>
<span data-ttu-id="03a45-137">Identyfikator zasobu strefy nadrzędnej w celu dodania delegowania (bez kropki kończącej).</span><span class="sxs-lookup"><span data-stu-id="03a45-137">The resource id of the parent zone to add delegation (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03a45-138">-ParentZoneName</span><span class="sxs-lookup"><span data-stu-id="03a45-138">-ParentZoneName</span></span>
<span data-ttu-id="03a45-139">Pełna nazwa strefy nadrzędnej w celu dodania delegowania (bez kropki kończącej).</span><span class="sxs-lookup"><span data-stu-id="03a45-139">The full name of the parent zone to add delegation (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Names
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03a45-140">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="03a45-140">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="03a45-141">Lista sieci wirtualnych, które będą rejestrować rekordy nazw hostów maszyn wirtualnych w tej strefie DNS, dostępna tylko dla stref prywatnych.</span><span class="sxs-lookup"><span data-stu-id="03a45-141">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03a45-142">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="03a45-142">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="03a45-143">Lista identyfikatorów sieci wirtualnej, które będą rejestrować rekordy nazw hostów maszyn wirtualnych w tej strefie DNS, dostępna tylko dla stref prywatnych.</span><span class="sxs-lookup"><span data-stu-id="03a45-143">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03a45-144">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="03a45-144">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="03a45-145">Lista sieci wirtualnych, które mogą rozwiązując rekordy w tej strefie DNS, dostępna tylko dla stref prywatnych.</span><span class="sxs-lookup"><span data-stu-id="03a45-145">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03a45-146">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="03a45-146">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="03a45-147">Lista identyfikatorów sieci wirtualnych, które mogą rozstrzygić rekordy w tej strefie DNS, dostępna tylko dla stref prywatnych.</span><span class="sxs-lookup"><span data-stu-id="03a45-147">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03a45-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03a45-148">-ResourceGroupName</span></span>
<span data-ttu-id="03a45-149">Określa grupę zasobów, w której ma być tworzyć strefę.</span><span class="sxs-lookup"><span data-stu-id="03a45-149">Specifies the resource group in which to create the zone.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03a45-150">— Tag</span><span class="sxs-lookup"><span data-stu-id="03a45-150">-Tag</span></span>
<span data-ttu-id="03a45-151">Pary klucz-wartość w postaci tabeli skrótu.</span><span class="sxs-lookup"><span data-stu-id="03a45-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="03a45-152">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="03a45-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03a45-153">-ZoneType</span><span class="sxs-lookup"><span data-stu-id="03a45-153">-ZoneType</span></span>
<span data-ttu-id="03a45-154">Typ strefy ( Publiczna lub Prywatna).</span><span class="sxs-lookup"><span data-stu-id="03a45-154">The type of the zone, Public or Private.</span></span> <span data-ttu-id="03a45-155">Strefy bez typu lub typu Public są udostępniane na publicznym samolocie usługi DNS do użycia w hierarchii DNS.</span><span class="sxs-lookup"><span data-stu-id="03a45-155">Zones without a type or with a type of Public are made available on the public DNS serving plane for use in the DNS hierarchy.</span></span> <span data-ttu-id="03a45-156">Strefy o typie Private są widoczne tylko w przypadku zestawu skojarzonych sieci wirtualnych (ta funkcja jest dostępna w wersji Preview).</span><span class="sxs-lookup"><span data-stu-id="03a45-156">Zones with a type of Private are only visible from with the set of associated virtual networks (this feature is in preview).</span></span> <span data-ttu-id="03a45-157">Tej właściwości nie można zmienić dla strefy.</span><span class="sxs-lookup"><span data-stu-id="03a45-157">This property cannot be changed for a zone.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Dns.Models.ZoneType]
Parameter Sets: (All)
Aliases:
Accepted values: Public, Private

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03a45-158">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="03a45-158">-Confirm</span></span>
<span data-ttu-id="03a45-159">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="03a45-159">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03a45-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03a45-160">-WhatIf</span></span>
<span data-ttu-id="03a45-161">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03a45-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="03a45-162">Polecenie cmdlet nie zostanie uruchomione. Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03a45-162">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="03a45-163">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="03a45-163">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03a45-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03a45-164">CommonParameters</span></span>
<span data-ttu-id="03a45-165">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03a45-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03a45-166">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03a45-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03a45-167">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03a45-167">INPUTS</span></span>

### <span data-ttu-id="03a45-168">System.String</span><span class="sxs-lookup"><span data-stu-id="03a45-168">System.String</span></span>

### <span data-ttu-id="03a45-169">System.Nullable'1[[Microsoft.Azure.Management.Dns.Models.ZoneType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="03a45-169">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.ZoneType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="03a45-170">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="03a45-170">System.Collections.Hashtable</span></span>

### <span data-ttu-id="03a45-171">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="03a45-171">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="03a45-172">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="03a45-172">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="03a45-173">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03a45-173">OUTPUTS</span></span>

### <span data-ttu-id="03a45-174">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="03a45-174">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="03a45-175">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="03a45-175">NOTES</span></span>
<span data-ttu-id="03a45-176">Za pomocą *parametru Confirm* można określić, czy to polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="03a45-176">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="03a45-177">Domyślnie polecenie cmdlet wyświetla monit o potwierdzenie, jeśli zmienna programu Windows PowerShell $ConfirmPreference wartość średnią lub niższą.</span><span class="sxs-lookup"><span data-stu-id="03a45-177">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="03a45-178">Jeśli określisz *potwierdź* *lub potwierdź:$True,* to polecenie cmdlet wyświetli monit o potwierdzenie przed jego rozpoczęciem.</span><span class="sxs-lookup"><span data-stu-id="03a45-178">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="03a45-179">Jeśli określisz *polecenie Potwierdź:$False,* polecenie cmdlet nie wyświetli monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="03a45-179">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="03a45-180">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03a45-180">RELATED LINKS</span></span>

[<span data-ttu-id="03a45-181">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="03a45-181">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="03a45-182">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="03a45-182">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="03a45-183">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="03a45-183">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)
