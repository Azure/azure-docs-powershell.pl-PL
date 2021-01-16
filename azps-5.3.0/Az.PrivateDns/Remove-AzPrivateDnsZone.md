---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
ms.openlocfilehash: d381af8de23b5eb781882f10670e6ba69afbc571
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490834"
---
# <span data-ttu-id="68016-101">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="68016-101">Remove-AzPrivateDnsZone</span></span>

## <span data-ttu-id="68016-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="68016-102">SYNOPSIS</span></span>
<span data-ttu-id="68016-103">Usuwa prywatną strefę DNS z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="68016-103">Removes a private DNS zone from a resource group.</span></span>

## <span data-ttu-id="68016-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="68016-104">SYNTAX</span></span>

### <span data-ttu-id="68016-105">Pola (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="68016-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68016-106">Stream</span><span class="sxs-lookup"><span data-stu-id="68016-106">Object</span></span>
```
Remove-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68016-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="68016-107">ResourceId</span></span>
```
Remove-AzPrivateDnsZone -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68016-108">Opis</span><span class="sxs-lookup"><span data-stu-id="68016-108">DESCRIPTION</span></span>
<span data-ttu-id="68016-109">Polecenie cmdlet **Remove-AzPrivateDnsZone** trwale usuwa prywatną strefę DNS (Domain Name System) z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="68016-109">The **Remove-AzPrivateDnsZone** cmdlet permanently deletes a private Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="68016-110">Wszystkie zestawy rekordów zawarte w tej strefie również zostaną usunięte.</span><span class="sxs-lookup"><span data-stu-id="68016-110">All record sets contained in the zone are also deleted.</span></span>
<span data-ttu-id="68016-111">Obiekt **PrivateDnsZone** można przekazać przy użyciu parametru *PrivateZone* lub za pomocą operatora potoku lub można też określić *nazwę* i *ResourceGroupName* parametry.</span><span class="sxs-lookup"><span data-stu-id="68016-111">You can pass a **PrivateDnsZone** object using the *PrivateZone* parameter or by using the pipeline operator, or alternatively you can specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="68016-112">Za pomocą zmiennej Confirm i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="68016-112">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="68016-113">Podczas określania strefy za pomocą obiektu **PrivateDnsZone** (przekazywanego za pośrednictwem parametru rurociągu lub *strefy* ) strefa nie jest usuwana, jeśli została zmieniona w usłudze DNS Azure od momentu pobrania lokalnego obiektu **PrivateDnsZone** (tylko operacje bezpośrednio dotyczące liczby zasobów stref DNS jako zmian, operacje na zestawach rekordów w strefie nie są).</span><span class="sxs-lookup"><span data-stu-id="68016-113">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="68016-114">Zapewnia to ochronę współbieżnych zmian stref.</span><span class="sxs-lookup"><span data-stu-id="68016-114">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="68016-115">Można to pominąć przy użyciu parametru *overwrite* , który usuwa strefę bez względu na współbieżne zmiany.</span><span class="sxs-lookup"><span data-stu-id="68016-115">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="68016-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="68016-116">EXAMPLES</span></span>

### <span data-ttu-id="68016-117">Przykład 1. Usuń strefę prywatną</span><span class="sxs-lookup"><span data-stu-id="68016-117">Example 1: Remove a private zone</span></span>
```
PS C:\>Remove-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="68016-118">To polecenie usuwa strefę o nazwie myzone.com z grupy zasobów o nazwie Moja zasobów.</span><span class="sxs-lookup"><span data-stu-id="68016-118">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="68016-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="68016-119">PARAMETERS</span></span>

### <span data-ttu-id="68016-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68016-120">-DefaultProfile</span></span>
<span data-ttu-id="68016-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="68016-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68016-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="68016-122">-Name</span></span>
<span data-ttu-id="68016-123">Określa nazwę prywatnej strefy DNS, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68016-123">Specifies the name of the private DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="68016-124">Musisz również określić parametr *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="68016-124">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="68016-125">Możesz też określić strefę DNS przy użyciu parametru *Zone* .</span><span class="sxs-lookup"><span data-stu-id="68016-125">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="68016-126">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="68016-126">-Overwrite</span></span>
<span data-ttu-id="68016-127">Podczas określania strefy za pomocą obiektu **PrivateDnsZone** (przekazywanego za pośrednictwem parametru rurociągu lub *strefy* ) strefa nie jest usuwana, jeśli została zmieniona w usłudze DNS Azure od momentu pobrania lokalnego obiektu **PrivateDnsZone** (tylko operacje bezpośrednio dotyczące liczby zasobów stref DNS jako zmian, operacje na zestawach rekordów w strefie nie są).</span><span class="sxs-lookup"><span data-stu-id="68016-127">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="68016-128">Zapewnia to ochronę współbieżnych zmian stref.</span><span class="sxs-lookup"><span data-stu-id="68016-128">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="68016-129">Można to pominąć przy użyciu parametru *overwrite* , który usuwa strefę bez względu na współbieżne zmiany.</span><span class="sxs-lookup"><span data-stu-id="68016-129">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="68016-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="68016-130">-PassThru</span></span>
<span data-ttu-id="68016-131">Służy do przekazywania wyniku (wartości logicznej) operacji Usuń strefę prywatną potoku.</span><span class="sxs-lookup"><span data-stu-id="68016-131">Used for passing the result (boolean) of the operation delete private zone further down the pipeline.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68016-132">-PrivateZone</span><span class="sxs-lookup"><span data-stu-id="68016-132">-PrivateZone</span></span>
<span data-ttu-id="68016-133">Obiekt strefy prywatnej do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="68016-133">The private zone object to delete.</span></span>

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

### <span data-ttu-id="68016-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68016-134">-ResourceGroupName</span></span>
<span data-ttu-id="68016-135">Określa nazwę grupy zasobów zawierającej strefę do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="68016-135">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="68016-136">Należy również określić parametr *zonename* .</span><span class="sxs-lookup"><span data-stu-id="68016-136">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="68016-137">Możesz też określić strefę DNS za pomocą obiektu **PrivateDnsZone** , przekazaną za pośrednictwem potoku lub parametru *Zone* .</span><span class="sxs-lookup"><span data-stu-id="68016-137">Alternatively, you can specify the DNS zone using a **PrivateDnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="68016-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68016-138">-ResourceId</span></span>
<span data-ttu-id="68016-139">Identyfikator zasobu prywatnej strefy DNS.</span><span class="sxs-lookup"><span data-stu-id="68016-139">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="68016-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="68016-140">-Confirm</span></span>
<span data-ttu-id="68016-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68016-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68016-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68016-142">-WhatIf</span></span>
<span data-ttu-id="68016-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68016-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68016-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="68016-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68016-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68016-145">CommonParameters</span></span>
<span data-ttu-id="68016-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68016-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68016-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68016-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68016-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="68016-148">INPUTS</span></span>

### <span data-ttu-id="68016-149">Microsoft. Azure. Commands. PrivateDns. models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="68016-149">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="68016-150">System. String</span><span class="sxs-lookup"><span data-stu-id="68016-150">System.String</span></span>

## <span data-ttu-id="68016-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="68016-151">OUTPUTS</span></span>

### <span data-ttu-id="68016-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="68016-152">System.Boolean</span></span>

## <span data-ttu-id="68016-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="68016-153">NOTES</span></span>

## <span data-ttu-id="68016-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="68016-154">RELATED LINKS</span></span>

[<span data-ttu-id="68016-155">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="68016-155">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="68016-156">Nowe — AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="68016-156">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="68016-157">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="68016-157">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
