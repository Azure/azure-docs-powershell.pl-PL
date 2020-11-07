---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplicationDefinition.md
ms.openlocfilehash: af8d117611eafbeaf79a107e0066ec60b58524e1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871855"
---
# <span data-ttu-id="a032e-101">Get-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="a032e-101">Get-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="a032e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a032e-102">SYNOPSIS</span></span>
<span data-ttu-id="a032e-103">Pobiera definicje aplikacji zarządzanych</span><span class="sxs-lookup"><span data-stu-id="a032e-103">Gets managed application definitions</span></span>

## <span data-ttu-id="a032e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a032e-104">SYNTAX</span></span>

### <span data-ttu-id="a032e-105">GetByNameAndResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a032e-105">GetByNameAndResourceGroup (Default)</span></span>
```
Get-AzManagedApplicationDefinition [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a032e-106">GetById</span><span class="sxs-lookup"><span data-stu-id="a032e-106">GetById</span></span>
```
Get-AzManagedApplicationDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a032e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a032e-107">DESCRIPTION</span></span>
<span data-ttu-id="a032e-108">Polecenie cmdlet **Get-AzManagedApplicationDefinition** umożliwia stosowanie definicji aplikacji zarządzanych</span><span class="sxs-lookup"><span data-stu-id="a032e-108">The **Get-AzManagedApplicationDefinition** cmdlet gets managed application definitions</span></span>

## <span data-ttu-id="a032e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a032e-109">EXAMPLES</span></span>

### <span data-ttu-id="a032e-110">Przykład 1: pobieranie wszystkich definicji aplikacji zarządzanych w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="a032e-110">Example 1: Get all managed application definitions under a resource group</span></span>
```
PS C:\>Get-AzManagedApplicationDefinition -ResourceGroupName "MyRG"
```

<span data-ttu-id="a032e-111">To polecenie pobiera definicje aplikacji zarządzanych w obszarze Grupa zasobów "MyRG"</span><span class="sxs-lookup"><span data-stu-id="a032e-111">This command gets the managed application definitions under resource group "MyRG"</span></span>

### <span data-ttu-id="a032e-112">Przykład 2: uzyskiwanie definicji aplikacji zarządzanej</span><span class="sxs-lookup"><span data-stu-id="a032e-112">Example 2: Get a managed application definition</span></span>
```
PS C:\>Get-AzManagedApplicationDefinition -ResourceGroupName "MyRG" -Name "myManagedAppDef"
```

<span data-ttu-id="a032e-113">To polecenie pobiera definicję aplikacji zarządzanej "myManagedAppDef" w grupie zasób "MyRG".</span><span class="sxs-lookup"><span data-stu-id="a032e-113">This command gets the managed application definition "myManagedAppDef" under resource group "MyRG"</span></span>

## <span data-ttu-id="a032e-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a032e-114">PARAMETERS</span></span>

### <span data-ttu-id="a032e-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a032e-115">-ApiVersion</span></span>
<span data-ttu-id="a032e-116">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="a032e-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="a032e-117">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="a032e-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="a032e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a032e-118">-DefaultProfile</span></span>
<span data-ttu-id="a032e-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a032e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a032e-120">-ID</span><span class="sxs-lookup"><span data-stu-id="a032e-120">-Id</span></span>
<span data-ttu-id="a032e-121">W pełni kwalifikowana nazwa definicji aplikacji zarządzanej, w tym abonament.</span><span class="sxs-lookup"><span data-stu-id="a032e-121">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="a032e-122">na przykład/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="a032e-122">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="a032e-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a032e-123">-Name</span></span>
<span data-ttu-id="a032e-124">Nazwa definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="a032e-124">The managed application definition name.</span></span>

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

### <span data-ttu-id="a032e-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="a032e-125">-Pre</span></span>
<span data-ttu-id="a032e-126">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="a032e-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="a032e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a032e-127">-ResourceGroupName</span></span>
<span data-ttu-id="a032e-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a032e-128">The resource group name.</span></span>

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

### <span data-ttu-id="a032e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a032e-129">CommonParameters</span></span>
<span data-ttu-id="a032e-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a032e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a032e-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a032e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a032e-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a032e-132">INPUTS</span></span>

### <span data-ttu-id="a032e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a032e-133">System.String</span></span>

## <span data-ttu-id="a032e-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a032e-134">OUTPUTS</span></span>

### <span data-ttu-id="a032e-135">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="a032e-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a032e-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a032e-136">NOTES</span></span>

## <span data-ttu-id="a032e-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a032e-137">RELATED LINKS</span></span>
