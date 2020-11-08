---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azdeploymentscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeploymentScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeploymentScript.md
ms.openlocfilehash: 647fd1f2f36d052d4d116f090fc438aa22dcc862
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234312"
---
# <span data-ttu-id="b5c2d-101">Remove-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="b5c2d-101">Remove-AzDeploymentScript</span></span>

## <span data-ttu-id="b5c2d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b5c2d-102">SYNOPSIS</span></span>
<span data-ttu-id="b5c2d-103">Usuwa skrypt wdrażania i skojarzone z nim zasoby.</span><span class="sxs-lookup"><span data-stu-id="b5c2d-103">Removes a deployment script and its associated resources.</span></span>


## <span data-ttu-id="b5c2d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b5c2d-104">SYNTAX</span></span>

### <span data-ttu-id="b5c2d-105">RemoveDeploymentScriptLogByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b5c2d-105">RemoveDeploymentScriptLogByName (Default)</span></span>
```
Remove-AzDeploymentScript [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5c2d-106">RemoveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="b5c2d-106">RemoveDeploymentScriptLogByResourceId</span></span>
```
Remove-AzDeploymentScript [-Id] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5c2d-107">RemoveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="b5c2d-107">RemoveDeploymentScriptLogByInputObject</span></span>
```
Remove-AzDeploymentScript [-InputObject] <PsDeploymentScript> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5c2d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b5c2d-108">DESCRIPTION</span></span>
<span data-ttu-id="b5c2d-109">Polecenie cmdlet **Remove-AzDeploymentScript** umożliwia usunięcie skryptu wdrażania i skojarzonych z nim zasobów.</span><span class="sxs-lookup"><span data-stu-id="b5c2d-109">The **Remove-AzDeploymentScript** cmdlet removes a deployment script and its associated resources.</span></span>

## <span data-ttu-id="b5c2d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b5c2d-110">EXAMPLES</span></span>

### <span data-ttu-id="b5c2d-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b5c2d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="b5c2d-112">Usuwa skrypt wdrażania z nazwą MyDeploymentScript w grupie zasobów usługi domenowych-TestRG.</span><span class="sxs-lookup"><span data-stu-id="b5c2d-112">Deletes a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

## <span data-ttu-id="b5c2d-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b5c2d-113">PARAMETERS</span></span>

### <span data-ttu-id="b5c2d-114">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b5c2d-114">-Confirm</span></span>
<span data-ttu-id="b5c2d-115">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5c2d-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5c2d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5c2d-116">-DefaultProfile</span></span>
<span data-ttu-id="b5c2d-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b5c2d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5c2d-118">-ID</span><span class="sxs-lookup"><span data-stu-id="b5c2d-118">-Id</span></span>
<span data-ttu-id="b5c2d-119">W pełni kwalifikowany identyfikator zasobu skryptu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="b5c2d-119">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="b5c2d-120">Przykład:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="b5c2d-120">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

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

### <span data-ttu-id="b5c2d-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b5c2d-121">-InputObject</span></span>
<span data-ttu-id="b5c2d-122">Obiekt programu PowerShell skryptu wdrażania.</span><span class="sxs-lookup"><span data-stu-id="b5c2d-122">The deployment script PowerShell object.</span></span>

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

### <span data-ttu-id="b5c2d-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b5c2d-123">-Name</span></span>
<span data-ttu-id="b5c2d-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b5c2d-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="b5c2d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b5c2d-125">-PassThru</span></span>
<span data-ttu-id="b5c2d-126">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="b5c2d-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b5c2d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5c2d-127">-ResourceGroupName</span></span>
<span data-ttu-id="b5c2d-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b5c2d-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="b5c2d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5c2d-129">-WhatIf</span></span>
<span data-ttu-id="b5c2d-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5c2d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5c2d-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b5c2d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5c2d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5c2d-132">CommonParameters</span></span>
<span data-ttu-id="b5c2d-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5c2d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b5c2d-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5c2d-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5c2d-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b5c2d-135">INPUTS</span></span>

### <span data-ttu-id="b5c2d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b5c2d-136">System.String</span></span>

### <span data-ttu-id="b5c2d-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="b5c2d-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="b5c2d-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b5c2d-138">OUTPUTS</span></span>

### <span data-ttu-id="b5c2d-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="b5c2d-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="b5c2d-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b5c2d-140">NOTES</span></span>

## <span data-ttu-id="b5c2d-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b5c2d-141">RELATED LINKS</span></span>