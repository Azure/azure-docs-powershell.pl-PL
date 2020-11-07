---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzManagedApplicationDefinition.md
ms.openlocfilehash: 4623634d72e78ab62deca43da698d218ddb9276e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892597"
---
# <span data-ttu-id="10d6a-101">Get-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="10d6a-101">Get-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="10d6a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="10d6a-102">SYNOPSIS</span></span>
<span data-ttu-id="10d6a-103">Pobiera definicje aplikacji zarządzanych</span><span class="sxs-lookup"><span data-stu-id="10d6a-103">Gets managed application definitions</span></span>

## <span data-ttu-id="10d6a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="10d6a-104">SYNTAX</span></span>

### <span data-ttu-id="10d6a-105">GetByNameAndResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="10d6a-105">GetByNameAndResourceGroup (Default)</span></span>
```
Get-AzManagedApplicationDefinition [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10d6a-106">GetById</span><span class="sxs-lookup"><span data-stu-id="10d6a-106">GetById</span></span>
```
Get-AzManagedApplicationDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10d6a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="10d6a-107">DESCRIPTION</span></span>
<span data-ttu-id="10d6a-108">Polecenie cmdlet **Get-AzManagedApplicationDefinition** umożliwia stosowanie definicji aplikacji zarządzanych</span><span class="sxs-lookup"><span data-stu-id="10d6a-108">The **Get-AzManagedApplicationDefinition** cmdlet gets managed application definitions</span></span>

## <span data-ttu-id="10d6a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="10d6a-109">EXAMPLES</span></span>

### <span data-ttu-id="10d6a-110">Przykład 1: pobieranie wszystkich definicji aplikacji zarządzanych w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="10d6a-110">Example 1: Get all managed application definitions under a resource group</span></span>
```
PS C:\>Get-AzManagedApplicationDefinition -ResourceGroupName "MyRG"
```

<span data-ttu-id="10d6a-111">To polecenie pobiera definicje aplikacji zarządzanych w obszarze Grupa zasobów "MyRG"</span><span class="sxs-lookup"><span data-stu-id="10d6a-111">This command gets the managed application definitions under resource group "MyRG"</span></span>

### <span data-ttu-id="10d6a-112">Przykład 2: uzyskiwanie definicji aplikacji zarządzanej</span><span class="sxs-lookup"><span data-stu-id="10d6a-112">Example 2: Get a managed application definition</span></span>
```
PS C:\>Get-AzManagedApplicationDefinition -ResourceGroupName "MyRG" -Name "myManagedAppDef"
```

<span data-ttu-id="10d6a-113">To polecenie pobiera definicję aplikacji zarządzanej "myManagedAppDef" w grupie zasób "MyRG".</span><span class="sxs-lookup"><span data-stu-id="10d6a-113">This command gets the managed application definition "myManagedAppDef" under resource group "MyRG"</span></span>

## <span data-ttu-id="10d6a-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="10d6a-114">PARAMETERS</span></span>

### <span data-ttu-id="10d6a-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="10d6a-115">-ApiVersion</span></span>
<span data-ttu-id="10d6a-116">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="10d6a-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="10d6a-117">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="10d6a-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="10d6a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10d6a-118">-DefaultProfile</span></span>
<span data-ttu-id="10d6a-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="10d6a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10d6a-120">-ID</span><span class="sxs-lookup"><span data-stu-id="10d6a-120">-Id</span></span>
<span data-ttu-id="10d6a-121">W pełni kwalifikowana nazwa definicji aplikacji zarządzanej, w tym abonament.</span><span class="sxs-lookup"><span data-stu-id="10d6a-121">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="10d6a-122">na przykład/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="10d6a-122">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="10d6a-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="10d6a-123">-Name</span></span>
<span data-ttu-id="10d6a-124">Nazwa definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="10d6a-124">The managed application definition name.</span></span>

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

### <span data-ttu-id="10d6a-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="10d6a-125">-Pre</span></span>
<span data-ttu-id="10d6a-126">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="10d6a-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="10d6a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10d6a-127">-ResourceGroupName</span></span>
<span data-ttu-id="10d6a-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="10d6a-128">The resource group name.</span></span>

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

### <span data-ttu-id="10d6a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10d6a-129">CommonParameters</span></span>
<span data-ttu-id="10d6a-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10d6a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10d6a-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10d6a-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10d6a-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10d6a-132">INPUTS</span></span>

### <span data-ttu-id="10d6a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="10d6a-133">System.String</span></span>

## <span data-ttu-id="10d6a-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="10d6a-134">OUTPUTS</span></span>

### <span data-ttu-id="10d6a-135">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="10d6a-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="10d6a-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="10d6a-136">NOTES</span></span>

## <span data-ttu-id="10d6a-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="10d6a-137">RELATED LINKS</span></span>
