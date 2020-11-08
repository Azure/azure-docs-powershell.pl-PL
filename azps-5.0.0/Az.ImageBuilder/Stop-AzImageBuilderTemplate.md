---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/stop-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Stop-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Stop-AzImageBuilderTemplate.md
ms.openlocfilehash: 01fd95dd41a7ee76c06f0423d33c4aba34329c18
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94231841"
---
# <span data-ttu-id="fa174-101">Stop-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="fa174-101">Stop-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="fa174-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fa174-102">SYNOPSIS</span></span>
<span data-ttu-id="fa174-103">Anulowanie długotrwałego działania kompilacji obrazu na podstawie szablonu obrazu</span><span class="sxs-lookup"><span data-stu-id="fa174-103">Cancel the long running image build based on the image template</span></span>

## <span data-ttu-id="fa174-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fa174-104">SYNTAX</span></span>

### <span data-ttu-id="fa174-105">Anuluj (domyślne)</span><span class="sxs-lookup"><span data-stu-id="fa174-105">Cancel (Default)</span></span>
```
Stop-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fa174-106">CancelViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fa174-106">CancelViaIdentity</span></span>
```
Stop-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fa174-107">Opis</span><span class="sxs-lookup"><span data-stu-id="fa174-107">DESCRIPTION</span></span>
<span data-ttu-id="fa174-108">Anulowanie długotrwałego działania kompilacji obrazu na podstawie szablonu obrazu</span><span class="sxs-lookup"><span data-stu-id="fa174-108">Cancel the long running image build based on the image template</span></span>

## <span data-ttu-id="fa174-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fa174-109">EXAMPLES</span></span>

### <span data-ttu-id="fa174-110">Przykład 1: zatrzymywanie tworzenia szablonu obrazu</span><span class="sxs-lookup"><span data-stu-id="fa174-110">Example 1: Stop image template creation</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder -AsJob 

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Start-AzImageB…                 Running       True            localhost            Start-AzImageBuilderTemp…

PS C:\> Stop-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder

```

<span data-ttu-id="fa174-111">To polecenie powoduje zatrzymanie tworzenia szablonu obrazu.</span><span class="sxs-lookup"><span data-stu-id="fa174-111">This command stops image template creation.</span></span>

### <span data-ttu-id="fa174-112">Przykład 2: zatrzymywanie tworzenia szablonu obrazu</span><span class="sxs-lookup"><span data-stu-id="fa174-112">Example 2: Stop image template creation</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ImageTemplateName template-name-sn78hg -ResourceGroupName wyunchi-imagebuilder -AsJob 

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
2      Start-AzImageB…                 Running       True            localhost            Start-AzImageBuilderTemp…

PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg
PS C:\> Stop-AzImageBuilderTemplate -InputObject $template 

```

<span data-ttu-id="fa174-113">To polecenie powoduje zatrzymanie tworzenia szablonu obrazu.</span><span class="sxs-lookup"><span data-stu-id="fa174-113">This command stops image template creation.</span></span>

## <span data-ttu-id="fa174-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fa174-114">PARAMETERS</span></span>

### <span data-ttu-id="fa174-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa174-115">-AsJob</span></span>
<span data-ttu-id="fa174-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="fa174-116">Run the command as a job</span></span>

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

### <span data-ttu-id="fa174-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa174-117">-DefaultProfile</span></span>
<span data-ttu-id="fa174-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fa174-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa174-119">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="fa174-119">-ImageTemplateName</span></span>
<span data-ttu-id="fa174-120">Nazwa szablonu obrazu</span><span class="sxs-lookup"><span data-stu-id="fa174-120">The name of the image Template</span></span>

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

### <span data-ttu-id="fa174-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fa174-121">-InputObject</span></span>
<span data-ttu-id="fa174-122">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="fa174-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="fa174-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="fa174-123">-NoWait</span></span>
<span data-ttu-id="fa174-124">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="fa174-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fa174-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa174-125">-PassThru</span></span>
<span data-ttu-id="fa174-126">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="fa174-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="fa174-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa174-127">-ResourceGroupName</span></span>
<span data-ttu-id="fa174-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fa174-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="fa174-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="fa174-129">-SubscriptionId</span></span>
<span data-ttu-id="fa174-130">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fa174-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="fa174-131">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="fa174-131">The subscription Id forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="fa174-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fa174-132">-Confirm</span></span>
<span data-ttu-id="fa174-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa174-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa174-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa174-134">-WhatIf</span></span>
<span data-ttu-id="fa174-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa174-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa174-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fa174-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa174-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa174-137">CommonParameters</span></span>
<span data-ttu-id="fa174-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa174-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa174-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fa174-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa174-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fa174-140">INPUTS</span></span>

### <span data-ttu-id="fa174-141">Microsoft. Azure. PowerShell. polecenia. ImageBuilder. models. IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="fa174-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="fa174-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fa174-142">OUTPUTS</span></span>

### <span data-ttu-id="fa174-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fa174-143">System.Boolean</span></span>

## <span data-ttu-id="fa174-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fa174-144">NOTES</span></span>

<span data-ttu-id="fa174-145">PISUJE</span><span class="sxs-lookup"><span data-stu-id="fa174-145">ALIASES</span></span>

<span data-ttu-id="fa174-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fa174-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fa174-147">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="fa174-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fa174-148">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fa174-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fa174-149">INPUTobject <IImageBuilderIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="fa174-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fa174-150">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="fa174-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fa174-151">`[ImageTemplateName <String>]`: Nazwa szablonu obrazu</span><span class="sxs-lookup"><span data-stu-id="fa174-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="fa174-152">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fa174-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="fa174-153">`[RunOutputName <String>]`: Nazwa wyjścia do uruchomienia</span><span class="sxs-lookup"><span data-stu-id="fa174-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="fa174-154">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fa174-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="fa174-155">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="fa174-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="fa174-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fa174-156">RELATED LINKS</span></span>

