---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
ms.openlocfilehash: a1cfbf131286a8bae7b8837f798c32b83d566b2d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192763"
---
# <span data-ttu-id="ec3e6-101">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="ec3e6-101">Get-AzTenantDeployment</span></span>

## <span data-ttu-id="ec3e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec3e6-102">SYNOPSIS</span></span>
<span data-ttu-id="ec3e6-103">Uzyskaj wdrożenie w zakresie dzierżawy</span><span class="sxs-lookup"><span data-stu-id="ec3e6-103">Get deployment at tenant scope</span></span>

## <span data-ttu-id="ec3e6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ec3e6-104">SYNTAX</span></span>

### <span data-ttu-id="ec3e6-105">GetByDeploymentName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="ec3e6-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeployment [[-Name] <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ec3e6-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="ec3e6-106">GetByDeploymentId</span></span>
```
Get-AzTenantDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec3e6-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="ec3e6-107">DESCRIPTION</span></span>
<span data-ttu-id="ec3e6-108">Polecenie **cmdlet Get-AzTenantDeployment** pobiera wdrożenia w zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="ec3e6-108">The **Get-AzTenantDeployment** cmdlet gets the deployments at the tenant scope.</span></span>
<span data-ttu-id="ec3e6-109">Określ parametr *Name (Nazwa)* *lub Id (Identyfikator),* aby filtrować wyniki.</span><span class="sxs-lookup"><span data-stu-id="ec3e6-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="ec3e6-110">Domyślnie **get-azTenantDeployment** pobiera wszystkie wdrożenia w zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="ec3e6-110">By default, **Get-AzTenantDeployment** gets all deployments at the tenant scope.</span></span>

## <span data-ttu-id="ec3e6-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ec3e6-111">EXAMPLES</span></span>

### <span data-ttu-id="ec3e6-112">Przykład 1. Uzyskiwanie wszystkich wdrożeń w zakresie dzierżawy</span><span class="sxs-lookup"><span data-stu-id="ec3e6-112">Example 1: Get all deployments at the tenant scope</span></span>
```
PS C:\>Get-AzTenantDeployment
```

<span data-ttu-id="ec3e6-113">To polecenie pobiera wszystkie wdrożenia w bieżącym zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="ec3e6-113">This command gets all deployments at the current tenant scope.</span></span>

### <span data-ttu-id="ec3e6-114">Przykład 2. Uzyskiwanie wdrożenia według nazwy</span><span class="sxs-lookup"><span data-stu-id="ec3e6-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "Deploy01"
```

<span data-ttu-id="ec3e6-115">To polecenie pobiera wdrożenie "Deploy01" w zakresie bieżącej dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="ec3e6-115">This command gets the "Deploy01" deployment at the current tenant scope.</span></span>
<span data-ttu-id="ec3e6-116">Możesz przypisać nazwę do wdrożenia podczas jego tworzenia przy użyciu polecenia **cmdlet New-AzTenantDeployment.**</span><span class="sxs-lookup"><span data-stu-id="ec3e6-116">You can assign a name to a deployment when you create it by using the **New-AzTenantDeployment** cmdlets.</span></span>
<span data-ttu-id="ec3e6-117">Jeśli nie przypiszesz nazwy, polecenia cmdlet będą używać domyślnej nazwy na podstawie szablonu użytego do utworzenia wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="ec3e6-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="ec3e6-118">Przykład 3. Uzyskiwanie wdrożenia według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="ec3e6-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="ec3e6-119">To polecenie pobiera wdrożenie "Deploy01" w zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="ec3e6-119">This command gets the "Deploy01" deployment at the tenant scope.</span></span>

## <span data-ttu-id="ec3e6-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec3e6-120">PARAMETERS</span></span>

### <span data-ttu-id="ec3e6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec3e6-121">-DefaultProfile</span></span>
<span data-ttu-id="ec3e6-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ec3e6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec3e6-123">— Id</span><span class="sxs-lookup"><span data-stu-id="ec3e6-123">-Id</span></span>
<span data-ttu-id="ec3e6-124">W pełni kwalifikowany identyfikator zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="ec3e6-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="ec3e6-125">przykład: /providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="ec3e6-125">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec3e6-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ec3e6-126">-Name</span></span>
<span data-ttu-id="ec3e6-127">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="ec3e6-127">The name of deployment.</span></span>

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

### <span data-ttu-id="ec3e6-128">— Przed</span><span class="sxs-lookup"><span data-stu-id="ec3e6-128">-Pre</span></span>
<span data-ttu-id="ec3e6-129">Po jej skonfigurowaniu polecenie cmdlet powinno automatycznie określać wersję do użycia przy użyciu wersji przedpremierowej interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="ec3e6-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="ec3e6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec3e6-130">CommonParameters</span></span>
<span data-ttu-id="ec3e6-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec3e6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec3e6-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ec3e6-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec3e6-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ec3e6-133">INPUTS</span></span>

### <span data-ttu-id="ec3e6-134">Brak</span><span class="sxs-lookup"><span data-stu-id="ec3e6-134">None</span></span>

## <span data-ttu-id="ec3e6-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ec3e6-135">OUTPUTS</span></span>

### <span data-ttu-id="ec3e6-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="ec3e6-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="ec3e6-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ec3e6-137">NOTES</span></span>

## <span data-ttu-id="ec3e6-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ec3e6-138">RELATED LINKS</span></span>
