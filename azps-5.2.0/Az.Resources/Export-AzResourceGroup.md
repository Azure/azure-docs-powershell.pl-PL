---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 63BBDF98-75FC-4A44-9FD0-95AD21ED93A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/export-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
ms.openlocfilehash: 74605a57ab3f2c0898bf3eeb80950f86d4f65d94
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352342"
---
# <span data-ttu-id="a9465-101">Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a9465-101">Export-AzResourceGroup</span></span>

## <span data-ttu-id="a9465-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a9465-102">SYNOPSIS</span></span>
<span data-ttu-id="a9465-103">Przechwytuje grupę zasobów jako szablon i zapisuje ją w pliku.</span><span class="sxs-lookup"><span data-stu-id="a9465-103">Captures a resource group as a template and saves it to a file.</span></span>

## <span data-ttu-id="a9465-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a9465-104">SYNTAX</span></span>

```
Export-AzResourceGroup -ResourceGroupName <String> [-Path <String>] [-IncludeParameterDefaultValue]
 [-IncludeComments] [-SkipResourceNameParameterization] [-SkipAllParameterization] [-Resource <String[]>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a9465-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a9465-105">DESCRIPTION</span></span>
<span data-ttu-id="a9465-106">Polecenie cmdlet **Export-AzResourceGroup** przechwytuje określoną grupę zasobów jako szablon i zapisuje ją w pliku JSON. Może to być przydatne w scenariuszach, w których utworzono już niektóre zasoby w grupie zasobów, a następnie chcesz skorzystać z zalet wdrożenia kopii zapasowej szablonu.</span><span class="sxs-lookup"><span data-stu-id="a9465-106">The **Export-AzResourceGroup** cmdlet captures the specified resource group as a template and saves it to a JSON file.This can be useful in scenarios where you have already created some resources in your resource group, and then want to leverage the benefits of using template backed deployments.</span></span>
<span data-ttu-id="a9465-107">To polecenie cmdlet zapewnia łatwy Start, generując szablon istniejących zasobów w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="a9465-107">This cmdlet gives you an easy start by generating the template for your existing resources in the resource group.</span></span>
<span data-ttu-id="a9465-108">Mogą wystąpić sytuacje, w których to polecenie cmdlet nie może wygenerować części szablonu.</span><span class="sxs-lookup"><span data-stu-id="a9465-108">There might be some cases where this cmdlet fails to generate some parts of the template.</span></span>
<span data-ttu-id="a9465-109">Komunikaty ostrzegawcze będą informować o błędach zasobów.</span><span class="sxs-lookup"><span data-stu-id="a9465-109">Warning messages will inform you of the resources that failed.</span></span>
<span data-ttu-id="a9465-110">Szablon będzie nadal generowany dla części, które powiodło się.</span><span class="sxs-lookup"><span data-stu-id="a9465-110">The template will still be generated for the parts that were successful.</span></span>

## <span data-ttu-id="a9465-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a9465-111">EXAMPLES</span></span>

### <span data-ttu-id="a9465-112">Przykład 1: eksportowanie grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a9465-112">Example 1: Export a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup"
```

<span data-ttu-id="a9465-113">To polecenie przechwytuje grupę zasobów o nazwie test jako szablon i zapisuje ją w pliku JSON w bieżącym katalogu.</span><span class="sxs-lookup"><span data-stu-id="a9465-113">This command captures the resource group named TestGroup as a template, and saves it to a JSON file in the current directory.</span></span>

### <span data-ttu-id="a9465-114">Przykład 2: eksportowanie pojedynczego zasobu z grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a9465-114">Example 2: Export a single resource from a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup" -Resource "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Compute/virtualMachines/TestVirtualMachine"
```

<span data-ttu-id="a9465-115">To polecenie przechwytuje zasób maszyny wirtualnej o nazwie "TestVirtualMachine" z grupy zasobów "Grupa Tester" jako szablon i zapisuje go w pliku JSON w bieżącym katalogu.</span><span class="sxs-lookup"><span data-stu-id="a9465-115">This command captures the Virtual Machine resource named "TestVirtualMachine" from the "TestGroup" resource group as a template, and saves it to a JSON file in the current directory.</span></span>

### <span data-ttu-id="a9465-116">Przykład 3: eksportowanie zaznaczenia zasobów z grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a9465-116">Example 3: Export a selection of resources from a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup" -SkipAllParameterization -Resource @(
  "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Compute/virtualMachines/TestVm",
  "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Network/networkInterfaces/TestNic"
)
```

<span data-ttu-id="a9465-117">To polecenie służy do przechwycenia dwóch zasobów z grupy zasobów "Tester" jako szablonu i zapisanie go w pliku JSON w bieżącym katalogu.</span><span class="sxs-lookup"><span data-stu-id="a9465-117">This command captures two resources from the "TestGroup" resource group as a template, and saves it to a JSON file in the current directory.</span></span> <span data-ttu-id="a9465-118">Wygenerowany szablon nie będzie zawierał żadnych wygenerowanych parametrów.</span><span class="sxs-lookup"><span data-stu-id="a9465-118">The generated template will not contain any generated parameters.</span></span>

## <span data-ttu-id="a9465-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a9465-119">PARAMETERS</span></span>

### <span data-ttu-id="a9465-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a9465-120">-ApiVersion</span></span>
<span data-ttu-id="a9465-121">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="a9465-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="a9465-122">Jeśli nie określono tej funkcji, używana jest Najnowsza wersja interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="a9465-122">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="a9465-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9465-123">-DefaultProfile</span></span>
<span data-ttu-id="a9465-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a9465-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9465-125">-Force</span><span class="sxs-lookup"><span data-stu-id="a9465-125">-Force</span></span>
<span data-ttu-id="a9465-126">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a9465-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a9465-127">-IncludeComments</span><span class="sxs-lookup"><span data-stu-id="a9465-127">-IncludeComments</span></span>
<span data-ttu-id="a9465-128">Wskazuje, że ta operacja powoduje wyeksportowanie szablonu za pomocą komentarzy.</span><span class="sxs-lookup"><span data-stu-id="a9465-128">Indicates that this operation exports the template with comments.</span></span>

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

### <span data-ttu-id="a9465-129">-IncludeParameterDefaultValue</span><span class="sxs-lookup"><span data-stu-id="a9465-129">-IncludeParameterDefaultValue</span></span>
<span data-ttu-id="a9465-130">Wskazuje, że ta operacja powoduje wyeksportowanie parametru szablonu z wartością domyślną.</span><span class="sxs-lookup"><span data-stu-id="a9465-130">Indicates that this operation exports the template parameter with the default value.</span></span>

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

### <span data-ttu-id="a9465-131">-Path</span><span class="sxs-lookup"><span data-stu-id="a9465-131">-Path</span></span>
<span data-ttu-id="a9465-132">Określa ścieżkę wyjściową pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="a9465-132">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="a9465-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="a9465-133">-Pre</span></span>
<span data-ttu-id="a9465-134">Wskazuje, że za pomocą tego polecenia cmdlet można korzystać z wersji wstępnej API podczas automatycznego ustalania, której wersji interfejsu API należy używać.</span><span class="sxs-lookup"><span data-stu-id="a9465-134">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="a9465-135">-Resource</span><span class="sxs-lookup"><span data-stu-id="a9465-135">-Resource</span></span>
<span data-ttu-id="a9465-136">Lista resourceId, według których mają być filtrowane wyniki.</span><span class="sxs-lookup"><span data-stu-id="a9465-136">A list of resourceIds to filter the results by.</span></span>

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

### <span data-ttu-id="a9465-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9465-137">-ResourceGroupName</span></span>
<span data-ttu-id="a9465-138">Określa nazwę grupy zasobów do wyeksportowania.</span><span class="sxs-lookup"><span data-stu-id="a9465-138">Specifies the name of the resource group to export.</span></span>

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

### <span data-ttu-id="a9465-139">-SkipAllParameterization</span><span class="sxs-lookup"><span data-stu-id="a9465-139">-SkipAllParameterization</span></span>
<span data-ttu-id="a9465-140">Pomiń wszystkie Parameterization.</span><span class="sxs-lookup"><span data-stu-id="a9465-140">Skip all parameterization.</span></span>

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

### <span data-ttu-id="a9465-141">-SkipResourceNameParameterization</span><span class="sxs-lookup"><span data-stu-id="a9465-141">-SkipResourceNameParameterization</span></span>
<span data-ttu-id="a9465-142">Pomiń nazwę zasobu Parameterization.</span><span class="sxs-lookup"><span data-stu-id="a9465-142">Skip resource name parameterization.</span></span>

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

### <span data-ttu-id="a9465-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a9465-143">-Confirm</span></span>
<span data-ttu-id="a9465-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9465-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9465-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9465-145">-WhatIf</span></span>
<span data-ttu-id="a9465-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9465-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9465-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a9465-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9465-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9465-148">CommonParameters</span></span>
<span data-ttu-id="a9465-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9465-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9465-150">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9465-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9465-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9465-151">INPUTS</span></span>

### <span data-ttu-id="a9465-152">System. String</span><span class="sxs-lookup"><span data-stu-id="a9465-152">System.String</span></span>

## <span data-ttu-id="a9465-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a9465-153">OUTPUTS</span></span>

### <span data-ttu-id="a9465-154">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="a9465-154">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a9465-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a9465-155">NOTES</span></span>

## <span data-ttu-id="a9465-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9465-156">RELATED LINKS</span></span>

[<span data-ttu-id="a9465-157">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a9465-157">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)


