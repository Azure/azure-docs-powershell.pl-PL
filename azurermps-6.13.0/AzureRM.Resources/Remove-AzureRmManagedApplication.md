---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplication.md
ms.openlocfilehash: 821bfe1048e17baaae9f24bcca5f4b94c2b959ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719381"
---
# <span data-ttu-id="d9d9c-101">Remove-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="d9d9c-101">Remove-AzureRmManagedApplication</span></span>

## <span data-ttu-id="d9d9c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d9d9c-102">SYNOPSIS</span></span>
<span data-ttu-id="d9d9c-103">Usuwa zarządzaną aplikację</span><span class="sxs-lookup"><span data-stu-id="d9d9c-103">Removes a managed application</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9d9c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d9d9c-104">SYNTAX</span></span>

### <span data-ttu-id="d9d9c-105">RemoveByNameAndResourceGroup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d9d9c-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzureRmManagedApplication -Name <String> -ResourceGroupName <String> [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9d9c-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="d9d9c-106">RemoveById</span></span>
```
Remove-AzureRmManagedApplication -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9d9c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d9d9c-107">DESCRIPTION</span></span>
<span data-ttu-id="d9d9c-108">Polecenie cmdlet **Remove-AzureRmManagedApplication** usuwa zarządzaną aplikację</span><span class="sxs-lookup"><span data-stu-id="d9d9c-108">The **Remove-AzureRmManagedApplication** cmdlet removes a managed application</span></span>

## <span data-ttu-id="d9d9c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d9d9c-109">EXAMPLES</span></span>

### <span data-ttu-id="d9d9c-110">Przykład 1: Usuwanie zarządzanej aplikacji według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="d9d9c-110">Example 1: Remove managed application by resource ID</span></span>
```
PS C:\>$Application = Get-AzureRmManagedApplication -Name "myApp" -ResourceGroupName "myRG"
PS C:\>Remove-AzureRmManagedApplication -Id $Application.ResourceId -Force
```

<span data-ttu-id="d9d9c-111">Pierwsze polecenie uzyskuje zarządzaną aplikację o nazwie MojaApl przy użyciu polecenia cmdlet Get-AzureRmManagedApplication.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-111">The first command gets a managed application named myApp by using the Get-AzureRmManagedApplication cmdlet.</span></span>
<span data-ttu-id="d9d9c-112">Polecenie zapisuje je w zmiennej $Application.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-112">The command stores it in the $Application variable.</span></span>
<span data-ttu-id="d9d9c-113">Drugie polecenie usuwa zarządzaną aplikację zidentyfikowaną przez właściwość **ResourceId** $Application.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-113">The second command removes the managed application identified by the **ResourceId** property of $Application.</span></span>

## <span data-ttu-id="d9d9c-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d9d9c-114">PARAMETERS</span></span>

### <span data-ttu-id="d9d9c-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d9d9c-115">-ApiVersion</span></span>
<span data-ttu-id="d9d9c-116">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="d9d9c-117">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="d9d9c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9d9c-118">-DefaultProfile</span></span>
<span data-ttu-id="d9d9c-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9d9c-120">-Force</span><span class="sxs-lookup"><span data-stu-id="d9d9c-120">-Force</span></span>
<span data-ttu-id="d9d9c-121">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d9d9c-122">-ID</span><span class="sxs-lookup"><span data-stu-id="d9d9c-122">-Id</span></span>
<span data-ttu-id="d9d9c-123">W pełni kwalifikowany identyfikator zarządzanej aplikacji, w tym abonament.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-123">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="d9d9c-124">na przykład/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="d9d9c-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="d9d9c-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d9d9c-125">-Name</span></span>
<span data-ttu-id="d9d9c-126">Nazwa zarządzanej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-126">The managed application name.</span></span>

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

### <span data-ttu-id="d9d9c-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="d9d9c-127">-Pre</span></span>
<span data-ttu-id="d9d9c-128">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="d9d9c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9d9c-129">-ResourceGroupName</span></span>
<span data-ttu-id="d9d9c-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-130">The resource group name.</span></span>

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

### <span data-ttu-id="d9d9c-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d9d9c-131">-Confirm</span></span>
<span data-ttu-id="d9d9c-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9d9c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9d9c-133">-WhatIf</span></span>
<span data-ttu-id="d9d9c-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9d9c-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9d9c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9d9c-136">CommonParameters</span></span>
<span data-ttu-id="d9d9c-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9d9c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9d9c-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9d9c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9d9c-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9d9c-139">INPUTS</span></span>

### <span data-ttu-id="d9d9c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="d9d9c-140">System.String</span></span>

## <span data-ttu-id="d9d9c-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d9d9c-141">OUTPUTS</span></span>

### <span data-ttu-id="d9d9c-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d9d9c-142">System.Boolean</span></span>

## <span data-ttu-id="d9d9c-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d9d9c-143">NOTES</span></span>

## <span data-ttu-id="d9d9c-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d9d9c-144">RELATED LINKS</span></span>