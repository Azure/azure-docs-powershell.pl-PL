---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8BB4AD6B-EBE3-442A-83E7-B77A31573208
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azresourcegroupdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzResourceGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzResourceGroupDeploymentTemplate.md
ms.openlocfilehash: f9532ebaffaaae6a1429cb7ce8680283572c1775
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708285"
---
# <span data-ttu-id="cadbd-101">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="cadbd-101">Save-AzResourceGroupDeploymentTemplate</span></span>

## <span data-ttu-id="cadbd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cadbd-102">SYNOPSIS</span></span>
<span data-ttu-id="cadbd-103">Zapisuje szablon rozmieszczania grup zasobów do pliku.</span><span class="sxs-lookup"><span data-stu-id="cadbd-103">Saves a resource group deployment template to a file.</span></span>

## <span data-ttu-id="cadbd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cadbd-104">SYNTAX</span></span>

```
Save-AzResourceGroupDeploymentTemplate -ResourceGroupName <String> -DeploymentName <String> [-Path <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cadbd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cadbd-105">DESCRIPTION</span></span>
<span data-ttu-id="cadbd-106">Polecenie cmdlet **Save-AzResourceGroupDeploymentTemplate**  umożliwia zapisanie szablonu rozmieszczania grup zasobów w pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="cadbd-106">The **Save-AzResourceGroupDeploymentTemplate**  cmdlet saves a resource group deployment template to a JSON file.</span></span>

## <span data-ttu-id="cadbd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cadbd-107">EXAMPLES</span></span>

### <span data-ttu-id="cadbd-108">Przykład 1. Zapisz szablon wdrożenia</span><span class="sxs-lookup"><span data-stu-id="cadbd-108">Example 1: Save a deployment template</span></span>
```
PS C:\>Save-AzResourceGroupDeploymentTemplate -DeploymentName "TestDeployment" -ResourceGroupName "TestGroup"
```

<span data-ttu-id="cadbd-109">To polecenie pobiera szablon wdrożenia z TestDeployment i zapisuje go jako plik JSON w bieżącym katalogu.</span><span class="sxs-lookup"><span data-stu-id="cadbd-109">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

## <span data-ttu-id="cadbd-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cadbd-110">PARAMETERS</span></span>

### <span data-ttu-id="cadbd-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="cadbd-111">-ApiVersion</span></span>
<span data-ttu-id="cadbd-112">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="cadbd-112">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="cadbd-113">Jeśli nie określono tej funkcji, używana jest Najnowsza wersja interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="cadbd-113">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="cadbd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cadbd-114">-DefaultProfile</span></span>
<span data-ttu-id="cadbd-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="cadbd-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cadbd-116">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="cadbd-116">-DeploymentName</span></span>
<span data-ttu-id="cadbd-117">Określa nazwę wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="cadbd-117">Specifies the name of the deployment.</span></span>

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

### <span data-ttu-id="cadbd-118">-Force</span><span class="sxs-lookup"><span data-stu-id="cadbd-118">-Force</span></span>
<span data-ttu-id="cadbd-119">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="cadbd-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cadbd-120">-Path</span><span class="sxs-lookup"><span data-stu-id="cadbd-120">-Path</span></span>
<span data-ttu-id="cadbd-121">Określa ścieżkę wyjściową pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="cadbd-121">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="cadbd-122">-Pre</span><span class="sxs-lookup"><span data-stu-id="cadbd-122">-Pre</span></span>
<span data-ttu-id="cadbd-123">Wskazuje, że za pomocą tego polecenia cmdlet można korzystać z wersji wstępnej API podczas automatycznego ustalania, której wersji interfejsu API należy używać.</span><span class="sxs-lookup"><span data-stu-id="cadbd-123">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="cadbd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cadbd-124">-ResourceGroupName</span></span>
<span data-ttu-id="cadbd-125">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cadbd-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="cadbd-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cadbd-126">-Confirm</span></span>
<span data-ttu-id="cadbd-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cadbd-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cadbd-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cadbd-128">-WhatIf</span></span>
<span data-ttu-id="cadbd-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cadbd-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cadbd-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cadbd-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cadbd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cadbd-131">CommonParameters</span></span>
<span data-ttu-id="cadbd-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cadbd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cadbd-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cadbd-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cadbd-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cadbd-134">INPUTS</span></span>

### <span data-ttu-id="cadbd-135">System. String</span><span class="sxs-lookup"><span data-stu-id="cadbd-135">System.String</span></span>

## <span data-ttu-id="cadbd-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cadbd-136">OUTPUTS</span></span>

### <span data-ttu-id="cadbd-137">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="cadbd-137">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="cadbd-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cadbd-138">NOTES</span></span>

## <span data-ttu-id="cadbd-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cadbd-139">RELATED LINKS</span></span>
