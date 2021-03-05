---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
ms.openlocfilehash: c95fe4a977c70964cf8b4dab86985d79315d3141
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008650"
---
# <span data-ttu-id="9c93d-101">Get-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="9c93d-101">Get-AzManagedApplication</span></span>

## <span data-ttu-id="9c93d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c93d-102">SYNOPSIS</span></span>
<span data-ttu-id="9c93d-103">Pobiera aplikacje zarządzane</span><span class="sxs-lookup"><span data-stu-id="9c93d-103">Gets managed applications</span></span>

## <span data-ttu-id="9c93d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9c93d-104">SYNTAX</span></span>

### <span data-ttu-id="9c93d-105">GetBySubscription (domyślne)</span><span class="sxs-lookup"><span data-stu-id="9c93d-105">GetBySubscription (Default)</span></span>
```
Get-AzManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9c93d-106">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9c93d-106">GetByNameAndResourceGroup</span></span>
```
Get-AzManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c93d-107">GetById</span><span class="sxs-lookup"><span data-stu-id="9c93d-107">GetById</span></span>
```
Get-AzManagedApplication -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9c93d-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="9c93d-108">DESCRIPTION</span></span>
<span data-ttu-id="9c93d-109">Polecenie **cmdlet Get-AzManagedApplication** pobiera aplikacje zarządzane</span><span class="sxs-lookup"><span data-stu-id="9c93d-109">The **Get-AzManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="9c93d-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9c93d-110">EXAMPLES</span></span>

### <span data-ttu-id="9c93d-111">Przykład 1. Uzyskiwanie wszystkich aplikacji zarządzanych w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="9c93d-111">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="9c93d-112">To polecenie pobiera aplikacje zarządzane w grupie zasobów "MyRG"</span><span class="sxs-lookup"><span data-stu-id="9c93d-112">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="9c93d-113">Przykład 2. Uzyskiwanie wszystkich aplikacji zarządzanych</span><span class="sxs-lookup"><span data-stu-id="9c93d-113">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzManagedApplication
```

<span data-ttu-id="9c93d-114">To polecenie pobierze wszystkie aplikacje zarządzane w ramach bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="9c93d-114">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="9c93d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c93d-115">PARAMETERS</span></span>

### <span data-ttu-id="9c93d-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9c93d-116">-ApiVersion</span></span>
<span data-ttu-id="9c93d-117">Po jego skonfigurowaniu wskazuje wersję interfejsu API dostawcy zasobów, która ma być dostępna.</span><span class="sxs-lookup"><span data-stu-id="9c93d-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="9c93d-118">Jeśli nie zostanie określona, wersja interfejsu API jest automatycznie określana jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="9c93d-118">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c93d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c93d-119">-DefaultProfile</span></span>
<span data-ttu-id="9c93d-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9c93d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c93d-121">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="9c93d-121">-Id</span></span>
<span data-ttu-id="9c93d-122">W pełni kwalifikowany identyfikator aplikacji zarządzanej, łącznie z subskrypcją.</span><span class="sxs-lookup"><span data-stu-id="9c93d-122">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="9c93d-123">np. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="9c93d-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c93d-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9c93d-124">-Name</span></span>
<span data-ttu-id="9c93d-125">Nazwa aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="9c93d-125">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c93d-126">— Przed</span><span class="sxs-lookup"><span data-stu-id="9c93d-126">-Pre</span></span>
<span data-ttu-id="9c93d-127">Po jej skonfigurowaniu polecenie cmdlet powinno automatycznie określać wersję do użycia przy użyciu wersji przedpremierowej interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="9c93d-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="9c93d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c93d-128">-ResourceGroupName</span></span>
<span data-ttu-id="9c93d-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9c93d-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c93d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c93d-130">CommonParameters</span></span>
<span data-ttu-id="9c93d-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c93d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c93d-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9c93d-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c93d-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9c93d-133">INPUTS</span></span>

### <span data-ttu-id="9c93d-134">System.String</span><span class="sxs-lookup"><span data-stu-id="9c93d-134">System.String</span></span>

## <span data-ttu-id="9c93d-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9c93d-135">OUTPUTS</span></span>

### <span data-ttu-id="9c93d-136">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="9c93d-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="9c93d-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9c93d-137">NOTES</span></span>

## <span data-ttu-id="9c93d-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9c93d-138">RELATED LINKS</span></span>
