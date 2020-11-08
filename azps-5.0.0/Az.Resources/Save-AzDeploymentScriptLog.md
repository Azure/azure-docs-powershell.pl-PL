---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
ms.openlocfilehash: 25f20b56ef7da59851d4726ad573c07d4da259e1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234290"
---
# <span data-ttu-id="3ca87-101">Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="3ca87-101">Save-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="3ca87-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3ca87-102">SYNOPSIS</span></span>
<span data-ttu-id="3ca87-103">Zapisuje dziennik wykonania skryptu wdrażania na dysku.</span><span class="sxs-lookup"><span data-stu-id="3ca87-103">Saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="3ca87-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3ca87-104">SYNTAX</span></span>

### <span data-ttu-id="3ca87-105">SaveDeploymentScriptLogByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3ca87-105">SaveDeploymentScriptLogByName (Default)</span></span>
```
Save-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [-OutputPath] <String>
 [[-Tail] <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3ca87-106">SaveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="3ca87-106">SaveDeploymentScriptLogByResourceId</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [-OutputPath] <String> [[-Tail] <Int32>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ca87-107">SaveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="3ca87-107">SaveDeploymentScriptLogByInputObject</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptObject] <PsDeploymentScript> [-OutputPath] <String>
 [[-Tail] <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3ca87-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3ca87-108">DESCRIPTION</span></span>
<span data-ttu-id="3ca87-109">**AzDeploymentScriptLog** zapisuje dziennik wykonania skryptu wdrażania na dysku.</span><span class="sxs-lookup"><span data-stu-id="3ca87-109">The **Save-AzDeploymentScriptLog** saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="3ca87-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3ca87-110">EXAMPLES</span></span>

### <span data-ttu-id="3ca87-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3ca87-111">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace
```

<span data-ttu-id="3ca87-112">Zapisuje dziennik skryptu wdrożenia o podanej nazwie i grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="3ca87-112">Saves the log of a deployment script with the given name and resource group.</span></span>

### <span data-ttu-id="3ca87-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="3ca87-113">Example 2</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace -Tail 3
```

<span data-ttu-id="3ca87-114">Zapisuje ostatnie 3 wiersze dziennika skryptu wdrożenia o danej nazwie i grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="3ca87-114">Saves the last 3 lines of the log of a deployment script with the given name and resource group.</span></span>

## <span data-ttu-id="3ca87-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3ca87-115">PARAMETERS</span></span>

### <span data-ttu-id="3ca87-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ca87-116">-DefaultProfile</span></span>
<span data-ttu-id="3ca87-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3ca87-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ca87-118">-DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="3ca87-118">-DeploymentScriptObject</span></span>
<span data-ttu-id="3ca87-119">Obiekt programu PowerShell skryptu wdrażania.</span><span class="sxs-lookup"><span data-stu-id="3ca87-119">The deployment script PowerShell object.</span></span>

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

### <span data-ttu-id="3ca87-120">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="3ca87-120">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="3ca87-121">W pełni kwalifikowany identyfikator zasobu skryptu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="3ca87-121">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="3ca87-122">Przykład:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="3ca87-122">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

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

### <span data-ttu-id="3ca87-123">-Force</span><span class="sxs-lookup"><span data-stu-id="3ca87-123">-Force</span></span>
<span data-ttu-id="3ca87-124">Wymusza zastąpienie istniejącego pliku.</span><span class="sxs-lookup"><span data-stu-id="3ca87-124">Forces the overwrite of the existing file.</span></span>

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

### <span data-ttu-id="3ca87-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3ca87-125">-Name</span></span>
<span data-ttu-id="3ca87-126">Nazwa skryptu wdrażania.</span><span class="sxs-lookup"><span data-stu-id="3ca87-126">The name of the deployment script.</span></span>

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

### <span data-ttu-id="3ca87-127">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="3ca87-127">-OutputPath</span></span>
<span data-ttu-id="3ca87-128">Ścieżka katalogu, w którym ma zostać zapisany dziennik skryptu wdrażania.</span><span class="sxs-lookup"><span data-stu-id="3ca87-128">The directory path to save deployment script log.</span></span>

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

### <span data-ttu-id="3ca87-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ca87-129">-ResourceGroupName</span></span>
<span data-ttu-id="3ca87-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3ca87-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="3ca87-131">-Koniec</span><span class="sxs-lookup"><span data-stu-id="3ca87-131">-Tail</span></span>
<span data-ttu-id="3ca87-132">Ogranicz dane wyjściowe do ostatnich n wierszy</span><span class="sxs-lookup"><span data-stu-id="3ca87-132">Limit output to last n lines</span></span>

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

### <span data-ttu-id="3ca87-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3ca87-133">-Confirm</span></span>
<span data-ttu-id="3ca87-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ca87-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ca87-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ca87-135">-WhatIf</span></span>
<span data-ttu-id="3ca87-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ca87-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ca87-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3ca87-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ca87-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ca87-138">CommonParameters</span></span>
<span data-ttu-id="3ca87-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ca87-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ca87-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ca87-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ca87-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3ca87-141">INPUTS</span></span>

### <span data-ttu-id="3ca87-142">System. String</span><span class="sxs-lookup"><span data-stu-id="3ca87-142">System.String</span></span>

## <span data-ttu-id="3ca87-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3ca87-143">OUTPUTS</span></span>

### <span data-ttu-id="3ca87-144">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span><span class="sxs-lookup"><span data-stu-id="3ca87-144">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span></span>

## <span data-ttu-id="3ca87-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3ca87-145">NOTES</span></span>

## <span data-ttu-id="3ca87-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3ca87-146">RELATED LINKS</span></span>
