---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/save-azmanagementgroupdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzManagementGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzManagementGroupDeploymentTemplate.md
ms.openlocfilehash: c5d01afa5cd583ac0d356913dc3633cfddba6204
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102016026"
---
# <span data-ttu-id="320c1-101">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="320c1-101">Save-AzManagementGroupDeploymentTemplate</span></span>

## <span data-ttu-id="320c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="320c1-102">SYNOPSIS</span></span>
<span data-ttu-id="320c1-103">Umożliwia zapisanie szablonu wdrożenia w pliku.</span><span class="sxs-lookup"><span data-stu-id="320c1-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="320c1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="320c1-104">SYNTAX</span></span>

### <span data-ttu-id="320c1-105">SaveByDeploymentName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="320c1-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzManagementGroupDeploymentTemplate -ManagementGroupId <String> -DeploymentName <String> [-Path <String>]
 [-Force] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="320c1-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="320c1-106">SaveByDeploymentObject</span></span>
```
Save-AzManagementGroupDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="320c1-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="320c1-107">DESCRIPTION</span></span>
<span data-ttu-id="320c1-108">Polecenie cmdlet **Save-AzManagementGroupDeploymentTemplate**  zapisuje szablon wdrożenia w pliku JSON dla wdrożenia w grupie zarządzania.</span><span class="sxs-lookup"><span data-stu-id="320c1-108">The **Save-AzManagementGroupDeploymentTemplate**  cmdlet saves a deployment template to a JSON file for a deployment at a management group.</span></span>

## <span data-ttu-id="320c1-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="320c1-109">EXAMPLES</span></span>

### <span data-ttu-id="320c1-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="320c1-110">Example 1</span></span>
```powershell
PS C:\> Save-AzManagementGroupDeploymentTemplate -ManagementGroupId "myMG" -DeploymentName "TestDeployment"
```

<span data-ttu-id="320c1-111">To polecenie pobiera szablon wdrożenia z witryny TestDeployment i zapisuje go jako plik JSON w bieżącym katalogu.</span><span class="sxs-lookup"><span data-stu-id="320c1-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="320c1-112">Przykład 2. Uzyskiwanie wdrożenia i zapisywanie jego szablonu</span><span class="sxs-lookup"><span data-stu-id="320c1-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzManagementGroupDeploymentTemplate -ManagementGroupId "myMG" -Name "RolesDeployment" | Save-AzManagementGroupDeploymentTemplate
```

<span data-ttu-id="320c1-113">To polecenie pobiera wdrożenie "RolesDeployment" w grupie zarządzania "myMG" i zapisuje jego szablon.</span><span class="sxs-lookup"><span data-stu-id="320c1-113">This command gets the deployment "RolesDeployment" at the management group "myMG" and saves its template.</span></span>

## <span data-ttu-id="320c1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="320c1-114">PARAMETERS</span></span>

### <span data-ttu-id="320c1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="320c1-115">-DefaultProfile</span></span>
<span data-ttu-id="320c1-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="320c1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="320c1-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="320c1-117">-DeploymentName</span></span>
<span data-ttu-id="320c1-118">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="320c1-118">The deployment name.</span></span>

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

### <span data-ttu-id="320c1-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="320c1-119">-DeploymentObject</span></span>
<span data-ttu-id="320c1-120">Obiekt wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="320c1-120">The deployment object.</span></span>

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

### <span data-ttu-id="320c1-121">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="320c1-121">-Force</span></span>
<span data-ttu-id="320c1-122">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="320c1-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="320c1-123">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="320c1-123">-ManagementGroupId</span></span>
<span data-ttu-id="320c1-124">Identyfikator grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="320c1-124">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: SaveByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="320c1-125">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="320c1-125">-Path</span></span>
<span data-ttu-id="320c1-126">Ścieżka wyjściowa pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="320c1-126">The output path of the template file.</span></span>

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

### <span data-ttu-id="320c1-127">— Przed</span><span class="sxs-lookup"><span data-stu-id="320c1-127">-Pre</span></span>
<span data-ttu-id="320c1-128">Po jej skonfigurowaniu polecenie cmdlet powinno automatycznie określać wersję do użycia przy użyciu wersji przedpremierowej interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="320c1-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="320c1-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="320c1-129">-Confirm</span></span>
<span data-ttu-id="320c1-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="320c1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="320c1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="320c1-131">-WhatIf</span></span>
<span data-ttu-id="320c1-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="320c1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="320c1-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="320c1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="320c1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="320c1-134">CommonParameters</span></span>
<span data-ttu-id="320c1-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="320c1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="320c1-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="320c1-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="320c1-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="320c1-137">INPUTS</span></span>

### <span data-ttu-id="320c1-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="320c1-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="320c1-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="320c1-139">OUTPUTS</span></span>

### <span data-ttu-id="320c1-140">Microsoft.Azure.Commands.ResourceManager.Cmdlet.SdkModels.PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="320c1-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="320c1-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="320c1-141">NOTES</span></span>

## <span data-ttu-id="320c1-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="320c1-142">RELATED LINKS</span></span>
