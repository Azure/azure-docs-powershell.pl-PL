---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsZone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
ms.openlocfilehash: a5c4ae9492d64bc8c84439f747031d6facd88673
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872811"
---
# <span data-ttu-id="26bf1-101">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="26bf1-101">Set-AzPrivateDnsZone</span></span>

## <span data-ttu-id="26bf1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="26bf1-102">SYNOPSIS</span></span>
<span data-ttu-id="26bf1-103">Aktualizuje prywatną strefę DNS na podstawie grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="26bf1-103">Updates a Private DNS zone from a resource group.</span></span>

## <span data-ttu-id="26bf1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="26bf1-104">SYNTAX</span></span>

### <span data-ttu-id="26bf1-105">Pola (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="26bf1-105">Fields (Default)</span></span>
```
Set-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26bf1-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="26bf1-106">ResourceId</span></span>
```
Set-AzPrivateDnsZone -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26bf1-107">Stream</span><span class="sxs-lookup"><span data-stu-id="26bf1-107">Object</span></span>
```
Set-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Tag <Hashtable>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26bf1-108">Opis</span><span class="sxs-lookup"><span data-stu-id="26bf1-108">DESCRIPTION</span></span>
<span data-ttu-id="26bf1-109">Polecenie cmdlet **Set-AzPrivateDnsZone** umożliwia trwałe aktualizowanie strefy prywatnego (Domain Name System) z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="26bf1-109">The **Set-AzPrivateDnsZone** cmdlet permanently updates a private Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="26bf1-110">Obiekt **PrivateDnsZone** można przekazać przy użyciu parametru *PrivateZone* lub za pomocą operatora potoku lub można też określić *nazwę* i *ResourceGroupName* parametry.</span><span class="sxs-lookup"><span data-stu-id="26bf1-110">You can pass a **PrivateDnsZone** object using the *PrivateZone* parameter or by using the pipeline operator, or alternatively you can specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="26bf1-111">Za pomocą zmiennej Confirm i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="26bf1-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="26bf1-112">Podczas określania strefy za pomocą obiektu **PrivateDnsZone** (przekazywanego za pośrednictwem parametru rurociągu lub *strefy* ) strefa nie jest aktualizowana, jeśli została zmieniona w usłudze DNS Azure od momentu pobrania lokalnego obiektu **PrivateDnsZone** (tylko operacje bezpośrednio dotyczące liczby zasobów stref DNS jako zmian, operacje na zestawach rekordów w strefie nie są).</span><span class="sxs-lookup"><span data-stu-id="26bf1-112">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not updated if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="26bf1-113">Zapewnia to ochronę współbieżnych zmian stref.</span><span class="sxs-lookup"><span data-stu-id="26bf1-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="26bf1-114">Można to pominąć za pomocą parametru *overwrite* , co powoduje zaktualizowanie strefy bez względu na jednoczesne zmiany.</span><span class="sxs-lookup"><span data-stu-id="26bf1-114">This can be suppressed using the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="26bf1-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="26bf1-115">EXAMPLES</span></span>

### <span data-ttu-id="26bf1-116">Przykład 1: aktualizowanie strefy prywatnej</span><span class="sxs-lookup"><span data-stu-id="26bf1-116">Example 1: Updates a private zone</span></span>
```
PS C:\>Set-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup" -Tag @{tag1="value1";tag2="value2"}


This command updates the zone named myzone.com from the resource group named MyResourceGroup with the tags provided. Use Get-AzPrivateDnsZone to retrieve the updated zone. Updated zone would look something like this:

Name                          : myzone.com
ResourceId                    : "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/PrivateZones/myzone.com"
ResourceGroupName             : MyResourceGroup
Location                      : 
Etag                          : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                          : {tag1="value1";tag2="value2"}
NumberOfRecordSets            : 1
MaxNumberOfRecordSets         : 5000
```

## <span data-ttu-id="26bf1-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="26bf1-117">PARAMETERS</span></span>

### <span data-ttu-id="26bf1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26bf1-118">-DefaultProfile</span></span>
<span data-ttu-id="26bf1-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="26bf1-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26bf1-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="26bf1-120">-Name</span></span>
<span data-ttu-id="26bf1-121">Określa nazwę prywatnej strefy DNS, którą aktualizuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26bf1-121">Specifies the name of the Private DNS zone that this cmdlet updates.</span></span>
<span data-ttu-id="26bf1-122">Musisz również określić parametr *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="26bf1-122">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="26bf1-123">Możesz też określić prywatną strefę DNS za pomocą parametru *Zone* .</span><span class="sxs-lookup"><span data-stu-id="26bf1-123">Alternatively, you can specify the private DNS zone using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26bf1-124">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="26bf1-124">-Overwrite</span></span>
<span data-ttu-id="26bf1-125">Podczas określania strefy za pomocą obiektu **PrivateDnsZone** (przekazywanego za pośrednictwem parametru rurociągu lub *strefy* ) strefa nie jest aktualizowana, jeśli została zmieniona w usłudze DNS Azure od momentu pobrania lokalnego obiektu **dnsZone** (tylko operacje bezpośrednio dotyczące liczby zasobów stref DNS jako zmian, operacje na zestawach rekordów w strefie nie są).</span><span class="sxs-lookup"><span data-stu-id="26bf1-125">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not updated if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="26bf1-126">Zapewnia to ochronę współbieżnych zmian stref.</span><span class="sxs-lookup"><span data-stu-id="26bf1-126">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="26bf1-127">Można to pominąć za pomocą parametru *overwrite* , co powoduje zaktualizowanie strefy bez względu na jednoczesne zmiany.</span><span class="sxs-lookup"><span data-stu-id="26bf1-127">This can be suppressed using the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26bf1-128">-PrivateZone</span><span class="sxs-lookup"><span data-stu-id="26bf1-128">-PrivateZone</span></span>
<span data-ttu-id="26bf1-129">Obiekt strefy do ustawienia.</span><span class="sxs-lookup"><span data-stu-id="26bf1-129">The zone object to set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26bf1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26bf1-130">-ResourceGroupName</span></span>
<span data-ttu-id="26bf1-131">Określa nazwę grupy zasobów zawierającej strefę, która ma zostać zaktualizowana.</span><span class="sxs-lookup"><span data-stu-id="26bf1-131">Specifies the name of the resource group that contains the zone to be updated.</span></span>
<span data-ttu-id="26bf1-132">Należy również określić parametr *zonename* .</span><span class="sxs-lookup"><span data-stu-id="26bf1-132">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="26bf1-133">Możesz też określić prywatną strefę DNS za pomocą obiektu **dnsZone** , przekazaną przez potok lub parametr *Zone* .</span><span class="sxs-lookup"><span data-stu-id="26bf1-133">Alternatively, you can specify the private DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26bf1-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26bf1-134">-ResourceId</span></span>
<span data-ttu-id="26bf1-135">Identyfikator zasobu prywatnej strefy DNS.</span><span class="sxs-lookup"><span data-stu-id="26bf1-135">Private DNS Zone ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26bf1-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="26bf1-136">-Tag</span></span>
<span data-ttu-id="26bf1-137">Tabela skrótów reprezentująca znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="26bf1-137">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26bf1-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="26bf1-138">-Confirm</span></span>
<span data-ttu-id="26bf1-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26bf1-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26bf1-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26bf1-140">-WhatIf</span></span>
<span data-ttu-id="26bf1-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26bf1-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26bf1-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="26bf1-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26bf1-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26bf1-143">CommonParameters</span></span>
<span data-ttu-id="26bf1-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26bf1-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26bf1-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26bf1-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26bf1-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26bf1-146">INPUTS</span></span>

### <span data-ttu-id="26bf1-147">System. String</span><span class="sxs-lookup"><span data-stu-id="26bf1-147">System.String</span></span>

### <span data-ttu-id="26bf1-148">Microsoft. Azure. Commands. PrivateDns. models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="26bf1-148">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="26bf1-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="26bf1-149">OUTPUTS</span></span>

### <span data-ttu-id="26bf1-150">Microsoft. Azure. Commands. PrivateDns. models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="26bf1-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="26bf1-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="26bf1-151">NOTES</span></span>

## <span data-ttu-id="26bf1-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="26bf1-152">RELATED LINKS</span></span>

[<span data-ttu-id="26bf1-153">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="26bf1-153">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="26bf1-154">Nowe — AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="26bf1-154">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="26bf1-155">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="26bf1-155">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
