---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplication.md
ms.openlocfilehash: 75e750aa13df16deb5c281a5914a6c21a1740e88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718714"
---
# <span data-ttu-id="34848-101">Remove-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="34848-101">Remove-AzureRmManagedApplication</span></span>

## <span data-ttu-id="34848-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="34848-102">SYNOPSIS</span></span>
<span data-ttu-id="34848-103">Usuwa zarządzaną aplikację</span><span class="sxs-lookup"><span data-stu-id="34848-103">Removes a managed application</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34848-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="34848-104">SYNTAX</span></span>

### <span data-ttu-id="34848-105">Zestaw parametrów nazwa aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="34848-105">The managed application name parameter set.</span></span> <span data-ttu-id="34848-106">Domyślne</span><span class="sxs-lookup"><span data-stu-id="34848-106">(Default)</span></span>
```
Remove-AzureRmManagedApplication -Name <String> -ResourceGroupName <String> [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34848-107">Zestaw parametrów zarządzany identyfikator aplikacji.</span><span class="sxs-lookup"><span data-stu-id="34848-107">The managed application Id parameter set.</span></span>
```
Remove-AzureRmManagedApplication -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34848-108">Opis</span><span class="sxs-lookup"><span data-stu-id="34848-108">DESCRIPTION</span></span>
<span data-ttu-id="34848-109">Polecenie cmdlet **Remove-AzureRmManagedApplication** usuwa zarządzaną aplikację</span><span class="sxs-lookup"><span data-stu-id="34848-109">The **Remove-AzureRmManagedApplication** cmdlet removes a managed application</span></span>

## <span data-ttu-id="34848-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="34848-110">EXAMPLES</span></span>

### <span data-ttu-id="34848-111">Przykład 1: Usuwanie zarządzanej aplikacji według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="34848-111">Example 1: Remove managed application by resource ID</span></span>
```
PS C:\>$Application = Get-AzureRmManagedApplication -Name "myApp" -ResourceGroupName "myRG"
PS C:\>Remove-AzureRmManagedApplication -Id $Application.ResourceId -Force
```

<span data-ttu-id="34848-112">Pierwsze polecenie uzyskuje zarządzaną aplikację o nazwie MojaApl przy użyciu polecenia cmdlet Get-AzureRmManagedApplication.</span><span class="sxs-lookup"><span data-stu-id="34848-112">The first command gets a managed application named myApp by using the Get-AzureRmManagedApplication cmdlet.</span></span>
<span data-ttu-id="34848-113">Polecenie zapisuje je w zmiennej $Application.</span><span class="sxs-lookup"><span data-stu-id="34848-113">The command stores it in the $Application variable.</span></span>

<span data-ttu-id="34848-114">Drugie polecenie usuwa zarządzaną aplikację zidentyfikowaną przez właściwość **ResourceId** $Application.</span><span class="sxs-lookup"><span data-stu-id="34848-114">The second command removes the managed application identified by the **ResourceId** property of $Application.</span></span>

## <span data-ttu-id="34848-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="34848-115">PARAMETERS</span></span>

### <span data-ttu-id="34848-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="34848-116">-ApiVersion</span></span>
<span data-ttu-id="34848-117">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="34848-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="34848-118">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="34848-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="34848-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34848-119">-DefaultProfile</span></span>
<span data-ttu-id="34848-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="34848-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34848-121">-Force</span><span class="sxs-lookup"><span data-stu-id="34848-121">-Force</span></span>
<span data-ttu-id="34848-122">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="34848-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="34848-123">-ID</span><span class="sxs-lookup"><span data-stu-id="34848-123">-Id</span></span>
<span data-ttu-id="34848-124">W pełni kwalifikowany identyfikator zarządzanej aplikacji, w tym abonament.</span><span class="sxs-lookup"><span data-stu-id="34848-124">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="34848-125">na przykład/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="34848-125">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34848-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="34848-126">-Name</span></span>
<span data-ttu-id="34848-127">Nazwa zarządzanej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="34848-127">The managed application name.</span></span>

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

### <span data-ttu-id="34848-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="34848-128">-Pre</span></span>
<span data-ttu-id="34848-129">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="34848-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="34848-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34848-130">-ResourceGroupName</span></span>
<span data-ttu-id="34848-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="34848-131">The resource group name.</span></span>

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

### <span data-ttu-id="34848-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="34848-132">-Confirm</span></span>
<span data-ttu-id="34848-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34848-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34848-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34848-134">-WhatIf</span></span>
<span data-ttu-id="34848-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34848-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34848-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="34848-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34848-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34848-137">CommonParameters</span></span>
<span data-ttu-id="34848-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34848-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34848-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34848-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34848-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34848-140">INPUTS</span></span>

### <span data-ttu-id="34848-141">System. String</span><span class="sxs-lookup"><span data-stu-id="34848-141">System.String</span></span>

## <span data-ttu-id="34848-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="34848-142">OUTPUTS</span></span>

### <span data-ttu-id="34848-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="34848-143">System.Boolean</span></span>

## <span data-ttu-id="34848-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="34848-144">NOTES</span></span>

## <span data-ttu-id="34848-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34848-145">RELATED LINKS</span></span>

