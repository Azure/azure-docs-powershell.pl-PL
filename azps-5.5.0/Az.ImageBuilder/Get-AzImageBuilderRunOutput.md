---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/get-azimagebuilderrunoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
ms.openlocfilehash: 4cc45f3b4cd21e41f1b2e410dd2b76b9571a4431
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192451"
---
# <span data-ttu-id="1ffdc-101">Get-AzImageBuilderRunOutput</span><span class="sxs-lookup"><span data-stu-id="1ffdc-101">Get-AzImageBuilderRunOutput</span></span>

## <span data-ttu-id="1ffdc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ffdc-102">SYNOPSIS</span></span>
<span data-ttu-id="1ffdc-103">Uzyskiwanie określonego wyniku uruchomienia dla określonego zasobu szablonu obrazu</span><span class="sxs-lookup"><span data-stu-id="1ffdc-103">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="1ffdc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1ffdc-104">SYNTAX</span></span>

### <span data-ttu-id="1ffdc-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="1ffdc-105">List (Default)</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1ffdc-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="1ffdc-106">Get</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String> -RunOutputName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1ffdc-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1ffdc-107">GetViaIdentity</span></span>
```
Get-AzImageBuilderRunOutput -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="1ffdc-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="1ffdc-108">DESCRIPTION</span></span>
<span data-ttu-id="1ffdc-109">Uzyskiwanie określonego wyniku uruchomienia dla określonego zasobu szablonu obrazu</span><span class="sxs-lookup"><span data-stu-id="1ffdc-109">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="1ffdc-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1ffdc-110">EXAMPLES</span></span>

### <span data-ttu-id="1ffdc-111">Przykład 1. Lista wszystkich wyników uruchomienia w szablonie</span><span class="sxs-lookup"><span data-stu-id="1ffdc-111">Example 1: List all run results under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName lucas-imagetemplate -ResourceGroupName wyunchi-imagebuilder

Name          Type
----          ----
image_lucas_1 Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="1ffdc-112">To polecenie wyświetla listę wszystkich wyników uruchamiania w szablonie.</span><span class="sxs-lookup"><span data-stu-id="1ffdc-112">This command lists all run results under a template.</span></span>

### <span data-ttu-id="1ffdc-113">Przykład 2. Uzyskiwanie wyniku uruchomienia w szablonie</span><span class="sxs-lookup"><span data-stu-id="1ffdc-113">Example 2: Get a run result under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx 

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="1ffdc-114">To polecenie uzyskuje wynik uruchomienia w obszarze szablonu.</span><span class="sxs-lookup"><span data-stu-id="1ffdc-114">This command gets a run result under a template.</span></span>

### <span data-ttu-id="1ffdc-115">Przykład 3. Uzyskiwanie wyniku uruchomienia w szablonie</span><span class="sxs-lookup"><span data-stu-id="1ffdc-115">Example 3: Get a run result under a template</span></span>
```powershell
PS C:\> $result = Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx
PS C:\> Get-AzImageBuilderRunOutput -InputObject $result

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="1ffdc-116">To polecenie uzyskuje wynik uruchomienia w obszarze szablonu.</span><span class="sxs-lookup"><span data-stu-id="1ffdc-116">This command gets a run result under a template.</span></span>

## <span data-ttu-id="1ffdc-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ffdc-117">PARAMETERS</span></span>

### <span data-ttu-id="1ffdc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ffdc-118">-DefaultProfile</span></span>
<span data-ttu-id="1ffdc-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1ffdc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ffdc-120">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="1ffdc-120">-ImageTemplateName</span></span>
<span data-ttu-id="1ffdc-121">Nazwa szablonu obrazu</span><span class="sxs-lookup"><span data-stu-id="1ffdc-121">The name of the image Template</span></span>

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

### <span data-ttu-id="1ffdc-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ffdc-122">-InputObject</span></span>
<span data-ttu-id="1ffdc-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="1ffdc-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1ffdc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ffdc-124">-ResourceGroupName</span></span>
<span data-ttu-id="1ffdc-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1ffdc-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="1ffdc-126">-RunOutputName</span><span class="sxs-lookup"><span data-stu-id="1ffdc-126">-RunOutputName</span></span>
<span data-ttu-id="1ffdc-127">Nazwa wyniku uruchomienia</span><span class="sxs-lookup"><span data-stu-id="1ffdc-127">The name of the run output</span></span>

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

### <span data-ttu-id="1ffdc-128">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1ffdc-128">-SubscriptionId</span></span>
<span data-ttu-id="1ffdc-129">Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1ffdc-129">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1ffdc-130">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia usługi.</span><span class="sxs-lookup"><span data-stu-id="1ffdc-130">The subscription Id forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1ffdc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ffdc-131">CommonParameters</span></span>
<span data-ttu-id="1ffdc-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ffdc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ffdc-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1ffdc-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ffdc-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1ffdc-134">INPUTS</span></span>

### <span data-ttu-id="1ffdc-135">Microsoft.Azure.PowerShell.Cmdlet.ImageBuilder.Models.IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="1ffdc-135">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="1ffdc-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1ffdc-136">OUTPUTS</span></span>

### <span data-ttu-id="1ffdc-137">Microsoft.Azure.PowerShell.cmdlet.ImageBuilder.Models.Api20200214.IRunOutput</span><span class="sxs-lookup"><span data-stu-id="1ffdc-137">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IRunOutput</span></span>

## <span data-ttu-id="1ffdc-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1ffdc-138">NOTES</span></span>

<span data-ttu-id="1ffdc-139">ALIASY</span><span class="sxs-lookup"><span data-stu-id="1ffdc-139">ALIASES</span></span>

<span data-ttu-id="1ffdc-140">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1ffdc-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1ffdc-141">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="1ffdc-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1ffdc-142">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1ffdc-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1ffdc-143">INPUTOBJECT: <IImageBuilderIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="1ffdc-143">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1ffdc-144">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="1ffdc-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1ffdc-145">`[ImageTemplateName <String>]`: nazwa szablonu obrazu</span><span class="sxs-lookup"><span data-stu-id="1ffdc-145">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="1ffdc-146">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1ffdc-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="1ffdc-147">`[RunOutputName <String>]`: nazwa wyniku uruchomienia</span><span class="sxs-lookup"><span data-stu-id="1ffdc-147">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="1ffdc-148">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1ffdc-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="1ffdc-149">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia usługi.</span><span class="sxs-lookup"><span data-stu-id="1ffdc-149">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="1ffdc-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1ffdc-150">RELATED LINKS</span></span>

