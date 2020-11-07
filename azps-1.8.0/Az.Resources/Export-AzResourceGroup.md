---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 63BBDF98-75FC-4A44-9FD0-95AD21ED93A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/export-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
ms.openlocfilehash: f1801aab91887b3dd0d6a9842c7d4a6de1988a88
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/08/2020
ms.locfileid: "93719696"
---
# <span data-ttu-id="0439c-101">Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0439c-101">Export-AzResourceGroup</span></span>

## <span data-ttu-id="0439c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0439c-102">SYNOPSIS</span></span>
<span data-ttu-id="0439c-103">Przechwytuje grupę zasobów jako szablon i zapisuje ją w pliku.</span><span class="sxs-lookup"><span data-stu-id="0439c-103">Captures a resource group as a template and saves it to a file.</span></span>

## <span data-ttu-id="0439c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0439c-104">SYNTAX</span></span>

```
Export-AzResourceGroup -ResourceGroupName <String> [-Path <String>] [-IncludeParameterDefaultValue]
 [-IncludeComments] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0439c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0439c-105">DESCRIPTION</span></span>
<span data-ttu-id="0439c-106">Polecenie cmdlet **Export-AzResourceGroup** przechwytuje określoną grupę zasobów jako szablon i zapisuje ją w pliku JSON. Może to być przydatne w scenariuszach, w których utworzono już niektóre zasoby w grupie zasobów, a następnie chcesz skorzystać z zalet wdrożenia kopii zapasowej szablonu.</span><span class="sxs-lookup"><span data-stu-id="0439c-106">The **Export-AzResourceGroup** cmdlet captures the specified resource group as a template and saves it to a JSON file.This can be useful in scenarios where you have already created some resources in your resource group, and then want to leverage the benefits of using template backed deployments.</span></span>
<span data-ttu-id="0439c-107">To polecenie cmdlet zapewnia łatwy Start, generując szablon istniejących zasobów w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="0439c-107">This cmdlet gives you an easy start by generating the template for your existing resources in the resource group.</span></span>
<span data-ttu-id="0439c-108">Mogą wystąpić sytuacje, w których to polecenie cmdlet nie może wygenerować części szablonu.</span><span class="sxs-lookup"><span data-stu-id="0439c-108">There might be some cases where this cmdlet fails to generate some parts of the template.</span></span>
<span data-ttu-id="0439c-109">Komunikaty ostrzegawcze będą informować o błędach zasobów.</span><span class="sxs-lookup"><span data-stu-id="0439c-109">Warning messages will inform you of the resources that failed.</span></span>
<span data-ttu-id="0439c-110">Szablon będzie nadal generowany dla części, które powiodło się.</span><span class="sxs-lookup"><span data-stu-id="0439c-110">The template will still be generated for the parts that were successful.</span></span>

## <span data-ttu-id="0439c-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0439c-111">EXAMPLES</span></span>

### <span data-ttu-id="0439c-112">Przykład 1: eksportowanie grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="0439c-112">Example 1: Export a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup"
```

<span data-ttu-id="0439c-113">To polecenie przechwytuje grupę zasobów o nazwie test jako szablon i zapisuje ją w pliku JSON w bieżącym katalogu.</span><span class="sxs-lookup"><span data-stu-id="0439c-113">This command captures the resource group named TestGroup as a template, and saves it to a JSON file in the current directory.</span></span>

## <span data-ttu-id="0439c-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0439c-114">PARAMETERS</span></span>

### <span data-ttu-id="0439c-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0439c-115">-ApiVersion</span></span>
<span data-ttu-id="0439c-116">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="0439c-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="0439c-117">Jeśli nie określono tej funkcji, używana jest Najnowsza wersja interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="0439c-117">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="0439c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0439c-118">-DefaultProfile</span></span>
<span data-ttu-id="0439c-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="0439c-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0439c-120">-Force</span><span class="sxs-lookup"><span data-stu-id="0439c-120">-Force</span></span>
<span data-ttu-id="0439c-121">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="0439c-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0439c-122">-IncludeComments</span><span class="sxs-lookup"><span data-stu-id="0439c-122">-IncludeComments</span></span>
<span data-ttu-id="0439c-123">Wskazuje, że ta operacja powoduje wyeksportowanie szablonu za pomocą komentarzy.</span><span class="sxs-lookup"><span data-stu-id="0439c-123">Indicates that this operation exports the template with comments.</span></span>

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

### <span data-ttu-id="0439c-124">-IncludeParameterDefaultValue</span><span class="sxs-lookup"><span data-stu-id="0439c-124">-IncludeParameterDefaultValue</span></span>
<span data-ttu-id="0439c-125">Wskazuje, że ta operacja powoduje wyeksportowanie parametru szablonu z wartością domyślną.</span><span class="sxs-lookup"><span data-stu-id="0439c-125">Indicates that this operation exports the template parameter with the default value.</span></span>

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

### <span data-ttu-id="0439c-126">-Path</span><span class="sxs-lookup"><span data-stu-id="0439c-126">-Path</span></span>
<span data-ttu-id="0439c-127">Określa ścieżkę wyjściową pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="0439c-127">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="0439c-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="0439c-128">-Pre</span></span>
<span data-ttu-id="0439c-129">Wskazuje, że za pomocą tego polecenia cmdlet można korzystać z wersji wstępnej API podczas automatycznego ustalania, której wersji interfejsu API należy używać.</span><span class="sxs-lookup"><span data-stu-id="0439c-129">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="0439c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0439c-130">-ResourceGroupName</span></span>
<span data-ttu-id="0439c-131">Określa nazwę grupy zasobów do wyeksportowania.</span><span class="sxs-lookup"><span data-stu-id="0439c-131">Specifies the name of the resource group to export.</span></span>

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

### <span data-ttu-id="0439c-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0439c-132">-Confirm</span></span>
<span data-ttu-id="0439c-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0439c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0439c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0439c-134">-WhatIf</span></span>
<span data-ttu-id="0439c-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0439c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0439c-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0439c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0439c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0439c-137">CommonParameters</span></span>
<span data-ttu-id="0439c-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0439c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0439c-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0439c-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0439c-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0439c-140">INPUTS</span></span>

### <span data-ttu-id="0439c-141">System. String</span><span class="sxs-lookup"><span data-stu-id="0439c-141">System.String</span></span>

## <span data-ttu-id="0439c-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0439c-142">OUTPUTS</span></span>

### <span data-ttu-id="0439c-143">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="0439c-143">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="0439c-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0439c-144">NOTES</span></span>

## <span data-ttu-id="0439c-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0439c-145">RELATED LINKS</span></span>

[<span data-ttu-id="0439c-146">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0439c-146">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)


