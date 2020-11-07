---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
ms.openlocfilehash: cde9c4f8827840047e7fa4a1c597ed6338ed8e54
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871875"
---
# <span data-ttu-id="f27af-101">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="f27af-101">Get-AzDeployment</span></span>

## <span data-ttu-id="f27af-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f27af-102">SYNOPSIS</span></span>
<span data-ttu-id="f27af-103">Pobierz wdrożenie</span><span class="sxs-lookup"><span data-stu-id="f27af-103">Get deployment</span></span>

## <span data-ttu-id="f27af-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f27af-104">SYNTAX</span></span>

### <span data-ttu-id="f27af-105">GetByDeploymentName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f27af-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeployment [[-Name] <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f27af-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="f27af-106">GetByDeploymentId</span></span>
```
Get-AzDeployment [-Id <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f27af-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f27af-107">DESCRIPTION</span></span>
<span data-ttu-id="f27af-108">Polecenie cmdlet **Get-AzDeployment** pobiera wdrożenia w bieżącym zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f27af-108">The **Get-AzDeployment** cmdlet gets the deployments at the current subscription scope.</span></span>
<span data-ttu-id="f27af-109">Określ *nazwę* lub parametr *ID* , aby przefiltrować wyniki.</span><span class="sxs-lookup"><span data-stu-id="f27af-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="f27af-110">Domyślnie polecenie **Get-AzDeployment** pobiera wszystkie wdrożenia w bieżącym zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f27af-110">By default, **Get-AzDeployment** gets all deployments at the current subscription scope.</span></span>

## <span data-ttu-id="f27af-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f27af-111">EXAMPLES</span></span>

### <span data-ttu-id="f27af-112">Przykład 1: pobieranie wszystkich wdrożeń w zakresie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="f27af-112">Example 1: Get all deployments at subscription scope</span></span>
```
PS C:\>Get-AzDeployment
```

<span data-ttu-id="f27af-113">To polecenie pobiera wszystkie wdrożenia w bieżącym zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f27af-113">This command gets all deployments at the current subscription scope.</span></span>

### <span data-ttu-id="f27af-114">Przykład 2: uzyskiwanie wdrożenia według nazwy</span><span class="sxs-lookup"><span data-stu-id="f27af-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "DeployRoles01"
```

<span data-ttu-id="f27af-115">To polecenie pobiera wdrożenie DeployRoles01 w bieżącym zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f27af-115">This command gets the DeployRoles01 deployment at the current subscription scope.</span></span>
<span data-ttu-id="f27af-116">Możesz przypisać nazwę do wdrożenia podczas tworzenia go za pomocą poleceń cmdlet **New-AzDeployment** .</span><span class="sxs-lookup"><span data-stu-id="f27af-116">You can assign a name to a deployment when you create it by using the **New-AzDeployment** cmdlets.</span></span>
<span data-ttu-id="f27af-117">Jeśli nie przypiszesz nazwy, aplety poleceń będą dostarczały nazwę domyślną na podstawie szablonu, który jest wykorzystywany do tworzenia wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="f27af-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

## <span data-ttu-id="f27af-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f27af-118">PARAMETERS</span></span>

### <span data-ttu-id="f27af-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f27af-119">-ApiVersion</span></span>
<span data-ttu-id="f27af-120">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="f27af-120">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="f27af-121">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="f27af-121">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="f27af-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f27af-122">-DefaultProfile</span></span>
<span data-ttu-id="f27af-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f27af-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f27af-124">-ID</span><span class="sxs-lookup"><span data-stu-id="f27af-124">-Id</span></span>
<span data-ttu-id="f27af-125">W pełni kwalifikowany identyfikator zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="f27af-125">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="f27af-126">przykład:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="f27af-126">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f27af-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f27af-127">-Name</span></span>
<span data-ttu-id="f27af-128">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="f27af-128">The name of deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f27af-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="f27af-129">-Pre</span></span>
<span data-ttu-id="f27af-130">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="f27af-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f27af-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f27af-131">CommonParameters</span></span>
<span data-ttu-id="f27af-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f27af-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f27af-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f27af-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f27af-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f27af-134">INPUTS</span></span>

### <span data-ttu-id="f27af-135">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f27af-135">None</span></span>

## <span data-ttu-id="f27af-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f27af-136">OUTPUTS</span></span>

### <span data-ttu-id="f27af-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="f27af-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="f27af-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f27af-138">NOTES</span></span>

## <span data-ttu-id="f27af-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f27af-139">RELATED LINKS</span></span>
