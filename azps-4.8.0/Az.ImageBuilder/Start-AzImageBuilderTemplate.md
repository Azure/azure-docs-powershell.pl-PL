---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/start-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Start-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Start-AzImageBuilderTemplate.md
ms.openlocfilehash: 710c39adca3f3a82b91b1e27a7f63e0ef1f6b693
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221722"
---
# <span data-ttu-id="41c9c-101">Start-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="41c9c-101">Start-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="41c9c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="41c9c-102">SYNOPSIS</span></span>
<span data-ttu-id="41c9c-103">Tworzenie artefaktów z istniejącego szablonu obrazu</span><span class="sxs-lookup"><span data-stu-id="41c9c-103">Create artifacts from a existing image template</span></span>

## <span data-ttu-id="41c9c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="41c9c-104">SYNTAX</span></span>

### <span data-ttu-id="41c9c-105">Uruchom (domyślne)</span><span class="sxs-lookup"><span data-stu-id="41c9c-105">Run (Default)</span></span>
```
Start-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="41c9c-106">RunViaIdentity</span><span class="sxs-lookup"><span data-stu-id="41c9c-106">RunViaIdentity</span></span>
```
Start-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="41c9c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="41c9c-107">DESCRIPTION</span></span>
<span data-ttu-id="41c9c-108">Tworzenie artefaktów z istniejącego szablonu obrazu</span><span class="sxs-lookup"><span data-stu-id="41c9c-108">Create artifacts from a existing image template</span></span>

## <span data-ttu-id="41c9c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="41c9c-109">EXAMPLES</span></span>

### <span data-ttu-id="41c9c-110">Przykład 1. Rozpocznij szablon obrazu</span><span class="sxs-lookup"><span data-stu-id="41c9c-110">Example 1: Start an image template</span></span>
```powershell
PS C:\> Start-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg

```

<span data-ttu-id="41c9c-111">To polecenie rozpoczyna szablon obrazu.</span><span class="sxs-lookup"><span data-stu-id="41c9c-111">This command starts an image template.</span></span>

### <span data-ttu-id="41c9c-112">Przykład 2: Rozpoczynanie szablonu obrazu</span><span class="sxs-lookup"><span data-stu-id="41c9c-112">Example 2: Start an image template</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg
PS C:\> Start-AzImageBuilderTemplate -InputObject $template

```

<span data-ttu-id="41c9c-113">To polecenie rozpoczyna szablon obrazu.</span><span class="sxs-lookup"><span data-stu-id="41c9c-113">This command starts an image template.</span></span>

## <span data-ttu-id="41c9c-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="41c9c-114">PARAMETERS</span></span>

### <span data-ttu-id="41c9c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41c9c-115">-AsJob</span></span>
<span data-ttu-id="41c9c-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="41c9c-116">Run the command as a job</span></span>

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

### <span data-ttu-id="41c9c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41c9c-117">-DefaultProfile</span></span>
<span data-ttu-id="41c9c-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="41c9c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41c9c-119">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="41c9c-119">-ImageTemplateName</span></span>
<span data-ttu-id="41c9c-120">Nazwa szablonu obrazu</span><span class="sxs-lookup"><span data-stu-id="41c9c-120">The name of the image Template</span></span>

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

### <span data-ttu-id="41c9c-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="41c9c-121">-InputObject</span></span>
<span data-ttu-id="41c9c-122">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="41c9c-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="41c9c-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="41c9c-123">-NoWait</span></span>
<span data-ttu-id="41c9c-124">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="41c9c-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="41c9c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41c9c-125">-PassThru</span></span>
<span data-ttu-id="41c9c-126">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="41c9c-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="41c9c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41c9c-127">-ResourceGroupName</span></span>
<span data-ttu-id="41c9c-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="41c9c-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="41c9c-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="41c9c-129">-SubscriptionId</span></span>
<span data-ttu-id="41c9c-130">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="41c9c-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="41c9c-131">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="41c9c-131">The subscription Id forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="41c9c-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="41c9c-132">-Confirm</span></span>
<span data-ttu-id="41c9c-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41c9c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41c9c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41c9c-134">-WhatIf</span></span>
<span data-ttu-id="41c9c-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41c9c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41c9c-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="41c9c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41c9c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41c9c-137">CommonParameters</span></span>
<span data-ttu-id="41c9c-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41c9c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41c9c-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41c9c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41c9c-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41c9c-140">INPUTS</span></span>

### <span data-ttu-id="41c9c-141">Microsoft. Azure. PowerShell. polecenia. ImageBuilder. models. IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="41c9c-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="41c9c-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="41c9c-142">OUTPUTS</span></span>

### <span data-ttu-id="41c9c-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="41c9c-143">System.Boolean</span></span>

## <span data-ttu-id="41c9c-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="41c9c-144">NOTES</span></span>

<span data-ttu-id="41c9c-145">PISUJE</span><span class="sxs-lookup"><span data-stu-id="41c9c-145">ALIASES</span></span>

<span data-ttu-id="41c9c-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="41c9c-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="41c9c-147">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="41c9c-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="41c9c-148">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="41c9c-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="41c9c-149">INPUTobject <IImageBuilderIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="41c9c-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="41c9c-150">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="41c9c-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="41c9c-151">`[ImageTemplateName <String>]`: Nazwa szablonu obrazu</span><span class="sxs-lookup"><span data-stu-id="41c9c-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="41c9c-152">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="41c9c-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="41c9c-153">`[RunOutputName <String>]`: Nazwa wyjścia do uruchomienia</span><span class="sxs-lookup"><span data-stu-id="41c9c-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="41c9c-154">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="41c9c-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="41c9c-155">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="41c9c-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="41c9c-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="41c9c-156">RELATED LINKS</span></span>

