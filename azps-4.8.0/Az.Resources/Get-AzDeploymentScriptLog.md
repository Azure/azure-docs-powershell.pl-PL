---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
ms.openlocfilehash: 608450112b7cd4f54ee0f08f0f29c3aa707fff9e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223195"
---
# <span data-ttu-id="ed879-101">Get-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="ed879-101">Get-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="ed879-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ed879-102">SYNOPSIS</span></span>
<span data-ttu-id="ed879-103">Pobiera dziennik wykonania skryptu wdrażania.</span><span class="sxs-lookup"><span data-stu-id="ed879-103">Gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="ed879-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ed879-104">SYNTAX</span></span>

### <span data-ttu-id="ed879-105">GetDeploymentScriptLogByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ed879-105">GetDeploymentScriptLogByName (Default)</span></span>
```
Get-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed879-106">GetDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="ed879-106">GetDeploymentScriptLogByResourceId</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed879-107">GetDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="ed879-107">GetDeploymentScriptLogByInputObject</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptObject] <PsDeploymentScript> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed879-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ed879-108">DESCRIPTION</span></span>
<span data-ttu-id="ed879-109">Polecenie cmdlet **Get-AzDeploymentScriptLog** pobiera dziennik wykonania skryptu wdrażania.</span><span class="sxs-lookup"><span data-stu-id="ed879-109">The **Get-AzDeploymentScriptLog** cmdlet gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="ed879-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ed879-110">EXAMPLES</span></span>

### <span data-ttu-id="ed879-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ed879-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="ed879-112">Pobiera dziennik skryptu wdrożenia o nazwie MyDeploymentScript w grupie zasobów usługi domenowych-TestRG.</span><span class="sxs-lookup"><span data-stu-id="ed879-112">Gets the log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="ed879-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ed879-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -Tail 3
```

<span data-ttu-id="ed879-114">Pobiera 3 ostatnie wiersze dziennika skryptu wdrożenia o nazwie MyDeploymentScript w grupie zasobów usługi domenowych-TestRG.</span><span class="sxs-lookup"><span data-stu-id="ed879-114">Gets the last 3 lines of the log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="ed879-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="ed879-115">Example 3</span></span>
```powershell
PS C:\> $ds = Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
PS C:\> Get-AzDeploymentScriptLog -DeploymentScriptInputObject $ds
```

<span data-ttu-id="ed879-116">Pierwsze polecenie uzyskuje skrypt wdrażania z nazwą MyDeploymentScript w grupie zasoby usługi TestRG.</span><span class="sxs-lookup"><span data-stu-id="ed879-116">The first command gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>
<span data-ttu-id="ed879-117">Drugie polecenie pobiera dziennik danego skryptu wdrażania.</span><span class="sxs-lookup"><span data-stu-id="ed879-117">The second command gets the log of given deployment script.</span></span>

## <span data-ttu-id="ed879-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ed879-118">PARAMETERS</span></span>

### <span data-ttu-id="ed879-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed879-119">-DefaultProfile</span></span>
<span data-ttu-id="ed879-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ed879-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed879-121">-DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="ed879-121">-DeploymentScriptObject</span></span>
<span data-ttu-id="ed879-122">Obiekt programu PowerShell skryptu wdrażania.</span><span class="sxs-lookup"><span data-stu-id="ed879-122">The deployment script PowerShell object.</span></span>

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

### <span data-ttu-id="ed879-123">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="ed879-123">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="ed879-124">W pełni kwalifikowany identyfikator zasobu skryptu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="ed879-124">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="ed879-125">Przykład:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="ed879-125">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

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

### <span data-ttu-id="ed879-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ed879-126">-Name</span></span>
<span data-ttu-id="ed879-127">Nazwa skryptu wdrażania.</span><span class="sxs-lookup"><span data-stu-id="ed879-127">The name of the deployment script.</span></span>

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

### <span data-ttu-id="ed879-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed879-128">-ResourceGroupName</span></span>
<span data-ttu-id="ed879-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ed879-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="ed879-130">-Koniec</span><span class="sxs-lookup"><span data-stu-id="ed879-130">-Tail</span></span>
<span data-ttu-id="ed879-131">Ogranicz dane wyjściowe do ostatnich n wierszy</span><span class="sxs-lookup"><span data-stu-id="ed879-131">Limit output to last n lines</span></span>

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

### <span data-ttu-id="ed879-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed879-132">CommonParameters</span></span>
<span data-ttu-id="ed879-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed879-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed879-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed879-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed879-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed879-135">INPUTS</span></span>

### <span data-ttu-id="ed879-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ed879-136">System.String</span></span>

### <span data-ttu-id="ed879-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="ed879-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="ed879-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ed879-138">OUTPUTS</span></span>

### <span data-ttu-id="ed879-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="ed879-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span></span>

## <span data-ttu-id="ed879-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ed879-140">NOTES</span></span>

## <span data-ttu-id="ed879-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ed879-141">RELATED LINKS</span></span>
