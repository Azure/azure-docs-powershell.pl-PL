---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScript.md
ms.openlocfilehash: 761969eea685c21bc513efdfde9ea79a9e1e4a70
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051290"
---
# <span data-ttu-id="ec5d7-101">Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="ec5d7-101">Get-AzDeploymentScript</span></span>

## <span data-ttu-id="ec5d7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ec5d7-102">SYNOPSIS</span></span>
<span data-ttu-id="ec5d7-103">Pobiera lub wyświetla skrypty wdrażania.</span><span class="sxs-lookup"><span data-stu-id="ec5d7-103">Gets or lists deployment scripts.</span></span>

## <span data-ttu-id="ec5d7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ec5d7-104">SYNTAX</span></span>

### <span data-ttu-id="ec5d7-105">ListDeploymentScript (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ec5d7-105">ListDeploymentScript (Default)</span></span>
```
Get-AzDeploymentScript [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ec5d7-106">GetDeploymentScriptByName</span><span class="sxs-lookup"><span data-stu-id="ec5d7-106">GetDeploymentScriptByName</span></span>
```
Get-AzDeploymentScript [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec5d7-107">GetDeploymentScriptByResourceId</span><span class="sxs-lookup"><span data-stu-id="ec5d7-107">GetDeploymentScriptByResourceId</span></span>
```
Get-AzDeploymentScript [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec5d7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ec5d7-108">DESCRIPTION</span></span>
<span data-ttu-id="ec5d7-109">Polecenie cmdlet **Get-AzDeploymentScript** pobiera jeden skrypt wdrażania lub listę skryptów wdrażania.</span><span class="sxs-lookup"><span data-stu-id="ec5d7-109">The **Get-AzDeploymentScript** cmdlet gets a single deployment script or a list of deployment scripts.</span></span>

## <span data-ttu-id="ec5d7-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ec5d7-110">EXAMPLES</span></span>

### <span data-ttu-id="ec5d7-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ec5d7-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScript
```

<span data-ttu-id="ec5d7-112">Wyświetla listę skryptów wdrażania w subskrypcji w kontekście bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="ec5d7-112">Lists deployment scripts in the subscription in current user's context.</span></span>

### <span data-ttu-id="ec5d7-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ec5d7-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="ec5d7-114">Wyświetla listę skryptów wdrażania w grupie DS grupy zasobów — TestRg.</span><span class="sxs-lookup"><span data-stu-id="ec5d7-114">Lists deployment scripts in resource group DS-TestRg.</span></span>

### <span data-ttu-id="ec5d7-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="ec5d7-115">Example 3</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="ec5d7-116">Pobiera skrypt wdrażania o nazwie MyDeploymentScript w usłudze domenowych w usłudze TestRG.</span><span class="sxs-lookup"><span data-stu-id="ec5d7-116">Gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="ec5d7-117">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="ec5d7-117">Example 4</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -Id "/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}"
```

<span data-ttu-id="ec5d7-118">Pobiera skrypt wdrażania o danym identyfikatorze zasobu.</span><span class="sxs-lookup"><span data-stu-id="ec5d7-118">Gets a deployment script with the given resource Id.</span></span> 

## <span data-ttu-id="ec5d7-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ec5d7-119">PARAMETERS</span></span>

### <span data-ttu-id="ec5d7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec5d7-120">-DefaultProfile</span></span>
<span data-ttu-id="ec5d7-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ec5d7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec5d7-122">-ID</span><span class="sxs-lookup"><span data-stu-id="ec5d7-122">-Id</span></span>
<span data-ttu-id="ec5d7-123">W pełni kwalifikowany identyfikator zasobu skryptu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="ec5d7-123">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="ec5d7-124">Przykład:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="ec5d7-124">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptByResourceId
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec5d7-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ec5d7-125">-Name</span></span>
<span data-ttu-id="ec5d7-126">Nazwa skryptu wdrażania</span><span class="sxs-lookup"><span data-stu-id="ec5d7-126">The name of the deployment script</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec5d7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec5d7-127">-ResourceGroupName</span></span>
<span data-ttu-id="ec5d7-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ec5d7-128">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ListDeploymentScript
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetDeploymentScriptByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec5d7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec5d7-129">CommonParameters</span></span>
<span data-ttu-id="ec5d7-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec5d7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ec5d7-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec5d7-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec5d7-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ec5d7-132">INPUTS</span></span>

### <span data-ttu-id="ec5d7-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ec5d7-133">System.String</span></span>

## <span data-ttu-id="ec5d7-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ec5d7-134">OUTPUTS</span></span>

### <span data-ttu-id="ec5d7-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="ec5d7-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="ec5d7-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ec5d7-136">NOTES</span></span>

## <span data-ttu-id="ec5d7-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ec5d7-137">RELATED LINKS</span></span>
