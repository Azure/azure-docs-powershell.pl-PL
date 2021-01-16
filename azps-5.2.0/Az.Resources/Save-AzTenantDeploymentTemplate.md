---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-aztenantdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzTenantDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzTenantDeploymentTemplate.md
ms.openlocfilehash: dcee9317e6aad113088dc3498a337e16e61b6320
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351766"
---
# <span data-ttu-id="5ebd9-101">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="5ebd9-101">Save-AzTenantDeploymentTemplate</span></span>

## <span data-ttu-id="5ebd9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5ebd9-102">SYNOPSIS</span></span>
<span data-ttu-id="5ebd9-103">Zapisuje szablon wdrożenia w pliku.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="5ebd9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5ebd9-104">SYNTAX</span></span>

### <span data-ttu-id="5ebd9-105">SaveByDeploymentName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5ebd9-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzTenantDeploymentTemplate -DeploymentName <String> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ebd9-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="5ebd9-106">SaveByDeploymentObject</span></span>
```
Save-AzTenantDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ebd9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5ebd9-107">DESCRIPTION</span></span>
<span data-ttu-id="5ebd9-108">Polecenie cmdlet **Save-AzTenantDeploymentTemplate**  zapisuje szablon wdrożenia w pliku JSON dla wdrożenia w zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-108">The **Save-AzTenantDeploymentTemplate**  cmdlet saves a deployment template to a JSON file for a deployment at tenant scope.</span></span>

## <span data-ttu-id="5ebd9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5ebd9-109">EXAMPLES</span></span>

### <span data-ttu-id="5ebd9-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5ebd9-110">Example 1</span></span>
```powershell
PS C:\> Save-AzTenantDeploymentTemplate -DeploymentName "TestDeployment"
```

<span data-ttu-id="5ebd9-111">To polecenie pobiera szablon wdrożenia z TestDeployment i zapisuje go jako plik JSON w bieżącym katalogu.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="5ebd9-112">Przykład 2: uzyskiwanie wdrożenia i zapisywanie jego szablonu</span><span class="sxs-lookup"><span data-stu-id="5ebd9-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzTenantDeploymentTemplate -Name "RolesDeployment" | Save-AzTenantDeploymentTemplate
```

<span data-ttu-id="5ebd9-113">To polecenie pobiera wdrożenie "RolesDeployment" w bieżącym zakresie dzierżawy i zapisuje jego szablon.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-113">This command gets the deployment "RolesDeployment" at the current tenant scope and saves its template.</span></span>

## <span data-ttu-id="5ebd9-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5ebd9-114">PARAMETERS</span></span>

### <span data-ttu-id="5ebd9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ebd9-115">-DefaultProfile</span></span>
<span data-ttu-id="5ebd9-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ebd9-117">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="5ebd9-117">-DeploymentName</span></span>
<span data-ttu-id="5ebd9-118">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-118">The deployment name.</span></span>

```yaml
Type: System.String
Parameter Sets: SaveByDeploymentName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ebd9-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="5ebd9-119">-DeploymentObject</span></span>
<span data-ttu-id="5ebd9-120">Obiekt wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-120">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: SaveByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ebd9-121">-Force</span><span class="sxs-lookup"><span data-stu-id="5ebd9-121">-Force</span></span>
<span data-ttu-id="5ebd9-122">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5ebd9-123">-Path</span><span class="sxs-lookup"><span data-stu-id="5ebd9-123">-Path</span></span>
<span data-ttu-id="5ebd9-124">Ścieżka wyjściowa pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-124">The output path of the template file.</span></span>

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

### <span data-ttu-id="5ebd9-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="5ebd9-125">-Pre</span></span>
<span data-ttu-id="5ebd9-126">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="5ebd9-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5ebd9-127">-Confirm</span></span>
<span data-ttu-id="5ebd9-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ebd9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ebd9-129">-WhatIf</span></span>
<span data-ttu-id="5ebd9-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ebd9-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ebd9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ebd9-132">CommonParameters</span></span>
<span data-ttu-id="5ebd9-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ebd9-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ebd9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ebd9-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ebd9-135">INPUTS</span></span>

### <span data-ttu-id="5ebd9-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="5ebd9-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="5ebd9-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5ebd9-137">OUTPUTS</span></span>

### <span data-ttu-id="5ebd9-138">Microsoft. Azure. Commands. resourceName. polecenia. cmdlet. SdkModels. PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="5ebd9-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="5ebd9-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5ebd9-139">NOTES</span></span>

## <span data-ttu-id="5ebd9-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ebd9-140">RELATED LINKS</span></span>
