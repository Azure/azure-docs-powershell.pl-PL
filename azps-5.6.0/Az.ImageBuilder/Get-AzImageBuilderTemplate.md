---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/powershell/module/az.imagebuilder/get-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderTemplate.md
ms.openlocfilehash: 82730525f6330336be72e922881d743345515926
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013066"
---
# <span data-ttu-id="d2edc-101">Get-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="d2edc-101">Get-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="d2edc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2edc-102">SYNOPSIS</span></span>
<span data-ttu-id="d2edc-103">Uzyskiwanie informacji o szablonie obrazu maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="d2edc-103">Get information about a virtual machine image template</span></span>

## <span data-ttu-id="d2edc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d2edc-104">SYNTAX</span></span>

### <span data-ttu-id="d2edc-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="d2edc-105">List (Default)</span></span>
```
Get-AzImageBuilderTemplate [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d2edc-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="d2edc-106">Get</span></span>
```
Get-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d2edc-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d2edc-107">GetViaIdentity</span></span>
```
Get-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="d2edc-108">Lista1</span><span class="sxs-lookup"><span data-stu-id="d2edc-108">List1</span></span>
```
Get-AzImageBuilderTemplate -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d2edc-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="d2edc-109">DESCRIPTION</span></span>
<span data-ttu-id="d2edc-110">Uzyskiwanie informacji o szablonie obrazu maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="d2edc-110">Get information about a virtual machine image template</span></span>

## <span data-ttu-id="d2edc-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d2edc-111">EXAMPLES</span></span>

### <span data-ttu-id="d2edc-112">Przykład 1. Lista wszystkich szablonów w ramach subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d2edc-112">Example 1: List all template under a subscription</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate

Location Name                      Type
-------- ----                      ----
eastus   HelloImageTemplateLinux01 Microsoft.VirtualMachineImages/imageTemplates
eastus   lucas-imagetemplate       Microsoft.VirtualMachineImages/imageTemplates
eastus   test-imagebuilder         Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="d2edc-113">To polecenie wyświetla listę wszystkich szablonów w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d2edc-113">This command lists all template under a subscription.</span></span>

### <span data-ttu-id="d2edc-114">Przykład 2. Lista wszystkich szablonów w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="d2edc-114">Example 2: List all template under a resource group</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder

Location Name                       Type
-------- ----                       ----
eastus   HelloImageTemplateLinux01  Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-ax01b7       Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-ep5z7v       Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-klcuav       Microsoft.VirtualMachineImages/imageTemplates
eastus   template-name-u7gjqx       Microsoft.VirtualMachineImages/imageTemplates
eastus   test-imagebuilder          Microsoft.VirtualMachineImages/imageTemplates
eastus   tmpl-managedimg-managedimg Microsoft.VirtualMachineImages/imageTemplates
eastus   tmpl-platform-managed      Microsoft.VirtualMachineImages/imageTemplates
eastus   tmpl-shareimg-managedimg   Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="d2edc-115">To polecenie wyświetla listę wszystkich szablonów w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="d2edc-115">This command lists all template under a resource group.</span></span>

### <span data-ttu-id="d2edc-116">Przykład 3. Uzyskiwanie szablonu pod grupą zasobów</span><span class="sxs-lookup"><span data-stu-id="d2edc-116">Example 3: Get a template under a resource group</span></span>
```powershell
PS C:\> Get-AzImageBuilderTemplate -ImageTemplateName lucas-imagetemplate -ResourceGroupName wyunchi-imagebuilder

Location Name                Type
-------- ----                ----
eastus   lucas-imagetemplate Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="d2edc-117">To polecenie pobiera szablon w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="d2edc-117">This command gets a template under a resource group.</span></span>

### <span data-ttu-id="d2edc-118">Przykład 4. Uzyskiwanie szablonu pod grupą zasobów</span><span class="sxs-lookup"><span data-stu-id="d2edc-118">Example 4: Get a template under a resource group</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -ImageTemplateName template-name-ep5z7v
PS C:\> Get-AzImageBuilderTemplate -InputObject $template

Location Name                 Type
-------- ----                 ----
eastus   template-name-ep5z7v Microsoft.VirtualMachineImages/imageTemplates
```

<span data-ttu-id="d2edc-119">To polecenie pobiera szablon w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="d2edc-119">This command gets a template under a resource group.</span></span>

## <span data-ttu-id="d2edc-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2edc-120">PARAMETERS</span></span>

### <span data-ttu-id="d2edc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2edc-121">-DefaultProfile</span></span>
<span data-ttu-id="d2edc-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d2edc-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2edc-123">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="d2edc-123">-ImageTemplateName</span></span>
<span data-ttu-id="d2edc-124">Nazwa szablonu obrazu</span><span class="sxs-lookup"><span data-stu-id="d2edc-124">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2edc-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2edc-125">-InputObject</span></span>
<span data-ttu-id="d2edc-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="d2edc-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2edc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2edc-127">-ResourceGroupName</span></span>
<span data-ttu-id="d2edc-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d2edc-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2edc-129">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d2edc-129">-SubscriptionId</span></span>
<span data-ttu-id="d2edc-130">Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d2edc-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d2edc-131">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="d2edc-131">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2edc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2edc-132">CommonParameters</span></span>
<span data-ttu-id="d2edc-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2edc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2edc-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d2edc-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2edc-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2edc-135">INPUTS</span></span>

### <span data-ttu-id="d2edc-136">Microsoft.Azure.PowerShell.Cmdlet.ImageBuilder.Models.IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="d2edc-136">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="d2edc-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2edc-137">OUTPUTS</span></span>

### <span data-ttu-id="d2edc-138">Microsoft.Azure.PowerShell.Cmdlet.ImageBuilder.Models.Api20200214.IImageTemplate</span><span class="sxs-lookup"><span data-stu-id="d2edc-138">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span></span>

## <span data-ttu-id="d2edc-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d2edc-139">NOTES</span></span>

<span data-ttu-id="d2edc-140">ALIASY</span><span class="sxs-lookup"><span data-stu-id="d2edc-140">ALIASES</span></span>

<span data-ttu-id="d2edc-141">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d2edc-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d2edc-142">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="d2edc-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d2edc-143">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d2edc-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d2edc-144">INPUTOBJECT: <IImageBuilderIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="d2edc-144">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d2edc-145">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="d2edc-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d2edc-146">`[ImageTemplateName <String>]`: nazwa szablonu obrazu</span><span class="sxs-lookup"><span data-stu-id="d2edc-146">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="d2edc-147">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d2edc-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="d2edc-148">`[RunOutputName <String>]`: nazwa wyniku uruchomienia</span><span class="sxs-lookup"><span data-stu-id="d2edc-148">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="d2edc-149">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d2edc-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d2edc-150">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="d2edc-150">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d2edc-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d2edc-151">RELATED LINKS</span></span>

