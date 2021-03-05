---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
ms.openlocfilehash: 92a0aac5043be520f6a7ed7afc2066e0532b79ec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960122"
---
# <span data-ttu-id="0b2cb-101">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="0b2cb-101">Get-AzDeployment</span></span>

## <span data-ttu-id="0b2cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b2cb-102">SYNOPSIS</span></span>
<span data-ttu-id="0b2cb-103">Uzyskaj wdrożenie</span><span class="sxs-lookup"><span data-stu-id="0b2cb-103">Get deployment</span></span>

## <span data-ttu-id="0b2cb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0b2cb-104">SYNTAX</span></span>

### <span data-ttu-id="0b2cb-105">GetByDeploymentName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="0b2cb-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeployment [[-Name] <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b2cb-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="0b2cb-106">GetByDeploymentId</span></span>
```
Get-AzDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b2cb-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="0b2cb-107">DESCRIPTION</span></span>
<span data-ttu-id="0b2cb-108">Polecenie **cmdlet Get-AzDeployment** pobiera wdrożenia w bieżącym zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="0b2cb-108">The **Get-AzDeployment** cmdlet gets the deployments at the current subscription scope.</span></span>
<span data-ttu-id="0b2cb-109">Określ parametr *Name (Nazwa)* *lub Id (Identyfikator),* aby filtrować wyniki.</span><span class="sxs-lookup"><span data-stu-id="0b2cb-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="0b2cb-110">Domyślnie **get-AzDeployment** otrzymuje wszystkie wdrożenia w bieżącym zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="0b2cb-110">By default, **Get-AzDeployment** gets all deployments at the current subscription scope.</span></span>

## <span data-ttu-id="0b2cb-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0b2cb-111">EXAMPLES</span></span>

### <span data-ttu-id="0b2cb-112">Przykład 1. Pobierz wszystkie wdrożenia w zakresie subskrypcji</span><span class="sxs-lookup"><span data-stu-id="0b2cb-112">Example 1: Get all deployments at subscription scope</span></span>
```
PS C:\>Get-AzDeployment
```

<span data-ttu-id="0b2cb-113">To polecenie pobiera wszystkie wdrożenia w bieżącym zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="0b2cb-113">This command gets all deployments at the current subscription scope.</span></span>

### <span data-ttu-id="0b2cb-114">Przykład 2. Uzyskiwanie wdrożenia według nazwy</span><span class="sxs-lookup"><span data-stu-id="0b2cb-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "DeployRoles01"
```

<span data-ttu-id="0b2cb-115">To polecenie pobiera wdrożenie DeployRoles01 w zakresie bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="0b2cb-115">This command gets the DeployRoles01 deployment at the current subscription scope.</span></span>
<span data-ttu-id="0b2cb-116">Możesz przypisać nazwę do wdrożenia podczas jego tworzenia przy użyciu polecenia **cmdlet New-AzDeployment.**</span><span class="sxs-lookup"><span data-stu-id="0b2cb-116">You can assign a name to a deployment when you create it by using the **New-AzDeployment** cmdlets.</span></span>
<span data-ttu-id="0b2cb-117">Jeśli nie przypiszesz nazwy, polecenia cmdlet będą mieć nazwę domyślną opartą na szablonie używanym do tworzenia wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="0b2cb-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

## <span data-ttu-id="0b2cb-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b2cb-118">PARAMETERS</span></span>

### <span data-ttu-id="0b2cb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b2cb-119">-DefaultProfile</span></span>
<span data-ttu-id="0b2cb-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0b2cb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b2cb-121">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="0b2cb-121">-Id</span></span>
<span data-ttu-id="0b2cb-122">W pełni kwalifikowany identyfikator zasobu wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="0b2cb-122">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="0b2cb-123">przykład: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="0b2cb-123">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="0b2cb-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0b2cb-124">-Name</span></span>
<span data-ttu-id="0b2cb-125">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="0b2cb-125">The name of deployment.</span></span>

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

### <span data-ttu-id="0b2cb-126">— Przed</span><span class="sxs-lookup"><span data-stu-id="0b2cb-126">-Pre</span></span>
<span data-ttu-id="0b2cb-127">Po jej skonfigurowaniu polecenie cmdlet powinno automatycznie określać wersję do użycia przy użyciu wersji przedpremierowej interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="0b2cb-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="0b2cb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b2cb-128">CommonParameters</span></span>
<span data-ttu-id="0b2cb-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b2cb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b2cb-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0b2cb-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b2cb-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0b2cb-131">INPUTS</span></span>

### <span data-ttu-id="0b2cb-132">Brak</span><span class="sxs-lookup"><span data-stu-id="0b2cb-132">None</span></span>

## <span data-ttu-id="0b2cb-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0b2cb-133">OUTPUTS</span></span>

### <span data-ttu-id="0b2cb-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="0b2cb-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="0b2cb-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0b2cb-135">NOTES</span></span>

## <span data-ttu-id="0b2cb-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0b2cb-136">RELATED LINKS</span></span>
