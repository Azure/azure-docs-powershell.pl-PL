---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
ms.openlocfilehash: d6afb06c05478066e4b76793625864a97e3b6758
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192762"
---
# <span data-ttu-id="d5d54-101">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="d5d54-101">Get-AzTenantDeploymentOperation</span></span>

## <span data-ttu-id="d5d54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5d54-102">SYNOPSIS</span></span>
<span data-ttu-id="d5d54-103">Uzyskaj operację wdrażania do wdrożenia w zakresie dzierżawy</span><span class="sxs-lookup"><span data-stu-id="d5d54-103">Get deployment operation for deployment at tenant scope</span></span>

## <span data-ttu-id="d5d54-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d5d54-104">SYNTAX</span></span>

### <span data-ttu-id="d5d54-105">GetByDeploymentName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="d5d54-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5d54-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="d5d54-106">GetByDeploymentObject</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentObject <PSDeployment> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5d54-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d5d54-107">DESCRIPTION</span></span>
<span data-ttu-id="d5d54-108">Polecenie **cmdlet Get-AzTenantDeploymentOperation** zawiera listę wszystkich operacji, które były częścią wdrożenia w bieżącym zakresie dzierżawy, co pomaga w zidentyfikowaniu i podawać więcej informacji o dokładnie tych operacjach, które zakończyły się niepowodzeniem w danym wdrożeniu.</span><span class="sxs-lookup"><span data-stu-id="d5d54-108">The **Get-AzTenantDeploymentOperation** cmdlet lists all the operations that were part of deployment at the current tenant scope to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>

## <span data-ttu-id="d5d54-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d5d54-109">EXAMPLES</span></span>

### <span data-ttu-id="d5d54-110">Przykład 1. Uzyskiwanie operacji wdrażania nadano nazwę wdrożenia</span><span class="sxs-lookup"><span data-stu-id="d5d54-110">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzTenantDeploymentOperation -DeploymentName Deploy01
```

<span data-ttu-id="d5d54-111">Pobiera operacje wdrażania o nazwie "Deploy01" w bieżącym zakresie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="d5d54-111">Gets deployment operations with name "Deploy01" at the current tenant scope.</span></span>

### <span data-ttu-id="d5d54-112">Przykład 2. Uzyskiwanie wdrożenia i uzyskiwanie jego operacji wdrażania</span><span class="sxs-lookup"><span data-stu-id="d5d54-112">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzTenantDeployment -Name Deploy01 | Get-AzTenantDeploymentOperation
```

<span data-ttu-id="d5d54-113">To polecenie pobiera wdrożenie "Deploy01" w bieżącym zakresie dzierżawy i pobiera jego operacje wdrażania.</span><span class="sxs-lookup"><span data-stu-id="d5d54-113">This command gets the deployment "Deploy01" at the current tenant scope and get its deployment operations.</span></span>

## <span data-ttu-id="d5d54-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5d54-114">PARAMETERS</span></span>

### <span data-ttu-id="d5d54-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5d54-115">-DefaultProfile</span></span>
<span data-ttu-id="d5d54-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d5d54-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5d54-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="d5d54-117">-DeploymentName</span></span>
<span data-ttu-id="d5d54-118">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="d5d54-118">The deployment name.</span></span>

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

### <span data-ttu-id="d5d54-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="d5d54-119">-DeploymentObject</span></span>
<span data-ttu-id="d5d54-120">Obiekt wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="d5d54-120">The deployment object.</span></span>

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

### <span data-ttu-id="d5d54-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="d5d54-121">-OperationId</span></span>
<span data-ttu-id="d5d54-122">Identyfikator operacji wdrażania.</span><span class="sxs-lookup"><span data-stu-id="d5d54-122">The deployment operation Id.</span></span>

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

### <span data-ttu-id="d5d54-123">— Przed</span><span class="sxs-lookup"><span data-stu-id="d5d54-123">-Pre</span></span>
<span data-ttu-id="d5d54-124">Po jej skonfigurowaniu polecenie cmdlet powinno automatycznie określać wersję do użycia przy użyciu wersji przedpremierowej interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="d5d54-124">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="d5d54-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5d54-125">CommonParameters</span></span>
<span data-ttu-id="d5d54-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5d54-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5d54-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d5d54-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5d54-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5d54-128">INPUTS</span></span>

### <span data-ttu-id="d5d54-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="d5d54-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="d5d54-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d5d54-130">OUTPUTS</span></span>

### <span data-ttu-id="d5d54-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="d5d54-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="d5d54-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d5d54-132">NOTES</span></span>

## <span data-ttu-id="d5d54-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d5d54-133">RELATED LINKS</span></span>
