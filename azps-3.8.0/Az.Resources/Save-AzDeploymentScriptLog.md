---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
ms.openlocfilehash: 4e32726b3e7af6608092d29fd52f7a41be042d42
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050753"
---
# <span data-ttu-id="cf2b3-101">Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="cf2b3-101">Save-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="cf2b3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cf2b3-102">SYNOPSIS</span></span>
<span data-ttu-id="cf2b3-103">Zapisuje dziennik wykonania skryptu wdrażania na dysku.</span><span class="sxs-lookup"><span data-stu-id="cf2b3-103">Saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="cf2b3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cf2b3-104">SYNTAX</span></span>

### <span data-ttu-id="cf2b3-105">SaveDeploymentScriptLogByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cf2b3-105">SaveDeploymentScriptLogByName (Default)</span></span>
```
Save-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [-OutputPath] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf2b3-106">SaveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="cf2b3-106">SaveDeploymentScriptLogByResourceId</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [-OutputPath] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf2b3-107">SaveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="cf2b3-107">SaveDeploymentScriptLogByInputObject</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptInputObject] <PsDeploymentScript> [-OutputPath] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf2b3-108">Opis</span><span class="sxs-lookup"><span data-stu-id="cf2b3-108">DESCRIPTION</span></span>
<span data-ttu-id="cf2b3-109">**AzDeploymentScriptLog** zapisuje dziennik wykonania skryptu wdrażania na dysku.</span><span class="sxs-lookup"><span data-stu-id="cf2b3-109">The **Save-AzDeploymentScriptLog** saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="cf2b3-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cf2b3-110">EXAMPLES</span></span>

### <span data-ttu-id="cf2b3-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cf2b3-111">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace
```

<span data-ttu-id="cf2b3-112">Zapisuje dziennik skryptu wdrożenia o podanej nazwie i grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="cf2b3-112">Saves the log of a deployment script with the given name and resource group.</span></span>

## <span data-ttu-id="cf2b3-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cf2b3-113">PARAMETERS</span></span>

### <span data-ttu-id="cf2b3-114">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cf2b3-114">-Confirm</span></span>
<span data-ttu-id="cf2b3-115">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf2b3-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf2b3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf2b3-116">-DefaultProfile</span></span>
<span data-ttu-id="cf2b3-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cf2b3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf2b3-118">-DeploymentScriptInputObject</span><span class="sxs-lookup"><span data-stu-id="cf2b3-118">-DeploymentScriptInputObject</span></span>
<span data-ttu-id="cf2b3-119">Obiekt programu PowerShell skryptu wdrażania.</span><span class="sxs-lookup"><span data-stu-id="cf2b3-119">The deployment script PowerShell object.</span></span>

```yaml
Type: PsDeploymentScript
Parameter Sets: SaveDeploymentScriptLogByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf2b3-120">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="cf2b3-120">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="cf2b3-121">W pełni kwalifikowany identyfikator zasobu skryptu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="cf2b3-121">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="cf2b3-122">Przykład:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="cf2b3-122">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: String
Parameter Sets: SaveDeploymentScriptLogByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf2b3-123">-Force</span><span class="sxs-lookup"><span data-stu-id="cf2b3-123">-Force</span></span>
<span data-ttu-id="cf2b3-124">Wymusza zastąpienie istniejącego pliku.</span><span class="sxs-lookup"><span data-stu-id="cf2b3-124">Forces the overwrite of the existing file.</span></span>

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

### <span data-ttu-id="cf2b3-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cf2b3-125">-Name</span></span>
<span data-ttu-id="cf2b3-126">Nazwa skryptu wdrażania.</span><span class="sxs-lookup"><span data-stu-id="cf2b3-126">The name of the deployment script.</span></span>

```yaml
Type: String
Parameter Sets: SaveDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf2b3-127">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="cf2b3-127">-OutputPath</span></span>
<span data-ttu-id="cf2b3-128">Ścieżka katalogu, w którym ma zostać zapisany dziennik skryptu wdrażania.</span><span class="sxs-lookup"><span data-stu-id="cf2b3-128">The directory path to save deployment script log.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf2b3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf2b3-129">-ResourceGroupName</span></span>
<span data-ttu-id="cf2b3-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cf2b3-130">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: SaveDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf2b3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf2b3-131">-WhatIf</span></span>
<span data-ttu-id="cf2b3-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf2b3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf2b3-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cf2b3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf2b3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf2b3-134">CommonParameters</span></span>
<span data-ttu-id="cf2b3-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf2b3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="cf2b3-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf2b3-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf2b3-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cf2b3-137">INPUTS</span></span>

### <span data-ttu-id="cf2b3-138">System. String</span><span class="sxs-lookup"><span data-stu-id="cf2b3-138">System.String</span></span>

## <span data-ttu-id="cf2b3-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cf2b3-139">OUTPUTS</span></span>

### <span data-ttu-id="cf2b3-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span><span class="sxs-lookup"><span data-stu-id="cf2b3-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span></span>

## <span data-ttu-id="cf2b3-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cf2b3-141">NOTES</span></span>

## <span data-ttu-id="cf2b3-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cf2b3-142">RELATED LINKS</span></span>
