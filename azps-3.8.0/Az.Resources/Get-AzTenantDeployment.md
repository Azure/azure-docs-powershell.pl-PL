---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
ms.openlocfilehash: c3218141e495bb92216e254830ddaa7dd7a0a0c9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052744"
---
# <span data-ttu-id="e22bc-101">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="e22bc-101">Get-AzTenantDeployment</span></span>

## <span data-ttu-id="e22bc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e22bc-102">SYNOPSIS</span></span>
<span data-ttu-id="e22bc-103">Pobierz wdrożenie w zakresie dzierżawy</span><span class="sxs-lookup"><span data-stu-id="e22bc-103">Get deployment at tenant scope</span></span>

## <span data-ttu-id="e22bc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e22bc-104">SYNTAX</span></span>

### <span data-ttu-id="e22bc-105">GetByDeploymentName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e22bc-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeployment [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e22bc-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="e22bc-106">GetByDeploymentId</span></span>
```
Get-AzTenantDeployment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e22bc-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e22bc-107">DESCRIPTION</span></span>
<span data-ttu-id="e22bc-108">Polecenie cmdlet **Get-AzTenantDeployment** pobiera wdrożenia w zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="e22bc-108">The **Get-AzTenantDeployment** cmdlet gets the deployments at the tenant scope.</span></span>
<span data-ttu-id="e22bc-109">Określ *nazwę* lub parametr *ID* , aby przefiltrować wyniki.</span><span class="sxs-lookup"><span data-stu-id="e22bc-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="e22bc-110">Domyślnie polecenie **Get-AzTenantDeployment** pobiera wszystkie wdrożenia w zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="e22bc-110">By default, **Get-AzTenantDeployment** gets all deployments at the tenant scope.</span></span>

## <span data-ttu-id="e22bc-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e22bc-111">EXAMPLES</span></span>

### <span data-ttu-id="e22bc-112">Przykład 1: pobieranie wszystkich wdrożeń w zakresie dzierżawy</span><span class="sxs-lookup"><span data-stu-id="e22bc-112">Example 1: Get all deployments at the tenant scope</span></span>
```
PS C:\>Get-AzTenantDeployment
```

<span data-ttu-id="e22bc-113">To polecenie pobiera wszystkie wdrożenia w bieżącym zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="e22bc-113">This command gets all deployments at the current tenant scope.</span></span>

### <span data-ttu-id="e22bc-114">Przykład 2: uzyskiwanie wdrożenia według nazwy</span><span class="sxs-lookup"><span data-stu-id="e22bc-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "Deploy01"
```

<span data-ttu-id="e22bc-115">To polecenie pobiera wdrożenie "Deploy01" w bieżącym zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="e22bc-115">This command gets the "Deploy01" deployment at the current tenant scope.</span></span>
<span data-ttu-id="e22bc-116">Możesz przypisać nazwę do wdrożenia podczas tworzenia go za pomocą poleceń cmdlet **New-AzTenantDeployment** .</span><span class="sxs-lookup"><span data-stu-id="e22bc-116">You can assign a name to a deployment when you create it by using the **New-AzTenantDeployment** cmdlets.</span></span>
<span data-ttu-id="e22bc-117">Jeśli nie przypiszesz nazwy, aplety poleceń będą dostarczały nazwę domyślną na podstawie szablonu, który jest wykorzystywany do tworzenia wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="e22bc-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="e22bc-118">Przykład 3: uzyskiwanie wdrożenia według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="e22bc-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="e22bc-119">To polecenie pobiera wdrożenie "Deploy01" w zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="e22bc-119">This command gets the "Deploy01" deployment at the tenant scope.</span></span>

## <span data-ttu-id="e22bc-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e22bc-120">PARAMETERS</span></span>

### <span data-ttu-id="e22bc-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e22bc-121">-ApiVersion</span></span>
<span data-ttu-id="e22bc-122">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="e22bc-122">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="e22bc-123">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="e22bc-123">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e22bc-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e22bc-124">-DefaultProfile</span></span>
<span data-ttu-id="e22bc-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e22bc-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e22bc-126">-ID</span><span class="sxs-lookup"><span data-stu-id="e22bc-126">-Id</span></span>
<span data-ttu-id="e22bc-127">W pełni kwalifikowany identyfikator zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="e22bc-127">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="e22bc-128">przykład:/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="e22bc-128">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e22bc-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e22bc-129">-Name</span></span>
<span data-ttu-id="e22bc-130">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="e22bc-130">The name of deployment.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e22bc-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="e22bc-131">-Pre</span></span>
<span data-ttu-id="e22bc-132">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="e22bc-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="e22bc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e22bc-133">CommonParameters</span></span>
<span data-ttu-id="e22bc-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e22bc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e22bc-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e22bc-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e22bc-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e22bc-136">INPUTS</span></span>

### <span data-ttu-id="e22bc-137">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e22bc-137">None</span></span>

## <span data-ttu-id="e22bc-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e22bc-138">OUTPUTS</span></span>

### <span data-ttu-id="e22bc-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="e22bc-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="e22bc-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e22bc-140">NOTES</span></span>

## <span data-ttu-id="e22bc-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e22bc-141">RELATED LINKS</span></span>
