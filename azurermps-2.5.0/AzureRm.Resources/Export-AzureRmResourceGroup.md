---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 63BBDF98-75FC-4A44-9FD0-95AD21ED93A6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/export-azurermresourcegroup
schema: 2.0.0
ms.openlocfilehash: a5390cd66e97f05e80f52685af6e43135ed64141
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898210"
---
# <span data-ttu-id="199cf-101">Export-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="199cf-101">Export-AzureRmResourceGroup</span></span>

## <span data-ttu-id="199cf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="199cf-102">SYNOPSIS</span></span>
<span data-ttu-id="199cf-103">Przechwytuje grupę zasobów jako szablon i zapisuje ją w pliku.</span><span class="sxs-lookup"><span data-stu-id="199cf-103">Captures a resource group as a template and saves it to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="199cf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="199cf-104">SYNTAX</span></span>

```
Export-AzureRmResourceGroup -ResourceGroupName <String> [-Path <String>] [-IncludeParameterDefaultValue]
 [-IncludeComments] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="199cf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="199cf-105">DESCRIPTION</span></span>
<span data-ttu-id="199cf-106">Polecenie cmdlet **Export-AzureRmResourceGroup** przechwytuje określoną grupę zasobów jako szablon i zapisuje ją w pliku JSON. Może to być przydatne w scenariuszach, w których utworzono już niektóre zasoby w grupie zasobów, a następnie chcesz skorzystać z zalet wdrożenia kopii zapasowej szablonu.</span><span class="sxs-lookup"><span data-stu-id="199cf-106">The **Export-AzureRmResourceGroup** cmdlet captures the specified resource group as a template and saves it to a JSON file.This can be useful in scenarios where you have already created some resources in your resource group, and then want to leverage the benefits of using template backed deployments.</span></span>
<span data-ttu-id="199cf-107">To polecenie cmdlet zapewnia łatwy Start, generując szablon istniejących zasobów w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="199cf-107">This cmdlet gives you an easy start by generating the template for your existing resources in the resource group.</span></span>
<span data-ttu-id="199cf-108">Mogą wystąpić sytuacje, w których to polecenie cmdlet nie może wygenerować części szablonu.</span><span class="sxs-lookup"><span data-stu-id="199cf-108">There might be some cases where this cmdlet fails to generate some parts of the template.</span></span>
<span data-ttu-id="199cf-109">Komunikaty ostrzegawcze będą informować o błędach zasobów.</span><span class="sxs-lookup"><span data-stu-id="199cf-109">Warning messages will inform you of the resources that failed.</span></span>
<span data-ttu-id="199cf-110">Szablon będzie nadal generowany dla części, które powiodło się.</span><span class="sxs-lookup"><span data-stu-id="199cf-110">The template will still be generated for the parts that were successful.</span></span>

## <span data-ttu-id="199cf-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="199cf-111">EXAMPLES</span></span>

### <span data-ttu-id="199cf-112">Przykład 1: eksportowanie grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="199cf-112">Example 1: Export a resource group</span></span>
```
PS C:\>Export-AzureRmResourceGroup -ResourceGroupName "TestGroup"
```

<span data-ttu-id="199cf-113">To polecenie przechwytuje grupę zasobów o nazwie test jako szablon i zapisuje ją w pliku JSON w bieżącym katalogu.</span><span class="sxs-lookup"><span data-stu-id="199cf-113">This command captures the resource group named TestGroup as a template, and saves it to a JSON file in the current directory.</span></span>

## <span data-ttu-id="199cf-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="199cf-114">PARAMETERS</span></span>

### <span data-ttu-id="199cf-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="199cf-115">-ApiVersion</span></span>
<span data-ttu-id="199cf-116">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="199cf-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="199cf-117">Jeśli nie określono tej funkcji, używana jest Najnowsza wersja interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="199cf-117">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="199cf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="199cf-118">-DefaultProfile</span></span>
<span data-ttu-id="199cf-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="199cf-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="199cf-120">-Force</span><span class="sxs-lookup"><span data-stu-id="199cf-120">-Force</span></span>
<span data-ttu-id="199cf-121">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="199cf-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="199cf-122">-IncludeComments</span><span class="sxs-lookup"><span data-stu-id="199cf-122">-IncludeComments</span></span>
<span data-ttu-id="199cf-123">Wskazuje, że ta operacja powoduje wyeksportowanie szablonu za pomocą komentarzy.</span><span class="sxs-lookup"><span data-stu-id="199cf-123">Indicates that this operation exports the template with comments.</span></span>

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

### <span data-ttu-id="199cf-124">-IncludeParameterDefaultValue</span><span class="sxs-lookup"><span data-stu-id="199cf-124">-IncludeParameterDefaultValue</span></span>
<span data-ttu-id="199cf-125">Wskazuje, że ta operacja powoduje wyeksportowanie parametru szablonu z wartością domyślną.</span><span class="sxs-lookup"><span data-stu-id="199cf-125">Indicates that this operation exports the template parameter with the default value.</span></span>

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

### <span data-ttu-id="199cf-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="199cf-126">-InformationAction</span></span>
<span data-ttu-id="199cf-127">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="199cf-127">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="199cf-128">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="199cf-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="199cf-129">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="199cf-129">Continue</span></span>
- <span data-ttu-id="199cf-130">Ignorować</span><span class="sxs-lookup"><span data-stu-id="199cf-130">Ignore</span></span>
- <span data-ttu-id="199cf-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="199cf-131">Inquire</span></span>
- <span data-ttu-id="199cf-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="199cf-132">SilentlyContinue</span></span>
- <span data-ttu-id="199cf-133">Przestaw</span><span class="sxs-lookup"><span data-stu-id="199cf-133">Stop</span></span>
- <span data-ttu-id="199cf-134">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="199cf-134">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="199cf-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="199cf-135">-InformationVariable</span></span>
<span data-ttu-id="199cf-136">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="199cf-136">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="199cf-137">-Path</span><span class="sxs-lookup"><span data-stu-id="199cf-137">-Path</span></span>
<span data-ttu-id="199cf-138">Określa ścieżkę wyjściową pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="199cf-138">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="199cf-139">-Pre</span><span class="sxs-lookup"><span data-stu-id="199cf-139">-Pre</span></span>
<span data-ttu-id="199cf-140">Wskazuje, że za pomocą tego polecenia cmdlet można korzystać z wersji wstępnej API podczas automatycznego ustalania, której wersji interfejsu API należy używać.</span><span class="sxs-lookup"><span data-stu-id="199cf-140">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="199cf-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="199cf-141">-ResourceGroupName</span></span>
<span data-ttu-id="199cf-142">Określa nazwę grupy zasobów do wyeksportowania.</span><span class="sxs-lookup"><span data-stu-id="199cf-142">Specifies the name of the resource group to export.</span></span>

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

### <span data-ttu-id="199cf-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="199cf-143">-Confirm</span></span>
<span data-ttu-id="199cf-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="199cf-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="199cf-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="199cf-145">-WhatIf</span></span>
<span data-ttu-id="199cf-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="199cf-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="199cf-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="199cf-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="199cf-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="199cf-148">CommonParameters</span></span>
<span data-ttu-id="199cf-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="199cf-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="199cf-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="199cf-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="199cf-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="199cf-151">INPUTS</span></span>

## <span data-ttu-id="199cf-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="199cf-152">OUTPUTS</span></span>

## <span data-ttu-id="199cf-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="199cf-153">NOTES</span></span>

## <span data-ttu-id="199cf-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="199cf-154">RELATED LINKS</span></span>




