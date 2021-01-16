---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsvirtualnetworklink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsVirtualNetworkLink.md
ms.openlocfilehash: 63fbe26fa0a9ac7ca5eb985a3806886adeb2a2f8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490837"
---
# <span data-ttu-id="d24ce-101">Remove-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="d24ce-101">Remove-AzPrivateDnsVirtualNetworkLink</span></span>

## <span data-ttu-id="d24ce-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d24ce-102">SYNOPSIS</span></span>
<span data-ttu-id="d24ce-103">Usuwa łącze sieci wirtualnej z grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d24ce-103">Removes a virtual network link from a resource group.</span></span>

## <span data-ttu-id="d24ce-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d24ce-104">SYNTAX</span></span>

### <span data-ttu-id="d24ce-105">Pola (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="d24ce-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName <String> -ZoneName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d24ce-106">Stream</span><span class="sxs-lookup"><span data-stu-id="d24ce-106">Object</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -InputObject <PSPrivateDnsVirtualNetworkLink> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d24ce-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="d24ce-107">ResourceId</span></span>
```
Remove-AzPrivateDnsVirtualNetworkLink -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d24ce-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d24ce-108">DESCRIPTION</span></span>
<span data-ttu-id="d24ce-109">Polecenie cmdlet **Remove-AzPrivateDnsVirtualNetworkLink** powoduje trwałe usunięcie linku prywatnego DNS (Domain Name System) z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d24ce-109">The **Remove-AzPrivateDnsVirtualNetworkLink** cmdlet permanently deletes a private Domain Name System (DNS) link from a specified resource group.</span></span>
<span data-ttu-id="d24ce-110">Obiekt **PSPrivateDnsVirtualNetworkLink** można przekazać przy użyciu parametru *link* lub za pomocą operatora potoku lub można też określić parametry *name (nazwa* *strefy* ) i *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="d24ce-110">You can pass a **PSPrivateDnsVirtualNetworkLink** object using the *Link* parameter or by using the pipeline operator, or alternatively you can specify the *Name* *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="d24ce-111">Za pomocą zmiennej Confirm i $ConfirmPreference programu Windows PowerShell można kontrolować, czy polecenie cmdlet monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d24ce-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="d24ce-112">Podczas określania linku przy użyciu obiektu **PSPrivateDnsVirtualNetworkLink** (przekazywanego za pośrednictwem parametru rurociągu lub *linku* ) link nie jest usuwany, jeśli został zmieniony w prywatnym systemie DNS platformy Azure, ponieważ obiekt lokalnego **PSPrivateDnsVirtualNetworkLink** został pobrany.</span><span class="sxs-lookup"><span data-stu-id="d24ce-112">When specifying the link using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the link is not deleted if it has been changed in Azure Private DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span> <span data-ttu-id="d24ce-113">Zapewnia to ochronę współbieżnych zmian stref.</span><span class="sxs-lookup"><span data-stu-id="d24ce-113">This provides protection for concurrent zone changes.</span></span> <span data-ttu-id="d24ce-114">Można to pominąć przy użyciu parametru *overwrite* , który usuwa strefę bez względu na współbieżne zmiany.</span><span class="sxs-lookup"><span data-stu-id="d24ce-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="d24ce-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d24ce-115">EXAMPLES</span></span>

### <span data-ttu-id="d24ce-116">Przykład 1: usuwanie linku</span><span class="sxs-lookup"><span data-stu-id="d24ce-116">Example 1: Remove a link</span></span>
```
PS C:\>Remove-AzPrivateDnsVirtualNetworkLink -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "mylink"
```

<span data-ttu-id="d24ce-117">To polecenie powoduje usunięcie linku o nazwie Moja link połączonego z strefą myzone.com z grupy zasobów o nazwie Moja zasobów.</span><span class="sxs-lookup"><span data-stu-id="d24ce-117">This command removes the link named mylink linked to zone myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="d24ce-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d24ce-118">PARAMETERS</span></span>

### <span data-ttu-id="d24ce-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d24ce-119">-DefaultProfile</span></span>
<span data-ttu-id="d24ce-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d24ce-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d24ce-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d24ce-121">-InputObject</span></span>
<span data-ttu-id="d24ce-122">Obiekt link sieci wirtualnej do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="d24ce-122">The virtual network link object to remove.</span></span>

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

### <span data-ttu-id="d24ce-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d24ce-123">-Name</span></span>
<span data-ttu-id="d24ce-124">Określa nazwę linku, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="d24ce-124">Specifies the name of the link to be deleted.</span></span>
<span data-ttu-id="d24ce-125">Musisz również określić parametr *ResourceGroupName* oraz *zonename* .</span><span class="sxs-lookup"><span data-stu-id="d24ce-125">You must also specify the *ResourceGroupName* and *ZoneName* parameter.</span></span>
<span data-ttu-id="d24ce-126">Możesz też określić link za pomocą parametru *link* .</span><span class="sxs-lookup"><span data-stu-id="d24ce-126">Alternatively, you can specify the link using the *Link* parameter.</span></span>

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

### <span data-ttu-id="d24ce-127">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="d24ce-127">-Overwrite</span></span>
<span data-ttu-id="d24ce-128">Podczas określania strefy za pomocą obiektu **PSPrivateDnsVirtualNetworkLink** (przekazywanego za pośrednictwem parametru rurociągu lub *linku* ) strefa nie jest usuwana, jeśli została zmieniona w usłudze DNS Azure, ponieważ obiekt lokalny **PSPrivateDnsVirtualNetworkLink** został pobrany.</span><span class="sxs-lookup"><span data-stu-id="d24ce-128">When specifying the zone using a **PSPrivateDnsVirtualNetworkLink** object (passed via the pipeline or *Link* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PSPrivateDnsVirtualNetworkLink** object was retrieved.</span></span>
<span data-ttu-id="d24ce-129">Zapewnia to ochronę współbieżnych zmian stref.</span><span class="sxs-lookup"><span data-stu-id="d24ce-129">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="d24ce-130">Można to pominąć przy użyciu parametru *overwrite* , który usuwa strefę bez względu na współbieżne zmiany.</span><span class="sxs-lookup"><span data-stu-id="d24ce-130">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="d24ce-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d24ce-131">-PassThru</span></span>
<span data-ttu-id="d24ce-132">Służy do przekazywania wyniku (wartości logicznej) operacji Usuń łącze sieci wirtualnej w dalszej części procesu.</span><span class="sxs-lookup"><span data-stu-id="d24ce-132">Used for passing the result (boolean) of the operation delete virtual network link further down the pipeline.</span></span>

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

### <span data-ttu-id="d24ce-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d24ce-133">-ResourceGroupName</span></span>
<span data-ttu-id="d24ce-134">Określa nazwę grupy zasobów zawierającej łącze do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="d24ce-134">Specifies the name of the resource group that contains the link to remove.</span></span>
<span data-ttu-id="d24ce-135">Należy również określić parametr *zonename* i *name* .</span><span class="sxs-lookup"><span data-stu-id="d24ce-135">You must also specify the *ZoneName* and *Name* parameter.</span></span>
<span data-ttu-id="d24ce-136">Możesz też określić strefę DNS za pomocą obiektu **PSPrivateDnsVirtualNetworkLink** , przekazaną za pośrednictwem rurociągu lub parametru *link* .</span><span class="sxs-lookup"><span data-stu-id="d24ce-136">Alternatively, you can specify the DNS zone using a **PSPrivateDnsVirtualNetworkLink** object, passed via either the pipeline or the *Link* parameter.</span></span>

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

### <span data-ttu-id="d24ce-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d24ce-137">-ResourceId</span></span>
<span data-ttu-id="d24ce-138">Określa identyfikator zasobu ARM łącza.</span><span class="sxs-lookup"><span data-stu-id="d24ce-138">Specifies the ARM resource ID of the link.</span></span>

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

### <span data-ttu-id="d24ce-139">-Nazwa_strefy</span><span class="sxs-lookup"><span data-stu-id="d24ce-139">-ZoneName</span></span>
<span data-ttu-id="d24ce-140">Określa nazwę prywatnej strefy DNS, z którą jest skojarzony link.</span><span class="sxs-lookup"><span data-stu-id="d24ce-140">Specifies the name of the private DNS zone that the link is associated with.</span></span>
<span data-ttu-id="d24ce-141">Musisz również określić parametr *ResourceGroupName* oraz *name (nazwa* ).</span><span class="sxs-lookup"><span data-stu-id="d24ce-141">You must also specify the *ResourceGroupName* and *Name* parameter.</span></span>
<span data-ttu-id="d24ce-142">Możesz też określić link za pomocą parametru *link* .</span><span class="sxs-lookup"><span data-stu-id="d24ce-142">Alternatively, you can specify the link using the *Link* parameter.</span></span>

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

### <span data-ttu-id="d24ce-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d24ce-143">-Confirm</span></span>
<span data-ttu-id="d24ce-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d24ce-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d24ce-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d24ce-145">-WhatIf</span></span>
<span data-ttu-id="d24ce-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d24ce-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d24ce-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d24ce-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d24ce-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d24ce-148">CommonParameters</span></span>
<span data-ttu-id="d24ce-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d24ce-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d24ce-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d24ce-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d24ce-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d24ce-151">INPUTS</span></span>

### <span data-ttu-id="d24ce-152">Microsoft. Azure. Commands. PrivateDns. models. PSPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="d24ce-152">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsVirtualNetworkLink</span></span>

### <span data-ttu-id="d24ce-153">System. String</span><span class="sxs-lookup"><span data-stu-id="d24ce-153">System.String</span></span>

## <span data-ttu-id="d24ce-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d24ce-154">OUTPUTS</span></span>

### <span data-ttu-id="d24ce-155">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d24ce-155">System.Boolean</span></span>

## <span data-ttu-id="d24ce-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d24ce-156">NOTES</span></span>

## <span data-ttu-id="d24ce-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d24ce-157">RELATED LINKS</span></span>

[<span data-ttu-id="d24ce-158">Get-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="d24ce-158">Get-AzPrivateDnsVirtualNetworkLink</span></span>](./Get-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="d24ce-159">Nowe — AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="d24ce-159">New-AzPrivateDnsVirtualNetworkLink</span></span>](./New-AzPrivateDnsVirtualNetworkLink.md)

[<span data-ttu-id="d24ce-160">Set-AzPrivateDnsVirtualNetworkLink</span><span class="sxs-lookup"><span data-stu-id="d24ce-160">Set-AzPrivateDnsVirtualNetworkLink</span></span>](./Set-AzPrivateDnsVirtualNetworkLink.md)
