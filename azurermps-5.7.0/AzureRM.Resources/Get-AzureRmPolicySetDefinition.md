---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
ms.openlocfilehash: 694f2ef459b50648e934e4ea0e434fe218d4b1f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550567"
---
# <span data-ttu-id="ae013-101">Get-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="ae013-101">Get-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="ae013-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ae013-102">SYNOPSIS</span></span>
<span data-ttu-id="ae013-103">Pobiera definicje zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="ae013-103">Gets policy set definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae013-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ae013-104">SYNTAX</span></span>

### <span data-ttu-id="ae013-105">GetBySubscription (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ae013-105">GetBySubscription (Default)</span></span>
```
Get-AzureRmPolicySetDefinition [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ae013-106">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ae013-106">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmPolicySetDefinition -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae013-107">GetById</span><span class="sxs-lookup"><span data-stu-id="ae013-107">GetById</span></span>
```
Get-AzureRmPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae013-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ae013-108">DESCRIPTION</span></span>
<span data-ttu-id="ae013-109">Polecenie cmdlet **Get-AzureRmPolicySetDefinition** pobiera wszystkie definicje zestawu zasad lub określoną definicję zestawu zasad określoną za pomocą nazwy lub identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="ae013-109">The **Get-AzureRmPolicySetDefinition** cmdlet gets all the policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="ae013-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ae013-110">EXAMPLES</span></span>

### <span data-ttu-id="ae013-111">Przykład 1: pobieranie wszystkich definicji zestawu zasad</span><span class="sxs-lookup"><span data-stu-id="ae013-111">Example 1: Get all policy set definition</span></span>
```
PS C:\>Get-AzureRmPolicySetDefinition
```

<span data-ttu-id="ae013-112">To polecenie umożliwia pobieranie wszystkich definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="ae013-112">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="ae013-113">Przykład 2: uzyskiwanie definicji zestawu zasad według nazwy</span><span class="sxs-lookup"><span data-stu-id="ae013-113">Example 2: Get policy set definition by name</span></span>
```
PS C:\>Get-AzureRmPolicySetDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="ae013-114">To polecenie pobiera definicję zestawu zasad o nazwie VMPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="ae013-114">This command gets the policy set definition named VMPolicyDefinition.</span></span>

## <span data-ttu-id="ae013-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ae013-115">PARAMETERS</span></span>

### <span data-ttu-id="ae013-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ae013-116">-ApiVersion</span></span>
<span data-ttu-id="ae013-117">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="ae013-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="ae013-118">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="ae013-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="ae013-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae013-119">-DefaultProfile</span></span>
<span data-ttu-id="ae013-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ae013-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae013-121">-ID</span><span class="sxs-lookup"><span data-stu-id="ae013-121">-Id</span></span>
<span data-ttu-id="ae013-122">W pełni kwalifikowany identyfikator definicji zestawu zasad, w tym abonament.</span><span class="sxs-lookup"><span data-stu-id="ae013-122">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="ae013-123">na przykład/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="ae013-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: GetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae013-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ae013-124">-Name</span></span>
<span data-ttu-id="ae013-125">Nazwa definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="ae013-125">The policy set definition name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae013-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="ae013-126">-Pre</span></span>
<span data-ttu-id="ae013-127">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="ae013-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="ae013-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae013-128">CommonParameters</span></span>
<span data-ttu-id="ae013-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae013-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae013-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae013-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae013-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae013-131">INPUTS</span></span>

### <span data-ttu-id="ae013-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ae013-132">System.String</span></span>

## <span data-ttu-id="ae013-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ae013-133">OUTPUTS</span></span>

### <span data-ttu-id="ae013-134">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="ae013-134">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="ae013-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ae013-135">NOTES</span></span>

## <span data-ttu-id="ae013-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae013-136">RELATED LINKS</span></span>
