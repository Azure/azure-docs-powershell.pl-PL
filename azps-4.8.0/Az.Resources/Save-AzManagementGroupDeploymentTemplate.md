---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azmanagementgroupdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzManagementGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzManagementGroupDeploymentTemplate.md
ms.openlocfilehash: 536d8f0d7f92e4ca880998293d74d0fc2f1617f1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219894"
---
# <span data-ttu-id="c688a-101">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="c688a-101">Save-AzManagementGroupDeploymentTemplate</span></span>

## <span data-ttu-id="c688a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c688a-102">SYNOPSIS</span></span>
<span data-ttu-id="c688a-103">Zapisuje szablon wdrożenia w pliku.</span><span class="sxs-lookup"><span data-stu-id="c688a-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="c688a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c688a-104">SYNTAX</span></span>

### <span data-ttu-id="c688a-105">SaveByDeploymentName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c688a-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzManagementGroupDeploymentTemplate -ManagementGroupId <String> -DeploymentName <String> [-Path <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c688a-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="c688a-106">SaveByDeploymentObject</span></span>
```
Save-AzManagementGroupDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c688a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c688a-107">DESCRIPTION</span></span>
<span data-ttu-id="c688a-108">Polecenie cmdlet **Save-AzManagementGroupDeploymentTemplate**  zapisuje szablon wdrożenia w pliku JSON dla wdrożenia w grupie zarządzania.</span><span class="sxs-lookup"><span data-stu-id="c688a-108">The **Save-AzManagementGroupDeploymentTemplate**  cmdlet saves a deployment template to a JSON file for a deployment at a management group.</span></span>

## <span data-ttu-id="c688a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c688a-109">EXAMPLES</span></span>

### <span data-ttu-id="c688a-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c688a-110">Example 1</span></span>
```powershell
PS C:\> Save-AzManagementGroupDeploymentTemplate -ManagementGroupId "myMG" -DeploymentName "TestDeployment"
```

<span data-ttu-id="c688a-111">To polecenie pobiera szablon wdrożenia z TestDeployment i zapisuje go jako plik JSON w bieżącym katalogu.</span><span class="sxs-lookup"><span data-stu-id="c688a-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="c688a-112">Przykład 2: uzyskiwanie wdrożenia i zapisywanie jego szablonu</span><span class="sxs-lookup"><span data-stu-id="c688a-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzManagementGroupDeploymentTemplate -ManagementGroupId "myMG" -Name "RolesDeployment" | Save-AzManagementGroupDeploymentTemplate
```

<span data-ttu-id="c688a-113">To polecenie pobiera wdrożenie "RolesDeployment" w grupie zarządzania "myMG" i zapisuje jego szablon.</span><span class="sxs-lookup"><span data-stu-id="c688a-113">This command gets the deployment "RolesDeployment" at the management group "myMG" and saves its template.</span></span>

## <span data-ttu-id="c688a-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c688a-114">PARAMETERS</span></span>

### <span data-ttu-id="c688a-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c688a-115">-ApiVersion</span></span>
<span data-ttu-id="c688a-116">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="c688a-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="c688a-117">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="c688a-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="c688a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c688a-118">-DefaultProfile</span></span>
<span data-ttu-id="c688a-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c688a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c688a-120">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="c688a-120">-DeploymentName</span></span>
<span data-ttu-id="c688a-121">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="c688a-121">The deployment name.</span></span>

```yaml
Type: String
Parameter Sets: SaveByDeploymentName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c688a-122">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="c688a-122">-DeploymentObject</span></span>
<span data-ttu-id="c688a-123">Obiekt wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="c688a-123">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: SaveByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c688a-124">-Force</span><span class="sxs-lookup"><span data-stu-id="c688a-124">-Force</span></span>
<span data-ttu-id="c688a-125">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c688a-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c688a-126">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="c688a-126">-ManagementGroupId</span></span>
<span data-ttu-id="c688a-127">Identyfikator grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="c688a-127">The management group id.</span></span>

```yaml
Type: String
Parameter Sets: SaveByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c688a-128">-Path</span><span class="sxs-lookup"><span data-stu-id="c688a-128">-Path</span></span>
<span data-ttu-id="c688a-129">Ścieżka wyjściowa pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="c688a-129">The output path of the template file.</span></span>

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

### <span data-ttu-id="c688a-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="c688a-130">-Pre</span></span>
<span data-ttu-id="c688a-131">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="c688a-131">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c688a-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c688a-132">-Confirm</span></span>
<span data-ttu-id="c688a-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c688a-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c688a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c688a-134">-WhatIf</span></span>
<span data-ttu-id="c688a-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c688a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c688a-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c688a-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c688a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c688a-137">CommonParameters</span></span>
<span data-ttu-id="c688a-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c688a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c688a-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c688a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c688a-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c688a-140">INPUTS</span></span>

### <span data-ttu-id="c688a-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="c688a-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="c688a-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c688a-142">OUTPUTS</span></span>

### <span data-ttu-id="c688a-143">Microsoft. Azure. Commands. resourceName. polecenia. cmdlet. SdkModels. PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="c688a-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="c688a-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c688a-144">NOTES</span></span>

## <span data-ttu-id="c688a-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c688a-145">RELATED LINKS</span></span>
