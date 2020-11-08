---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
ms.openlocfilehash: 855127362fbcbf906755affde0bec6de5e7f2698
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053285"
---
# <span data-ttu-id="a2796-101">Get-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="a2796-101">Get-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="a2796-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a2796-102">SYNOPSIS</span></span>
<span data-ttu-id="a2796-103">Pobiera dziennik wykonania skryptu wdrażania.</span><span class="sxs-lookup"><span data-stu-id="a2796-103">Gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="a2796-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a2796-104">SYNTAX</span></span>

### <span data-ttu-id="a2796-105">GetDeploymentScriptLogByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a2796-105">GetDeploymentScriptLogByName (Default)</span></span>
```
Get-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2796-106">GetDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="a2796-106">GetDeploymentScriptLogByResourceId</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a2796-107">GetDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="a2796-107">GetDeploymentScriptLogByInputObject</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptInputObject] <PsDeploymentScript>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2796-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a2796-108">DESCRIPTION</span></span>
<span data-ttu-id="a2796-109">Polecenie cmdlet **Get-AzDeploymentScriptLog** pobiera dziennik wykonania skryptu wdrażania.</span><span class="sxs-lookup"><span data-stu-id="a2796-109">The **Get-AzDeploymentScriptLog** cmdlet gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="a2796-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a2796-110">EXAMPLES</span></span>

### <span data-ttu-id="a2796-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a2796-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="a2796-112">Pobiera dziennik skryptu wdrożenia o nazwie MyDeploymentScript w grupie zasobów usługi domenowych-TestRG.</span><span class="sxs-lookup"><span data-stu-id="a2796-112">Gets log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="a2796-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a2796-113">Example 2</span></span>
```powershell
PS C:\> $ds = Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
PS C:\> Get-AzDeploymentScriptLog -DeploymentScriptInputObject $ds
```

<span data-ttu-id="a2796-114">Pierwsze polecenie uzyskuje skrypt wdrażania z nazwą MyDeploymentScript w grupie zasoby usługi TestRG.</span><span class="sxs-lookup"><span data-stu-id="a2796-114">The first command gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>
<span data-ttu-id="a2796-115">Drugie polecenie pobiera dziennik danego skryptu wdrażania.</span><span class="sxs-lookup"><span data-stu-id="a2796-115">The second command gets the log of given deployment script.</span></span>

## <span data-ttu-id="a2796-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a2796-116">PARAMETERS</span></span>

### <span data-ttu-id="a2796-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2796-117">-DefaultProfile</span></span>
<span data-ttu-id="a2796-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a2796-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2796-119">-DeploymentScriptInputObject</span><span class="sxs-lookup"><span data-stu-id="a2796-119">-DeploymentScriptInputObject</span></span>
<span data-ttu-id="a2796-120">Obiekt programu PowerShell skryptu wdrażania.</span><span class="sxs-lookup"><span data-stu-id="a2796-120">The deployment script PowerShell object.</span></span>

```yaml
Type: PsDeploymentScript
Parameter Sets: GetDeploymentScriptLogByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2796-121">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="a2796-121">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="a2796-122">W pełni kwalifikowany identyfikator zasobu skryptu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="a2796-122">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="a2796-123">Przykład:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="a2796-123">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptLogByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2796-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a2796-124">-Name</span></span>
<span data-ttu-id="a2796-125">Nazwa skryptu wdrażania.</span><span class="sxs-lookup"><span data-stu-id="a2796-125">The name of the deployment script.</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2796-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2796-126">-ResourceGroupName</span></span>
<span data-ttu-id="a2796-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a2796-127">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2796-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2796-128">CommonParameters</span></span>
<span data-ttu-id="a2796-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2796-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a2796-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2796-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2796-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a2796-131">INPUTS</span></span>

### <span data-ttu-id="a2796-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a2796-132">System.String</span></span>

### <span data-ttu-id="a2796-133">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="a2796-133">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="a2796-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a2796-134">OUTPUTS</span></span>

### <span data-ttu-id="a2796-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="a2796-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span></span>

## <span data-ttu-id="a2796-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a2796-136">NOTES</span></span>

## <span data-ttu-id="a2796-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a2796-137">RELATED LINKS</span></span>
