---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermdeployment
schema: 2.0.0
ms.openlocfilehash: 1a86eb136fe976ba5e229ff36bd5d0e2a2cad340
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897806"
---
# <span data-ttu-id="3275a-101">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="3275a-101">Get-AzureRmDeployment</span></span>

## <span data-ttu-id="3275a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3275a-102">SYNOPSIS</span></span>
<span data-ttu-id="3275a-103">Pobierz wdrożenie</span><span class="sxs-lookup"><span data-stu-id="3275a-103">Get deployment</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3275a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3275a-104">SYNTAX</span></span>

### <span data-ttu-id="3275a-105">GetByDeploymentName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3275a-105">GetByDeploymentName (Default)</span></span>
```
Get-AzureRmDeployment [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3275a-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="3275a-106">GetByDeploymentId</span></span>
```
Get-AzureRmDeployment [-Id <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3275a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3275a-107">DESCRIPTION</span></span>
<span data-ttu-id="3275a-108">Polecenie cmdlet **Get-AzureRmDeployment** pobiera wdrożenia w bieżącym zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="3275a-108">The **Get-AzureRmDeployment** cmdlet gets the deployments at the current subscription scope.</span></span>
<span data-ttu-id="3275a-109">Określ *nazwę* lub parametr *ID* , aby przefiltrować wyniki.</span><span class="sxs-lookup"><span data-stu-id="3275a-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="3275a-110">Domyślnie polecenie **Get-AzureRmDeployment** pobiera wszystkie wdrożenia w bieżącym zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="3275a-110">By default, **Get-AzureRmDeployment** gets all deployments at the current subscription scope.</span></span>

## <span data-ttu-id="3275a-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3275a-111">EXAMPLES</span></span>

### <span data-ttu-id="3275a-112">Przykład 1: pobieranie wszystkich wdrożeń w zakresie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="3275a-112">Example 1: Get all deployments at subscription scope</span></span>
```
PS C:\>Get-AzureRmDeployment
```

<span data-ttu-id="3275a-113">To polecenie pobiera wszystkie wdrożenia w bieżącym zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="3275a-113">This command gets all deployments at the current subscription scope.</span></span>

### <span data-ttu-id="3275a-114">Przykład 2: uzyskiwanie wdrożenia według nazwy</span><span class="sxs-lookup"><span data-stu-id="3275a-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzureRmDeployment -Name "DeployRoles01"
```

<span data-ttu-id="3275a-115">To polecenie pobiera wdrożenie DeployRoles01 w bieżącym zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="3275a-115">This command gets the DeployRoles01 deployment at the current subscription scope.</span></span>
<span data-ttu-id="3275a-116">Możesz przypisać nazwę do wdrożenia podczas tworzenia go za pomocą poleceń cmdlet **New-AzureRmDeployment** .</span><span class="sxs-lookup"><span data-stu-id="3275a-116">You can assign a name to a deployment when you create it by using the **New-AzureRmDeployment** cmdlets.</span></span>
<span data-ttu-id="3275a-117">Jeśli nie przypiszesz nazwy, aplety poleceń będą dostarczały nazwę domyślną na podstawie szablonu, który jest wykorzystywany do tworzenia wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="3275a-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

## <span data-ttu-id="3275a-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3275a-118">PARAMETERS</span></span>

### <span data-ttu-id="3275a-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3275a-119">-ApiVersion</span></span>
<span data-ttu-id="3275a-120">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="3275a-120">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="3275a-121">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="3275a-121">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="3275a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3275a-122">-DefaultProfile</span></span>
<span data-ttu-id="3275a-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3275a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3275a-124">-ID</span><span class="sxs-lookup"><span data-stu-id="3275a-124">-Id</span></span>
<span data-ttu-id="3275a-125">W pełni kwalifikowany identyfikator zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="3275a-125">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="3275a-126">przykład:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="3275a-126">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3275a-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3275a-127">-Name</span></span>
<span data-ttu-id="3275a-128">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="3275a-128">The name of deployment.</span></span>

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

### <span data-ttu-id="3275a-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="3275a-129">-Pre</span></span>
<span data-ttu-id="3275a-130">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="3275a-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="3275a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3275a-131">CommonParameters</span></span>
<span data-ttu-id="3275a-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3275a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3275a-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3275a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3275a-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3275a-134">INPUTS</span></span>

### <span data-ttu-id="3275a-135">System. String</span><span class="sxs-lookup"><span data-stu-id="3275a-135">System.String</span></span>

## <span data-ttu-id="3275a-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3275a-136">OUTPUTS</span></span>

### <span data-ttu-id="3275a-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="3275a-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="3275a-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3275a-138">NOTES</span></span>

## <span data-ttu-id="3275a-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3275a-139">RELATED LINKS</span></span>
