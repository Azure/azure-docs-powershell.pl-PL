---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplicationDefinition.md
ms.openlocfilehash: 42acc50c5e370f20e168e6c7cd757f57b1dacc4d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708314"
---
# <span data-ttu-id="2f708-101">Remove-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="2f708-101">Remove-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="2f708-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2f708-102">SYNOPSIS</span></span>
<span data-ttu-id="2f708-103">Usuwa definicję aplikacji zarządzanej</span><span class="sxs-lookup"><span data-stu-id="2f708-103">Removes a managed application definition</span></span>

## <span data-ttu-id="2f708-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2f708-104">SYNTAX</span></span>

### <span data-ttu-id="2f708-105">RemoveByNameAndResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2f708-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2f708-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="2f708-106">RemoveById</span></span>
```
Remove-AzManagedApplicationDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f708-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2f708-107">DESCRIPTION</span></span>
<span data-ttu-id="2f708-108">Polecenie cmdlet **Remove-AzManagedApplicationDefinition** usuwa definicję aplikacji zarządzanej</span><span class="sxs-lookup"><span data-stu-id="2f708-108">The **Remove-AzManagedApplicationDefinition** cmdlet removes a managed application definition</span></span>

## <span data-ttu-id="2f708-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2f708-109">EXAMPLES</span></span>

### <span data-ttu-id="2f708-110">Przykład 1: usuwanie definicji aplikacji zarządzanej według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="2f708-110">Example 1: Remove managed application definition by resource ID</span></span>
```
PS C:\>$ApplicationDefinition = Get-AzManagedApplicationDefinition -Name "myAppDef" -ResourceGroupName "myRG"
PS C:\>Remove-AzManagedApplicationDefinition -Id $ApplicationDefinition.ResourceId -Force
```

<span data-ttu-id="2f708-111">Pierwsze polecenie pobiera definicję aplikacji zarządzanej o nazwie myAppDef przy użyciu polecenia cmdlet Get-AzManagedApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="2f708-111">The first command gets a managed application definition named myAppDef by using the Get-AzManagedApplicationDefinition cmdlet.</span></span>
<span data-ttu-id="2f708-112">Polecenie zapisuje je w zmiennej $ApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="2f708-112">The command stores it in the $ApplicationDefinition variable.</span></span>
<span data-ttu-id="2f708-113">Drugie polecenie usuwa definicję aplikacji zarządzanej zidentyfikowaną przez właściwość **ResourceId** $ApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="2f708-113">The second command removes the managed application definition identified by the **ResourceId** property of $ApplicationDefinition.</span></span>

## <span data-ttu-id="2f708-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2f708-114">PARAMETERS</span></span>

### <span data-ttu-id="2f708-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2f708-115">-ApiVersion</span></span>
<span data-ttu-id="2f708-116">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="2f708-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="2f708-117">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="2f708-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="2f708-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f708-118">-DefaultProfile</span></span>
<span data-ttu-id="2f708-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2f708-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f708-120">-Force</span><span class="sxs-lookup"><span data-stu-id="2f708-120">-Force</span></span>
<span data-ttu-id="2f708-121">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2f708-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2f708-122">-ID</span><span class="sxs-lookup"><span data-stu-id="2f708-122">-Id</span></span>
<span data-ttu-id="2f708-123">W pełni kwalifikowana nazwa definicji aplikacji zarządzanej, w tym abonament.</span><span class="sxs-lookup"><span data-stu-id="2f708-123">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="2f708-124">na przykład/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="2f708-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f708-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2f708-125">-Name</span></span>
<span data-ttu-id="2f708-126">Nazwa definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="2f708-126">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f708-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="2f708-127">-Pre</span></span>
<span data-ttu-id="2f708-128">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="2f708-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="2f708-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f708-129">-ResourceGroupName</span></span>
<span data-ttu-id="2f708-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2f708-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f708-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2f708-131">-Confirm</span></span>
<span data-ttu-id="2f708-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f708-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f708-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f708-133">-WhatIf</span></span>
<span data-ttu-id="2f708-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f708-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f708-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2f708-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f708-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f708-136">CommonParameters</span></span>
<span data-ttu-id="2f708-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f708-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f708-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f708-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f708-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2f708-139">INPUTS</span></span>

### <span data-ttu-id="2f708-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2f708-140">System.String</span></span>

## <span data-ttu-id="2f708-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2f708-141">OUTPUTS</span></span>

### <span data-ttu-id="2f708-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2f708-142">System.Boolean</span></span>

## <span data-ttu-id="2f708-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2f708-143">NOTES</span></span>

## <span data-ttu-id="2f708-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2f708-144">RELATED LINKS</span></span>
