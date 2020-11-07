---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 8BB4AD6B-EBE3-442A-83E7-B77A31573208
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Save-AzureRmResourceGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Save-AzureRmResourceGroupDeploymentTemplate.md
ms.openlocfilehash: 8f146c6516226c800f45489e1f7fa5d37173e151
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719250"
---
# <span data-ttu-id="7a74a-101">Save-AzureRmResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="7a74a-101">Save-AzureRmResourceGroupDeploymentTemplate</span></span>

## <span data-ttu-id="7a74a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7a74a-102">SYNOPSIS</span></span>
<span data-ttu-id="7a74a-103">Zapisuje szablon rozmieszczania grup zasobów do pliku.</span><span class="sxs-lookup"><span data-stu-id="7a74a-103">Saves a resource group deployment template to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a74a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7a74a-104">SYNTAX</span></span>

```
Save-AzureRmResourceGroupDeploymentTemplate -ResourceGroupName <String> -DeploymentName <String>
 [-Path <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7a74a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7a74a-105">DESCRIPTION</span></span>
<span data-ttu-id="7a74a-106">Polecenie cmdlet **Save-AzureRmResourceGroupDeploymentTemplate**  umożliwia zapisanie szablonu rozmieszczania grup zasobów w pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="7a74a-106">The **Save-AzureRmResourceGroupDeploymentTemplate**  cmdlet saves a resource group deployment template to a JSON file.</span></span>

## <span data-ttu-id="7a74a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7a74a-107">EXAMPLES</span></span>

### <span data-ttu-id="7a74a-108">Przykład 1. Zapisz szablon wdrożenia</span><span class="sxs-lookup"><span data-stu-id="7a74a-108">Example 1: Save a deployment template</span></span>
```
PS C:\>Save-AzureRmResourceGroupDeploymentTemplate -DeploymentName "TestDeployment" -ResourceGroupName "TestGroup"
```

<span data-ttu-id="7a74a-109">To polecenie pobiera szablon wdrożenia z TestDeployment i zapisuje go jako plik JSON w bieżącym katalogu.</span><span class="sxs-lookup"><span data-stu-id="7a74a-109">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

## <span data-ttu-id="7a74a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7a74a-110">PARAMETERS</span></span>

### <span data-ttu-id="7a74a-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7a74a-111">-ApiVersion</span></span>
<span data-ttu-id="7a74a-112">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="7a74a-112">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="7a74a-113">Jeśli nie określono tej funkcji, używana jest Najnowsza wersja interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="7a74a-113">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="7a74a-114">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="7a74a-114">-DeploymentName</span></span>
<span data-ttu-id="7a74a-115">Określa nazwę wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="7a74a-115">Specifies the name of the deployment.</span></span>

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

### <span data-ttu-id="7a74a-116">-Force</span><span class="sxs-lookup"><span data-stu-id="7a74a-116">-Force</span></span>
<span data-ttu-id="7a74a-117">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7a74a-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7a74a-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="7a74a-118">-InformationAction</span></span>
<span data-ttu-id="7a74a-119">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="7a74a-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7a74a-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="7a74a-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7a74a-121">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="7a74a-121">Continue</span></span>
- <span data-ttu-id="7a74a-122">Ignorować</span><span class="sxs-lookup"><span data-stu-id="7a74a-122">Ignore</span></span>
- <span data-ttu-id="7a74a-123">Inquire</span><span class="sxs-lookup"><span data-stu-id="7a74a-123">Inquire</span></span>
- <span data-ttu-id="7a74a-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7a74a-124">SilentlyContinue</span></span>
- <span data-ttu-id="7a74a-125">Przestaw</span><span class="sxs-lookup"><span data-stu-id="7a74a-125">Stop</span></span>
- <span data-ttu-id="7a74a-126">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="7a74a-126">Suspend</span></span>

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

### <span data-ttu-id="7a74a-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7a74a-127">-InformationVariable</span></span>
<span data-ttu-id="7a74a-128">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="7a74a-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="7a74a-129">-Path</span><span class="sxs-lookup"><span data-stu-id="7a74a-129">-Path</span></span>
<span data-ttu-id="7a74a-130">Określa ścieżkę wyjściową pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="7a74a-130">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="7a74a-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="7a74a-131">-Pre</span></span>
<span data-ttu-id="7a74a-132">Wskazuje, że za pomocą tego polecenia cmdlet można korzystać z wersji wstępnej API podczas automatycznego ustalania, której wersji interfejsu API należy używać.</span><span class="sxs-lookup"><span data-stu-id="7a74a-132">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="7a74a-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a74a-133">-ResourceGroupName</span></span>
<span data-ttu-id="7a74a-134">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7a74a-134">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="7a74a-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7a74a-135">-Confirm</span></span>
<span data-ttu-id="7a74a-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a74a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a74a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a74a-137">-WhatIf</span></span>
<span data-ttu-id="7a74a-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a74a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a74a-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7a74a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a74a-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a74a-140">-DefaultProfile</span></span>
<span data-ttu-id="7a74a-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7a74a-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a74a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a74a-142">CommonParameters</span></span>
<span data-ttu-id="7a74a-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a74a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a74a-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a74a-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a74a-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a74a-145">INPUTS</span></span>

## <span data-ttu-id="7a74a-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7a74a-146">OUTPUTS</span></span>

### <span data-ttu-id="7a74a-147">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="7a74a-147">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="7a74a-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7a74a-148">NOTES</span></span>

## <span data-ttu-id="7a74a-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7a74a-149">RELATED LINKS</span></span>

