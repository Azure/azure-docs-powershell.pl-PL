---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
ms.openlocfilehash: 5fba45e50076952a0a2e11e2e5541ab9546d3bc6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549927"
---
# <span data-ttu-id="ec5da-101">Get-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="ec5da-101">Get-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="ec5da-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ec5da-102">SYNOPSIS</span></span>
<span data-ttu-id="ec5da-103">Pobiera definicje zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="ec5da-103">Gets policy set definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec5da-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ec5da-104">SYNTAX</span></span>

### <span data-ttu-id="ec5da-105">Zestaw parametrów lista wszystkich definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="ec5da-105">The list all policy set definitions parameter set.</span></span> <span data-ttu-id="ec5da-106">Domyślne</span><span class="sxs-lookup"><span data-stu-id="ec5da-106">(Default)</span></span>
```
Get-AzureRmPolicySetDefinition [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ec5da-107">Zestaw parametrów Nazwa definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="ec5da-107">The policy set definition name parameter set.</span></span>
```
Get-AzureRmPolicySetDefinition -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec5da-108">Zestaw parametrów identyfikatora definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="ec5da-108">The policy set definition Id parameter set.</span></span>
```
Get-AzureRmPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec5da-109">Opis</span><span class="sxs-lookup"><span data-stu-id="ec5da-109">DESCRIPTION</span></span>
<span data-ttu-id="ec5da-110">Polecenie cmdlet **Get-AzureRmPolicySetDefinition** pobiera wszystkie definicje zestawu zasad lub określoną definicję zestawu zasad określoną za pomocą nazwy lub identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="ec5da-110">The **Get-AzureRmPolicySetDefinition** cmdlet gets all the policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="ec5da-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ec5da-111">EXAMPLES</span></span>

### <span data-ttu-id="ec5da-112">Przykład 1: pobieranie wszystkich definicji zestawu zasad</span><span class="sxs-lookup"><span data-stu-id="ec5da-112">Example 1: Get all policy set definition</span></span>
```
PS C:\>Get-AzureRmPolicySetDefinition
```

<span data-ttu-id="ec5da-113">To polecenie umożliwia pobieranie wszystkich definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="ec5da-113">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="ec5da-114">Przykład 2: uzyskiwanie definicji zestawu zasad według nazwy</span><span class="sxs-lookup"><span data-stu-id="ec5da-114">Example 2: Get policy set definition by name</span></span>
```
PS C:\>Get-AzureRmPolicySetDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="ec5da-115">To polecenie pobiera definicję zestawu zasad o nazwie VMPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="ec5da-115">This command gets the policy set definition named VMPolicyDefinition.</span></span>

## <span data-ttu-id="ec5da-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ec5da-116">PARAMETERS</span></span>

### <span data-ttu-id="ec5da-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ec5da-117">-ApiVersion</span></span>
<span data-ttu-id="ec5da-118">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="ec5da-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="ec5da-119">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="ec5da-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="ec5da-120">-ID</span><span class="sxs-lookup"><span data-stu-id="ec5da-120">-Id</span></span>
<span data-ttu-id="ec5da-121">W pełni kwalifikowany identyfikator definicji zestawu zasad, w tym abonament.</span><span class="sxs-lookup"><span data-stu-id="ec5da-121">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="ec5da-122">na przykład/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="ec5da-122">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The policy set definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec5da-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ec5da-123">-Name</span></span>
<span data-ttu-id="ec5da-124">Nazwa definicji zestawu zasad.</span><span class="sxs-lookup"><span data-stu-id="ec5da-124">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy set definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec5da-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="ec5da-125">-Pre</span></span>
<span data-ttu-id="ec5da-126">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="ec5da-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="ec5da-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec5da-127">-DefaultProfile</span></span>
<span data-ttu-id="ec5da-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ec5da-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec5da-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec5da-129">CommonParameters</span></span>
<span data-ttu-id="ec5da-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec5da-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec5da-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec5da-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec5da-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ec5da-132">INPUTS</span></span>

### <span data-ttu-id="ec5da-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ec5da-133">System.String</span></span>

## <span data-ttu-id="ec5da-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ec5da-134">OUTPUTS</span></span>

### <span data-ttu-id="ec5da-135">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="ec5da-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="ec5da-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ec5da-136">NOTES</span></span>

## <span data-ttu-id="ec5da-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ec5da-137">RELATED LINKS</span></span>

