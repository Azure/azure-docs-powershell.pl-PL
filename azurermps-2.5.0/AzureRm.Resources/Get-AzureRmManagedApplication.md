---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermmanagedapplication
schema: 2.0.0
ms.openlocfilehash: 482bf9a2158fc299d78c993255e390dc480245a3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898682"
---
# <span data-ttu-id="bf70b-101">Get-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="bf70b-101">Get-AzureRmManagedApplication</span></span>

## <span data-ttu-id="bf70b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bf70b-102">SYNOPSIS</span></span>
<span data-ttu-id="bf70b-103">Pobiera zarządzane aplikacje</span><span class="sxs-lookup"><span data-stu-id="bf70b-103">Gets managed applications</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf70b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bf70b-104">SYNTAX</span></span>

### <span data-ttu-id="bf70b-105">GetBySubscription (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bf70b-105">GetBySubscription (Default)</span></span>
```
Get-AzureRmManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bf70b-106">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bf70b-106">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf70b-107">GetById</span><span class="sxs-lookup"><span data-stu-id="bf70b-107">GetById</span></span>
```
Get-AzureRmManagedApplication -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf70b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="bf70b-108">DESCRIPTION</span></span>
<span data-ttu-id="bf70b-109">Polecenie cmdlet **Get-AzureRmManagedApplication** umożliwia zarządzanie aplikacjami</span><span class="sxs-lookup"><span data-stu-id="bf70b-109">The **Get-AzureRmManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="bf70b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bf70b-110">EXAMPLES</span></span>

### <span data-ttu-id="bf70b-111">Przykład 1: pobieranie wszystkich zarządzanych aplikacji w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="bf70b-111">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzureRmManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="bf70b-112">To polecenie pobiera zarządzane aplikacje w grupie zasób "MyRG"</span><span class="sxs-lookup"><span data-stu-id="bf70b-112">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="bf70b-113">Przykład 2: uzyskiwanie wszystkich zarządzanych aplikacji</span><span class="sxs-lookup"><span data-stu-id="bf70b-113">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzureRmManagedApplication
```

<span data-ttu-id="bf70b-114">To polecenie umożliwia uzyskiwanie wszystkich zarządzanych aplikacji w ramach bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="bf70b-114">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="bf70b-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bf70b-115">PARAMETERS</span></span>

### <span data-ttu-id="bf70b-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="bf70b-116">-ApiVersion</span></span>
<span data-ttu-id="bf70b-117">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="bf70b-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="bf70b-118">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="bf70b-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="bf70b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf70b-119">-DefaultProfile</span></span>
<span data-ttu-id="bf70b-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bf70b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf70b-121">-ID</span><span class="sxs-lookup"><span data-stu-id="bf70b-121">-Id</span></span>
<span data-ttu-id="bf70b-122">W pełni kwalifikowany identyfikator zarządzanej aplikacji, w tym abonament.</span><span class="sxs-lookup"><span data-stu-id="bf70b-122">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="bf70b-123">na przykład/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="bf70b-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf70b-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bf70b-124">-Name</span></span>
<span data-ttu-id="bf70b-125">Nazwa zarządzanej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="bf70b-125">The managed application name.</span></span>

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

### <span data-ttu-id="bf70b-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="bf70b-126">-Pre</span></span>
<span data-ttu-id="bf70b-127">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="bf70b-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="bf70b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf70b-128">-ResourceGroupName</span></span>
<span data-ttu-id="bf70b-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bf70b-129">The resource group name.</span></span>

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

### <span data-ttu-id="bf70b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf70b-130">CommonParameters</span></span>
<span data-ttu-id="bf70b-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf70b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf70b-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf70b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf70b-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bf70b-133">INPUTS</span></span>

### <span data-ttu-id="bf70b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="bf70b-134">System.String</span></span>

## <span data-ttu-id="bf70b-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bf70b-135">OUTPUTS</span></span>

### <span data-ttu-id="bf70b-136">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="bf70b-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="bf70b-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bf70b-137">NOTES</span></span>

## <span data-ttu-id="bf70b-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bf70b-138">RELATED LINKS</span></span>
