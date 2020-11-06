---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: 2e951452789d57d6d5e126fca80713ef7fd2c584
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552367"
---
# <span data-ttu-id="134fd-101">Remove-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="134fd-101">Remove-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="134fd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="134fd-102">SYNOPSIS</span></span>
<span data-ttu-id="134fd-103">Usuwa definicję aplikacji zarządzanej</span><span class="sxs-lookup"><span data-stu-id="134fd-103">Removes a managed application definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="134fd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="134fd-104">SYNTAX</span></span>

### <span data-ttu-id="134fd-105">Zestaw parametrów Nazwa definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="134fd-105">The managed application definition name parameter set.</span></span> <span data-ttu-id="134fd-106">Domyślne</span><span class="sxs-lookup"><span data-stu-id="134fd-106">(Default)</span></span>
```
Remove-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="134fd-107">Zestaw parametrów identyfikatora definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="134fd-107">The managed application definition Id parameter set.</span></span>
```
Remove-AzureRmManagedApplicationDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="134fd-108">Opis</span><span class="sxs-lookup"><span data-stu-id="134fd-108">DESCRIPTION</span></span>
<span data-ttu-id="134fd-109">Polecenie cmdlet **Remove-AzureRmManagedApplicationDefinition** usuwa definicję aplikacji zarządzanej</span><span class="sxs-lookup"><span data-stu-id="134fd-109">The **Remove-AzureRmManagedApplicationDefinition** cmdlet removes a managed application definition</span></span>

## <span data-ttu-id="134fd-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="134fd-110">EXAMPLES</span></span>

### <span data-ttu-id="134fd-111">Przykład 1: usuwanie definicji aplikacji zarządzanej według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="134fd-111">Example 1: Remove managed application definition by resource ID</span></span>
```
PS C:\>$ApplicationDefinition = Get-AzureRmManagedApplicationDefinition -Name "myAppDef" -ResourceGroupName "myRG"
PS C:\>Remove-AzureRmManagedApplicationDefinition -Id $ApplicationDefinition.ResourceId -Force
```

<span data-ttu-id="134fd-112">Pierwsze polecenie pobiera definicję aplikacji zarządzanej o nazwie myAppDef przy użyciu polecenia cmdlet Get-AzureRmManagedApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="134fd-112">The first command gets a managed application definition named myAppDef by using the Get-AzureRmManagedApplicationDefinition cmdlet.</span></span>
<span data-ttu-id="134fd-113">Polecenie zapisuje je w zmiennej $ApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="134fd-113">The command stores it in the $ApplicationDefinition variable.</span></span>

<span data-ttu-id="134fd-114">Drugie polecenie usuwa definicję aplikacji zarządzanej zidentyfikowaną przez właściwość **ResourceId** $ApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="134fd-114">The second command removes the managed application definition identified by the **ResourceId** property of $ApplicationDefinition.</span></span>

## <span data-ttu-id="134fd-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="134fd-115">PARAMETERS</span></span>

### <span data-ttu-id="134fd-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="134fd-116">-ApiVersion</span></span>
<span data-ttu-id="134fd-117">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="134fd-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="134fd-118">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="134fd-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="134fd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="134fd-119">-DefaultProfile</span></span>
<span data-ttu-id="134fd-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="134fd-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="134fd-121">-Force</span><span class="sxs-lookup"><span data-stu-id="134fd-121">-Force</span></span>
<span data-ttu-id="134fd-122">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="134fd-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="134fd-123">-ID</span><span class="sxs-lookup"><span data-stu-id="134fd-123">-Id</span></span>
<span data-ttu-id="134fd-124">W pełni kwalifikowana nazwa definicji aplikacji zarządzanej, w tym abonament.</span><span class="sxs-lookup"><span data-stu-id="134fd-124">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="134fd-125">na przykład/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="134fd-125">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="134fd-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="134fd-126">-Name</span></span>
<span data-ttu-id="134fd-127">Nazwa definicji aplikacji zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="134fd-127">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="134fd-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="134fd-128">-Pre</span></span>
<span data-ttu-id="134fd-129">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="134fd-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="134fd-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="134fd-130">-ResourceGroupName</span></span>
<span data-ttu-id="134fd-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="134fd-131">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="134fd-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="134fd-132">-Confirm</span></span>
<span data-ttu-id="134fd-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="134fd-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="134fd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="134fd-134">-WhatIf</span></span>
<span data-ttu-id="134fd-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="134fd-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="134fd-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="134fd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="134fd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="134fd-137">CommonParameters</span></span>
<span data-ttu-id="134fd-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="134fd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="134fd-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="134fd-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="134fd-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="134fd-140">INPUTS</span></span>

### <span data-ttu-id="134fd-141">System. String</span><span class="sxs-lookup"><span data-stu-id="134fd-141">System.String</span></span>

## <span data-ttu-id="134fd-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="134fd-142">OUTPUTS</span></span>

### <span data-ttu-id="134fd-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="134fd-143">System.Boolean</span></span>

## <span data-ttu-id="134fd-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="134fd-144">NOTES</span></span>

## <span data-ttu-id="134fd-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="134fd-145">RELATED LINKS</span></span>

