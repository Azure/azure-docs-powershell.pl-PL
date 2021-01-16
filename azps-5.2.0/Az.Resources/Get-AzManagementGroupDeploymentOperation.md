---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
ms.openlocfilehash: 5054fe397c49e437b34755200b7f53c583e6e94f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368669"
---
# <span data-ttu-id="d5c27-101">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="d5c27-101">Get-AzManagementGroupDeploymentOperation</span></span>

## <span data-ttu-id="d5c27-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d5c27-102">SYNOPSIS</span></span>
<span data-ttu-id="d5c27-103">Pobieranie operacji wdrażania grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="d5c27-103">Get deployment operation for management group deployment</span></span>

## <span data-ttu-id="d5c27-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d5c27-104">SYNTAX</span></span>

### <span data-ttu-id="d5c27-105">GetByDeploymentName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d5c27-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeploymentOperation -ManagementGroupId <String> -DeploymentName <String>
 [-OperationId <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5c27-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="d5c27-106">GetByDeploymentObject</span></span>
```
Get-AzManagementGroupDeploymentOperation -DeploymentObject <PSDeployment> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5c27-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d5c27-107">DESCRIPTION</span></span>
<span data-ttu-id="d5c27-108">Polecenie cmdlet **Get-AzManagementGroupDeploymentOperation** wyświetla wszystkie operacje, które były częścią wdrożenia grupy zarządzania, aby ułatwić identyfikację i udzielenie dodatkowych informacji na temat operacji, które nie powiodły się dla określonego wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="d5c27-108">The **Get-AzManagementGroupDeploymentOperation** cmdlet lists all the operations that were part of a management group deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="d5c27-109">Są to te same informacje, które są dostępne w szczegółach wdrażania w portalu.</span><span class="sxs-lookup"><span data-stu-id="d5c27-109">This is the same information provided in the deployment details on the portal.</span></span>

## <span data-ttu-id="d5c27-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d5c27-110">EXAMPLES</span></span>

### <span data-ttu-id="d5c27-111">Przykład 1: Uzyskaj operacje wdrażania pod nazwą wdrożenia</span><span class="sxs-lookup"><span data-stu-id="d5c27-111">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzManagementGroupDeploymentOperation -ManagementGroupId myMG -DeploymentName Deploy01
```

<span data-ttu-id="d5c27-112">Pobiera operacje wdrażania o nazwie "Deploy01" w grupie zarządzania "myMG".</span><span class="sxs-lookup"><span data-stu-id="d5c27-112">Gets deployment operations with name "Deploy01" at the management group "myMG".</span></span>

### <span data-ttu-id="d5c27-113">Przykład 2: przygotowywanie wdrożenia i pobieranie jego operacji wdrażania</span><span class="sxs-lookup"><span data-stu-id="d5c27-113">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId myMG -Name Deploy01 | Get-AzManagementGroupDeploymentOperation
```

<span data-ttu-id="d5c27-114">To polecenie pobiera wdrożenie "Deploy01" w grupie zarządzania "myMG" i przeprowadza operacje wdrażania.</span><span class="sxs-lookup"><span data-stu-id="d5c27-114">This command gets the deployment "Deploy01" at the management group "myMG" and get its deployment operations.</span></span>

## <span data-ttu-id="d5c27-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d5c27-115">PARAMETERS</span></span>

### <span data-ttu-id="d5c27-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5c27-116">-DefaultProfile</span></span>
<span data-ttu-id="d5c27-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d5c27-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5c27-118">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="d5c27-118">-DeploymentName</span></span>
<span data-ttu-id="d5c27-119">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="d5c27-119">The deployment name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5c27-120">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="d5c27-120">-DeploymentObject</span></span>
<span data-ttu-id="d5c27-121">Obiekt wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="d5c27-121">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: GetByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5c27-122">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="d5c27-122">-ManagementGroupId</span></span>
<span data-ttu-id="d5c27-123">Identyfikator grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="d5c27-123">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5c27-124">-OperationId</span><span class="sxs-lookup"><span data-stu-id="d5c27-124">-OperationId</span></span>
<span data-ttu-id="d5c27-125">Identyfikator operacji wdrażania.</span><span class="sxs-lookup"><span data-stu-id="d5c27-125">The deployment operation Id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5c27-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="d5c27-126">-Pre</span></span>
<span data-ttu-id="d5c27-127">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="d5c27-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="d5c27-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5c27-128">CommonParameters</span></span>
<span data-ttu-id="d5c27-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5c27-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5c27-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d5c27-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5c27-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5c27-131">INPUTS</span></span>

### <span data-ttu-id="d5c27-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="d5c27-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="d5c27-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d5c27-133">OUTPUTS</span></span>

### <span data-ttu-id="d5c27-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="d5c27-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="d5c27-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d5c27-135">NOTES</span></span>

## <span data-ttu-id="d5c27-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d5c27-136">RELATED LINKS</span></span>
