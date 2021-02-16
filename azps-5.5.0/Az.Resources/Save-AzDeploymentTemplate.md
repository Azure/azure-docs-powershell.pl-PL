---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentTemplate.md
ms.openlocfilehash: dc6f7c5b66d72ae5c01ecbb8ec93fa737199d06e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189202"
---
# <span data-ttu-id="88e15-101">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="88e15-101">Save-AzDeploymentTemplate</span></span>

## <span data-ttu-id="88e15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88e15-102">SYNOPSIS</span></span>
<span data-ttu-id="88e15-103">Umożliwia zapisanie szablonu wdrożenia w pliku.</span><span class="sxs-lookup"><span data-stu-id="88e15-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="88e15-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="88e15-104">SYNTAX</span></span>

### <span data-ttu-id="88e15-105">SaveByDeploymentName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="88e15-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzDeploymentTemplate -DeploymentName <String> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88e15-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="88e15-106">SaveByDeploymentObject</span></span>
```
Save-AzDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88e15-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="88e15-107">DESCRIPTION</span></span>
<span data-ttu-id="88e15-108">Polecenie **cmdlet Save-AzDeploymentTemplate**  zapisuje szablon wdrożenia w pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="88e15-108">The **Save-AzDeploymentTemplate**  cmdlet saves a deployment template to a JSON file.</span></span>

## <span data-ttu-id="88e15-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="88e15-109">EXAMPLES</span></span>

### <span data-ttu-id="88e15-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="88e15-110">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentTemplate -DeploymentName "TestDeployment"
```

<span data-ttu-id="88e15-111">To polecenie pobiera szablon wdrożenia z witryny TestDeployment i zapisuje go jako plik JSON w bieżącym katalogu.</span><span class="sxs-lookup"><span data-stu-id="88e15-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="88e15-112">Przykład 2. Uzyskiwanie wdrożenia i zapisywanie jego szablonu</span><span class="sxs-lookup"><span data-stu-id="88e15-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzDeployment -Name "RolesDeployment" | Save-AzDeploymentTemplate
```

<span data-ttu-id="88e15-113">To polecenie pobiera wdrożenie "RolesDeployment" w bieżącym zakresie subskrypcji i zapisuje jego szablon.</span><span class="sxs-lookup"><span data-stu-id="88e15-113">This command gets the deployment "RolesDeployment" at the current subscription scope and saves its template.</span></span>

## <span data-ttu-id="88e15-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88e15-114">PARAMETERS</span></span>

### <span data-ttu-id="88e15-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88e15-115">-DefaultProfile</span></span>
<span data-ttu-id="88e15-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="88e15-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88e15-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="88e15-117">-DeploymentName</span></span>
<span data-ttu-id="88e15-118">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="88e15-118">The deployment name.</span></span>

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

### <span data-ttu-id="88e15-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="88e15-119">-DeploymentObject</span></span>
<span data-ttu-id="88e15-120">Obiekt wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="88e15-120">The deployment object.</span></span>

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

### <span data-ttu-id="88e15-121">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="88e15-121">-Force</span></span>
<span data-ttu-id="88e15-122">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="88e15-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="88e15-123">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="88e15-123">-Path</span></span>
<span data-ttu-id="88e15-124">Ścieżka wyjściowa pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="88e15-124">The output path of the template file.</span></span>

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

### <span data-ttu-id="88e15-125">— Przed</span><span class="sxs-lookup"><span data-stu-id="88e15-125">-Pre</span></span>
<span data-ttu-id="88e15-126">Po jej skonfigurowaniu polecenie cmdlet powinno automatycznie określać wersję do użycia przy użyciu wersji przedpremierowej interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="88e15-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="88e15-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="88e15-127">-Confirm</span></span>
<span data-ttu-id="88e15-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="88e15-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88e15-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88e15-129">-WhatIf</span></span>
<span data-ttu-id="88e15-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88e15-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88e15-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="88e15-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88e15-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88e15-132">CommonParameters</span></span>
<span data-ttu-id="88e15-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88e15-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88e15-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="88e15-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88e15-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88e15-135">INPUTS</span></span>

### <span data-ttu-id="88e15-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="88e15-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="88e15-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88e15-137">OUTPUTS</span></span>

### <span data-ttu-id="88e15-138">Microsoft.Azure.Commands.ResourceManager.Cmdlet.SdkModels.PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="88e15-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="88e15-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="88e15-139">NOTES</span></span>

## <span data-ttu-id="88e15-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="88e15-140">RELATED LINKS</span></span>
