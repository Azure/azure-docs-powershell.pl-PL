---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/stop-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Stop-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Stop-AzImageBuilderTemplate.md
ms.openlocfilehash: 01fd95dd41a7ee76c06f0423d33c4aba34329c18
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194330"
---
# <span data-ttu-id="d2f8e-101">Stop-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="d2f8e-101">Stop-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="d2f8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2f8e-102">SYNOPSIS</span></span>
<span data-ttu-id="d2f8e-103">Anulowanie długo działającej kompilacji obrazu opartej na szablonie obrazu</span><span class="sxs-lookup"><span data-stu-id="d2f8e-103">Cancel the long running image build based on the image template</span></span>

## <span data-ttu-id="d2f8e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d2f8e-104">SYNTAX</span></span>

### <span data-ttu-id="d2f8e-105">Anuluj (domyślne)</span><span class="sxs-lookup"><span data-stu-id="d2f8e-105">Cancel (Default)</span></span>
```
Stop-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d2f8e-106">CancelViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d2f8e-106">CancelViaIdentity</span></span>
```
Stop-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d2f8e-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d2f8e-107">DESCRIPTION</span></span>
<span data-ttu-id="d2f8e-108">Anulowanie długo działającej kompilacji obrazu opartej na szablonie obrazu</span><span class="sxs-lookup"><span data-stu-id="d2f8e-108">Cancel the long running image build based on the image template</span></span>

## <span data-ttu-id="d2f8e-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d2f8e-109">EXAMPLES</span></span>

### <span data-ttu-id="d2f8e-110">Przykład 1. Zatrzymywanie tworzenia szablonów obrazów</span><span class="sxs-lookup"><span data-stu-id="d2f8e-110">Example 1: Stop image template creation</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder -AsJob 

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Start-AzImageB…                 Running       True            localhost            Start-AzImageBuilderTemp…

PS C:\> Stop-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder

```

<span data-ttu-id="d2f8e-111">To polecenie zatrzymuje tworzenie szablonu obrazu.</span><span class="sxs-lookup"><span data-stu-id="d2f8e-111">This command stops image template creation.</span></span>

### <span data-ttu-id="d2f8e-112">Przykład 2. Zatrzymywanie tworzenia szablonów obrazów</span><span class="sxs-lookup"><span data-stu-id="d2f8e-112">Example 2: Stop image template creation</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder -AsJob 

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
2      Start-AzImageB…                 Running       True            localhost            Start-AzImageBuilderTemp…

PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg
PS C:\> Stop-AzImageBuilderTemplate -InputObject $template 

```

<span data-ttu-id="d2f8e-113">To polecenie zatrzymuje tworzenie szablonu obrazu.</span><span class="sxs-lookup"><span data-stu-id="d2f8e-113">This command stops image template creation.</span></span>

## <span data-ttu-id="d2f8e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2f8e-114">PARAMETERS</span></span>

### <span data-ttu-id="d2f8e-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d2f8e-115">-AsJob</span></span>
<span data-ttu-id="d2f8e-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="d2f8e-116">Run the command as a job</span></span>

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

### <span data-ttu-id="d2f8e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2f8e-117">-DefaultProfile</span></span>
<span data-ttu-id="d2f8e-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d2f8e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2f8e-119">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="d2f8e-119">-ImageTemplateName</span></span>
<span data-ttu-id="d2f8e-120">Nazwa szablonu obrazu</span><span class="sxs-lookup"><span data-stu-id="d2f8e-120">The name of the image Template</span></span>

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

### <span data-ttu-id="d2f8e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2f8e-121">-InputObject</span></span>
<span data-ttu-id="d2f8e-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="d2f8e-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d2f8e-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d2f8e-123">-NoWait</span></span>
<span data-ttu-id="d2f8e-124">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="d2f8e-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d2f8e-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2f8e-125">-PassThru</span></span>
<span data-ttu-id="d2f8e-126">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="d2f8e-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d2f8e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2f8e-127">-ResourceGroupName</span></span>
<span data-ttu-id="d2f8e-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d2f8e-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="d2f8e-129">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d2f8e-129">-SubscriptionId</span></span>
<span data-ttu-id="d2f8e-130">Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d2f8e-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d2f8e-131">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia usługi.</span><span class="sxs-lookup"><span data-stu-id="d2f8e-131">The subscription Id forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d2f8e-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d2f8e-132">-Confirm</span></span>
<span data-ttu-id="d2f8e-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d2f8e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2f8e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2f8e-134">-WhatIf</span></span>
<span data-ttu-id="d2f8e-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2f8e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2f8e-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d2f8e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2f8e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2f8e-137">CommonParameters</span></span>
<span data-ttu-id="d2f8e-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2f8e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2f8e-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d2f8e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2f8e-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2f8e-140">INPUTS</span></span>

### <span data-ttu-id="d2f8e-141">Microsoft.Azure.PowerShell.Cmdlet.ImageBuilder.Models.IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="d2f8e-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="d2f8e-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d2f8e-142">OUTPUTS</span></span>

### <span data-ttu-id="d2f8e-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d2f8e-143">System.Boolean</span></span>

## <span data-ttu-id="d2f8e-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d2f8e-144">NOTES</span></span>

<span data-ttu-id="d2f8e-145">ALIASY</span><span class="sxs-lookup"><span data-stu-id="d2f8e-145">ALIASES</span></span>

<span data-ttu-id="d2f8e-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="d2f8e-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d2f8e-147">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="d2f8e-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d2f8e-148">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d2f8e-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d2f8e-149">INPUTOBJECT: <IImageBuilderIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="d2f8e-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d2f8e-150">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="d2f8e-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d2f8e-151">`[ImageTemplateName <String>]`: nazwa szablonu obrazu</span><span class="sxs-lookup"><span data-stu-id="d2f8e-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="d2f8e-152">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d2f8e-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="d2f8e-153">`[RunOutputName <String>]`: nazwa wyniku uruchomienia</span><span class="sxs-lookup"><span data-stu-id="d2f8e-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="d2f8e-154">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d2f8e-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d2f8e-155">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia usługi.</span><span class="sxs-lookup"><span data-stu-id="d2f8e-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d2f8e-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d2f8e-156">RELATED LINKS</span></span>

