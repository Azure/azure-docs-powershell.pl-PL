---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/update-azdigitaltwinsinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Update-AzDigitalTwinsInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/Update-AzDigitalTwinsInstance.md
ms.openlocfilehash: 4de7ab82f60c651e23565569ccf2cda7f4d949b5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499118"
---
# <span data-ttu-id="6b98c-101">Update-AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="6b98c-101">Update-AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="6b98c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6b98c-102">SYNOPSIS</span></span>
<span data-ttu-id="6b98c-103">Aktualizowanie metadanych DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="6b98c-103">Update metadata of DigitalTwinsInstance.</span></span>

## <span data-ttu-id="6b98c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6b98c-104">SYNTAX</span></span>

### <span data-ttu-id="6b98c-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6b98c-105">UpdateExpanded (Default)</span></span>
```
Update-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6b98c-106">Aktualizowane</span><span class="sxs-lookup"><span data-stu-id="6b98c-106">Update</span></span>
```
Update-AzDigitalTwinsInstance -ResourceGroupName <String> -ResourceName <String>
 -DigitalTwinsPatchDescription <IDigitalTwinsPatchDescription> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6b98c-107">UpdateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6b98c-107">UpdateViaIdentity</span></span>
```
Update-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity>
 -DigitalTwinsPatchDescription <IDigitalTwinsPatchDescription> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6b98c-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6b98c-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzDigitalTwinsInstance -InputObject <IDigitalTwinsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6b98c-109">Opis</span><span class="sxs-lookup"><span data-stu-id="6b98c-109">DESCRIPTION</span></span>
<span data-ttu-id="6b98c-110">Aktualizowanie metadanych DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="6b98c-110">Update metadata of DigitalTwinsInstance.</span></span>

## <span data-ttu-id="6b98c-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6b98c-111">EXAMPLES</span></span>

### <span data-ttu-id="6b98c-112">Przykład 1: UpdateExpanded (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="6b98c-112">Example 1: UpdateExpanded (Default)</span></span>
```powershell
PS C:\> Update-AzDigitalTwinsInstance -ResourcegroupName youritemp -ResourceName youriDigitalTwinsTest -Tag @{“dtt”="001"}

Location Name                  Type
-------- ----                  ----
eastus   youriDigitalTwinsTest Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="6b98c-113">Aktualizowanie określonego DigitalTwinsInstance przez ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b98c-113">Update the specified DigitalTwinsInstance by ResourceGroupName</span></span>

### <span data-ttu-id="6b98c-114">Przykład 2: aktualizowanie AzDigitalTwinsInstance przez inną AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="6b98c-114">Example 2: Update the AzDigitalTwinsInstance by another AzDigitalTwinsInstance</span></span>
```powershell
PS C:\> $updateDigitalTwinInstance1 = Update-AzDigitalTwinsInstance -ResourcegroupName youritemp -ResourceName youriDigitalTwin1 -Tag @{"dtt"="002"}
Update-AzDigitalTwinsInstance -ResourceGroupName youritemp -ResourceName youriDigitalTwinsTest -DigitalTwinsPatchDescription $updateDigitalTwinInstance1

Location Name                  Type
-------- ----                  ----
eastus   youriDigitalTwinsTest Microsoft.DigitalTwins/digitalTwinsInstances
```

<span data-ttu-id="6b98c-115">Aktualizowanie AzDigitalTwinsInstance przez inną AzDigitalTwinsInstance</span><span class="sxs-lookup"><span data-stu-id="6b98c-115">Update the AzDigitalTwinsInstance by another AzDigitalTwinsInstance</span></span>

## <span data-ttu-id="6b98c-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6b98c-116">PARAMETERS</span></span>

### <span data-ttu-id="6b98c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b98c-117">-DefaultProfile</span></span>
<span data-ttu-id="6b98c-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6b98c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b98c-119">-DigitalTwinsPatchDescription</span><span class="sxs-lookup"><span data-stu-id="6b98c-119">-DigitalTwinsPatchDescription</span></span>
<span data-ttu-id="6b98c-120">Opis usługi DigitalTwins.</span><span class="sxs-lookup"><span data-stu-id="6b98c-120">The description of the DigitalTwins service.</span></span>
<span data-ttu-id="6b98c-121">Aby skonstruować, zobacz sekcję notatki dla właściwości DIGITALTWINSPATCHDESCRIPTION i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="6b98c-121">To construct, see NOTES section for DIGITALTWINSPATCHDESCRIPTION properties and create a hash table.</span></span>

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

### <span data-ttu-id="6b98c-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6b98c-122">-InputObject</span></span>
<span data-ttu-id="6b98c-123">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="6b98c-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6b98c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b98c-124">-ResourceGroupName</span></span>
<span data-ttu-id="6b98c-125">Nazwa grupy zasobów zawierającej DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="6b98c-125">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="6b98c-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="6b98c-126">-ResourceName</span></span>
<span data-ttu-id="6b98c-127">Nazwa DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="6b98c-127">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="6b98c-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="6b98c-128">-SubscriptionId</span></span>
<span data-ttu-id="6b98c-129">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6b98c-129">The subscription identifier.</span></span>

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

### <span data-ttu-id="6b98c-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="6b98c-130">-Tag</span></span>
<span data-ttu-id="6b98c-131">Znaczniki wystąpienia</span><span class="sxs-lookup"><span data-stu-id="6b98c-131">Instance tags</span></span>

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

### <span data-ttu-id="6b98c-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6b98c-132">-Confirm</span></span>
<span data-ttu-id="6b98c-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b98c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b98c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b98c-134">-WhatIf</span></span>
<span data-ttu-id="6b98c-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b98c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b98c-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6b98c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b98c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b98c-137">CommonParameters</span></span>
<span data-ttu-id="6b98c-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b98c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b98c-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b98c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b98c-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6b98c-140">INPUTS</span></span>

### <span data-ttu-id="6b98c-141">Microsoft. Azure. PowerShell. polecenia. DigitalTwins. models. Api20201031. IDigitalTwinsPatchDescription</span><span class="sxs-lookup"><span data-stu-id="6b98c-141">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsPatchDescription</span></span>

### <span data-ttu-id="6b98c-142">Microsoft. Azure. PowerShell. polecenia. DigitalTwins. models. IDigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="6b98c-142">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.IDigitalTwinsIdentity</span></span>

## <span data-ttu-id="6b98c-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6b98c-143">OUTPUTS</span></span>

### <span data-ttu-id="6b98c-144">Microsoft. Azure. PowerShell. polecenia. DigitalTwins. models. Api20201031. IDigitalTwinsDescription</span><span class="sxs-lookup"><span data-stu-id="6b98c-144">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsDescription</span></span>

## <span data-ttu-id="6b98c-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6b98c-145">NOTES</span></span>

<span data-ttu-id="6b98c-146">PISUJE</span><span class="sxs-lookup"><span data-stu-id="6b98c-146">ALIASES</span></span>

<span data-ttu-id="6b98c-147">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6b98c-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6b98c-148">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="6b98c-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6b98c-149">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6b98c-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6b98c-150">DIGITALTWINSPATCHDESCRIPTION <IDigitalTwinsPatchDescription> : Opis usługi DigitalTwins.</span><span class="sxs-lookup"><span data-stu-id="6b98c-150">DIGITALTWINSPATCHDESCRIPTION <IDigitalTwinsPatchDescription>: The description of the DigitalTwins service.</span></span>
  - <span data-ttu-id="6b98c-151">`[Tag <IDigitalTwinsPatchDescriptionTags>]`: Znaczniki wystąpienia</span><span class="sxs-lookup"><span data-stu-id="6b98c-151">`[Tag <IDigitalTwinsPatchDescriptionTags>]`: Instance tags</span></span>
    - <span data-ttu-id="6b98c-152">`[(Any) <String>]`: Wskazuje, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="6b98c-152">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

<span data-ttu-id="6b98c-153">INPUTobject <IDigitalTwinsIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="6b98c-153">INPUTOBJECT <IDigitalTwinsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6b98c-154">`[EndpointName <String>]`: Nazwa zasobu punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="6b98c-154">`[EndpointName <String>]`: Name of Endpoint Resource.</span></span>
  - <span data-ttu-id="6b98c-155">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="6b98c-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6b98c-156">`[Location <String>]`: Lokalizacja DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="6b98c-156">`[Location <String>]`: Location of DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="6b98c-157">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="6b98c-157">`[ResourceGroupName <String>]`: The name of the resource group that contains the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="6b98c-158">`[ResourceName <String>]`: Nazwa DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="6b98c-158">`[ResourceName <String>]`: The name of the DigitalTwinsInstance.</span></span>
  - <span data-ttu-id="6b98c-159">`[SubscriptionId <String>]`: Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6b98c-159">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="6b98c-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6b98c-160">RELATED LINKS</span></span>

