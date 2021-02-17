---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azdeploymentscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeploymentScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeploymentScript.md
ms.openlocfilehash: 647fd1f2f36d052d4d116f090fc438aa22dcc862
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186371"
---
# <span data-ttu-id="69518-101">Remove-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="69518-101">Remove-AzDeploymentScript</span></span>

## <span data-ttu-id="69518-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69518-102">SYNOPSIS</span></span>
<span data-ttu-id="69518-103">Usuwa skrypt wdrożenia i skojarzone z nim zasoby.</span><span class="sxs-lookup"><span data-stu-id="69518-103">Removes a deployment script and its associated resources.</span></span>


## <span data-ttu-id="69518-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="69518-104">SYNTAX</span></span>

### <span data-ttu-id="69518-105">RemoveDeploymentScriptLogByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="69518-105">RemoveDeploymentScriptLogByName (Default)</span></span>
```
Remove-AzDeploymentScript [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69518-106">RemoveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="69518-106">RemoveDeploymentScriptLogByResourceId</span></span>
```
Remove-AzDeploymentScript [-Id] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69518-107">RemoveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="69518-107">RemoveDeploymentScriptLogByInputObject</span></span>
```
Remove-AzDeploymentScript [-InputObject] <PsDeploymentScript> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69518-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="69518-108">DESCRIPTION</span></span>
<span data-ttu-id="69518-109">Polecenie **cmdlet Remove-AzDeploymentScript** usuwa skrypt wdrożenia i skojarzone z nim zasoby.</span><span class="sxs-lookup"><span data-stu-id="69518-109">The **Remove-AzDeploymentScript** cmdlet removes a deployment script and its associated resources.</span></span>

## <span data-ttu-id="69518-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="69518-110">EXAMPLES</span></span>

### <span data-ttu-id="69518-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="69518-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="69518-112">Usuwa skrypt wdrożenia o nazwie MyDeploymentScript w grupie zasobów DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="69518-112">Deletes a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

## <span data-ttu-id="69518-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69518-113">PARAMETERS</span></span>

### <span data-ttu-id="69518-114">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="69518-114">-Confirm</span></span>
<span data-ttu-id="69518-115">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="69518-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69518-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69518-116">-DefaultProfile</span></span>
<span data-ttu-id="69518-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="69518-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69518-118">— Id</span><span class="sxs-lookup"><span data-stu-id="69518-118">-Id</span></span>
<span data-ttu-id="69518-119">W pełni kwalifikowany identyfikator zasobu skryptu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="69518-119">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="69518-120">Przykład: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="69518-120">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveDeploymentScriptLogByResourceId
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69518-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69518-121">-InputObject</span></span>
<span data-ttu-id="69518-122">Obiekt skryptu wdrażania programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="69518-122">The deployment script PowerShell object.</span></span>

```yaml
Type: PsDeploymentScript
Parameter Sets: RemoveDeploymentScriptLogByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69518-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="69518-123">-Name</span></span>
<span data-ttu-id="69518-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="69518-124">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69518-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69518-125">-PassThru</span></span>
<span data-ttu-id="69518-126">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="69518-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="69518-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69518-127">-ResourceGroupName</span></span>
<span data-ttu-id="69518-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="69518-128">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69518-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69518-129">-WhatIf</span></span>
<span data-ttu-id="69518-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69518-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69518-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="69518-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69518-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69518-132">CommonParameters</span></span>
<span data-ttu-id="69518-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69518-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="69518-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69518-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69518-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69518-135">INPUTS</span></span>

### <span data-ttu-id="69518-136">System.String</span><span class="sxs-lookup"><span data-stu-id="69518-136">System.String</span></span>

### <span data-ttu-id="69518-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="69518-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="69518-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="69518-138">OUTPUTS</span></span>

### <span data-ttu-id="69518-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="69518-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="69518-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="69518-140">NOTES</span></span>

## <span data-ttu-id="69518-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="69518-141">RELATED LINKS</span></span>