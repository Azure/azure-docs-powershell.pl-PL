---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/powershell/module/az.imagebuilder/get-azimagebuilderrunoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
ms.openlocfilehash: 4f1c88e48847c1ecf560d7ed9d390131455b1d39
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013082"
---
# <span data-ttu-id="774dc-101">Get-AzImageBuilderRunOutput</span><span class="sxs-lookup"><span data-stu-id="774dc-101">Get-AzImageBuilderRunOutput</span></span>

## <span data-ttu-id="774dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="774dc-102">SYNOPSIS</span></span>
<span data-ttu-id="774dc-103">Uzyskiwanie określonego wyniku uruchomienia dla określonego zasobu szablonu obrazu</span><span class="sxs-lookup"><span data-stu-id="774dc-103">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="774dc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="774dc-104">SYNTAX</span></span>

### <span data-ttu-id="774dc-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="774dc-105">List (Default)</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="774dc-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="774dc-106">Get</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String> -RunOutputName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="774dc-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="774dc-107">GetViaIdentity</span></span>
```
Get-AzImageBuilderRunOutput -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="774dc-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="774dc-108">DESCRIPTION</span></span>
<span data-ttu-id="774dc-109">Uzyskiwanie określonego wyniku uruchomienia dla określonego zasobu szablonu obrazu</span><span class="sxs-lookup"><span data-stu-id="774dc-109">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="774dc-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="774dc-110">EXAMPLES</span></span>

### <span data-ttu-id="774dc-111">Przykład 1. Lista wszystkich wyników uruchamiania w szablonie</span><span class="sxs-lookup"><span data-stu-id="774dc-111">Example 1: List all run results under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName lucas-imagetemplate -ResourceGroupName wyunchi-imagebuilder

Name          Type
----          ----
image_lucas_1 Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="774dc-112">To polecenie wyświetla listę wszystkich wyników uruchamiania w szablonie.</span><span class="sxs-lookup"><span data-stu-id="774dc-112">This command lists all run results under a template.</span></span>

### <span data-ttu-id="774dc-113">Przykład 2. Uzyskiwanie wyniku uruchomienia w szablonie</span><span class="sxs-lookup"><span data-stu-id="774dc-113">Example 2: Get a run result under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx 

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="774dc-114">To polecenie uzyskuje wynik uruchomienia w obszarze szablonu.</span><span class="sxs-lookup"><span data-stu-id="774dc-114">This command gets a run result under a template.</span></span>

### <span data-ttu-id="774dc-115">Przykład 3. Uzyskiwanie wyniku uruchomienia w szablonie</span><span class="sxs-lookup"><span data-stu-id="774dc-115">Example 3: Get a run result under a template</span></span>
```powershell
PS C:\> $result = Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx
PS C:\> Get-AzImageBuilderRunOutput -InputObject $result

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="774dc-116">To polecenie uzyskuje wynik uruchomienia w obszarze szablonu.</span><span class="sxs-lookup"><span data-stu-id="774dc-116">This command gets a run result under a template.</span></span>

## <span data-ttu-id="774dc-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="774dc-117">PARAMETERS</span></span>

### <span data-ttu-id="774dc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="774dc-118">-DefaultProfile</span></span>
<span data-ttu-id="774dc-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="774dc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="774dc-120">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="774dc-120">-ImageTemplateName</span></span>
<span data-ttu-id="774dc-121">Nazwa szablonu obrazu</span><span class="sxs-lookup"><span data-stu-id="774dc-121">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="774dc-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="774dc-122">-InputObject</span></span>
<span data-ttu-id="774dc-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="774dc-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="774dc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="774dc-124">-ResourceGroupName</span></span>
<span data-ttu-id="774dc-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="774dc-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="774dc-126">-RunOutputName</span><span class="sxs-lookup"><span data-stu-id="774dc-126">-RunOutputName</span></span>
<span data-ttu-id="774dc-127">Nazwa wyniku uruchomienia</span><span class="sxs-lookup"><span data-stu-id="774dc-127">The name of the run output</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="774dc-128">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="774dc-128">-SubscriptionId</span></span>
<span data-ttu-id="774dc-129">Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="774dc-129">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="774dc-130">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="774dc-130">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="774dc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="774dc-131">CommonParameters</span></span>
<span data-ttu-id="774dc-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="774dc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="774dc-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="774dc-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="774dc-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="774dc-134">INPUTS</span></span>

### <span data-ttu-id="774dc-135">Microsoft.Azure.PowerShell.Cmdlet.ImageBuilder.Models.IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="774dc-135">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="774dc-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="774dc-136">OUTPUTS</span></span>

### <span data-ttu-id="774dc-137">Microsoft.Azure.PowerShell.cmdlet.ImageBuilder.Models.Api20200214.IRunOutput</span><span class="sxs-lookup"><span data-stu-id="774dc-137">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IRunOutput</span></span>

## <span data-ttu-id="774dc-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="774dc-138">NOTES</span></span>

<span data-ttu-id="774dc-139">ALIASY</span><span class="sxs-lookup"><span data-stu-id="774dc-139">ALIASES</span></span>

<span data-ttu-id="774dc-140">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="774dc-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="774dc-141">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="774dc-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="774dc-142">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="774dc-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="774dc-143">INPUTOBJECT: <IImageBuilderIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="774dc-143">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="774dc-144">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="774dc-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="774dc-145">`[ImageTemplateName <String>]`: nazwa szablonu obrazu</span><span class="sxs-lookup"><span data-stu-id="774dc-145">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="774dc-146">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="774dc-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="774dc-147">`[RunOutputName <String>]`: nazwa wyniku uruchomienia</span><span class="sxs-lookup"><span data-stu-id="774dc-147">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="774dc-148">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="774dc-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="774dc-149">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="774dc-149">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="774dc-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="774dc-150">RELATED LINKS</span></span>

