---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/Set-AzPrivateDnsZone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Set-AzPrivateDnsZone.md
ms.openlocfilehash: 06b8a8bd7027b95d7f51e186b0184707ffd296a8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341773"
---
# <span data-ttu-id="4927e-101">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="4927e-101">Set-AzPrivateDnsZone</span></span>

## <span data-ttu-id="4927e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4927e-102">SYNOPSIS</span></span>
<span data-ttu-id="4927e-103">Aktualizuje prywatną strefę DNS na podstawie grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4927e-103">Updates a Private DNS zone from a resource group.</span></span>

## <span data-ttu-id="4927e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4927e-104">SYNTAX</span></span>

### <span data-ttu-id="4927e-105">Pola (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="4927e-105">Fields (Default)</span></span>
```
Set-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4927e-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="4927e-106">ResourceId</span></span>
```
Set-AzPrivateDnsZone -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4927e-107">Stream</span><span class="sxs-lookup"><span data-stu-id="4927e-107">Object</span></span>
```
Set-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Tag <Hashtable>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4927e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="4927e-108">DESCRIPTION</span></span>
<span data-ttu-id="4927e-109">Polecenie cmdlet **Set-AzPrivateDnsZone** umożliwia trwałe aktualizowanie strefy prywatnego (Domain Name System) z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4927e-109">The **Set-AzPrivateDnsZone** cmdlet permanently updates a private Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="4927e-110">Obiekt **PrivateDnsZone** można przekazać przy użyciu parametru *PrivateZone* lub za pomocą operatora potoku lub można też określić *nazwę* i *ResourceGroupName* parametry.</span><span class="sxs-lookup"><span data-stu-id="4927e-110">You can pass a **PrivateDnsZone** object using the *PrivateZone* parameter or by using the pipeline operator, or alternatively you can specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="4927e-111">Za pomocą zmiennej Confirm i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4927e-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="4927e-112">Podczas określania strefy za pomocą obiektu **PrivateDnsZone** (przekazywanego za pośrednictwem parametru rurociągu lub *strefy* ) strefa nie jest aktualizowana, jeśli została zmieniona w usłudze DNS Azure od momentu pobrania lokalnego obiektu **PrivateDnsZone** (tylko operacje bezpośrednio dotyczące liczby zasobów stref DNS jako zmian, operacje na zestawach rekordów w strefie nie są).</span><span class="sxs-lookup"><span data-stu-id="4927e-112">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not updated if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="4927e-113">Zapewnia to ochronę współbieżnych zmian stref.</span><span class="sxs-lookup"><span data-stu-id="4927e-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="4927e-114">Można to pominąć za pomocą parametru *overwrite* , co powoduje zaktualizowanie strefy bez względu na jednoczesne zmiany.</span><span class="sxs-lookup"><span data-stu-id="4927e-114">This can be suppressed using the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="4927e-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4927e-115">EXAMPLES</span></span>

### <span data-ttu-id="4927e-116">Przykład 1: aktualizowanie strefy prywatnej</span><span class="sxs-lookup"><span data-stu-id="4927e-116">Example 1: Updates a private zone</span></span>
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

## <span data-ttu-id="4927e-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4927e-117">PARAMETERS</span></span>

### <span data-ttu-id="4927e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4927e-118">-DefaultProfile</span></span>
<span data-ttu-id="4927e-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="4927e-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4927e-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4927e-120">-Name</span></span>
<span data-ttu-id="4927e-121">Określa nazwę prywatnej strefy DNS, którą aktualizuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4927e-121">Specifies the name of the Private DNS zone that this cmdlet updates.</span></span>
<span data-ttu-id="4927e-122">Musisz również określić parametr *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="4927e-122">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="4927e-123">Możesz też określić prywatną strefę DNS za pomocą parametru *Zone* .</span><span class="sxs-lookup"><span data-stu-id="4927e-123">Alternatively, you can specify the private DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="4927e-124">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="4927e-124">-Overwrite</span></span>
<span data-ttu-id="4927e-125">Podczas określania strefy za pomocą obiektu **PrivateDnsZone** (przekazywanego za pośrednictwem parametru rurociągu lub *strefy* ) strefa nie jest aktualizowana, jeśli została zmieniona w usłudze DNS Azure od momentu pobrania lokalnego obiektu **dnsZone** (tylko operacje bezpośrednio dotyczące liczby zasobów stref DNS jako zmian, operacje na zestawach rekordów w strefie nie są).</span><span class="sxs-lookup"><span data-stu-id="4927e-125">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not updated if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="4927e-126">Zapewnia to ochronę współbieżnych zmian stref.</span><span class="sxs-lookup"><span data-stu-id="4927e-126">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="4927e-127">Można to pominąć za pomocą parametru *overwrite* , co powoduje zaktualizowanie strefy bez względu na jednoczesne zmiany.</span><span class="sxs-lookup"><span data-stu-id="4927e-127">This can be suppressed using the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="4927e-128">-PrivateZone</span><span class="sxs-lookup"><span data-stu-id="4927e-128">-PrivateZone</span></span>
<span data-ttu-id="4927e-129">Obiekt strefy do ustawienia.</span><span class="sxs-lookup"><span data-stu-id="4927e-129">The zone object to set.</span></span>

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

### <span data-ttu-id="4927e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4927e-130">-ResourceGroupName</span></span>
<span data-ttu-id="4927e-131">Określa nazwę grupy zasobów zawierającej strefę, która ma zostać zaktualizowana.</span><span class="sxs-lookup"><span data-stu-id="4927e-131">Specifies the name of the resource group that contains the zone to be updated.</span></span>
<span data-ttu-id="4927e-132">Należy również określić parametr *zonename* .</span><span class="sxs-lookup"><span data-stu-id="4927e-132">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="4927e-133">Możesz też określić prywatną strefę DNS za pomocą obiektu **dnsZone** , przekazaną przez potok lub parametr *Zone* .</span><span class="sxs-lookup"><span data-stu-id="4927e-133">Alternatively, you can specify the private DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="4927e-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4927e-134">-ResourceId</span></span>
<span data-ttu-id="4927e-135">Identyfikator zasobu prywatnej strefy DNS.</span><span class="sxs-lookup"><span data-stu-id="4927e-135">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="4927e-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="4927e-136">-Tag</span></span>
<span data-ttu-id="4927e-137">Tabela skrótów reprezentująca znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="4927e-137">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="4927e-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4927e-138">-Confirm</span></span>
<span data-ttu-id="4927e-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4927e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4927e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4927e-140">-WhatIf</span></span>
<span data-ttu-id="4927e-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4927e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4927e-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4927e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4927e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4927e-143">CommonParameters</span></span>
<span data-ttu-id="4927e-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4927e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4927e-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4927e-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4927e-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4927e-146">INPUTS</span></span>

### <span data-ttu-id="4927e-147">System. String</span><span class="sxs-lookup"><span data-stu-id="4927e-147">System.String</span></span>

### <span data-ttu-id="4927e-148">Microsoft. Azure. Commands. PrivateDns. models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="4927e-148">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="4927e-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4927e-149">OUTPUTS</span></span>

### <span data-ttu-id="4927e-150">Microsoft. Azure. Commands. PrivateDns. models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="4927e-150">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="4927e-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4927e-151">NOTES</span></span>

## <span data-ttu-id="4927e-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4927e-152">RELATED LINKS</span></span>

[<span data-ttu-id="4927e-153">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="4927e-153">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="4927e-154">Nowe — AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="4927e-154">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="4927e-155">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="4927e-155">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
