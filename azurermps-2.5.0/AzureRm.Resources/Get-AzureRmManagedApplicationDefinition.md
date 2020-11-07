---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermmanagedapplicationdefinition
schema: 2.0.0
ms.openlocfilehash: e6df93dee8599c6bae42cc9428b2a7691abf4740
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898680"
---
# <span data-ttu-id="ed327-101">Get-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="ed327-101">Get-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="ed327-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ed327-102">SYNOPSIS</span></span>
<span data-ttu-id="ed327-103">Pobiera definicje aplikacji zarządzanych</span><span class="sxs-lookup"><span data-stu-id="ed327-103">Gets managed application definitions</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed327-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ed327-104">SYNTAX</span></span>

### <span data-ttu-id="ed327-105">GetByNameAndResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ed327-105">GetByNameAndResourceGroup (Default)</span></span>
```
Get-AzureRmManagedApplicationDefinition [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed327-106">GetById</span><span class="sxs-lookup"><span data-stu-id="ed327-106">GetById</span></span>
```
Get-AzureRmManagedApplicationDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed327-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ed327-107">DESCRIPTION</span></span>
<span data-ttu-id="ed327-108">Polecenie cmdlet **Get-AzureRmManagedApplicationDefinition** umożliwia stosowanie definicji aplikacji zarządzanych</span><span class="sxs-lookup"><span data-stu-id="ed327-108">The **Get-AzureRmManagedApplicationDefinition** cmdlet gets managed application definitions</span></span>

## <span data-ttu-id="ed327-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ed327-109">EXAMPLES</span></span>

### <span data-ttu-id="ed327-110">Przykład 1: pobieranie wszystkich definicji aplikacji zarządzanych w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="ed327-110">Example 1: Get all managed application definitions under a resource group</span></span>
```
PS C:\>Get-AzureRmManagedApplicationDefinition -ResourceGroupName "MyRG"
```

<span data-ttu-id="ed327-111">To polecenie pobiera definicje aplikacji zarządzanych w obszarze Grupa zasobów "MyRG"</span><span class="sxs-lookup"><span data-stu-id="ed327-111">This command gets the managed application definitions under resource group "MyRG"</span></span>

### <span data-ttu-id="ed327-112">Przykład 2: uzyskiwanie definicji aplikacji zarządzanej</span><span class="sxs-lookup"><span data-stu-id="ed327-112">Example 2: Get a managed application definition</span></span>
```
PS C:\>Get-AzureRmManagedApplicationDefinition -ResourceGroupName "MyRG" -Name "myManagedAppDef"
```

<span data-ttu-id="ed327-113">To polecenie pobiera definicję aplikacji zarządzanej "myManagedAppDef" w grupie zasób "MyRG".</span><span class="sxs-lookup"><span data-stu-id="ed327-113">This command gets the managed application definition "myManagedAppDef" under resource group "MyRG"</span></span>

## <span data-ttu-id="ed327-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ed327-114">PARAMETERS</span></span>

### <span data-ttu-id="ed327-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ed327-115">-ApiVersion</span></span>
<span data-ttu-id="ed327-116">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="ed327-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="ed327-117">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="ed327-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="ed327-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed327-118">-DefaultProfile</span></span>
<span data-ttu-id="ed327-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ed327-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed327-120">-ID</span><span class="sxs-lookup"><span data-stu-id="ed327-120">-Id</span></span>
<span data-ttu-id="ed327-121">W pełni kwalifikowana nazwa definicji aplikacji zarządzanej, w tym abonament.</span><span class="sxs-lookup"><span data-stu-id="ed327-121">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="ed327-122">na przykład/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="ed327-122">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationDefinitionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed327-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ed327-123">-Name</span></span>
<span data-ttu-id="ed327-124">Nazwa definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="ed327-124">The managed application definition name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed327-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="ed327-125">-Pre</span></span>
<span data-ttu-id="ed327-126">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="ed327-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="ed327-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed327-127">-ResourceGroupName</span></span>
<span data-ttu-id="ed327-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ed327-128">The resource group name.</span></span>

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

### <span data-ttu-id="ed327-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed327-129">CommonParameters</span></span>
<span data-ttu-id="ed327-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed327-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed327-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed327-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed327-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed327-132">INPUTS</span></span>

### <span data-ttu-id="ed327-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ed327-133">System.String</span></span>

## <span data-ttu-id="ed327-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ed327-134">OUTPUTS</span></span>

### <span data-ttu-id="ed327-135">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="ed327-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="ed327-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ed327-136">NOTES</span></span>

## <span data-ttu-id="ed327-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ed327-137">RELATED LINKS</span></span>
