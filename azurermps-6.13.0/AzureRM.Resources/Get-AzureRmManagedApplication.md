---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplication.md
ms.openlocfilehash: dd0bb1bb72aa1193cba75c44905be37a70b62d4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541520"
---
# <span data-ttu-id="baa8f-101">Get-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="baa8f-101">Get-AzureRmManagedApplication</span></span>

## <span data-ttu-id="baa8f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="baa8f-102">SYNOPSIS</span></span>
<span data-ttu-id="baa8f-103">Pobiera zarządzane aplikacje</span><span class="sxs-lookup"><span data-stu-id="baa8f-103">Gets managed applications</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="baa8f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="baa8f-104">SYNTAX</span></span>

### <span data-ttu-id="baa8f-105">GetBySubscription (domyślny)</span><span class="sxs-lookup"><span data-stu-id="baa8f-105">GetBySubscription (Default)</span></span>
```
Get-AzureRmManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="baa8f-106">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="baa8f-106">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="baa8f-107">GetById</span><span class="sxs-lookup"><span data-stu-id="baa8f-107">GetById</span></span>
```
Get-AzureRmManagedApplication -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="baa8f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="baa8f-108">DESCRIPTION</span></span>
<span data-ttu-id="baa8f-109">Polecenie cmdlet **Get-AzureRmManagedApplication** umożliwia zarządzanie aplikacjami</span><span class="sxs-lookup"><span data-stu-id="baa8f-109">The **Get-AzureRmManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="baa8f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="baa8f-110">EXAMPLES</span></span>

### <span data-ttu-id="baa8f-111">Przykład 1: pobieranie wszystkich zarządzanych aplikacji w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="baa8f-111">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzureRmManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="baa8f-112">To polecenie pobiera zarządzane aplikacje w grupie zasób "MyRG"</span><span class="sxs-lookup"><span data-stu-id="baa8f-112">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="baa8f-113">Przykład 2: uzyskiwanie wszystkich zarządzanych aplikacji</span><span class="sxs-lookup"><span data-stu-id="baa8f-113">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzureRmManagedApplication
```

<span data-ttu-id="baa8f-114">To polecenie umożliwia uzyskiwanie wszystkich zarządzanych aplikacji w ramach bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="baa8f-114">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="baa8f-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="baa8f-115">PARAMETERS</span></span>

### <span data-ttu-id="baa8f-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="baa8f-116">-ApiVersion</span></span>
<span data-ttu-id="baa8f-117">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="baa8f-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="baa8f-118">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="baa8f-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="baa8f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baa8f-119">-DefaultProfile</span></span>
<span data-ttu-id="baa8f-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="baa8f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="baa8f-121">-ID</span><span class="sxs-lookup"><span data-stu-id="baa8f-121">-Id</span></span>
<span data-ttu-id="baa8f-122">W pełni kwalifikowany identyfikator zarządzanej aplikacji, w tym abonament.</span><span class="sxs-lookup"><span data-stu-id="baa8f-122">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="baa8f-123">na przykład/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="baa8f-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="baa8f-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="baa8f-124">-Name</span></span>
<span data-ttu-id="baa8f-125">Nazwa zarządzanej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="baa8f-125">The managed application name.</span></span>

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

### <span data-ttu-id="baa8f-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="baa8f-126">-Pre</span></span>
<span data-ttu-id="baa8f-127">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="baa8f-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="baa8f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="baa8f-128">-ResourceGroupName</span></span>
<span data-ttu-id="baa8f-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="baa8f-129">The resource group name.</span></span>

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

### <span data-ttu-id="baa8f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baa8f-130">CommonParameters</span></span>
<span data-ttu-id="baa8f-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="baa8f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baa8f-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="baa8f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baa8f-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="baa8f-133">INPUTS</span></span>

### <span data-ttu-id="baa8f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="baa8f-134">System.String</span></span>

## <span data-ttu-id="baa8f-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="baa8f-135">OUTPUTS</span></span>

### <span data-ttu-id="baa8f-136">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="baa8f-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="baa8f-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="baa8f-137">NOTES</span></span>

## <span data-ttu-id="baa8f-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="baa8f-138">RELATED LINKS</span></span>
