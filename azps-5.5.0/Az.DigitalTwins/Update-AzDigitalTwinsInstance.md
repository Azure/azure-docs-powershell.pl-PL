---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/update-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Update-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Update-AzDigitalTwinsInstance.md
ms.openlocfilehash: 4de7ab82f60c651e23565569ccf2cda7f4d949b5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243690"
---
# <span data-ttu-id="37b65-101">Update-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="37b65-101">Update-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="37b65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37b65-102">SYNOPSIS</span></span>
<span data-ttu-id="37b65-103">Aktualizowanie metadanych pliku DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="37b65-103">Update metadata of DigitalTwinsInstance.</span></span>

## <span data-ttu-id="37b65-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="37b65-104">SYNTAX</span></span>

### <span data-ttu-id="37b65-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="37b65-105">UpdateExpanded (Default)</span></span>
```
Update-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="37b65-106">Aktualizacja</span><span class="sxs-lookup"><span data-stu-id="37b65-106">Update</span></span>
```
Update-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String>
 -DigitalTwinsPatchDescription <IDigitalTwinsPatchDescription> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="37b65-107">UpdateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="37b65-107">UpdateViaIdentity</span></span>
```
Update-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity>
 -DigitalTwinsPatchDescription <IDigitalTwinsPatchDescription> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="37b65-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="37b65-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="37b65-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="37b65-109">DESCRIPTION</span></span>
<span data-ttu-id="37b65-110">Aktualizowanie metadanych pliku DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="37b65-110">Update metadata of DigitalTwinsInstance.</span></span>

## <span data-ttu-id="37b65-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="37b65-111">EXAMPLES</span></span>

### <span data-ttu-id="37b65-112">Przykład 1. Aktualizacja Nierozwiązywalna (domyślna)</span><span class="sxs-lookup"><span data-stu-id="37b65-112">Example 1: UpdateExpanded (Default)</span></span>
```powershell
PS C:\> Update-AzDigitalTwinsInstance -ResourcegroupName youritemp -ResourceName youriDigitalTwinsTest -Tag @{“dtt”="001"}

Location Name                  Type
-------- ----                  ----
eastus   youriDigitalTwinsTest Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="37b65-113">Aktualizowanie określonego rekordu DigitalTwinsInstance przez nazwę ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37b65-113">Update the specified DigitalTwinsInstance by ResourceGroupName</span></span>

### <span data-ttu-id="37b65-114">Przykład 2. Aktualizowanie ciągu AzDigitalTwinsInstance przez inną aktualizację AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="37b65-114">Example 2: Update the AzDigitalTwinsInstance by another AzDigitalTwinsInstance</span></span>
```powershell
PS C:\> $updateDigitalTwinInstance1 = Update-AzDigitalTwinsInstance -ResourcegroupName youritemp -ResourceName youriDigitalTwin1 -Tag @{"dtt"="002"}
Update-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest -DigitalTwinsPatchDescription $updateDigitalTwinInstance1

Location Name                  Type
-------- ----                  ----
eastus   youriDigitalTwinsTest Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="37b65-115">Aktualizowanie azDigitalTwinsInstance przez inną azDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="37b65-115">Update the AzDigitalTwinsInstance by another AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="37b65-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37b65-116">PARAMETERS</span></span>

### <span data-ttu-id="37b65-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37b65-117">-DefaultProfile</span></span>
<span data-ttu-id="37b65-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="37b65-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37b65-119">-DigitalTwinsPatchDescription</span><span class="sxs-lookup"><span data-stu-id="37b65-119">-DigitalTwinsPatchDescription</span></span>
<span data-ttu-id="37b65-120">Opis usługi DigitalTwins.</span><span class="sxs-lookup"><span data-stu-id="37b65-120">The description of the DigitalTwins service.</span></span>
<span data-ttu-id="37b65-121">Aby skonstruować, zobacz sekcję NOTES dla właściwości DIGITALTWINSPATCHDESCRIPTION i utwórz tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="37b65-121">To construct, see NOTES section for DIGITALTWINSPATCHDESCRIPTION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsPatchDescription
Parameter Sets: Update, UpdateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37b65-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37b65-122">-InputObject</span></span>
<span data-ttu-id="37b65-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="37b65-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity
Parameter Sets: UpdateViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37b65-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37b65-124">-ResourceGroupName</span></span>
<span data-ttu-id="37b65-125">Nazwa grupy zasobów zawierającej nazwę DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="37b65-125">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37b65-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="37b65-126">-ResourceName</span></span>
<span data-ttu-id="37b65-127">Nazwa pliku DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="37b65-127">The name of the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37b65-128">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="37b65-128">-SubscriptionId</span></span>
<span data-ttu-id="37b65-129">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="37b65-129">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37b65-130">— Tag</span><span class="sxs-lookup"><span data-stu-id="37b65-130">-Tag</span></span>
<span data-ttu-id="37b65-131">Tagi wystąpienia</span><span class="sxs-lookup"><span data-stu-id="37b65-131">Instance tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37b65-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="37b65-132">-Confirm</span></span>
<span data-ttu-id="37b65-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="37b65-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37b65-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37b65-134">-WhatIf</span></span>
<span data-ttu-id="37b65-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37b65-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37b65-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="37b65-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37b65-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37b65-137">CommonParameters</span></span>
<span data-ttu-id="37b65-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37b65-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37b65-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37b65-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37b65-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="37b65-140">INPUTS</span></span>

### <span data-ttu-id="37b65-141">Microsoft.Azure.PowerShell.cmdlet.DigitalTwins.Models.Api20201031.IDigitalTwinsPatchDescription</span><span class="sxs-lookup"><span data-stu-id="37b65-141">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsPatchDescription</span></span>

### <span data-ttu-id="37b65-142">Microsoft.Azure.PowerShell.Cmdlet.DigitalTwins.Models.IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="37b65-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="37b65-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="37b65-143">OUTPUTS</span></span>

### <span data-ttu-id="37b65-144">Microsoft.Azure.PowerShell.Cmdlet.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="37b65-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="37b65-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="37b65-145">NOTES</span></span>

<span data-ttu-id="37b65-146">ALIASY</span><span class="sxs-lookup"><span data-stu-id="37b65-146">ALIASES</span></span>

<span data-ttu-id="37b65-147">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="37b65-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="37b65-148">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="37b65-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="37b65-149">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="37b65-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="37b65-150">DIGITALTWINSPATCHDESCRIPTION: <IDigitalTwinsPatchDescription> Opis usługi DigitalTwins.</span><span class="sxs-lookup"><span data-stu-id="37b65-150">DIGITALTWINSPATCHDESCRIPTION <IDigitalTwinsPatchDescription>: The description of the DigitalTwins service.</span></span>
  - <span data-ttu-id="37b65-151">`[Tag <IDigitalTwinsPatchDescriptionTags>]`: Tagi wystąpienia</span><span class="sxs-lookup"><span data-stu-id="37b65-151">`[Tag <IDigitalTwinsPatchDescriptionTags>]`: Instance tags</span></span>
    - <span data-ttu-id="37b65-152">`[(Any) <String>]`: Wskazuje to, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="37b65-152">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

<span data-ttu-id="37b65-153">INPUTOBJECT: <IDigitalTwinsIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="37b65-153">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="37b65-154">`[EndpointName <String>]`: Nazwa zasobu punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="37b65-154">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="37b65-155">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="37b65-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="37b65-156">`[Location <String>]`: Lokalizacja technologii DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="37b65-156">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="37b65-157">`[ResourceGroupName <String>]`: nazwa grupy zasobów zawierającej nazwę DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="37b65-157">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="37b65-158">`[ResourceName <String>]`: nazwa pliku DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="37b65-158">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="37b65-159">`[SubscriptionId <String>]`: Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="37b65-159">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="37b65-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="37b65-160">RELATED LINKS</span></span>

