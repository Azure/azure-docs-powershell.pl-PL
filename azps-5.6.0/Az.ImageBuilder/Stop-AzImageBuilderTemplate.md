---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/powershell/module/az.imagebuilder/stop-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Stop-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Stop-AzImageBuilderTemplate.md
ms.openlocfilehash: 7b32d3e3b03cfd38ba4cc6eda896eae92674d530
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963025"
---
# <span data-ttu-id="47e44-101">Stop-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="47e44-101">Stop-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="47e44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47e44-102">SYNOPSIS</span></span>
<span data-ttu-id="47e44-103">Anulowanie długo działającej kompilacji obrazu opartej na szablonie obrazu</span><span class="sxs-lookup"><span data-stu-id="47e44-103">Cancel the long running image build based on the image template</span></span>

## <span data-ttu-id="47e44-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="47e44-104">SYNTAX</span></span>

### <span data-ttu-id="47e44-105">Anuluj (domyślne)</span><span class="sxs-lookup"><span data-stu-id="47e44-105">Cancel (Default)</span></span>
```
Stop-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="47e44-106">CancelViaIdentity</span><span class="sxs-lookup"><span data-stu-id="47e44-106">CancelViaIdentity</span></span>
```
Stop-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="47e44-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="47e44-107">DESCRIPTION</span></span>
<span data-ttu-id="47e44-108">Anulowanie długo działającej kompilacji obrazu opartej na szablonie obrazu</span><span class="sxs-lookup"><span data-stu-id="47e44-108">Cancel the long running image build based on the image template</span></span>

## <span data-ttu-id="47e44-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="47e44-109">EXAMPLES</span></span>

### <span data-ttu-id="47e44-110">Przykład 1. Zatrzymywanie tworzenia szablonów obrazów</span><span class="sxs-lookup"><span data-stu-id="47e44-110">Example 1: Stop image template creation</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder -AsJob 

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Start-AzImageB…                 Running       True            localhost            Start-AzImageBuilderTemp…

PS C:\> Stop-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder

```

<span data-ttu-id="47e44-111">To polecenie zatrzymuje tworzenie szablonu obrazu.</span><span class="sxs-lookup"><span data-stu-id="47e44-111">This command stops image template creation.</span></span>

### <span data-ttu-id="47e44-112">Przykład 2. Zatrzymywanie tworzenia szablonów obrazów</span><span class="sxs-lookup"><span data-stu-id="47e44-112">Example 2: Stop image template creation</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder -AsJob 

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
2      Start-AzImageB…                 Running       True            localhost            Start-AzImageBuilderTemp…

PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg
PS C:\> Stop-AzImageBuilderTemplate -InputObject $template 

```

<span data-ttu-id="47e44-113">To polecenie zatrzymuje tworzenie szablonu obrazu.</span><span class="sxs-lookup"><span data-stu-id="47e44-113">This command stops image template creation.</span></span>

## <span data-ttu-id="47e44-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47e44-114">PARAMETERS</span></span>

### <span data-ttu-id="47e44-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="47e44-115">-AsJob</span></span>
<span data-ttu-id="47e44-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="47e44-116">Run the command as a job</span></span>

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

### <span data-ttu-id="47e44-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47e44-117">-DefaultProfile</span></span>
<span data-ttu-id="47e44-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="47e44-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47e44-119">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="47e44-119">-ImageTemplateName</span></span>
<span data-ttu-id="47e44-120">Nazwa szablonu obrazu</span><span class="sxs-lookup"><span data-stu-id="47e44-120">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Cancel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47e44-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47e44-121">-InputObject</span></span>
<span data-ttu-id="47e44-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="47e44-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity
Parameter Sets: CancelViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47e44-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="47e44-123">-NoWait</span></span>
<span data-ttu-id="47e44-124">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="47e44-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="47e44-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="47e44-125">-PassThru</span></span>
<span data-ttu-id="47e44-126">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="47e44-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="47e44-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47e44-127">-ResourceGroupName</span></span>
<span data-ttu-id="47e44-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="47e44-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Cancel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47e44-129">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="47e44-129">-SubscriptionId</span></span>
<span data-ttu-id="47e44-130">Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="47e44-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="47e44-131">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="47e44-131">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Cancel
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47e44-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="47e44-132">-Confirm</span></span>
<span data-ttu-id="47e44-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="47e44-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47e44-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47e44-134">-WhatIf</span></span>
<span data-ttu-id="47e44-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47e44-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47e44-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="47e44-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47e44-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47e44-137">CommonParameters</span></span>
<span data-ttu-id="47e44-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47e44-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47e44-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47e44-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47e44-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="47e44-140">INPUTS</span></span>

### <span data-ttu-id="47e44-141">Microsoft.Azure.PowerShell.Cmdlet.ImageBuilder.Models.IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="47e44-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="47e44-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="47e44-142">OUTPUTS</span></span>

### <span data-ttu-id="47e44-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="47e44-143">System.Boolean</span></span>

## <span data-ttu-id="47e44-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="47e44-144">NOTES</span></span>

<span data-ttu-id="47e44-145">ALIASY</span><span class="sxs-lookup"><span data-stu-id="47e44-145">ALIASES</span></span>

<span data-ttu-id="47e44-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="47e44-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="47e44-147">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="47e44-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="47e44-148">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="47e44-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="47e44-149">INPUTOBJECT: <IImageBuilderIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="47e44-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="47e44-150">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="47e44-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="47e44-151">`[ImageTemplateName <String>]`: nazwa szablonu obrazu</span><span class="sxs-lookup"><span data-stu-id="47e44-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="47e44-152">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="47e44-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="47e44-153">`[RunOutputName <String>]`: nazwa wyniku uruchomienia</span><span class="sxs-lookup"><span data-stu-id="47e44-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="47e44-154">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="47e44-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="47e44-155">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="47e44-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="47e44-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="47e44-156">RELATED LINKS</span></span>

