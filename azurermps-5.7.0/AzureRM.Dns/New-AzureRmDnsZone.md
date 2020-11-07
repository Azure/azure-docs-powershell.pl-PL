---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/new-azurermdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsZone.md
ms.openlocfilehash: 28fabce7590644c230643822c206515957839127
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717117"
---
# <span data-ttu-id="e20f6-101">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="e20f6-101">New-AzureRmDnsZone</span></span>

## <span data-ttu-id="e20f6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e20f6-102">SYNOPSIS</span></span>
<span data-ttu-id="e20f6-103">Tworzy nową strefę DNS.</span><span class="sxs-lookup"><span data-stu-id="e20f6-103">Creates a new DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e20f6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e20f6-104">SYNTAX</span></span>

### <span data-ttu-id="e20f6-105">Identyfikatory (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="e20f6-105">Ids (Default)</span></span>
```
New-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e20f6-106">Obiekty</span><span class="sxs-lookup"><span data-stu-id="e20f6-106">Objects</span></span>
```
New-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e20f6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e20f6-107">DESCRIPTION</span></span>
<span data-ttu-id="e20f6-108">Polecenie cmdlet **New-AzureRmDnsZone** tworzy nową strefę DNS (Domain Name System) w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="e20f6-108">The **New-AzureRmDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="e20f6-109">Musisz określić unikatową nazwę strefy DNS dla parametru *name* lub polecenie cmdlet zwróci błąd.</span><span class="sxs-lookup"><span data-stu-id="e20f6-109">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="e20f6-110">Po utworzeniu strefy Użyj polecenia cmdlet New-AzureRmDnsRecordSet, aby utworzyć zestaw rekordów w strefie.</span><span class="sxs-lookup"><span data-stu-id="e20f6-110">After the zone is created, use the New-AzureRmDnsRecordSet cmdlet to create record sets in the zone.</span></span>

<span data-ttu-id="e20f6-111">Za pomocą zmiennej *Confirm* i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e20f6-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="e20f6-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e20f6-112">EXAMPLES</span></span>

### <span data-ttu-id="e20f6-113">Przykład 1: Tworzenie strefy DNS</span><span class="sxs-lookup"><span data-stu-id="e20f6-113">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="e20f6-114">To polecenie tworzy nową strefę DNS o nazwie myzone.com w określonej grupie zasobów, a następnie zapisuje ją w zmiennej $Zone.</span><span class="sxs-lookup"><span data-stu-id="e20f6-114">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="e20f6-115">Przykład 2: Tworzenie prywatnej strefy DNS przez określenie wirtualnych numerów sieciowych</span><span class="sxs-lookup"><span data-stu-id="e20f6-115">Example 2: Create a Private DNS zone by specifying virtual network IDs</span></span>
```
PS C:\>$ResVirtualNetworkId = "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testresgroup/providers/Microsoft.Network/virtualNetworks/resvnet"
PS C:\>$Zone = New-AzureRmDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetworkId @($ResVirtualNetworkId)
```

<span data-ttu-id="e20f6-116">To polecenie tworzy nową prywatną strefę DNS o nazwie myprivatezone.com w określonej grupie zasobów za pomocą skojarzonej sieci wirtualnej rozdzielczości (określając jej identyfikator), a następnie zapisuje ją w zmiennej $Zone.</span><span class="sxs-lookup"><span data-stu-id="e20f6-116">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (specifying its ID), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="e20f6-117">Przykład 3: Tworzenie prywatnej strefy DNS przez określenie obiektów sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="e20f6-117">Example 3: Create a Private DNS zone by specifying virtual network objects</span></span>
```
PS C:\>$ResVirtualNetwork = Get-AzureRmVirtualNetwork -Name "resvnet" -ResourceGroupName "testresgroup"
PS C:\>$Zone = New-AzureRmDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetwork @($ResVirtualNetwork)
```

<span data-ttu-id="e20f6-118">To polecenie tworzy nową prywatną strefę DNS o nazwie myprivatezone.com w określonej grupie zasobów ze skojarzoną siecią wirtualną rezolucji (określoną przez zmienną $ResVirtualNetwork), a następnie zapisuje ją w zmiennej $Zone.</span><span class="sxs-lookup"><span data-stu-id="e20f6-118">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (referred to by $ResVirtualNetwork variable), and then stores it in the $Zone variable.</span></span>

## <span data-ttu-id="e20f6-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e20f6-119">PARAMETERS</span></span>

### <span data-ttu-id="e20f6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e20f6-120">-DefaultProfile</span></span>
<span data-ttu-id="e20f6-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e20f6-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e20f6-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e20f6-122">-Name</span></span>
<span data-ttu-id="e20f6-123">Określa nazwę strefy DNS do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="e20f6-123">Specifies the name of the DNS zone to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e20f6-124">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e20f6-124">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="e20f6-125">Lista sieci wirtualnych, które rejestrują rekordy hosta maszyny wirtualnej w tej strefie DNS, są dostępne tylko dla stref prywatnych.</span><span class="sxs-lookup"><span data-stu-id="e20f6-125">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="e20f6-126">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="e20f6-126">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="e20f6-127">Lista identyfikatorów sieci wirtualnych, które będą rejestrowały rekordy hosta maszyny wirtualnej w tej strefie DNS, są dostępne tylko dla stref prywatnych.</span><span class="sxs-lookup"><span data-stu-id="e20f6-127">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="e20f6-128">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e20f6-128">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="e20f6-129">Lista sieci wirtualnych zdolnych do tłumaczenia rekordów w tej strefie DNS, które są dostępne tylko dla stref prywatnych.</span><span class="sxs-lookup"><span data-stu-id="e20f6-129">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="e20f6-130">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="e20f6-130">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="e20f6-131">Lista identyfikatorów sieci wirtualnych, które mogą rozpoznawać rekordy w tej strefie DNS, są dostępne tylko dla stref prywatnych.</span><span class="sxs-lookup"><span data-stu-id="e20f6-131">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="e20f6-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e20f6-132">-ResourceGroupName</span></span>
<span data-ttu-id="e20f6-133">Określa grupę zasobów, w której ma zostać utworzona strefa.</span><span class="sxs-lookup"><span data-stu-id="e20f6-133">Specifies the resource group in which to create the zone.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e20f6-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="e20f6-134">-Tag</span></span>
<span data-ttu-id="e20f6-135">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="e20f6-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e20f6-136">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="e20f6-136">For example:</span></span>

<span data-ttu-id="e20f6-137">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="e20f6-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e20f6-138">-Zonetype</span><span class="sxs-lookup"><span data-stu-id="e20f6-138">-ZoneType</span></span>
<span data-ttu-id="e20f6-139">Typ strefy publicznej lub prywatnej.</span><span class="sxs-lookup"><span data-stu-id="e20f6-139">The type of the zone, Public or Private.</span></span> <span data-ttu-id="e20f6-140">Strefy bez typu lub z typem publicznym są dostępne na publicznej płaszczyźnie obsługującej system DNS, aby można było ich używać w hierarchii DNS.</span><span class="sxs-lookup"><span data-stu-id="e20f6-140">Zones without a type or with a type of Public are made available on the public DNS serving plane for use in the DNS hierarchy.</span></span> <span data-ttu-id="e20f6-141">Strefy z typem prywatnym są widoczne tylko z zestawu skojarzonych sieci wirtualnych (Ta funkcja jest w wersji Preview).</span><span class="sxs-lookup"><span data-stu-id="e20f6-141">Zones with a type of Private are only visible from with the set of associated virtual networks (this feature is in preview).</span></span> <span data-ttu-id="e20f6-142">Tej właściwości nie można zmienić dla strefy.</span><span class="sxs-lookup"><span data-stu-id="e20f6-142">This property cannot be changed for a zone.</span></span>

```yaml
Type: ZoneType
Parameter Sets: (All)
Aliases:
Accepted values: Public, Private

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e20f6-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e20f6-143">-Confirm</span></span>
<span data-ttu-id="e20f6-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e20f6-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e20f6-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e20f6-145">-WhatIf</span></span>
<span data-ttu-id="e20f6-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e20f6-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e20f6-147">Polecenie cmdlet nie jest uruchamiane. Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e20f6-147">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e20f6-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e20f6-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e20f6-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e20f6-149">CommonParameters</span></span>
<span data-ttu-id="e20f6-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e20f6-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e20f6-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e20f6-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e20f6-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e20f6-152">INPUTS</span></span>

### <span data-ttu-id="e20f6-153">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e20f6-153">None</span></span>
<span data-ttu-id="e20f6-154">Nie możesz popotokować danych wejściowych tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e20f6-154">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="e20f6-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e20f6-155">OUTPUTS</span></span>

### <span data-ttu-id="e20f6-156">Microsoft. Azure. Commands. DNS. DnsZone</span><span class="sxs-lookup"><span data-stu-id="e20f6-156">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="e20f6-157">To polecenie cmdlet zwraca obiekt Microsoft. Azure. Commands. DNS. DnsZone reprezentujący nową strefę DNS.</span><span class="sxs-lookup"><span data-stu-id="e20f6-157">This cmdlet returns a Microsoft.Azure.Commands.Dns.DnsZone object that represents the new DNS zone.</span></span>

## <span data-ttu-id="e20f6-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e20f6-158">NOTES</span></span>
<span data-ttu-id="e20f6-159">Za pomocą parametru *Confirm* można kontrolować, czy to polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e20f6-159">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="e20f6-160">Domyślnie polecenie cmdlet monituje o potwierdzenie, jeśli zmienna $ConfirmPreference Windows PowerShell ma wartość średnią lub niższą.</span><span class="sxs-lookup"><span data-stu-id="e20f6-160">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="e20f6-161">Jeśli określisz pozycję *Potwierdź* lub *Potwierdź: $true* , to polecenie cmdlet wyświetli monit o potwierdzenie przed jego uruchomieniem.</span><span class="sxs-lookup"><span data-stu-id="e20f6-161">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="e20f6-162">Jeśli określisz pozycję *Confirm (Potwierdź): $false* , polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e20f6-162">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="e20f6-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e20f6-163">RELATED LINKS</span></span>

[<span data-ttu-id="e20f6-164">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="e20f6-164">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="e20f6-165">Nowe — AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="e20f6-165">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="e20f6-166">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="e20f6-166">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)
