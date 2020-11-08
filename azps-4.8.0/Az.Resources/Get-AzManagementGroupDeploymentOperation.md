---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
ms.openlocfilehash: 4820a1aec02355a535ec7798eb7f8e3dba6458b1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223196"
---
# <span data-ttu-id="1c935-101">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="1c935-101">Get-AzManagementGroupDeploymentOperation</span></span>

## <span data-ttu-id="1c935-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1c935-102">SYNOPSIS</span></span>
<span data-ttu-id="1c935-103">Pobieranie operacji wdrażania grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="1c935-103">Get deployment operation for management group deployment</span></span>

## <span data-ttu-id="1c935-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1c935-104">SYNTAX</span></span>

### <span data-ttu-id="1c935-105">GetByDeploymentName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1c935-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeploymentOperation -ManagementGroupId <String> -DeploymentName <String>
 [-OperationId <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1c935-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="1c935-106">GetByDeploymentObject</span></span>
```
Get-AzManagementGroupDeploymentOperation -DeploymentObject <PSDeployment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c935-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1c935-107">DESCRIPTION</span></span>
<span data-ttu-id="1c935-108">Polecenie cmdlet **Get-AzManagementGroupDeploymentOperation** wyświetla wszystkie operacje, które były częścią wdrożenia grupy zarządzania, aby ułatwić identyfikację i udzielenie dodatkowych informacji na temat operacji, które nie powiodły się dla określonego wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="1c935-108">The **Get-AzManagementGroupDeploymentOperation** cmdlet lists all the operations that were part of a management group deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="1c935-109">Są to te same informacje, które są dostępne w szczegółach wdrażania w portalu.</span><span class="sxs-lookup"><span data-stu-id="1c935-109">This is the same information provided in the deployment details on the portal.</span></span>

## <span data-ttu-id="1c935-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1c935-110">EXAMPLES</span></span>

### <span data-ttu-id="1c935-111">Przykład 1: Uzyskaj operacje wdrażania pod nazwą wdrożenia</span><span class="sxs-lookup"><span data-stu-id="1c935-111">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzManagementGroupDeploymentOperation -ManagementGroupId myMG -DeploymentName Deploy01
```

<span data-ttu-id="1c935-112">Pobiera operacje wdrażania o nazwie "Deploy01" w grupie zarządzania "myMG".</span><span class="sxs-lookup"><span data-stu-id="1c935-112">Gets deployment operations with name "Deploy01" at the management group "myMG".</span></span>

### <span data-ttu-id="1c935-113">Przykład 2: przygotowywanie wdrożenia i pobieranie jego operacji wdrażania</span><span class="sxs-lookup"><span data-stu-id="1c935-113">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId myMG -Name Deploy01 | Get-AzManagementGroupDeploymentOperation
```

<span data-ttu-id="1c935-114">To polecenie pobiera wdrożenie "Deploy01" w grupie zarządzania "myMG" i przeprowadza operacje wdrażania.</span><span class="sxs-lookup"><span data-stu-id="1c935-114">This command gets the deployment "Deploy01" at the management group "myMG" and get its deployment operations.</span></span>

## <span data-ttu-id="1c935-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1c935-115">PARAMETERS</span></span>

### <span data-ttu-id="1c935-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1c935-116">-ApiVersion</span></span>
<span data-ttu-id="1c935-117">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="1c935-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="1c935-118">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="1c935-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="1c935-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c935-119">-DefaultProfile</span></span>
<span data-ttu-id="1c935-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1c935-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c935-121">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="1c935-121">-DeploymentName</span></span>
<span data-ttu-id="1c935-122">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="1c935-122">The deployment name.</span></span>

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

### <span data-ttu-id="1c935-123">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="1c935-123">-DeploymentObject</span></span>
<span data-ttu-id="1c935-124">Obiekt wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="1c935-124">The deployment object.</span></span>

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

### <span data-ttu-id="1c935-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="1c935-125">-ManagementGroupId</span></span>
<span data-ttu-id="1c935-126">Identyfikator grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="1c935-126">The management group id.</span></span>

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

### <span data-ttu-id="1c935-127">-OperationId</span><span class="sxs-lookup"><span data-stu-id="1c935-127">-OperationId</span></span>
<span data-ttu-id="1c935-128">Identyfikator operacji wdrażania.</span><span class="sxs-lookup"><span data-stu-id="1c935-128">The deployment operation Id.</span></span>

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

### <span data-ttu-id="1c935-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="1c935-129">-Pre</span></span>
<span data-ttu-id="1c935-130">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="1c935-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="1c935-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c935-131">CommonParameters</span></span>
<span data-ttu-id="1c935-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c935-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c935-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c935-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c935-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1c935-134">INPUTS</span></span>

### <span data-ttu-id="1c935-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="1c935-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="1c935-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1c935-136">OUTPUTS</span></span>

### <span data-ttu-id="1c935-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="1c935-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="1c935-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1c935-138">NOTES</span></span>

## <span data-ttu-id="1c935-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1c935-139">RELATED LINKS</span></span>
