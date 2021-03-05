---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/powershell/module/az.privatedns/remove-azprivatednsvirtualnetworklink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 8de4922b5d71902fe22a17a6c02f21a40e35ddc7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965553"
---
# <span data-ttu-id="396b9-101">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="396b9-101">Remove-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="396b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="396b9-102">SYNOPSIS</span></span>
<span data-ttu-id="396b9-103">Usuwa link sieci wirtualnej z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="396b9-103">Removes a virtual network link from a resource group.</span></span>

## <span data-ttu-id="396b9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="396b9-104">SYNTAX</span></span>

### <span data-ttu-id="396b9-105">Pola (domyślne)</span><span class="sxs-lookup"><span data-stu-id="396b9-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="396b9-106">Obiekt</span><span class="sxs-lookup"><span data-stu-id="396b9-106">Object</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="396b9-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="396b9-107">ResourceId</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="396b9-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="396b9-108">DESCRIPTION</span></span>
<span data-ttu-id="396b9-109">Polecenie cmdlet **Remove-AzPrivateDnsVirtualNetworkLink** trwale usuwa link do prywatnego systemu nazw domen (DNS) z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="396b9-109">The **Remove-AzPrivateDnsVirtualNetworkLink** cmdlet permanently deletes a private Domain Name System (DNS) link from a specified resource group.</span></span>
<span data-ttu-id="396b9-110">Obiekt **PSPrivateDnsVirtualNetworkLink** można przekazać przy użyciu parametru *Link* lub operatora potoku   albo określić parametry Nazwa Strefy i *NazwaGrupy* Zasobów.</span><span class="sxs-lookup"><span data-stu-id="396b9-110">You can pass a **PSPrivateDnsVirtualNetworkLink** object using the *Link* parameter or by using the pipeline operator, or alternatively you can specify the *Name* *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="396b9-111">Możesz użyć parametru Confirm i $ConfirmPreference zmienną programu Windows PowerShell, aby określić, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="396b9-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="396b9-112">Podczas określania linku przy użyciu obiektu **PSPrivateDnsVirtualNetworkLink** (przekazywanego za pośrednictwem parametru potoku lub linku) link nie jest usuwany, jeśli został zmieniony w prywatnym systemie DNS platformy Azure od czasu pobrania lokalnego obiektu **PSPrivateDnsVirtualNetworkLink.** </span><span class="sxs-lookup"><span data-stu-id="396b9-112">When specifying the link using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not deleted if it has been changed in Azure Private DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span> <span data-ttu-id="396b9-113">Zapewnia to ochronę przed jednoczesnym zmianą strefy.</span><span class="sxs-lookup"><span data-stu-id="396b9-113">This provides protection for concurrent zone changes.</span></span> <span data-ttu-id="396b9-114">Można to pominąć przy użyciu *parametru Zastąp,* który usuwa strefę niezależnie od jednoczesnych zmian.</span><span class="sxs-lookup"><span data-stu-id="396b9-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="396b9-115">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="396b9-115">EXAMPLES</span></span>

### <span data-ttu-id="396b9-116">Przykład 1. Usuwanie linku</span><span class="sxs-lookup"><span data-stu-id="396b9-116">Example 1: Remove a link</span></span>
```
PS C:\>Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "mylink"
```

<span data-ttu-id="396b9-117">To polecenie usuwa link o nazwie mójlink połączony ze strefą myzone.com z grupy zasobów o nazwie MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="396b9-117">This command removes the link named mylink linked to zone myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="396b9-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="396b9-118">PARAMETERS</span></span>

### <span data-ttu-id="396b9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="396b9-119">-DefaultProfile</span></span>
<span data-ttu-id="396b9-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="396b9-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="396b9-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="396b9-121">-InputObject</span></span>
<span data-ttu-id="396b9-122">Obiekt łącza sieci wirtualnej do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="396b9-122">The virtual network link object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="396b9-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="396b9-123">-Name</span></span>
<span data-ttu-id="396b9-124">Określa nazwę linku do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="396b9-124">Specifies the name of the link to be deleted.</span></span>
<span data-ttu-id="396b9-125">Musisz także określić parametr *ResourceGroupName* i *ZoneName.*</span><span class="sxs-lookup"><span data-stu-id="396b9-125">You must also specify the *ResourceGroupName* and *ZoneName* parameter.</span></span>
<span data-ttu-id="396b9-126">Możesz również określić link, używając *parametru Link.*</span><span class="sxs-lookup"><span data-stu-id="396b9-126">Alternatively, you can specify the link using the *Link* parameter.</span></span>

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

### <span data-ttu-id="396b9-127">— Zastąp</span><span class="sxs-lookup"><span data-stu-id="396b9-127">-Overwrite</span></span>
<span data-ttu-id="396b9-128">Podczas określania strefy za pomocą obiektu **PSPrivateDnsVirtualNetworkLink**  (przekazywanego za pośrednictwem parametru potoku lub linku) strefa nie jest usuwana, jeśli została zmieniona w usłudze Azure DNS od czasu pobrania lokalnego obiektu **PSPrivateDnsVirtualNetworkLink.**</span><span class="sxs-lookup"><span data-stu-id="396b9-128">When specifying the zone using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span>
<span data-ttu-id="396b9-129">Zapewnia to ochronę przed jednoczesnym zmianą strefy.</span><span class="sxs-lookup"><span data-stu-id="396b9-129">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="396b9-130">Można to pominąć przy użyciu *parametru Zastąp,* który usuwa strefę niezależnie od jednoczesnych zmian.</span><span class="sxs-lookup"><span data-stu-id="396b9-130">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="396b9-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="396b9-131">-PassThru</span></span>
<span data-ttu-id="396b9-132">Służy do przekazywania wyniku (wartości logicznych) operacji usunięcia linku do sieci wirtualnej w dalszej części potoku.</span><span class="sxs-lookup"><span data-stu-id="396b9-132">Used for passing the result (boolean) of the operation delete virtual network link further down the pipeline.</span></span>

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

### <span data-ttu-id="396b9-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="396b9-133">-ResourceGroupName</span></span>
<span data-ttu-id="396b9-134">Określa nazwę grupy zasobów zawierającej link do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="396b9-134">Specifies the name of the resource group that contains the link to remove.</span></span>
<span data-ttu-id="396b9-135">Musisz także określić parametr *ZoneName (Nazwa* *strefy) i Name (Nazwa).*</span><span class="sxs-lookup"><span data-stu-id="396b9-135">You must also specify the *ZoneName* and *Name* parameter.</span></span>
<span data-ttu-id="396b9-136">Możesz również określić strefę DNS przy użyciu obiektu **PSPrivateDnsVirtualNetworkLink,** przekazywanego za pośrednictwem potoku lub *parametru Link.*</span><span class="sxs-lookup"><span data-stu-id="396b9-136">Alternatively, you can specify the DNS zone using a **PSPrivateDnsVirtualNetworkLink** object, passed via either the pipeline or the *Link* parameter.</span></span>

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

### <span data-ttu-id="396b9-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="396b9-137">-ResourceId</span></span>
<span data-ttu-id="396b9-138">Określa ARM identyfikatora zasobu linku.</span><span class="sxs-lookup"><span data-stu-id="396b9-138">Specifies the ARM resource ID of the link.</span></span>

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

### <span data-ttu-id="396b9-139">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="396b9-139">-ZoneName</span></span>
<span data-ttu-id="396b9-140">Określa nazwę prywatnej strefy DNS, z która jest skojarzony link.</span><span class="sxs-lookup"><span data-stu-id="396b9-140">Specifies the name of the private DNS zone that the link is associated with.</span></span>
<span data-ttu-id="396b9-141">Musisz także określić parametr *ResourceGroupName* i *Name.*</span><span class="sxs-lookup"><span data-stu-id="396b9-141">You must also specify the *ResourceGroupName* and *Name* parameter.</span></span>
<span data-ttu-id="396b9-142">Możesz również określić link, używając *parametru Link.*</span><span class="sxs-lookup"><span data-stu-id="396b9-142">Alternatively, you can specify the link using the *Link* parameter.</span></span>

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

### <span data-ttu-id="396b9-143">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="396b9-143">-Confirm</span></span>
<span data-ttu-id="396b9-144">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="396b9-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="396b9-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="396b9-145">-WhatIf</span></span>
<span data-ttu-id="396b9-146">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="396b9-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="396b9-147">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="396b9-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="396b9-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="396b9-148">CommonParameters</span></span>
<span data-ttu-id="396b9-149">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="396b9-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="396b9-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="396b9-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="396b9-151">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="396b9-151">INPUTS</span></span>

### <span data-ttu-id="396b9-152">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="396b9-152">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

### <span data-ttu-id="396b9-153">System.String</span><span class="sxs-lookup"><span data-stu-id="396b9-153">System.String</span></span>

## <span data-ttu-id="396b9-154">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="396b9-154">OUTPUTS</span></span>

### <span data-ttu-id="396b9-155">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="396b9-155">System.Boolean</span></span>

## <span data-ttu-id="396b9-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="396b9-156">NOTES</span></span>

## <span data-ttu-id="396b9-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="396b9-157">RELATED LINKS</span></span>

[<span data-ttu-id="396b9-158">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="396b9-158">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="396b9-159">New-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="396b9-159">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="396b9-160">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="396b9-160">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)
