---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 8BB4AD6B-EBE3-442A-83E7-B77A31573208
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/save-azurermresourcegroupdeploymenttemplate
schema: 2.0.0
ms.openlocfilehash: 78ad8ee76aeeec4f57e0d2f2a6b2a1f4d9424d97
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897805"
---
# <span data-ttu-id="e082e-101">Save-AzureRmResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="e082e-101">Save-AzureRmResourceGroupDeploymentTemplate</span></span>

## <span data-ttu-id="e082e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e082e-102">SYNOPSIS</span></span>
<span data-ttu-id="e082e-103">Zapisuje szablon rozmieszczania grup zasobów do pliku.</span><span class="sxs-lookup"><span data-stu-id="e082e-103">Saves a resource group deployment template to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e082e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e082e-104">SYNTAX</span></span>

```
Save-AzureRmResourceGroupDeploymentTemplate -ResourceGroupName <String> -DeploymentName <String>
 [-Path <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e082e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e082e-105">DESCRIPTION</span></span>
<span data-ttu-id="e082e-106">Polecenie cmdlet **Save-AzureRmResourceGroupDeploymentTemplate**  umożliwia zapisanie szablonu rozmieszczania grup zasobów w pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="e082e-106">The **Save-AzureRmResourceGroupDeploymentTemplate**  cmdlet saves a resource group deployment template to a JSON file.</span></span>

## <span data-ttu-id="e082e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e082e-107">EXAMPLES</span></span>

### <span data-ttu-id="e082e-108">Przykład 1. Zapisz szablon wdrożenia</span><span class="sxs-lookup"><span data-stu-id="e082e-108">Example 1: Save a deployment template</span></span>
```
PS C:\>Save-AzureRmResourceGroupDeploymentTemplate -DeploymentName "TestDeployment" -ResourceGroupName "TestGroup"
```

<span data-ttu-id="e082e-109">To polecenie pobiera szablon wdrożenia z TestDeployment i zapisuje go jako plik JSON w bieżącym katalogu.</span><span class="sxs-lookup"><span data-stu-id="e082e-109">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

## <span data-ttu-id="e082e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e082e-110">PARAMETERS</span></span>

### <span data-ttu-id="e082e-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e082e-111">-ApiVersion</span></span>
<span data-ttu-id="e082e-112">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="e082e-112">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="e082e-113">Jeśli nie określono tej funkcji, używana jest Najnowsza wersja interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="e082e-113">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="e082e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e082e-114">-DefaultProfile</span></span>
<span data-ttu-id="e082e-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e082e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e082e-116">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="e082e-116">-DeploymentName</span></span>
<span data-ttu-id="e082e-117">Określa nazwę wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="e082e-117">Specifies the name of the deployment.</span></span>

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

### <span data-ttu-id="e082e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e082e-118">-Force</span></span>
<span data-ttu-id="e082e-119">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e082e-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e082e-120">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e082e-120">-InformationAction</span></span>
<span data-ttu-id="e082e-121">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="e082e-121">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="e082e-122">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e082e-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e082e-123">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="e082e-123">Continue</span></span>
- <span data-ttu-id="e082e-124">Ignorować</span><span class="sxs-lookup"><span data-stu-id="e082e-124">Ignore</span></span>
- <span data-ttu-id="e082e-125">Inquire</span><span class="sxs-lookup"><span data-stu-id="e082e-125">Inquire</span></span>
- <span data-ttu-id="e082e-126">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e082e-126">SilentlyContinue</span></span>
- <span data-ttu-id="e082e-127">Przestaw</span><span class="sxs-lookup"><span data-stu-id="e082e-127">Stop</span></span>
- <span data-ttu-id="e082e-128">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="e082e-128">Suspend</span></span>

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

### <span data-ttu-id="e082e-129">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e082e-129">-InformationVariable</span></span>
<span data-ttu-id="e082e-130">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="e082e-130">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e082e-131">-Path</span><span class="sxs-lookup"><span data-stu-id="e082e-131">-Path</span></span>
<span data-ttu-id="e082e-132">Określa ścieżkę wyjściową pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="e082e-132">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="e082e-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="e082e-133">-Pre</span></span>
<span data-ttu-id="e082e-134">Wskazuje, że za pomocą tego polecenia cmdlet można korzystać z wersji wstępnej API podczas automatycznego ustalania, której wersji interfejsu API należy używać.</span><span class="sxs-lookup"><span data-stu-id="e082e-134">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="e082e-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e082e-135">-ResourceGroupName</span></span>
<span data-ttu-id="e082e-136">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e082e-136">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e082e-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e082e-137">-Confirm</span></span>
<span data-ttu-id="e082e-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e082e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e082e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e082e-139">-WhatIf</span></span>
<span data-ttu-id="e082e-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e082e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e082e-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e082e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e082e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e082e-142">CommonParameters</span></span>
<span data-ttu-id="e082e-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e082e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e082e-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e082e-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e082e-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e082e-145">INPUTS</span></span>

## <span data-ttu-id="e082e-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e082e-146">OUTPUTS</span></span>

## <span data-ttu-id="e082e-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e082e-147">NOTES</span></span>

## <span data-ttu-id="e082e-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e082e-148">RELATED LINKS</span></span>
