---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/remove-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Remove-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Remove-AzImageBuilderTemplate.md
ms.openlocfilehash: 998c4f05e8b6a03749a4872e3f4b069e29ef634d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503541"
---
# <span data-ttu-id="46d79-101">Remove-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="46d79-101">Remove-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="46d79-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="46d79-102">SYNOPSIS</span></span>
<span data-ttu-id="46d79-103">Usuwanie szablonu obrazu maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="46d79-103">Delete a virtual machine image template</span></span>

## <span data-ttu-id="46d79-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="46d79-104">SYNTAX</span></span>

### <span data-ttu-id="46d79-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="46d79-105">Delete (Default)</span></span>
```
Remove-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="46d79-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="46d79-106">DeleteViaIdentity</span></span>
```
Remove-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="46d79-107">Opis</span><span class="sxs-lookup"><span data-stu-id="46d79-107">DESCRIPTION</span></span>
<span data-ttu-id="46d79-108">Usuwanie szablonu obrazu maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="46d79-108">Delete a virtual machine image template</span></span>

## <span data-ttu-id="46d79-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="46d79-109">EXAMPLES</span></span>

### <span data-ttu-id="46d79-110">Przykład 1: usuwanie szablonu obrazu</span><span class="sxs-lookup"><span data-stu-id="46d79-110">Example 1: Remove a image template</span></span>
```powershell
PS C:\> Remove-AzImageBuilderTemplate -ImageTemplateName template-name-dmt6ze -ResourceGroupName wyunchi-imagebuilder

```

<span data-ttu-id="46d79-111">To polecenie umożliwia usunięcie szablonu obrazu.</span><span class="sxs-lookup"><span data-stu-id="46d79-111">This command removes a image template.</span></span>

### <span data-ttu-id="46d79-112">Przykład 2: usuwanie szablonu obrazu</span><span class="sxs-lookup"><span data-stu-id="46d79-112">Example 2: Remove a image template</span></span>
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ImageTemplateName template-name-3uo8p6 -ResourceGroupName wyunchi-imagebuilder
PS C:\> Remove-AzImageBuilderTemplate -InputObject $template

```

<span data-ttu-id="46d79-113">To polecenie umożliwia usunięcie szablonu obrazu.</span><span class="sxs-lookup"><span data-stu-id="46d79-113">This command removes a image template.</span></span>

## <span data-ttu-id="46d79-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="46d79-114">PARAMETERS</span></span>

### <span data-ttu-id="46d79-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46d79-115">-AsJob</span></span>
<span data-ttu-id="46d79-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="46d79-116">Run the command as a job</span></span>

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

### <span data-ttu-id="46d79-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46d79-117">-DefaultProfile</span></span>
<span data-ttu-id="46d79-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="46d79-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46d79-119">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="46d79-119">-ImageTemplateName</span></span>
<span data-ttu-id="46d79-120">Nazwa szablonu obrazu</span><span class="sxs-lookup"><span data-stu-id="46d79-120">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46d79-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="46d79-121">-InputObject</span></span>
<span data-ttu-id="46d79-122">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="46d79-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46d79-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="46d79-123">-NoWait</span></span>
<span data-ttu-id="46d79-124">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="46d79-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="46d79-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="46d79-125">-PassThru</span></span>
<span data-ttu-id="46d79-126">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="46d79-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="46d79-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46d79-127">-ResourceGroupName</span></span>
<span data-ttu-id="46d79-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="46d79-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46d79-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="46d79-129">-SubscriptionId</span></span>
<span data-ttu-id="46d79-130">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="46d79-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="46d79-131">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="46d79-131">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46d79-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="46d79-132">-Confirm</span></span>
<span data-ttu-id="46d79-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46d79-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46d79-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46d79-134">-WhatIf</span></span>
<span data-ttu-id="46d79-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46d79-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46d79-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="46d79-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46d79-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46d79-137">CommonParameters</span></span>
<span data-ttu-id="46d79-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46d79-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46d79-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46d79-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46d79-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46d79-140">INPUTS</span></span>

### <span data-ttu-id="46d79-141">Microsoft. Azure. PowerShell. polecenia. ImageBuilder. models. IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="46d79-141">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="46d79-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="46d79-142">OUTPUTS</span></span>

### <span data-ttu-id="46d79-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="46d79-143">System.Boolean</span></span>

## <span data-ttu-id="46d79-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="46d79-144">NOTES</span></span>

<span data-ttu-id="46d79-145">PISUJE</span><span class="sxs-lookup"><span data-stu-id="46d79-145">ALIASES</span></span>

<span data-ttu-id="46d79-146">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="46d79-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="46d79-147">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="46d79-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="46d79-148">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="46d79-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="46d79-149">INPUTobject <IImageBuilderIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="46d79-149">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="46d79-150">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="46d79-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="46d79-151">`[ImageTemplateName <String>]`: Nazwa szablonu obrazu</span><span class="sxs-lookup"><span data-stu-id="46d79-151">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="46d79-152">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="46d79-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="46d79-153">`[RunOutputName <String>]`: Nazwa wyjścia do uruchomienia</span><span class="sxs-lookup"><span data-stu-id="46d79-153">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="46d79-154">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="46d79-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="46d79-155">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="46d79-155">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="46d79-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="46d79-156">RELATED LINKS</span></span>

