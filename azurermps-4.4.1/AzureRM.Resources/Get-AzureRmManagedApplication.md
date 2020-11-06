---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplication.md
ms.openlocfilehash: 953a810585550ec8895fc9306f78633beb4846a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527314"
---
# <span data-ttu-id="fc417-101">Get-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="fc417-101">Get-AzureRmManagedApplication</span></span>

## <span data-ttu-id="fc417-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fc417-102">SYNOPSIS</span></span>
<span data-ttu-id="fc417-103">Pobiera zarządzane aplikacje</span><span class="sxs-lookup"><span data-stu-id="fc417-103">Gets managed applications</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc417-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fc417-104">SYNTAX</span></span>

### <span data-ttu-id="fc417-105">Zestaw parametrów lista wszystkich zarządzanych aplikacji.</span><span class="sxs-lookup"><span data-stu-id="fc417-105">The list all managed applications parameter set.</span></span> <span data-ttu-id="fc417-106">Domyślne</span><span class="sxs-lookup"><span data-stu-id="fc417-106">(Default)</span></span>
```
Get-AzureRmManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fc417-107">Zestaw parametrów nazwa aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="fc417-107">The managed application name parameter set.</span></span>
```
Get-AzureRmManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc417-108">Zestaw parametrów zarządzany identyfikator aplikacji.</span><span class="sxs-lookup"><span data-stu-id="fc417-108">The managed application Id parameter set.</span></span>
```
Get-AzureRmManagedApplication -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc417-109">Opis</span><span class="sxs-lookup"><span data-stu-id="fc417-109">DESCRIPTION</span></span>
<span data-ttu-id="fc417-110">Polecenie cmdlet **Get-AzureRmManagedApplication** umożliwia zarządzanie aplikacjami</span><span class="sxs-lookup"><span data-stu-id="fc417-110">The **Get-AzureRmManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="fc417-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fc417-111">EXAMPLES</span></span>

### <span data-ttu-id="fc417-112">Przykład 1: pobieranie wszystkich zarządzanych aplikacji w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="fc417-112">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzureRmManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="fc417-113">To polecenie pobiera zarządzane aplikacje w grupie zasób "MyRG"</span><span class="sxs-lookup"><span data-stu-id="fc417-113">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="fc417-114">Przykład 2: uzyskiwanie wszystkich zarządzanych aplikacji</span><span class="sxs-lookup"><span data-stu-id="fc417-114">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzureRmManagedApplication
```

<span data-ttu-id="fc417-115">To polecenie umożliwia uzyskiwanie wszystkich zarządzanych aplikacji w ramach bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="fc417-115">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="fc417-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fc417-116">PARAMETERS</span></span>

### <span data-ttu-id="fc417-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="fc417-117">-ApiVersion</span></span>
<span data-ttu-id="fc417-118">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="fc417-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="fc417-119">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="fc417-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="fc417-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc417-120">-DefaultProfile</span></span>
<span data-ttu-id="fc417-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fc417-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc417-122">-ID</span><span class="sxs-lookup"><span data-stu-id="fc417-122">-Id</span></span>
<span data-ttu-id="fc417-123">W pełni kwalifikowany identyfikator zarządzanej aplikacji, w tym abonament.</span><span class="sxs-lookup"><span data-stu-id="fc417-123">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="fc417-124">na przykład/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="fc417-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application Id parameter set.
Aliases: ResourceId, ManagedApplicationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc417-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fc417-125">-Name</span></span>
<span data-ttu-id="fc417-126">Nazwa zarządzanej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="fc417-126">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application name parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc417-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="fc417-127">-Pre</span></span>
<span data-ttu-id="fc417-128">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="fc417-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="fc417-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc417-129">-ResourceGroupName</span></span>
<span data-ttu-id="fc417-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fc417-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc417-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc417-131">CommonParameters</span></span>
<span data-ttu-id="fc417-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc417-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc417-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc417-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc417-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fc417-134">INPUTS</span></span>

### <span data-ttu-id="fc417-135">System. String</span><span class="sxs-lookup"><span data-stu-id="fc417-135">System.String</span></span>

## <span data-ttu-id="fc417-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fc417-136">OUTPUTS</span></span>

### <span data-ttu-id="fc417-137">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="fc417-137">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="fc417-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fc417-138">NOTES</span></span>

## <span data-ttu-id="fc417-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fc417-139">RELATED LINKS</span></span>

