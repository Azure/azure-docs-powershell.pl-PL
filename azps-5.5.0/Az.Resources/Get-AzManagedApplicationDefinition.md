---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplicationDefinition.md
ms.openlocfilehash: 499b2c68dbebdcc16e816c5ce5e76f9b671139f3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178819"
---
# <span data-ttu-id="a63ae-101">Get-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="a63ae-101">Get-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="a63ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a63ae-102">SYNOPSIS</span></span>
<span data-ttu-id="a63ae-103">Pobiera definicje aplikacji zarządzanych</span><span class="sxs-lookup"><span data-stu-id="a63ae-103">Gets managed application definitions</span></span>

## <span data-ttu-id="a63ae-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a63ae-104">SYNTAX</span></span>

### <span data-ttu-id="a63ae-105">GetByNameAndResourceGroup (domyślne)</span><span class="sxs-lookup"><span data-stu-id="a63ae-105">GetByNameAndResourceGroup (Default)</span></span>
```
Get-AzManagedApplicationDefinition [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a63ae-106">GetById</span><span class="sxs-lookup"><span data-stu-id="a63ae-106">GetById</span></span>
```
Get-AzManagedApplicationDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a63ae-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="a63ae-107">DESCRIPTION</span></span>
<span data-ttu-id="a63ae-108">Polecenie **cmdlet Get-AzManagedApplicationDefinition** pobiera zarządzane definicje aplikacji</span><span class="sxs-lookup"><span data-stu-id="a63ae-108">The **Get-AzManagedApplicationDefinition** cmdlet gets managed application definitions</span></span>

## <span data-ttu-id="a63ae-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a63ae-109">EXAMPLES</span></span>

### <span data-ttu-id="a63ae-110">Przykład 1. Uzyskiwanie wszystkich definicji aplikacji zarządzanych w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="a63ae-110">Example 1: Get all managed application definitions under a resource group</span></span>
```
PS C:\>Get-AzManagedApplicationDefinition -ResourceGroupName "MyRG"
```

<span data-ttu-id="a63ae-111">To polecenie pobiera definicje aplikacji zarządzanych w grupie zasobów "MyRG"</span><span class="sxs-lookup"><span data-stu-id="a63ae-111">This command gets the managed application definitions under resource group "MyRG"</span></span>

### <span data-ttu-id="a63ae-112">Przykład 2. Uzyskiwanie definicji aplikacji zarządzanej</span><span class="sxs-lookup"><span data-stu-id="a63ae-112">Example 2: Get a managed application definition</span></span>
```
PS C:\>Get-AzManagedApplicationDefinition -ResourceGroupName "MyRG" -Name "myManagedAppDef"
```

<span data-ttu-id="a63ae-113">To polecenie pobiera definicję aplikacji zarządzanej "myManagedAppDef" w grupie zasobów "MyRG"</span><span class="sxs-lookup"><span data-stu-id="a63ae-113">This command gets the managed application definition "myManagedAppDef" under resource group "MyRG"</span></span>

## <span data-ttu-id="a63ae-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a63ae-114">PARAMETERS</span></span>

### <span data-ttu-id="a63ae-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a63ae-115">-ApiVersion</span></span>
<span data-ttu-id="a63ae-116">Po jego skonfigurowaniu wskazuje wersję interfejsu API dostawcy zasobów, która ma być dostępna.</span><span class="sxs-lookup"><span data-stu-id="a63ae-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="a63ae-117">Jeśli nie zostanie określona, wersja interfejsu API jest automatycznie określana jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="a63ae-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="a63ae-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a63ae-118">-DefaultProfile</span></span>
<span data-ttu-id="a63ae-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a63ae-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a63ae-120">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="a63ae-120">-Id</span></span>
<span data-ttu-id="a63ae-121">W pełni kwalifikowany identyfikator definicji aplikacji zarządzanej, łącznie z subskrypcją.</span><span class="sxs-lookup"><span data-stu-id="a63ae-121">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="a63ae-122">np. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="a63ae-122">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="a63ae-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a63ae-123">-Name</span></span>
<span data-ttu-id="a63ae-124">Nazwa definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="a63ae-124">The managed application definition name.</span></span>

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

### <span data-ttu-id="a63ae-125">— Przed</span><span class="sxs-lookup"><span data-stu-id="a63ae-125">-Pre</span></span>
<span data-ttu-id="a63ae-126">Po jej skonfigurowaniu polecenie cmdlet powinno automatycznie określać wersję do użycia przy użyciu wersji przedpremierowej interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="a63ae-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="a63ae-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a63ae-127">-ResourceGroupName</span></span>
<span data-ttu-id="a63ae-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a63ae-128">The resource group name.</span></span>

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

### <span data-ttu-id="a63ae-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a63ae-129">CommonParameters</span></span>
<span data-ttu-id="a63ae-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a63ae-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a63ae-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a63ae-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a63ae-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a63ae-132">INPUTS</span></span>

### <span data-ttu-id="a63ae-133">System.String</span><span class="sxs-lookup"><span data-stu-id="a63ae-133">System.String</span></span>

## <span data-ttu-id="a63ae-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a63ae-134">OUTPUTS</span></span>

### <span data-ttu-id="a63ae-135">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="a63ae-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a63ae-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a63ae-136">NOTES</span></span>

## <span data-ttu-id="a63ae-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a63ae-137">RELATED LINKS</span></span>
