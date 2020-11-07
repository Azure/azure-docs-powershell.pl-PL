---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8BB4AD6B-EBE3-442A-83E7-B77A31573208
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-Azresourcegroupdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Save-AzResourceGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Save-AzResourceGroupDeploymentTemplate.md
ms.openlocfilehash: 1ffdcef1bb27ec06873c12f64a135adc0e433929
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892365"
---
# <span data-ttu-id="866c8-101">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="866c8-101">Save-AzResourceGroupDeploymentTemplate</span></span>

## <span data-ttu-id="866c8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="866c8-102">SYNOPSIS</span></span>
<span data-ttu-id="866c8-103">Zapisuje szablon rozmieszczania grup zasobów do pliku.</span><span class="sxs-lookup"><span data-stu-id="866c8-103">Saves a resource group deployment template to a file.</span></span>

## <span data-ttu-id="866c8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="866c8-104">SYNTAX</span></span>

```
Save-AzResourceGroupDeploymentTemplate -ResourceGroupName <String> -DeploymentName <String>
 [-Path <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="866c8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="866c8-105">DESCRIPTION</span></span>
<span data-ttu-id="866c8-106">Polecenie cmdlet **Save-AzResourceGroupDeploymentTemplate**  umożliwia zapisanie szablonu rozmieszczania grup zasobów w pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="866c8-106">The **Save-AzResourceGroupDeploymentTemplate**  cmdlet saves a resource group deployment template to a JSON file.</span></span>

## <span data-ttu-id="866c8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="866c8-107">EXAMPLES</span></span>

### <span data-ttu-id="866c8-108">Przykład 1. Zapisz szablon wdrożenia</span><span class="sxs-lookup"><span data-stu-id="866c8-108">Example 1: Save a deployment template</span></span>
```
PS C:\>Save-AzResourceGroupDeploymentTemplate -DeploymentName "TestDeployment" -ResourceGroupName "TestGroup"
```

<span data-ttu-id="866c8-109">To polecenie pobiera szablon wdrożenia z TestDeployment i zapisuje go jako plik JSON w bieżącym katalogu.</span><span class="sxs-lookup"><span data-stu-id="866c8-109">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

## <span data-ttu-id="866c8-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="866c8-110">PARAMETERS</span></span>

### <span data-ttu-id="866c8-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="866c8-111">-ApiVersion</span></span>
<span data-ttu-id="866c8-112">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="866c8-112">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="866c8-113">Jeśli nie określono tej funkcji, używana jest Najnowsza wersja interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="866c8-113">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="866c8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="866c8-114">-DefaultProfile</span></span>
<span data-ttu-id="866c8-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="866c8-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="866c8-116">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="866c8-116">-DeploymentName</span></span>
<span data-ttu-id="866c8-117">Określa nazwę wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="866c8-117">Specifies the name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="866c8-118">-Force</span><span class="sxs-lookup"><span data-stu-id="866c8-118">-Force</span></span>
<span data-ttu-id="866c8-119">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="866c8-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="866c8-120">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="866c8-120">-InformationAction</span></span>
<span data-ttu-id="866c8-121">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="866c8-121">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="866c8-122">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="866c8-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="866c8-123">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="866c8-123">Continue</span></span>
- <span data-ttu-id="866c8-124">Ignorować</span><span class="sxs-lookup"><span data-stu-id="866c8-124">Ignore</span></span>
- <span data-ttu-id="866c8-125">Inquire</span><span class="sxs-lookup"><span data-stu-id="866c8-125">Inquire</span></span>
- <span data-ttu-id="866c8-126">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="866c8-126">SilentlyContinue</span></span>
- <span data-ttu-id="866c8-127">Przestaw</span><span class="sxs-lookup"><span data-stu-id="866c8-127">Stop</span></span>
- <span data-ttu-id="866c8-128">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="866c8-128">Suspend</span></span>

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

### <span data-ttu-id="866c8-129">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="866c8-129">-InformationVariable</span></span>
<span data-ttu-id="866c8-130">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="866c8-130">Specifies an information variable.</span></span>

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

### <span data-ttu-id="866c8-131">-Path</span><span class="sxs-lookup"><span data-stu-id="866c8-131">-Path</span></span>
<span data-ttu-id="866c8-132">Określa ścieżkę wyjściową pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="866c8-132">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="866c8-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="866c8-133">-Pre</span></span>
<span data-ttu-id="866c8-134">Wskazuje, że za pomocą tego polecenia cmdlet można korzystać z wersji wstępnej API podczas automatycznego ustalania, której wersji interfejsu API należy używać.</span><span class="sxs-lookup"><span data-stu-id="866c8-134">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="866c8-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="866c8-135">-ResourceGroupName</span></span>
<span data-ttu-id="866c8-136">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="866c8-136">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="866c8-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="866c8-137">-Confirm</span></span>
<span data-ttu-id="866c8-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="866c8-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="866c8-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="866c8-139">-WhatIf</span></span>
<span data-ttu-id="866c8-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="866c8-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="866c8-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="866c8-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="866c8-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="866c8-142">CommonParameters</span></span>
<span data-ttu-id="866c8-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="866c8-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="866c8-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="866c8-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="866c8-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="866c8-145">INPUTS</span></span>

## <span data-ttu-id="866c8-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="866c8-146">OUTPUTS</span></span>

## <span data-ttu-id="866c8-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="866c8-147">NOTES</span></span>

## <span data-ttu-id="866c8-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="866c8-148">RELATED LINKS</span></span>
