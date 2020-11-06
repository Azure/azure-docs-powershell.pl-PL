---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 63BBDF98-75FC-4A44-9FD0-95AD21ED93A6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/export-azurermresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Export-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Export-AzureRmResourceGroup.md
ms.openlocfilehash: 489e1fed20231dbd4fbb20d52365e7e46b1d4230
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544136"
---
# <span data-ttu-id="5c371-101">Export-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5c371-101">Export-AzureRmResourceGroup</span></span>

## <span data-ttu-id="5c371-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5c371-102">SYNOPSIS</span></span>
<span data-ttu-id="5c371-103">Przechwytuje grupę zasobów jako szablon i zapisuje ją w pliku.</span><span class="sxs-lookup"><span data-stu-id="5c371-103">Captures a resource group as a template and saves it to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c371-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5c371-104">SYNTAX</span></span>

```
Export-AzureRmResourceGroup -ResourceGroupName <String> [-Path <String>] [-IncludeParameterDefaultValue]
 [-IncludeComments] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5c371-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5c371-105">DESCRIPTION</span></span>
<span data-ttu-id="5c371-106">Polecenie cmdlet **Export-AzureRmResourceGroup** przechwytuje określoną grupę zasobów jako szablon i zapisuje ją w pliku JSON. Może to być przydatne w scenariuszach, w których utworzono już niektóre zasoby w grupie zasobów, a następnie chcesz skorzystać z zalet wdrożenia kopii zapasowej szablonu.</span><span class="sxs-lookup"><span data-stu-id="5c371-106">The **Export-AzureRmResourceGroup** cmdlet captures the specified resource group as a template and saves it to a JSON file.This can be useful in scenarios where you have already created some resources in your resource group, and then want to leverage the benefits of using template backed deployments.</span></span>
<span data-ttu-id="5c371-107">To polecenie cmdlet zapewnia łatwy Start, generując szablon istniejących zasobów w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="5c371-107">This cmdlet gives you an easy start by generating the template for your existing resources in the resource group.</span></span>

<span data-ttu-id="5c371-108">Mogą wystąpić sytuacje, w których to polecenie cmdlet nie może wygenerować części szablonu.</span><span class="sxs-lookup"><span data-stu-id="5c371-108">There might be some cases where this cmdlet fails to generate some parts of the template.</span></span>
<span data-ttu-id="5c371-109">Komunikaty ostrzegawcze będą informować o błędach zasobów.</span><span class="sxs-lookup"><span data-stu-id="5c371-109">Warning messages will inform you of the resources that failed.</span></span>
<span data-ttu-id="5c371-110">Szablon będzie nadal generowany dla części, które powiodło się.</span><span class="sxs-lookup"><span data-stu-id="5c371-110">The template will still be generated for the parts that were successful.</span></span>

## <span data-ttu-id="5c371-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5c371-111">EXAMPLES</span></span>

### <span data-ttu-id="5c371-112">Przykład 1: eksportowanie grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="5c371-112">Example 1: Export a resource group</span></span>
```
PS C:\>Export-AzureRmResourceGroup -ResourceGroupName "TestGroup"
```

<span data-ttu-id="5c371-113">To polecenie przechwytuje grupę zasobów o nazwie test jako szablon i zapisuje ją w pliku JSON w bieżącym katalogu.</span><span class="sxs-lookup"><span data-stu-id="5c371-113">This command captures the resource group named TestGroup as a template, and saves it to a JSON file in the current directory.</span></span>

## <span data-ttu-id="5c371-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5c371-114">PARAMETERS</span></span>

### <span data-ttu-id="5c371-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5c371-115">-ApiVersion</span></span>
<span data-ttu-id="5c371-116">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="5c371-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="5c371-117">Jeśli nie określono tej funkcji, używana jest Najnowsza wersja interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="5c371-117">If not specified, the latest API version is used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c371-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c371-118">-DefaultProfile</span></span>
<span data-ttu-id="5c371-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5c371-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c371-120">-Force</span><span class="sxs-lookup"><span data-stu-id="5c371-120">-Force</span></span>
<span data-ttu-id="5c371-121">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="5c371-121">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c371-122">-IncludeComments</span><span class="sxs-lookup"><span data-stu-id="5c371-122">-IncludeComments</span></span>
<span data-ttu-id="5c371-123">Wskazuje, że ta operacja powoduje wyeksportowanie szablonu za pomocą komentarzy.</span><span class="sxs-lookup"><span data-stu-id="5c371-123">Indicates that this operation exports the template with comments.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c371-124">-IncludeParameterDefaultValue</span><span class="sxs-lookup"><span data-stu-id="5c371-124">-IncludeParameterDefaultValue</span></span>
<span data-ttu-id="5c371-125">Wskazuje, że ta operacja powoduje wyeksportowanie parametru szablonu z wartością domyślną.</span><span class="sxs-lookup"><span data-stu-id="5c371-125">Indicates that this operation exports the template parameter with the default value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c371-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="5c371-126">-InformationAction</span></span>
<span data-ttu-id="5c371-127">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="5c371-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5c371-128">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="5c371-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5c371-129">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="5c371-129">Continue</span></span>
- <span data-ttu-id="5c371-130">Ignorować</span><span class="sxs-lookup"><span data-stu-id="5c371-130">Ignore</span></span>
- <span data-ttu-id="5c371-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="5c371-131">Inquire</span></span>
- <span data-ttu-id="5c371-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5c371-132">SilentlyContinue</span></span>
- <span data-ttu-id="5c371-133">Przestaw</span><span class="sxs-lookup"><span data-stu-id="5c371-133">Stop</span></span>
- <span data-ttu-id="5c371-134">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="5c371-134">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c371-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5c371-135">-InformationVariable</span></span>
<span data-ttu-id="5c371-136">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="5c371-136">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c371-137">-Path</span><span class="sxs-lookup"><span data-stu-id="5c371-137">-Path</span></span>
<span data-ttu-id="5c371-138">Określa ścieżkę wyjściową pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="5c371-138">Specifies the output path of the template file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c371-139">-Pre</span><span class="sxs-lookup"><span data-stu-id="5c371-139">-Pre</span></span>
<span data-ttu-id="5c371-140">Wskazuje, że za pomocą tego polecenia cmdlet można korzystać z wersji wstępnej API podczas automatycznego ustalania, której wersji interfejsu API należy używać.</span><span class="sxs-lookup"><span data-stu-id="5c371-140">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c371-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c371-141">-ResourceGroupName</span></span>
<span data-ttu-id="5c371-142">Określa nazwę grupy zasobów do wyeksportowania.</span><span class="sxs-lookup"><span data-stu-id="5c371-142">Specifies the name of the resource group to export.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c371-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5c371-143">-Confirm</span></span>
<span data-ttu-id="5c371-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c371-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c371-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c371-145">-WhatIf</span></span>
<span data-ttu-id="5c371-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c371-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c371-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5c371-147">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c371-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c371-148">CommonParameters</span></span>
<span data-ttu-id="5c371-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c371-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c371-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c371-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c371-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5c371-151">INPUTS</span></span>

### <span data-ttu-id="5c371-152">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5c371-152">None</span></span>
<span data-ttu-id="5c371-153">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="5c371-153">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5c371-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5c371-154">OUTPUTS</span></span>

### <span data-ttu-id="5c371-155">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="5c371-155">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="5c371-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5c371-156">NOTES</span></span>

## <span data-ttu-id="5c371-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5c371-157">RELATED LINKS</span></span>

[<span data-ttu-id="5c371-158">Znajdź-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5c371-158">Find-AzureRmResourceGroup</span></span>](./Find-AzureRmResourceGroup.md)


