---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/save-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
ms.openlocfilehash: 876414b754a259d253dc56e5d92c570aa8f48318
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995205"
---
# <span data-ttu-id="99b7d-101">Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="99b7d-101">Save-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="99b7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99b7d-102">SYNOPSIS</span></span>
<span data-ttu-id="99b7d-103">Zapisuje dziennik wykonywania skryptu wdrożenia na dysku.</span><span class="sxs-lookup"><span data-stu-id="99b7d-103">Saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="99b7d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="99b7d-104">SYNTAX</span></span>

### <span data-ttu-id="99b7d-105">SaveDeploymentScriptLogByName (domyślne)</span><span class="sxs-lookup"><span data-stu-id="99b7d-105">SaveDeploymentScriptLogByName (Default)</span></span>
```
Save-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [-OutputPath] <String>
 [[-Tail] <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="99b7d-106">SaveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="99b7d-106">SaveDeploymentScriptLogByResourceId</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [-OutputPath] <String> [[-Tail] <Int32>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99b7d-107">SaveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="99b7d-107">SaveDeploymentScriptLogByInputObject</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptObject] <PsDeploymentScript> [-OutputPath] <String>
 [[-Tail] <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="99b7d-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="99b7d-108">DESCRIPTION</span></span>
<span data-ttu-id="99b7d-109">Narzędzie **Save-AzDeploymentScriptLog** zapisuje dziennik wykonywania skryptu wdrożenia na dysku.</span><span class="sxs-lookup"><span data-stu-id="99b7d-109">The **Save-AzDeploymentScriptLog** saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="99b7d-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="99b7d-110">EXAMPLES</span></span>

### <span data-ttu-id="99b7d-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="99b7d-111">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace
```

<span data-ttu-id="99b7d-112">Umożliwia zapisanie dziennika skryptu wdrożenia z podaną nazwą i grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="99b7d-112">Saves the log of a deployment script with the given name and resource group.</span></span>

### <span data-ttu-id="99b7d-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="99b7d-113">Example 2</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace -Tail 3
```

<span data-ttu-id="99b7d-114">Umożliwia zapisanie 3 ostatnich wierszy dziennika skryptu wdrożenia z podaną nazwą i grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="99b7d-114">Saves the last 3 lines of the log of a deployment script with the given name and resource group.</span></span>

## <span data-ttu-id="99b7d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99b7d-115">PARAMETERS</span></span>

### <span data-ttu-id="99b7d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99b7d-116">-DefaultProfile</span></span>
<span data-ttu-id="99b7d-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="99b7d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99b7d-118">-DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="99b7d-118">-DeploymentScriptObject</span></span>
<span data-ttu-id="99b7d-119">Obiekt skryptu wdrażania programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="99b7d-119">The deployment script PowerShell object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript
Parameter Sets: SaveDeploymentScriptLogByInputObject
Aliases: DeploymentScriptInputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99b7d-120">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="99b7d-120">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="99b7d-121">W pełni kwalifikowany identyfikator zasobu skryptu wdrażania.</span><span class="sxs-lookup"><span data-stu-id="99b7d-121">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="99b7d-122">Przykład: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="99b7d-122">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: System.String
Parameter Sets: SaveDeploymentScriptLogByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99b7d-123">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="99b7d-123">-Force</span></span>
<span data-ttu-id="99b7d-124">Wymusza zastąpienie istniejącego pliku.</span><span class="sxs-lookup"><span data-stu-id="99b7d-124">Forces the overwrite of the existing file.</span></span>

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

### <span data-ttu-id="99b7d-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="99b7d-125">-Name</span></span>
<span data-ttu-id="99b7d-126">Nazwa skryptu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="99b7d-126">The name of the deployment script.</span></span>

```yaml
Type: System.String
Parameter Sets: SaveDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99b7d-127">- OutputPath</span><span class="sxs-lookup"><span data-stu-id="99b7d-127">-OutputPath</span></span>
<span data-ttu-id="99b7d-128">Ścieżka katalogu do zapisywania dziennika skryptów wdrażania.</span><span class="sxs-lookup"><span data-stu-id="99b7d-128">The directory path to save deployment script log.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99b7d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99b7d-129">-ResourceGroupName</span></span>
<span data-ttu-id="99b7d-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="99b7d-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SaveDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99b7d-131">- Tail</span><span class="sxs-lookup"><span data-stu-id="99b7d-131">-Tail</span></span>
<span data-ttu-id="99b7d-132">Ograniczanie danych wyjściowych do ostatnich n wierszy</span><span class="sxs-lookup"><span data-stu-id="99b7d-132">Limit output to last n lines</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99b7d-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="99b7d-133">-Confirm</span></span>
<span data-ttu-id="99b7d-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="99b7d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99b7d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99b7d-135">-WhatIf</span></span>
<span data-ttu-id="99b7d-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99b7d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99b7d-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="99b7d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99b7d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99b7d-138">CommonParameters</span></span>
<span data-ttu-id="99b7d-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99b7d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99b7d-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="99b7d-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99b7d-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99b7d-141">INPUTS</span></span>

### <span data-ttu-id="99b7d-142">System.String</span><span class="sxs-lookup"><span data-stu-id="99b7d-142">System.String</span></span>

## <span data-ttu-id="99b7d-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99b7d-143">OUTPUTS</span></span>

### <span data-ttu-id="99b7d-144">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span><span class="sxs-lookup"><span data-stu-id="99b7d-144">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span></span>

## <span data-ttu-id="99b7d-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="99b7d-145">NOTES</span></span>

## <span data-ttu-id="99b7d-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="99b7d-146">RELATED LINKS</span></span>
