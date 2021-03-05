---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplicationDefinition.md
ms.openlocfilehash: f1f71d188a6b25146103fe3fe5d91b8ba53eaaf8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985636"
---
# <span data-ttu-id="29f79-101">Get-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="29f79-101">Get-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="29f79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29f79-102">SYNOPSIS</span></span>
<span data-ttu-id="29f79-103">Pobiera definicje aplikacji zarządzanych</span><span class="sxs-lookup"><span data-stu-id="29f79-103">Gets managed application definitions</span></span>

## <span data-ttu-id="29f79-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="29f79-104">SYNTAX</span></span>

### <span data-ttu-id="29f79-105">GetByNameAndResourceGroup (domyślne)</span><span class="sxs-lookup"><span data-stu-id="29f79-105">GetByNameAndResourceGroup (Default)</span></span>
```
Get-AzManagedApplicationDefinition [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29f79-106">GetById</span><span class="sxs-lookup"><span data-stu-id="29f79-106">GetById</span></span>
```
Get-AzManagedApplicationDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29f79-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="29f79-107">DESCRIPTION</span></span>
<span data-ttu-id="29f79-108">Polecenie **cmdlet Get-AzManagedApplicationDefinition** pobiera zarządzane definicje aplikacji</span><span class="sxs-lookup"><span data-stu-id="29f79-108">The **Get-AzManagedApplicationDefinition** cmdlet gets managed application definitions</span></span>

## <span data-ttu-id="29f79-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="29f79-109">EXAMPLES</span></span>

### <span data-ttu-id="29f79-110">Przykład 1. Uzyskiwanie wszystkich definicji aplikacji zarządzanych w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="29f79-110">Example 1: Get all managed application definitions under a resource group</span></span>
```
PS C:\>Get-AzManagedApplicationDefinition -ResourceGroupName "MyRG"
```

<span data-ttu-id="29f79-111">To polecenie pobiera definicje aplikacji zarządzanych w grupie zasobów "MyRG"</span><span class="sxs-lookup"><span data-stu-id="29f79-111">This command gets the managed application definitions under resource group "MyRG"</span></span>

### <span data-ttu-id="29f79-112">Przykład 2. Uzyskiwanie definicji aplikacji zarządzanej</span><span class="sxs-lookup"><span data-stu-id="29f79-112">Example 2: Get a managed application definition</span></span>
```
PS C:\>Get-AzManagedApplicationDefinition -ResourceGroupName "MyRG" -Name "myManagedAppDef"
```

<span data-ttu-id="29f79-113">To polecenie pobiera definicję aplikacji zarządzanej "myManagedAppDef" w grupie zasobów "MyRG"</span><span class="sxs-lookup"><span data-stu-id="29f79-113">This command gets the managed application definition "myManagedAppDef" under resource group "MyRG"</span></span>

## <span data-ttu-id="29f79-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29f79-114">PARAMETERS</span></span>

### <span data-ttu-id="29f79-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="29f79-115">-ApiVersion</span></span>
<span data-ttu-id="29f79-116">Po jego skonfigurowaniu wskazuje wersję interfejsu API dostawcy zasobów, która ma być dostępna.</span><span class="sxs-lookup"><span data-stu-id="29f79-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="29f79-117">Jeśli nie zostanie określona, wersja interfejsu API jest automatycznie określana jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="29f79-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="29f79-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29f79-118">-DefaultProfile</span></span>
<span data-ttu-id="29f79-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="29f79-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29f79-120">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="29f79-120">-Id</span></span>
<span data-ttu-id="29f79-121">W pełni kwalifikowany identyfikator definicji aplikacji zarządzanej, łącznie z subskrypcją.</span><span class="sxs-lookup"><span data-stu-id="29f79-121">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="29f79-122">np. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="29f79-122">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationDefinitionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29f79-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="29f79-123">-Name</span></span>
<span data-ttu-id="29f79-124">Nazwa definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="29f79-124">The managed application definition name.</span></span>

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

### <span data-ttu-id="29f79-125">— Przed</span><span class="sxs-lookup"><span data-stu-id="29f79-125">-Pre</span></span>
<span data-ttu-id="29f79-126">Po jej skonfigurowaniu polecenie cmdlet powinno automatycznie określać wersję do użycia przy użyciu wersji przedpremierowej interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="29f79-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="29f79-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29f79-127">-ResourceGroupName</span></span>
<span data-ttu-id="29f79-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="29f79-128">The resource group name.</span></span>

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

### <span data-ttu-id="29f79-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29f79-129">CommonParameters</span></span>
<span data-ttu-id="29f79-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29f79-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29f79-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="29f79-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29f79-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29f79-132">INPUTS</span></span>

### <span data-ttu-id="29f79-133">System.String</span><span class="sxs-lookup"><span data-stu-id="29f79-133">System.String</span></span>

## <span data-ttu-id="29f79-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29f79-134">OUTPUTS</span></span>

### <span data-ttu-id="29f79-135">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="29f79-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="29f79-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="29f79-136">NOTES</span></span>

## <span data-ttu-id="29f79-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="29f79-137">RELATED LINKS</span></span>
