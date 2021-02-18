---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
ms.openlocfilehash: d381af8de23b5eb781882f10670e6ba69afbc571
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193099"
---
# <span data-ttu-id="8740c-101">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="8740c-101">Remove-AzPrivateDnsZone</span></span>

## <span data-ttu-id="8740c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8740c-102">SYNOPSIS</span></span>
<span data-ttu-id="8740c-103">Usuwa prywatną strefę DNS z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8740c-103">Removes a private DNS zone from a resource group.</span></span>

## <span data-ttu-id="8740c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8740c-104">SYNTAX</span></span>

### <span data-ttu-id="8740c-105">Pola (domyślne)</span><span class="sxs-lookup"><span data-stu-id="8740c-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8740c-106">Obiekt</span><span class="sxs-lookup"><span data-stu-id="8740c-106">Object</span></span>
```
Remove-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8740c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8740c-107">ResourceId</span></span>
```
Remove-AzPrivateDnsZone -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8740c-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="8740c-108">DESCRIPTION</span></span>
<span data-ttu-id="8740c-109">Polecenie cmdlet **Remove-AzPrivateDnsZone** trwale usuwa strefę prywatnego systemu nazw domen (DNS) z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8740c-109">The **Remove-AzPrivateDnsZone** cmdlet permanently deletes a private Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="8740c-110">Usuwane są również wszystkie zestawy rekordów zawarte w strefie.</span><span class="sxs-lookup"><span data-stu-id="8740c-110">All record sets contained in the zone are also deleted.</span></span>
<span data-ttu-id="8740c-111">Obiekt **PrivateDnsZone** można przekazać za pomocą parametru *PrivateZone* lub za pomocą operatora potoku albo możesz również określić parametry *Name* (Nazwa) i *ResourceGroupName (Nazwa* grupy zasobów).</span><span class="sxs-lookup"><span data-stu-id="8740c-111">You can pass a **PrivateDnsZone** object using the *PrivateZone* parameter or by using the pipeline operator, or alternatively you can specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="8740c-112">Możesz użyć parametru Confirm i $ConfirmPreference zmienną programu Windows PowerShell, aby określić, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8740c-112">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="8740c-113">Podczas określania strefy przy użyciu obiektu **PrivateDnsZone** (przekazywanego za pośrednictwem potoku lub parametru *Zone)* strefa nie jest usuwana, jeśli została zmieniona w systemie Azure DNS od czasu pobrania lokalnego obiektu **PrivateDnsZone** (tylko operacje bezpośrednio na liczniku zasobów strefy DNS jako zmiany, operacje na zestawach rekordów w strefie nie).</span><span class="sxs-lookup"><span data-stu-id="8740c-113">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="8740c-114">Zapewnia to ochronę przed jednoczesnym zmianą strefy.</span><span class="sxs-lookup"><span data-stu-id="8740c-114">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="8740c-115">Można to pominąć przy użyciu *parametru Zastąp,* który usuwa strefę niezależnie od jednoczesnych zmian.</span><span class="sxs-lookup"><span data-stu-id="8740c-115">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="8740c-116">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8740c-116">EXAMPLES</span></span>

### <span data-ttu-id="8740c-117">Przykład 1. Usuwanie strefy prywatnej</span><span class="sxs-lookup"><span data-stu-id="8740c-117">Example 1: Remove a private zone</span></span>
```
PS C:\>Remove-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="8740c-118">To polecenie usuwa strefę o nazwie myzone.com z grupy zasobów o nazwie MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8740c-118">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="8740c-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8740c-119">PARAMETERS</span></span>

### <span data-ttu-id="8740c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8740c-120">-DefaultProfile</span></span>
<span data-ttu-id="8740c-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="8740c-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8740c-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8740c-122">-Name</span></span>
<span data-ttu-id="8740c-123">Określa nazwę prywatnej strefy DNS, która jest usuwana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8740c-123">Specifies the name of the private DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="8740c-124">Musisz także określić parametr *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="8740c-124">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="8740c-125">Możesz również określić strefę DNS, używając *parametru Zone.*</span><span class="sxs-lookup"><span data-stu-id="8740c-125">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="8740c-126">— Zastąp</span><span class="sxs-lookup"><span data-stu-id="8740c-126">-Overwrite</span></span>
<span data-ttu-id="8740c-127">Podczas określania strefy przy użyciu obiektu **PrivateDnsZone** (przekazywanego za pośrednictwem potoku lub parametru *Zone)* strefa nie jest usuwana, jeśli została zmieniona w systemie Azure DNS od czasu pobrania lokalnego obiektu **PrivateDnsZone** (tylko operacje bezpośrednio na liczniku zasobów strefy DNS jako zmiany, operacje na zestawach rekordów w strefie nie).</span><span class="sxs-lookup"><span data-stu-id="8740c-127">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="8740c-128">Zapewnia to ochronę przed jednoczesnym zmianą strefy.</span><span class="sxs-lookup"><span data-stu-id="8740c-128">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="8740c-129">Można to pominąć przy użyciu *parametru Zastąp,* który usuwa strefę niezależnie od jednoczesnych zmian.</span><span class="sxs-lookup"><span data-stu-id="8740c-129">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="8740c-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8740c-130">-PassThru</span></span>
<span data-ttu-id="8740c-131">Służy do przekazywania wyniku (wartości logicznych) operacji usunięcia strefy prywatnej w dalszej części potoku.</span><span class="sxs-lookup"><span data-stu-id="8740c-131">Used for passing the result (boolean) of the operation delete private zone further down the pipeline.</span></span>

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

### <span data-ttu-id="8740c-132">— PrivateZone</span><span class="sxs-lookup"><span data-stu-id="8740c-132">-PrivateZone</span></span>
<span data-ttu-id="8740c-133">Obiekt strefy prywatnej do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="8740c-133">The private zone object to delete.</span></span>

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

### <span data-ttu-id="8740c-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8740c-134">-ResourceGroupName</span></span>
<span data-ttu-id="8740c-135">Określa nazwę grupy zasobów zawierającej strefę do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="8740c-135">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="8740c-136">Musisz także określić parametr *ZoneName.*</span><span class="sxs-lookup"><span data-stu-id="8740c-136">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="8740c-137">Możesz również określić strefę DNS przy użyciu **obiektu PrivateDnsZone** przekazywanego za pośrednictwem potoku lub *parametru Zone.*</span><span class="sxs-lookup"><span data-stu-id="8740c-137">Alternatively, you can specify the DNS zone using a **PrivateDnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="8740c-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8740c-138">-ResourceId</span></span>
<span data-ttu-id="8740c-139">Private DNS Zone ResourceID (Prywatny adres DNS Strefy ResourceID).</span><span class="sxs-lookup"><span data-stu-id="8740c-139">Private DNS Zone ResourceID.</span></span>

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

### <span data-ttu-id="8740c-140">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8740c-140">-Confirm</span></span>
<span data-ttu-id="8740c-141">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8740c-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8740c-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8740c-142">-WhatIf</span></span>
<span data-ttu-id="8740c-143">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8740c-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8740c-144">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8740c-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8740c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8740c-145">CommonParameters</span></span>
<span data-ttu-id="8740c-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8740c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8740c-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8740c-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8740c-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8740c-148">INPUTS</span></span>

### <span data-ttu-id="8740c-149">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="8740c-149">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="8740c-150">System.String</span><span class="sxs-lookup"><span data-stu-id="8740c-150">System.String</span></span>

## <span data-ttu-id="8740c-151">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8740c-151">OUTPUTS</span></span>

### <span data-ttu-id="8740c-152">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8740c-152">System.Boolean</span></span>

## <span data-ttu-id="8740c-153">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8740c-153">NOTES</span></span>

## <span data-ttu-id="8740c-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8740c-154">RELATED LINKS</span></span>

[<span data-ttu-id="8740c-155">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="8740c-155">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="8740c-156">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="8740c-156">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="8740c-157">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="8740c-157">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
