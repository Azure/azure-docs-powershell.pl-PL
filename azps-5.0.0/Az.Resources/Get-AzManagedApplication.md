---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagedApplication.md
ms.openlocfilehash: e0577342a839424d9a45a91b6c9289a72fe9df12
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224864"
---
# <span data-ttu-id="e0dba-101">Get-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="e0dba-101">Get-AzManagedApplication</span></span>

## <span data-ttu-id="e0dba-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e0dba-102">SYNOPSIS</span></span>
<span data-ttu-id="e0dba-103">Pobiera zarządzane aplikacje</span><span class="sxs-lookup"><span data-stu-id="e0dba-103">Gets managed applications</span></span>

## <span data-ttu-id="e0dba-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e0dba-104">SYNTAX</span></span>

### <span data-ttu-id="e0dba-105">GetBySubscription (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e0dba-105">GetBySubscription (Default)</span></span>
```
Get-AzManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e0dba-106">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e0dba-106">GetByNameAndResourceGroup</span></span>
```
Get-AzManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0dba-107">GetById</span><span class="sxs-lookup"><span data-stu-id="e0dba-107">GetById</span></span>
```
Get-AzManagedApplication -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e0dba-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e0dba-108">DESCRIPTION</span></span>
<span data-ttu-id="e0dba-109">Polecenie cmdlet **Get-AzManagedApplication** umożliwia zarządzanie aplikacjami</span><span class="sxs-lookup"><span data-stu-id="e0dba-109">The **Get-AzManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="e0dba-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e0dba-110">EXAMPLES</span></span>

### <span data-ttu-id="e0dba-111">Przykład 1: pobieranie wszystkich zarządzanych aplikacji w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="e0dba-111">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="e0dba-112">To polecenie pobiera zarządzane aplikacje w grupie zasób "MyRG"</span><span class="sxs-lookup"><span data-stu-id="e0dba-112">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="e0dba-113">Przykład 2: uzyskiwanie wszystkich zarządzanych aplikacji</span><span class="sxs-lookup"><span data-stu-id="e0dba-113">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzManagedApplication
```

<span data-ttu-id="e0dba-114">To polecenie umożliwia uzyskiwanie wszystkich zarządzanych aplikacji w ramach bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e0dba-114">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="e0dba-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e0dba-115">PARAMETERS</span></span>

### <span data-ttu-id="e0dba-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e0dba-116">-ApiVersion</span></span>
<span data-ttu-id="e0dba-117">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="e0dba-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="e0dba-118">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="e0dba-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="e0dba-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0dba-119">-DefaultProfile</span></span>
<span data-ttu-id="e0dba-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e0dba-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0dba-121">-ID</span><span class="sxs-lookup"><span data-stu-id="e0dba-121">-Id</span></span>
<span data-ttu-id="e0dba-122">W pełni kwalifikowany identyfikator zarządzanej aplikacji, w tym abonament.</span><span class="sxs-lookup"><span data-stu-id="e0dba-122">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="e0dba-123">na przykład/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="e0dba-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="e0dba-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e0dba-124">-Name</span></span>
<span data-ttu-id="e0dba-125">Nazwa zarządzanej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e0dba-125">The managed application name.</span></span>

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

### <span data-ttu-id="e0dba-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="e0dba-126">-Pre</span></span>
<span data-ttu-id="e0dba-127">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="e0dba-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="e0dba-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0dba-128">-ResourceGroupName</span></span>
<span data-ttu-id="e0dba-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e0dba-129">The resource group name.</span></span>

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

### <span data-ttu-id="e0dba-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0dba-130">CommonParameters</span></span>
<span data-ttu-id="e0dba-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0dba-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0dba-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0dba-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0dba-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0dba-133">INPUTS</span></span>

### <span data-ttu-id="e0dba-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e0dba-134">System.String</span></span>

## <span data-ttu-id="e0dba-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e0dba-135">OUTPUTS</span></span>

### <span data-ttu-id="e0dba-136">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="e0dba-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="e0dba-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e0dba-137">NOTES</span></span>

## <span data-ttu-id="e0dba-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e0dba-138">RELATED LINKS</span></span>
