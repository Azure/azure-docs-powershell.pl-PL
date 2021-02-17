---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
ms.openlocfilehash: 5054fe397c49e437b34755200b7f53c583e6e94f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197995"
---
# <span data-ttu-id="0e07c-101">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="0e07c-101">Get-AzManagementGroupDeploymentOperation</span></span>

## <span data-ttu-id="0e07c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e07c-102">SYNOPSIS</span></span>
<span data-ttu-id="0e07c-103">Uzyskaj operację wdrażania dla wdrożenia grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="0e07c-103">Get deployment operation for management group deployment</span></span>

## <span data-ttu-id="0e07c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0e07c-104">SYNTAX</span></span>

### <span data-ttu-id="0e07c-105">GetByDeploymentName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="0e07c-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeploymentOperation -ManagementGroupId <String> -DeploymentName <String>
 [-OperationId <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e07c-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="0e07c-106">GetByDeploymentObject</span></span>
```
Get-AzManagementGroupDeploymentOperation -DeploymentObject <PSDeployment> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e07c-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="0e07c-107">DESCRIPTION</span></span>
<span data-ttu-id="0e07c-108">Polecenie **cmdlet Get-AzManagementGroupDeploymentOperation** zawiera listę wszystkich operacji, które były częścią wdrożenia grupy zarządzania, aby ułatwić zidentyfikowanie i podaj więcej informacji o dokładnie tych operacjach, których operacja nie powiodła się w danym wdrożeniu.</span><span class="sxs-lookup"><span data-stu-id="0e07c-108">The **Get-AzManagementGroupDeploymentOperation** cmdlet lists all the operations that were part of a management group deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="0e07c-109">Są to te same informacje, które podano w szczegółach wdrożenia w portalu.</span><span class="sxs-lookup"><span data-stu-id="0e07c-109">This is the same information provided in the deployment details on the portal.</span></span>

## <span data-ttu-id="0e07c-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0e07c-110">EXAMPLES</span></span>

### <span data-ttu-id="0e07c-111">Przykład 1. Uzyskiwanie operacji wdrażania nadano nazwę wdrożenia</span><span class="sxs-lookup"><span data-stu-id="0e07c-111">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzManagementGroupDeploymentOperation -ManagementGroupId myMG -DeploymentName Deploy01
```

<span data-ttu-id="0e07c-112">Pobiera operacje wdrażania o nazwie "Deploy01" w grupie zarządzania "myMG".</span><span class="sxs-lookup"><span data-stu-id="0e07c-112">Gets deployment operations with name "Deploy01" at the management group "myMG".</span></span>

### <span data-ttu-id="0e07c-113">Przykład 2. Uzyskiwanie wdrożenia i uzyskiwanie jego operacji wdrażania</span><span class="sxs-lookup"><span data-stu-id="0e07c-113">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId myMG -Name Deploy01 | Get-AzManagementGroupDeploymentOperation
```

<span data-ttu-id="0e07c-114">To polecenie pobiera wdrożenie "Deploy01" w grupie zarządzania "myMG" i otrzymuje operacje wdrażania.</span><span class="sxs-lookup"><span data-stu-id="0e07c-114">This command gets the deployment "Deploy01" at the management group "myMG" and get its deployment operations.</span></span>

## <span data-ttu-id="0e07c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e07c-115">PARAMETERS</span></span>

### <span data-ttu-id="0e07c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e07c-116">-DefaultProfile</span></span>
<span data-ttu-id="0e07c-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0e07c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e07c-118">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="0e07c-118">-DeploymentName</span></span>
<span data-ttu-id="0e07c-119">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="0e07c-119">The deployment name.</span></span>

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

### <span data-ttu-id="0e07c-120">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="0e07c-120">-DeploymentObject</span></span>
<span data-ttu-id="0e07c-121">Obiekt wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="0e07c-121">The deployment object.</span></span>

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

### <span data-ttu-id="0e07c-122">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="0e07c-122">-ManagementGroupId</span></span>
<span data-ttu-id="0e07c-123">Identyfikator grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="0e07c-123">The management group id.</span></span>

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

### <span data-ttu-id="0e07c-124">-OperationId</span><span class="sxs-lookup"><span data-stu-id="0e07c-124">-OperationId</span></span>
<span data-ttu-id="0e07c-125">Identyfikator operacji wdrażania.</span><span class="sxs-lookup"><span data-stu-id="0e07c-125">The deployment operation Id.</span></span>

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

### <span data-ttu-id="0e07c-126">— Przed</span><span class="sxs-lookup"><span data-stu-id="0e07c-126">-Pre</span></span>
<span data-ttu-id="0e07c-127">Po jej skonfigurowaniu polecenie cmdlet powinno automatycznie określać wersję do użycia przy użyciu wersji przedpremierowej interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="0e07c-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="0e07c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e07c-128">CommonParameters</span></span>
<span data-ttu-id="0e07c-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e07c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e07c-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e07c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e07c-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e07c-131">INPUTS</span></span>

### <span data-ttu-id="0e07c-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="0e07c-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="0e07c-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0e07c-133">OUTPUTS</span></span>

### <span data-ttu-id="0e07c-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="0e07c-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="0e07c-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0e07c-135">NOTES</span></span>

## <span data-ttu-id="0e07c-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0e07c-136">RELATED LINKS</span></span>
