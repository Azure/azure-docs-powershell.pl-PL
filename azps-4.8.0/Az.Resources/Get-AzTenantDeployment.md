---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
ms.openlocfilehash: c3218141e495bb92216e254830ddaa7dd7a0a0c9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063822"
---
# <span data-ttu-id="d0d0c-101">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="d0d0c-101">Get-AzTenantDeployment</span></span>

## <span data-ttu-id="d0d0c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d0d0c-102">SYNOPSIS</span></span>
<span data-ttu-id="d0d0c-103">Pobierz wdrożenie w zakresie dzierżawy</span><span class="sxs-lookup"><span data-stu-id="d0d0c-103">Get deployment at tenant scope</span></span>

## <span data-ttu-id="d0d0c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d0d0c-104">SYNTAX</span></span>

### <span data-ttu-id="d0d0c-105">GetByDeploymentName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d0d0c-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeployment [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0d0c-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="d0d0c-106">GetByDeploymentId</span></span>
```
Get-AzTenantDeployment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d0d0c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d0d0c-107">DESCRIPTION</span></span>
<span data-ttu-id="d0d0c-108">Polecenie cmdlet **Get-AzTenantDeployment** pobiera wdrożenia w zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="d0d0c-108">The **Get-AzTenantDeployment** cmdlet gets the deployments at the tenant scope.</span></span>
<span data-ttu-id="d0d0c-109">Określ *nazwę* lub parametr *ID* , aby przefiltrować wyniki.</span><span class="sxs-lookup"><span data-stu-id="d0d0c-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="d0d0c-110">Domyślnie polecenie **Get-AzTenantDeployment** pobiera wszystkie wdrożenia w zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="d0d0c-110">By default, **Get-AzTenantDeployment** gets all deployments at the tenant scope.</span></span>

## <span data-ttu-id="d0d0c-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d0d0c-111">EXAMPLES</span></span>

### <span data-ttu-id="d0d0c-112">Przykład 1: pobieranie wszystkich wdrożeń w zakresie dzierżawy</span><span class="sxs-lookup"><span data-stu-id="d0d0c-112">Example 1: Get all deployments at the tenant scope</span></span>
```
PS C:\>Get-AzTenantDeployment
```

<span data-ttu-id="d0d0c-113">To polecenie pobiera wszystkie wdrożenia w bieżącym zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="d0d0c-113">This command gets all deployments at the current tenant scope.</span></span>

### <span data-ttu-id="d0d0c-114">Przykład 2: uzyskiwanie wdrożenia według nazwy</span><span class="sxs-lookup"><span data-stu-id="d0d0c-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "Deploy01"
```

<span data-ttu-id="d0d0c-115">To polecenie pobiera wdrożenie "Deploy01" w bieżącym zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="d0d0c-115">This command gets the "Deploy01" deployment at the current tenant scope.</span></span>
<span data-ttu-id="d0d0c-116">Możesz przypisać nazwę do wdrożenia podczas tworzenia go za pomocą poleceń cmdlet **New-AzTenantDeployment** .</span><span class="sxs-lookup"><span data-stu-id="d0d0c-116">You can assign a name to a deployment when you create it by using the **New-AzTenantDeployment** cmdlets.</span></span>
<span data-ttu-id="d0d0c-117">Jeśli nie przypiszesz nazwy, aplety poleceń będą dostarczały nazwę domyślną na podstawie szablonu, który jest wykorzystywany do tworzenia wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="d0d0c-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="d0d0c-118">Przykład 3: uzyskiwanie wdrożenia według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="d0d0c-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="d0d0c-119">To polecenie pobiera wdrożenie "Deploy01" w zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="d0d0c-119">This command gets the "Deploy01" deployment at the tenant scope.</span></span>

## <span data-ttu-id="d0d0c-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d0d0c-120">PARAMETERS</span></span>

### <span data-ttu-id="d0d0c-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d0d0c-121">-ApiVersion</span></span>
<span data-ttu-id="d0d0c-122">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="d0d0c-122">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="d0d0c-123">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="d0d0c-123">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="d0d0c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0d0c-124">-DefaultProfile</span></span>
<span data-ttu-id="d0d0c-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d0d0c-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0d0c-126">-ID</span><span class="sxs-lookup"><span data-stu-id="d0d0c-126">-Id</span></span>
<span data-ttu-id="d0d0c-127">W pełni kwalifikowany identyfikator zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="d0d0c-127">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="d0d0c-128">przykład:/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="d0d0c-128">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="d0d0c-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d0d0c-129">-Name</span></span>
<span data-ttu-id="d0d0c-130">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="d0d0c-130">The name of deployment.</span></span>

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

### <span data-ttu-id="d0d0c-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="d0d0c-131">-Pre</span></span>
<span data-ttu-id="d0d0c-132">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="d0d0c-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="d0d0c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0d0c-133">CommonParameters</span></span>
<span data-ttu-id="d0d0c-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0d0c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0d0c-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0d0c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0d0c-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0d0c-136">INPUTS</span></span>

### <span data-ttu-id="d0d0c-137">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d0d0c-137">None</span></span>

## <span data-ttu-id="d0d0c-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d0d0c-138">OUTPUTS</span></span>

### <span data-ttu-id="d0d0c-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="d0d0c-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="d0d0c-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d0d0c-140">NOTES</span></span>

## <span data-ttu-id="d0d0c-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d0d0c-141">RELATED LINKS</span></span>
