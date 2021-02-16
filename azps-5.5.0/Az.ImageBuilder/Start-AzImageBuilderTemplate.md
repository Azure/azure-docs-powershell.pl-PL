---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/start-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Start-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Start-AzImageBuilderTemplate.md
ms.openlocfilehash: 710c39adca3f3a82b91b1e27a7f63e0ef1f6b693
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194338"
---
# <span data-ttu-id="ed2e4-101">Start-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="ed2e4-101">Start-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="ed2e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed2e4-102">SYNOPSIS</span></span>
<span data-ttu-id="ed2e4-103">Tworzenie artefaktów na podstawie istniejącego szablonu obrazu</span><span class="sxs-lookup"><span data-stu-id="ed2e4-103">Create artifacts from a existing image template</span></span>

## <span data-ttu-id="ed2e4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ed2e4-104">SYNTAX</span></span>

### <span data-ttu-id="ed2e4-105">Uruchamianie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="ed2e4-105">Run (Default)</span></span>
```
Start-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="ed2e4-106">RunViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ed2e4-106">RunViaIdentity</span></span>
```
Start-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ed2e4-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="ed2e4-107">DESCRIPTION</span></span>
<span data-ttu-id="ed2e4-108">Tworzenie artefaktów na podstawie istniejącego szablonu obrazu</span><span class="sxs-lookup"><span data-stu-id="ed2e4-108">Create artifacts from a existing image template</span></span>

## <span data-ttu-id="ed2e4-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ed2e4-109">EXAMPLES</span></span>

### <span data-ttu-id="ed2e4-110">Przykład 1. Uruchamianie szablonu obrazu</span><span class="sxs-lookup"><span data-stu-id="ed2e4-110">Example 1: Start an image template</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg

```

<span data-ttu-id="ed2e4-111">To polecenie pozwala na rozpoczęcie pracy z szablonem obrazu.</span><span class="sxs-lookup"><span data-stu-id="ed2e4-111">This command starts an image template.</span></span>

### <span data-ttu-id="ed2e4-112">Przykład 2. Uruchamianie szablonu obrazu</span><span class="sxs-lookup"><span data-stu-id="ed2e4-112">Example 2: Start an image template</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg
PS C:\> Start-AzImageBuilderTemplate -InputObject $template

```

<span data-ttu-id="ed2e4-113">To polecenie pozwala na rozpoczęcie pracy z szablonem obrazu.</span><span class="sxs-lookup"><span data-stu-id="ed2e4-113">This command starts an image template.</span></span>

## <span data-ttu-id="ed2e4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed2e4-114">PARAMETERS</span></span>

### <span data-ttu-id="ed2e4-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="ed2e4-115">-AsJob</span></span>
<span data-ttu-id="ed2e4-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="ed2e4-116">Run the command as a job</span></span>

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

### <span data-ttu-id="ed2e4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed2e4-117">-DefaultProfile</span></span>
<span data-ttu-id="ed2e4-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ed2e4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed2e4-119">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="ed2e4-119">-ImageTemplateName</span></span>
<span data-ttu-id="ed2e4-120">Nazwa szablonu obrazu</span><span class="sxs-lookup"><span data-stu-id="ed2e4-120">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Run
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed2e4-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed2e4-121">-InputObject</span></span>
<span data-ttu-id="ed2e4-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="ed2e4-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity
Parameter Sets: RunViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed2e4-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ed2e4-123">-NoWait</span></span>
<span data-ttu-id="ed2e4-124">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="ed2e4-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ed2e4-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ed2e4-125">-PassThru</span></span>
<span data-ttu-id="ed2e4-126">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="ed2e4-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ed2e4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed2e4-127">-ResourceGroupName</span></span>
<span data-ttu-id="ed2e4-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ed2e4-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Run
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed2e4-129">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ed2e4-129">-SubscriptionId</span></span>
<span data-ttu-id="ed2e4-130">Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ed2e4-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ed2e4-131">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia usługi.</span><span class="sxs-lookup"><span data-stu-id="ed2e4-131">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Run
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed2e4-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ed2e4-132">-Confirm</span></span>
<span data-ttu-id="ed2e4-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ed2e4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed2e4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed2e4-134">-WhatIf</span></span>
<span data-ttu-id="ed2e4-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed2e4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed2e4-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ed2e4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed2e4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed2e4-137">CommonParameters</span></span>
<span data-ttu-id="ed2e4-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed2e4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed2e4-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed2e4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed2e4-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed2e4-140">INPUTS</span></span>

### <span data-ttu-id="ed2e4-141">Microsoft.Azure.PowerShell.Cmdlet.ImageBuilder.Models.IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="ed2e4-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="ed2e4-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ed2e4-142">OUTPUTS</span></span>

### <span data-ttu-id="ed2e4-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ed2e4-143">System.Boolean</span></span>

## <span data-ttu-id="ed2e4-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ed2e4-144">NOTES</span></span>

<span data-ttu-id="ed2e4-145">ALIASY</span><span class="sxs-lookup"><span data-stu-id="ed2e4-145">ALIASES</span></span>

<span data-ttu-id="ed2e4-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ed2e4-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ed2e4-147">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="ed2e4-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ed2e4-148">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ed2e4-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ed2e4-149">INPUTOBJECT: <IImageBuilderIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="ed2e4-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ed2e4-150">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="ed2e4-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ed2e4-151">`[ImageTemplateName <String>]`: nazwa szablonu obrazu</span><span class="sxs-lookup"><span data-stu-id="ed2e4-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="ed2e4-152">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ed2e4-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="ed2e4-153">`[RunOutputName <String>]`: nazwa wyniku uruchomienia</span><span class="sxs-lookup"><span data-stu-id="ed2e4-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="ed2e4-154">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ed2e4-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ed2e4-155">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia usługi.</span><span class="sxs-lookup"><span data-stu-id="ed2e4-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ed2e4-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ed2e4-156">RELATED LINKS</span></span>

