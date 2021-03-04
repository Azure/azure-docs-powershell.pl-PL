---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/save-azdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentTemplate.md
ms.openlocfilehash: 64ed7e109877912d7a74937e6bdf6707519aa1e8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967665"
---
# <span data-ttu-id="c8fd3-101">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="c8fd3-101">Save-AzDeploymentTemplate</span></span>

## <span data-ttu-id="c8fd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8fd3-102">SYNOPSIS</span></span>
<span data-ttu-id="c8fd3-103">Umożliwia zapisanie szablonu wdrożenia w pliku.</span><span class="sxs-lookup"><span data-stu-id="c8fd3-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="c8fd3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c8fd3-104">SYNTAX</span></span>

### <span data-ttu-id="c8fd3-105">SaveByDeploymentName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="c8fd3-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzDeploymentTemplate -DeploymentName <String> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8fd3-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="c8fd3-106">SaveByDeploymentObject</span></span>
```
Save-AzDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8fd3-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="c8fd3-107">DESCRIPTION</span></span>
<span data-ttu-id="c8fd3-108">Polecenie **cmdlet Save-AzDeploymentTemplate**  zapisuje szablon wdrożenia w pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="c8fd3-108">The **Save-AzDeploymentTemplate**  cmdlet saves a deployment template to a JSON file.</span></span>

## <span data-ttu-id="c8fd3-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c8fd3-109">EXAMPLES</span></span>

### <span data-ttu-id="c8fd3-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c8fd3-110">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentTemplate -DeploymentName "TestDeployment"
```

<span data-ttu-id="c8fd3-111">To polecenie pobiera szablon wdrożenia z witryny TestDeployment i zapisuje go jako plik JSON w bieżącym katalogu.</span><span class="sxs-lookup"><span data-stu-id="c8fd3-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="c8fd3-112">Przykład 2. Uzyskiwanie wdrożenia i zapisywanie jego szablonu</span><span class="sxs-lookup"><span data-stu-id="c8fd3-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzDeployment -Name "RolesDeployment" | Save-AzDeploymentTemplate
```

<span data-ttu-id="c8fd3-113">To polecenie pobiera wdrożenie "RolesDeployment" w bieżącym zakresie subskrypcji i zapisuje jego szablon.</span><span class="sxs-lookup"><span data-stu-id="c8fd3-113">This command gets the deployment "RolesDeployment" at the current subscription scope and saves its template.</span></span>

## <span data-ttu-id="c8fd3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8fd3-114">PARAMETERS</span></span>

### <span data-ttu-id="c8fd3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8fd3-115">-DefaultProfile</span></span>
<span data-ttu-id="c8fd3-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c8fd3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8fd3-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="c8fd3-117">-DeploymentName</span></span>
<span data-ttu-id="c8fd3-118">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="c8fd3-118">The deployment name.</span></span>

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

### <span data-ttu-id="c8fd3-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="c8fd3-119">-DeploymentObject</span></span>
<span data-ttu-id="c8fd3-120">Obiekt wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="c8fd3-120">The deployment object.</span></span>

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

### <span data-ttu-id="c8fd3-121">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="c8fd3-121">-Force</span></span>
<span data-ttu-id="c8fd3-122">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c8fd3-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c8fd3-123">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="c8fd3-123">-Path</span></span>
<span data-ttu-id="c8fd3-124">Ścieżka wyjściowa pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="c8fd3-124">The output path of the template file.</span></span>

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

### <span data-ttu-id="c8fd3-125">— Przed</span><span class="sxs-lookup"><span data-stu-id="c8fd3-125">-Pre</span></span>
<span data-ttu-id="c8fd3-126">Po jej skonfigurowaniu polecenie cmdlet powinno automatycznie określać wersję do użycia przy użyciu wersji przedpremierowej interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="c8fd3-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c8fd3-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c8fd3-127">-Confirm</span></span>
<span data-ttu-id="c8fd3-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c8fd3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8fd3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8fd3-129">-WhatIf</span></span>
<span data-ttu-id="c8fd3-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8fd3-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8fd3-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c8fd3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8fd3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8fd3-132">CommonParameters</span></span>
<span data-ttu-id="c8fd3-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8fd3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8fd3-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8fd3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8fd3-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c8fd3-135">INPUTS</span></span>

### <span data-ttu-id="c8fd3-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="c8fd3-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="c8fd3-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c8fd3-137">OUTPUTS</span></span>

### <span data-ttu-id="c8fd3-138">Microsoft.Azure.Commands.ResourceManager.Cmdlet.SdkModels.PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="c8fd3-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="c8fd3-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c8fd3-139">NOTES</span></span>

## <span data-ttu-id="c8fd3-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c8fd3-140">RELATED LINKS</span></span>
