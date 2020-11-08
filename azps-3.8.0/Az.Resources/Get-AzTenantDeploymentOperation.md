---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
ms.openlocfilehash: 4505a64b25f0022763541e6cd5d700e7c6c05988
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052743"
---
# <span data-ttu-id="56048-101">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="56048-101">Get-AzTenantDeploymentOperation</span></span>

## <span data-ttu-id="56048-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="56048-102">SYNOPSIS</span></span>
<span data-ttu-id="56048-103">Pobierz operację wdrażania wdrożenia w zakresie dzierżawy</span><span class="sxs-lookup"><span data-stu-id="56048-103">Get deployment operation for deployment at tenant scope</span></span>

## <span data-ttu-id="56048-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="56048-104">SYNTAX</span></span>

### <span data-ttu-id="56048-105">GetByDeploymentName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="56048-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56048-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="56048-106">GetByDeploymentObject</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentObject <PSDeployment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56048-107">Opis</span><span class="sxs-lookup"><span data-stu-id="56048-107">DESCRIPTION</span></span>
<span data-ttu-id="56048-108">Polecenie cmdlet **Get-AzTenantDeploymentOperation** wyświetla wszystkie operacje, które były częścią wdrożenia w bieżącym zakresie dzierżawy, aby ułatwić identyfikację i udzielenie dodatkowych informacji na temat dokładnych operacji, których nie udało się wykonać w przypadku określonego wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="56048-108">The **Get-AzTenantDeploymentOperation** cmdlet lists all the operations that were part of deployment at the current tenant scope to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>

## <span data-ttu-id="56048-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="56048-109">EXAMPLES</span></span>

### <span data-ttu-id="56048-110">Przykład 1: Uzyskaj operacje wdrażania pod nazwą wdrożenia</span><span class="sxs-lookup"><span data-stu-id="56048-110">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzTenantDeploymentOperation -DeploymentName Deploy01
```

<span data-ttu-id="56048-111">Pobiera operacje wdrażania o nazwie "Deploy01" w bieżącym zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="56048-111">Gets deployment operations with name "Deploy01" at the current tenant scope.</span></span>

### <span data-ttu-id="56048-112">Przykład 2: przygotowywanie wdrożenia i pobieranie jego operacji wdrażania</span><span class="sxs-lookup"><span data-stu-id="56048-112">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzTenantDeployment -Name Deploy01 | Get-AzTenantDeploymentOperation
```

<span data-ttu-id="56048-113">To polecenie pobiera wdrożenie "Deploy01" w bieżącym zakresie dzierżawy i uzyskuje jego działania wdrożeniowe.</span><span class="sxs-lookup"><span data-stu-id="56048-113">This command gets the deployment "Deploy01" at the current tenant scope and get its deployment operations.</span></span>

## <span data-ttu-id="56048-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="56048-114">PARAMETERS</span></span>

### <span data-ttu-id="56048-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="56048-115">-ApiVersion</span></span>
<span data-ttu-id="56048-116">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="56048-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="56048-117">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="56048-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="56048-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56048-118">-DefaultProfile</span></span>
<span data-ttu-id="56048-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="56048-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56048-120">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="56048-120">-DeploymentName</span></span>
<span data-ttu-id="56048-121">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="56048-121">The deployment name.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56048-122">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="56048-122">-DeploymentObject</span></span>
<span data-ttu-id="56048-123">Obiekt wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="56048-123">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: GetByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56048-124">-OperationId</span><span class="sxs-lookup"><span data-stu-id="56048-124">-OperationId</span></span>
<span data-ttu-id="56048-125">Identyfikator operacji wdrażania.</span><span class="sxs-lookup"><span data-stu-id="56048-125">The deployment operation Id.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56048-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="56048-126">-Pre</span></span>
<span data-ttu-id="56048-127">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="56048-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="56048-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56048-128">CommonParameters</span></span>
<span data-ttu-id="56048-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56048-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56048-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56048-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56048-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56048-131">INPUTS</span></span>

### <span data-ttu-id="56048-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="56048-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="56048-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="56048-133">OUTPUTS</span></span>

### <span data-ttu-id="56048-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="56048-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="56048-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="56048-135">NOTES</span></span>

## <span data-ttu-id="56048-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="56048-136">RELATED LINKS</span></span>
