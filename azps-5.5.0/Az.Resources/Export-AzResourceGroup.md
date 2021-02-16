---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 63BBDF98-75FC-4A44-9FD0-95AD21ED93A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/export-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
ms.openlocfilehash: 74605a57ab3f2c0898bf3eeb80950f86d4f65d94
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178922"
---
# <span data-ttu-id="4dd4c-101">Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4dd4c-101">Export-AzResourceGroup</span></span>

## <span data-ttu-id="4dd4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4dd4c-102">SYNOPSIS</span></span>
<span data-ttu-id="4dd4c-103">Przechwytuje grupę zasobów jako szablon i zapisuje ją w pliku.</span><span class="sxs-lookup"><span data-stu-id="4dd4c-103">Captures a resource group as a template and saves it to a file.</span></span>

## <span data-ttu-id="4dd4c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4dd4c-104">SYNTAX</span></span>

```
Export-AzResourceGroup -ResourceGroupName <String> [-Path <String>] [-IncludeParameterDefaultValue]
 [-IncludeComments] [-SkipResourceNameParameterization] [-SkipAllParameterization] [-Resource <String[]>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4dd4c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4dd4c-105">DESCRIPTION</span></span>
<span data-ttu-id="4dd4c-106">Polecenie **cmdlet Export-AzResourceGroup** przechwyci określoną grupę zasobów jako szablon i zapisuje ją w pliku JSON. Może to być przydatne w scenariuszach, w których utworzono już niektóre zasoby w grupie zasobów, a następnie chcesz wykorzystać zalety korzystania z wdrożeń w kopii zapasowej szablonów.</span><span class="sxs-lookup"><span data-stu-id="4dd4c-106">The **Export-AzResourceGroup** cmdlet captures the specified resource group as a template and saves it to a JSON file.This can be useful in scenarios where you have already created some resources in your resource group, and then want to leverage the benefits of using template backed deployments.</span></span>
<span data-ttu-id="4dd4c-107">To polecenie cmdlet zapewnia łatwy start, generując szablon dla istniejących zasobów w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="4dd4c-107">This cmdlet gives you an easy start by generating the template for your existing resources in the resource group.</span></span>
<span data-ttu-id="4dd4c-108">W niektórych przypadkach to polecenie cmdlet nie generuje części szablonu.</span><span class="sxs-lookup"><span data-stu-id="4dd4c-108">There might be some cases where this cmdlet fails to generate some parts of the template.</span></span>
<span data-ttu-id="4dd4c-109">Komunikaty ostrzegawcze informują o zasobach, które zakończyły się niepowodzeniem.</span><span class="sxs-lookup"><span data-stu-id="4dd4c-109">Warning messages will inform you of the resources that failed.</span></span>
<span data-ttu-id="4dd4c-110">Szablon nadal zostanie wygenerowany dla części, które się powiedzieły.</span><span class="sxs-lookup"><span data-stu-id="4dd4c-110">The template will still be generated for the parts that were successful.</span></span>

## <span data-ttu-id="4dd4c-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4dd4c-111">EXAMPLES</span></span>

### <span data-ttu-id="4dd4c-112">Przykład 1. Eksportowanie grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="4dd4c-112">Example 1: Export a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup"
```

<span data-ttu-id="4dd4c-113">To polecenie rejestruje grupę zasobów o nazwie TestGroup jako szablon i zapisuje ją w pliku JSON w bieżącym katalogu.</span><span class="sxs-lookup"><span data-stu-id="4dd4c-113">This command captures the resource group named TestGroup as a template, and saves it to a JSON file in the current directory.</span></span>

### <span data-ttu-id="4dd4c-114">Przykład 2. Eksportowanie pojedynczego zasobu z grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="4dd4c-114">Example 2: Export a single resource from a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup" -Resource "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Compute/virtualMachines/TestVirtualMachine"
```

<span data-ttu-id="4dd4c-115">To polecenie przechwyci zasób maszyny wirtualnej o nazwie "TestVirtualMachine" z grupy zasobów "TestGroup" jako szablon, a następnie zapisuje go w pliku JSON w bieżącym katalogu.</span><span class="sxs-lookup"><span data-stu-id="4dd4c-115">This command captures the Virtual Machine resource named "TestVirtualMachine" from the "TestGroup" resource group as a template, and saves it to a JSON file in the current directory.</span></span>

### <span data-ttu-id="4dd4c-116">Przykład 3. Eksportowanie wybranego zasobu z grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="4dd4c-116">Example 3: Export a selection of resources from a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup" -SkipAllParameterization -Resource @(
  "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Compute/virtualMachines/TestVm",
  "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Network/networkInterfaces/TestNic"
)
```

<span data-ttu-id="4dd4c-117">To polecenie przechwyci dwa zasoby z grupy zasobów "TestGroup" jako szablon i zapisuje je w pliku JSON w bieżącym katalogu.</span><span class="sxs-lookup"><span data-stu-id="4dd4c-117">This command captures two resources from the "TestGroup" resource group as a template, and saves it to a JSON file in the current directory.</span></span> <span data-ttu-id="4dd4c-118">Wygenerowany szablon nie będzie zawierać żadnych wygenerowanych parametrów.</span><span class="sxs-lookup"><span data-stu-id="4dd4c-118">The generated template will not contain any generated parameters.</span></span>

## <span data-ttu-id="4dd4c-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4dd4c-119">PARAMETERS</span></span>

### <span data-ttu-id="4dd4c-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4dd4c-120">-ApiVersion</span></span>
<span data-ttu-id="4dd4c-121">Określa wersję interfejsu API dostawcy zasobów do użycia.</span><span class="sxs-lookup"><span data-stu-id="4dd4c-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="4dd4c-122">Jeśli nie zostanie określona, zostanie użyta najnowsza wersja interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="4dd4c-122">If not specified, the latest API version is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dd4c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dd4c-123">-DefaultProfile</span></span>
<span data-ttu-id="4dd4c-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="4dd4c-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dd4c-125">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="4dd4c-125">-Force</span></span>
<span data-ttu-id="4dd4c-126">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="4dd4c-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4dd4c-127">- IncludeComments</span><span class="sxs-lookup"><span data-stu-id="4dd4c-127">-IncludeComments</span></span>
<span data-ttu-id="4dd4c-128">Oznacza, że ta operacja eksportuje szablon z komentarzami.</span><span class="sxs-lookup"><span data-stu-id="4dd4c-128">Indicates that this operation exports the template with comments.</span></span>

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

### <span data-ttu-id="4dd4c-129">-IncludeParameterDefaultValue</span><span class="sxs-lookup"><span data-stu-id="4dd4c-129">-IncludeParameterDefaultValue</span></span>
<span data-ttu-id="4dd4c-130">Wskazuje, że ta operacja eksportuje parametr szablonu z wartością domyślną.</span><span class="sxs-lookup"><span data-stu-id="4dd4c-130">Indicates that this operation exports the template parameter with the default value.</span></span>

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

### <span data-ttu-id="4dd4c-131">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="4dd4c-131">-Path</span></span>
<span data-ttu-id="4dd4c-132">Określa ścieżkę wyjściową pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="4dd4c-132">Specifies the output path of the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dd4c-133">— Przed</span><span class="sxs-lookup"><span data-stu-id="4dd4c-133">-Pre</span></span>
<span data-ttu-id="4dd4c-134">Wskazuje, że to polecenie cmdlet automatycznie określa wersję interfejsu API do użycia przy użyciu wersji przedpremierowej interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="4dd4c-134">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="4dd4c-135">— Zasób</span><span class="sxs-lookup"><span data-stu-id="4dd4c-135">-Resource</span></span>
<span data-ttu-id="4dd4c-136">Lista rekordów resourceId, według których mają być filtrowane wyniki.</span><span class="sxs-lookup"><span data-stu-id="4dd4c-136">A list of resourceIds to filter the results by.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dd4c-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dd4c-137">-ResourceGroupName</span></span>
<span data-ttu-id="4dd4c-138">Określa nazwę grupy zasobów do wyeksportowania.</span><span class="sxs-lookup"><span data-stu-id="4dd4c-138">Specifies the name of the resource group to export.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dd4c-139">-SkipAllParameterization</span><span class="sxs-lookup"><span data-stu-id="4dd4c-139">-SkipAllParameterization</span></span>
<span data-ttu-id="4dd4c-140">Pomiń całą parametrację.</span><span class="sxs-lookup"><span data-stu-id="4dd4c-140">Skip all parameterization.</span></span>

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

### <span data-ttu-id="4dd4c-141">-SkipResourceNameParameterization</span><span class="sxs-lookup"><span data-stu-id="4dd4c-141">-SkipResourceNameParameterization</span></span>
<span data-ttu-id="4dd4c-142">Pomiń parametrację nazwy zasobu.</span><span class="sxs-lookup"><span data-stu-id="4dd4c-142">Skip resource name parameterization.</span></span>

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

### <span data-ttu-id="4dd4c-143">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4dd4c-143">-Confirm</span></span>
<span data-ttu-id="4dd4c-144">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4dd4c-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dd4c-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dd4c-145">-WhatIf</span></span>
<span data-ttu-id="4dd4c-146">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4dd4c-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dd4c-147">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4dd4c-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dd4c-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dd4c-148">CommonParameters</span></span>
<span data-ttu-id="4dd4c-149">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dd4c-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dd4c-150">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4dd4c-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dd4c-151">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4dd4c-151">INPUTS</span></span>

### <span data-ttu-id="4dd4c-152">System.String</span><span class="sxs-lookup"><span data-stu-id="4dd4c-152">System.String</span></span>

## <span data-ttu-id="4dd4c-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4dd4c-153">OUTPUTS</span></span>

### <span data-ttu-id="4dd4c-154">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="4dd4c-154">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="4dd4c-155">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4dd4c-155">NOTES</span></span>

## <span data-ttu-id="4dd4c-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4dd4c-156">RELATED LINKS</span></span>

[<span data-ttu-id="4dd4c-157">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4dd4c-157">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)


