---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
ms.openlocfilehash: dc62e4766a83e1a2046b15fbdf6619e08c4b8e28
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956634"
---
# <span data-ttu-id="67575-101">Get-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="67575-101">Get-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="67575-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67575-102">SYNOPSIS</span></span>
<span data-ttu-id="67575-103">Pobiera dziennik wykonywania skryptu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="67575-103">Gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="67575-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="67575-104">SYNTAX</span></span>

### <span data-ttu-id="67575-105">GetDeploymentScriptLogByName (domyślne)</span><span class="sxs-lookup"><span data-stu-id="67575-105">GetDeploymentScriptLogByName (Default)</span></span>
```
Get-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67575-106">GetDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="67575-106">GetDeploymentScriptLogByResourceId</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67575-107">GetDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="67575-107">GetDeploymentScriptLogByInputObject</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptObject] <PsDeploymentScript> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67575-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="67575-108">DESCRIPTION</span></span>
<span data-ttu-id="67575-109">Polecenie **cmdlet Get-AzDeploymentScriptLog** pobiera dziennik wykonywania skryptu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="67575-109">The **Get-AzDeploymentScriptLog** cmdlet gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="67575-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="67575-110">EXAMPLES</span></span>

### <span data-ttu-id="67575-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="67575-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="67575-112">Pobiera dziennik skryptu wdrożenia o nazwie MyDeploymentScript w grupie zasobów DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="67575-112">Gets the log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="67575-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="67575-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -Tail 3
```

<span data-ttu-id="67575-114">Pobiera 3 ostatnie wiersze dziennika skryptu wdrożenia o nazwie MyDeploymentScript w grupie zasobów DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="67575-114">Gets the last 3 lines of the log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="67575-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="67575-115">Example 3</span></span>
```powershell
PS C:\> $ds = Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
PS C:\> Get-AzDeploymentScriptLog -DeploymentScriptInputObject $ds
```

<span data-ttu-id="67575-116">Pierwsze polecenie otrzymuje skrypt wdrożenia o nazwie MyDeploymentScript w grupie zasobów DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="67575-116">The first command gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>
<span data-ttu-id="67575-117">Drugie polecenie pobiera dziennik danego skryptu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="67575-117">The second command gets the log of given deployment script.</span></span>

## <span data-ttu-id="67575-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67575-118">PARAMETERS</span></span>

### <span data-ttu-id="67575-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67575-119">-DefaultProfile</span></span>
<span data-ttu-id="67575-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="67575-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67575-121">-DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="67575-121">-DeploymentScriptObject</span></span>
<span data-ttu-id="67575-122">Obiekt skryptu wdrażania programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="67575-122">The deployment script PowerShell object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript
Parameter Sets: GetDeploymentScriptLogByInputObject
Aliases: DeploymentScriptInputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67575-123">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="67575-123">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="67575-124">W pełni kwalifikowany identyfikator zasobu skryptu wdrażania.</span><span class="sxs-lookup"><span data-stu-id="67575-124">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="67575-125">Przykład: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="67575-125">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetDeploymentScriptLogByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67575-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="67575-126">-Name</span></span>
<span data-ttu-id="67575-127">Nazwa skryptu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="67575-127">The name of the deployment script.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67575-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67575-128">-ResourceGroupName</span></span>
<span data-ttu-id="67575-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="67575-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67575-130">- Tail</span><span class="sxs-lookup"><span data-stu-id="67575-130">-Tail</span></span>
<span data-ttu-id="67575-131">Ograniczanie danych wyjściowych do ostatnich n wierszy</span><span class="sxs-lookup"><span data-stu-id="67575-131">Limit output to last n lines</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67575-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67575-132">CommonParameters</span></span>
<span data-ttu-id="67575-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67575-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67575-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="67575-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67575-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="67575-135">INPUTS</span></span>

### <span data-ttu-id="67575-136">System.String</span><span class="sxs-lookup"><span data-stu-id="67575-136">System.String</span></span>

### <span data-ttu-id="67575-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="67575-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="67575-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="67575-138">OUTPUTS</span></span>

### <span data-ttu-id="67575-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="67575-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span></span>

## <span data-ttu-id="67575-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="67575-140">NOTES</span></span>

## <span data-ttu-id="67575-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="67575-141">RELATED LINKS</span></span>
