---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
ms.openlocfilehash: a1cfbf131286a8bae7b8837f798c32b83d566b2d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308809"
---
# <span data-ttu-id="75ce7-101">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="75ce7-101">Get-AzTenantDeployment</span></span>

## <span data-ttu-id="75ce7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="75ce7-102">SYNOPSIS</span></span>
<span data-ttu-id="75ce7-103">Pobierz wdrożenie w zakresie dzierżawy</span><span class="sxs-lookup"><span data-stu-id="75ce7-103">Get deployment at tenant scope</span></span>

## <span data-ttu-id="75ce7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="75ce7-104">SYNTAX</span></span>

### <span data-ttu-id="75ce7-105">GetByDeploymentName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="75ce7-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeployment [[-Name] <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="75ce7-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="75ce7-106">GetByDeploymentId</span></span>
```
Get-AzTenantDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75ce7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="75ce7-107">DESCRIPTION</span></span>
<span data-ttu-id="75ce7-108">Polecenie cmdlet **Get-AzTenantDeployment** pobiera wdrożenia w zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="75ce7-108">The **Get-AzTenantDeployment** cmdlet gets the deployments at the tenant scope.</span></span>
<span data-ttu-id="75ce7-109">Określ *nazwę* lub parametr *ID* , aby przefiltrować wyniki.</span><span class="sxs-lookup"><span data-stu-id="75ce7-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="75ce7-110">Domyślnie polecenie **Get-AzTenantDeployment** pobiera wszystkie wdrożenia w zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="75ce7-110">By default, **Get-AzTenantDeployment** gets all deployments at the tenant scope.</span></span>

## <span data-ttu-id="75ce7-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="75ce7-111">EXAMPLES</span></span>

### <span data-ttu-id="75ce7-112">Przykład 1: pobieranie wszystkich wdrożeń w zakresie dzierżawy</span><span class="sxs-lookup"><span data-stu-id="75ce7-112">Example 1: Get all deployments at the tenant scope</span></span>
```
PS C:\>Get-AzTenantDeployment
```

<span data-ttu-id="75ce7-113">To polecenie pobiera wszystkie wdrożenia w bieżącym zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="75ce7-113">This command gets all deployments at the current tenant scope.</span></span>

### <span data-ttu-id="75ce7-114">Przykład 2: uzyskiwanie wdrożenia według nazwy</span><span class="sxs-lookup"><span data-stu-id="75ce7-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "Deploy01"
```

<span data-ttu-id="75ce7-115">To polecenie pobiera wdrożenie "Deploy01" w bieżącym zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="75ce7-115">This command gets the "Deploy01" deployment at the current tenant scope.</span></span>
<span data-ttu-id="75ce7-116">Możesz przypisać nazwę do wdrożenia podczas tworzenia go za pomocą poleceń cmdlet **New-AzTenantDeployment** .</span><span class="sxs-lookup"><span data-stu-id="75ce7-116">You can assign a name to a deployment when you create it by using the **New-AzTenantDeployment** cmdlets.</span></span>
<span data-ttu-id="75ce7-117">Jeśli nie przypiszesz nazwy, aplety poleceń będą dostarczały nazwę domyślną na podstawie szablonu, który jest wykorzystywany do tworzenia wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="75ce7-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="75ce7-118">Przykład 3: uzyskiwanie wdrożenia według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="75ce7-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="75ce7-119">To polecenie pobiera wdrożenie "Deploy01" w zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="75ce7-119">This command gets the "Deploy01" deployment at the tenant scope.</span></span>

## <span data-ttu-id="75ce7-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="75ce7-120">PARAMETERS</span></span>

### <span data-ttu-id="75ce7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75ce7-121">-DefaultProfile</span></span>
<span data-ttu-id="75ce7-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="75ce7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75ce7-123">-ID</span><span class="sxs-lookup"><span data-stu-id="75ce7-123">-Id</span></span>
<span data-ttu-id="75ce7-124">W pełni kwalifikowany identyfikator zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="75ce7-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="75ce7-125">przykład:/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="75ce7-125">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="75ce7-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="75ce7-126">-Name</span></span>
<span data-ttu-id="75ce7-127">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="75ce7-127">The name of deployment.</span></span>

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

### <span data-ttu-id="75ce7-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="75ce7-128">-Pre</span></span>
<span data-ttu-id="75ce7-129">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="75ce7-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="75ce7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75ce7-130">CommonParameters</span></span>
<span data-ttu-id="75ce7-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75ce7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75ce7-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75ce7-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75ce7-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="75ce7-133">INPUTS</span></span>

### <span data-ttu-id="75ce7-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="75ce7-134">None</span></span>

## <span data-ttu-id="75ce7-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="75ce7-135">OUTPUTS</span></span>

### <span data-ttu-id="75ce7-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="75ce7-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="75ce7-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="75ce7-137">NOTES</span></span>

## <span data-ttu-id="75ce7-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="75ce7-138">RELATED LINKS</span></span>
