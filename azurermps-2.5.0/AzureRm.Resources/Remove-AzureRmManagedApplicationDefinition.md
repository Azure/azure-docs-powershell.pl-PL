---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermmanagedapplicationdefinition
schema: 2.0.0
ms.openlocfilehash: 41cf22aab3cc79499d5a2c8918197c1cd6d092e6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899200"
---
# <span data-ttu-id="c416a-101">Remove-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="c416a-101">Remove-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="c416a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c416a-102">SYNOPSIS</span></span>
<span data-ttu-id="c416a-103">Usuwa definicję aplikacji zarządzanej</span><span class="sxs-lookup"><span data-stu-id="c416a-103">Removes a managed application definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c416a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c416a-104">SYNTAX</span></span>

### <span data-ttu-id="c416a-105">RemoveByNameAndResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c416a-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c416a-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="c416a-106">RemoveById</span></span>
```
Remove-AzureRmManagedApplicationDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c416a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c416a-107">DESCRIPTION</span></span>
<span data-ttu-id="c416a-108">Polecenie cmdlet **Remove-AzureRmManagedApplicationDefinition** usuwa definicję aplikacji zarządzanej</span><span class="sxs-lookup"><span data-stu-id="c416a-108">The **Remove-AzureRmManagedApplicationDefinition** cmdlet removes a managed application definition</span></span>

## <span data-ttu-id="c416a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c416a-109">EXAMPLES</span></span>

### <span data-ttu-id="c416a-110">Przykład 1: usuwanie definicji aplikacji zarządzanej według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="c416a-110">Example 1: Remove managed application definition by resource ID</span></span>
```
PS C:\>$ApplicationDefinition = Get-AzureRmManagedApplicationDefinition -Name "myAppDef" -ResourceGroupName "myRG"
PS C:\>Remove-AzureRmManagedApplicationDefinition -Id $ApplicationDefinition.ResourceId -Force
```

<span data-ttu-id="c416a-111">Pierwsze polecenie pobiera definicję aplikacji zarządzanej o nazwie myAppDef przy użyciu polecenia cmdlet Get-AzureRmManagedApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="c416a-111">The first command gets a managed application definition named myAppDef by using the Get-AzureRmManagedApplicationDefinition cmdlet.</span></span>
<span data-ttu-id="c416a-112">Polecenie zapisuje je w zmiennej $ApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="c416a-112">The command stores it in the $ApplicationDefinition variable.</span></span>

<span data-ttu-id="c416a-113">Drugie polecenie usuwa definicję aplikacji zarządzanej zidentyfikowaną przez właściwość **ResourceId** $ApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="c416a-113">The second command removes the managed application definition identified by the **ResourceId** property of $ApplicationDefinition.</span></span>

## <span data-ttu-id="c416a-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c416a-114">PARAMETERS</span></span>

### <span data-ttu-id="c416a-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c416a-115">-ApiVersion</span></span>
<span data-ttu-id="c416a-116">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="c416a-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="c416a-117">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="c416a-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="c416a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c416a-118">-DefaultProfile</span></span>
<span data-ttu-id="c416a-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c416a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c416a-120">-Force</span><span class="sxs-lookup"><span data-stu-id="c416a-120">-Force</span></span>
<span data-ttu-id="c416a-121">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c416a-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c416a-122">-ID</span><span class="sxs-lookup"><span data-stu-id="c416a-122">-Id</span></span>
<span data-ttu-id="c416a-123">W pełni kwalifikowana nazwa definicji aplikacji zarządzanej, w tym abonament.</span><span class="sxs-lookup"><span data-stu-id="c416a-123">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="c416a-124">na przykład/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="c416a-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c416a-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c416a-125">-Name</span></span>
<span data-ttu-id="c416a-126">Nazwa definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="c416a-126">The managed application definition name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c416a-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="c416a-127">-Pre</span></span>
<span data-ttu-id="c416a-128">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="c416a-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c416a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c416a-129">-ResourceGroupName</span></span>
<span data-ttu-id="c416a-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c416a-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c416a-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c416a-131">-Confirm</span></span>
<span data-ttu-id="c416a-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c416a-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c416a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c416a-133">-WhatIf</span></span>
<span data-ttu-id="c416a-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c416a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c416a-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c416a-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c416a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c416a-136">CommonParameters</span></span>
<span data-ttu-id="c416a-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c416a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c416a-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c416a-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c416a-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c416a-139">INPUTS</span></span>

### <span data-ttu-id="c416a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="c416a-140">System.String</span></span>

## <span data-ttu-id="c416a-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c416a-141">OUTPUTS</span></span>

### <span data-ttu-id="c416a-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c416a-142">System.Boolean</span></span>

## <span data-ttu-id="c416a-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c416a-143">NOTES</span></span>

## <span data-ttu-id="c416a-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c416a-144">RELATED LINKS</span></span>
