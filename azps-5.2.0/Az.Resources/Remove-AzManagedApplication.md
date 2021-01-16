---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplication.md
ms.openlocfilehash: 17a28da26aa26860b7fd4a28ec922932bb089da3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355561"
---
# <span data-ttu-id="034f0-101">Remove-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="034f0-101">Remove-AzManagedApplication</span></span>

## <span data-ttu-id="034f0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="034f0-102">SYNOPSIS</span></span>
<span data-ttu-id="034f0-103">Usuwa zarządzaną aplikację</span><span class="sxs-lookup"><span data-stu-id="034f0-103">Removes a managed application</span></span>

## <span data-ttu-id="034f0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="034f0-104">SYNTAX</span></span>

### <span data-ttu-id="034f0-105">RemoveByNameAndResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="034f0-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzManagedApplication -Name <String> -ResourceGroupName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="034f0-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="034f0-106">RemoveById</span></span>
```
Remove-AzManagedApplication -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="034f0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="034f0-107">DESCRIPTION</span></span>
<span data-ttu-id="034f0-108">Polecenie cmdlet **Remove-AzManagedApplication** usuwa zarządzaną aplikację</span><span class="sxs-lookup"><span data-stu-id="034f0-108">The **Remove-AzManagedApplication** cmdlet removes a managed application</span></span>

## <span data-ttu-id="034f0-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="034f0-109">EXAMPLES</span></span>

### <span data-ttu-id="034f0-110">Przykład 1: Usuwanie zarządzanej aplikacji według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="034f0-110">Example 1: Remove managed application by resource ID</span></span>
```
PS C:\>$Application = Get-AzManagedApplication -Name "myApp" -ResourceGroupName "myRG"
PS C:\>Remove-AzManagedApplication -Id $Application.ResourceId -Force
```

<span data-ttu-id="034f0-111">Pierwsze polecenie uzyskuje zarządzaną aplikację o nazwie MojaApl przy użyciu polecenia cmdlet Get-AzManagedApplication.</span><span class="sxs-lookup"><span data-stu-id="034f0-111">The first command gets a managed application named myApp by using the Get-AzManagedApplication cmdlet.</span></span>
<span data-ttu-id="034f0-112">Polecenie zapisuje je w zmiennej $Application.</span><span class="sxs-lookup"><span data-stu-id="034f0-112">The command stores it in the $Application variable.</span></span>
<span data-ttu-id="034f0-113">Drugie polecenie usuwa zarządzaną aplikację zidentyfikowaną przez właściwość **ResourceId** $Application.</span><span class="sxs-lookup"><span data-stu-id="034f0-113">The second command removes the managed application identified by the **ResourceId** property of $Application.</span></span>

## <span data-ttu-id="034f0-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="034f0-114">PARAMETERS</span></span>

### <span data-ttu-id="034f0-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="034f0-115">-ApiVersion</span></span>
<span data-ttu-id="034f0-116">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="034f0-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="034f0-117">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="034f0-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="034f0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="034f0-118">-DefaultProfile</span></span>
<span data-ttu-id="034f0-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="034f0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="034f0-120">-Force</span><span class="sxs-lookup"><span data-stu-id="034f0-120">-Force</span></span>
<span data-ttu-id="034f0-121">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="034f0-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="034f0-122">-ID</span><span class="sxs-lookup"><span data-stu-id="034f0-122">-Id</span></span>
<span data-ttu-id="034f0-123">W pełni kwalifikowany identyfikator zarządzanej aplikacji, w tym abonament.</span><span class="sxs-lookup"><span data-stu-id="034f0-123">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="034f0-124">na przykład/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="034f0-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="034f0-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="034f0-125">-Name</span></span>
<span data-ttu-id="034f0-126">Nazwa zarządzanej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="034f0-126">The managed application name.</span></span>

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

### <span data-ttu-id="034f0-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="034f0-127">-Pre</span></span>
<span data-ttu-id="034f0-128">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="034f0-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="034f0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="034f0-129">-ResourceGroupName</span></span>
<span data-ttu-id="034f0-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="034f0-130">The resource group name.</span></span>

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

### <span data-ttu-id="034f0-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="034f0-131">-Confirm</span></span>
<span data-ttu-id="034f0-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="034f0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="034f0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="034f0-133">-WhatIf</span></span>
<span data-ttu-id="034f0-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="034f0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="034f0-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="034f0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="034f0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="034f0-136">CommonParameters</span></span>
<span data-ttu-id="034f0-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="034f0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="034f0-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="034f0-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="034f0-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="034f0-139">INPUTS</span></span>

### <span data-ttu-id="034f0-140">System. String</span><span class="sxs-lookup"><span data-stu-id="034f0-140">System.String</span></span>

## <span data-ttu-id="034f0-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="034f0-141">OUTPUTS</span></span>

### <span data-ttu-id="034f0-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="034f0-142">System.Boolean</span></span>

## <span data-ttu-id="034f0-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="034f0-143">NOTES</span></span>

## <span data-ttu-id="034f0-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="034f0-144">RELATED LINKS</span></span>
