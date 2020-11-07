---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 880D321E-30F2-4CAE-B14A-5F6DD8E1DB99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcegroup
schema: 2.0.0
ms.openlocfilehash: d2038823b769a93d290b9685acf75bbfa86532de
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899025"
---
# <span data-ttu-id="e4220-101">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e4220-101">Remove-AzureRmResourceGroup</span></span>

## <span data-ttu-id="e4220-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e4220-102">SYNOPSIS</span></span>
<span data-ttu-id="e4220-103">Usuwa grupę zasobów.</span><span class="sxs-lookup"><span data-stu-id="e4220-103">Removes a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4220-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e4220-104">SYNTAX</span></span>

### <span data-ttu-id="e4220-105">RemoveByResourceGroupName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e4220-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzureRmResourceGroup [-Name] <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4220-106">RemoveByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="e4220-106">RemoveByResourceGroupId</span></span>
```
Remove-AzureRmResourceGroup [-Id] <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4220-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e4220-107">DESCRIPTION</span></span>
<span data-ttu-id="e4220-108">Polecenie cmdlet **Remove-AzureRmResourceGroup** usuwa grupę zasobów platformy Azure oraz jej zasoby z bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e4220-108">The **Remove-AzureRmResourceGroup** cmdlet removes an Azure resource group and its resources from the current subscription.</span></span>
<span data-ttu-id="e4220-109">Aby usunąć zasób, ale pozostawić grupę zasobów, użyj polecenia cmdlet Remove-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="e4220-109">To delete a resource, but leave the resource group, use the Remove-AzureRmResource cmdlet.</span></span>

## <span data-ttu-id="e4220-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e4220-110">EXAMPLES</span></span>

### <span data-ttu-id="e4220-111">Przykład 1. Usuń grupę zasobów</span><span class="sxs-lookup"><span data-stu-id="e4220-111">Example 1: Remove a resource group</span></span>
```
PS C:\>Remove-AzureRmResourceGroup -Name "ContosoRG01"
```

<span data-ttu-id="e4220-112">To polecenie usuwa grupę zasobów ContosoRG01 z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e4220-112">This command removes the ContosoRG01 resource group from the subscription.</span></span>
<span data-ttu-id="e4220-113">Polecenie cmdlet monituje o potwierdzenie i nie zwraca wyników.</span><span class="sxs-lookup"><span data-stu-id="e4220-113">The cmdlet prompts you for confirmation and returns no output.</span></span>

### <span data-ttu-id="e4220-114">Przykład 2: Usuwanie grupy zasobów bez potwierdzenia</span><span class="sxs-lookup"><span data-stu-id="e4220-114">Example 2: Remove a resource group without confirmation</span></span>
```
PS C:\>Get-AzureRmResourceGroup -Name "ContosoRG01" | Remove-AzureRmResourceGroup -Verbose -Force
```

<span data-ttu-id="e4220-115">To polecenie używa polecenia cmdlet Get-AzureRmResourceGroup, aby uzyskać ContosoRG01 grupy zasobów, a następnie przekazuje je do polecenia **Remove-AzureRmResourceGroup** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="e4220-115">This command uses the Get-AzureRmResourceGroup cmdlet to get the resource group ContosoRG01, and then passes it to **Remove-AzureRmResourceGroup** by using the pipeline operator.</span></span>
<span data-ttu-id="e4220-116">*Pełny* parametr Common jest pobierany na informacje o stanie operacji, a parametr *Force* pomija monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e4220-116">The *Verbose* common parameter gets status information about the operation, and the *Force* parameter suppresses the confirmation prompt.</span></span>

### <span data-ttu-id="e4220-117">Przykład 3: Usuwanie wszystkich grup zasobów</span><span class="sxs-lookup"><span data-stu-id="e4220-117">Example 3: Remove all resource groups</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Remove-AzureRmResourceGroup
```

<span data-ttu-id="e4220-118">To polecenie używa polecenia cmdlet **Get-AzureRmResourceGroup** w celu uzyskania wszystkich grup zasobów, a następnie przekazuje je do polecenia **Remove-AzureRmResourceGroup** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="e4220-118">This command uses the **Get-AzureRmResourceGroup** cmdlet to get all resource groups, and then passes them to **Remove-AzureRmResourceGroup** by using the pipeline operator.</span></span>

## <span data-ttu-id="e4220-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e4220-119">PARAMETERS</span></span>

### <span data-ttu-id="e4220-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e4220-120">-ApiVersion</span></span>
<span data-ttu-id="e4220-121">Określa wersję API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="e4220-121">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="e4220-122">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="e4220-122">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="e4220-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e4220-123">-AsJob</span></span>
<span data-ttu-id="e4220-124">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e4220-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e4220-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4220-125">-DefaultProfile</span></span>
<span data-ttu-id="e4220-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e4220-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4220-127">-Force</span><span class="sxs-lookup"><span data-stu-id="e4220-127">-Force</span></span>
<span data-ttu-id="e4220-128">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e4220-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e4220-129">-ID</span><span class="sxs-lookup"><span data-stu-id="e4220-129">-Id</span></span>
<span data-ttu-id="e4220-130">Określa identyfikator grupy zasobów do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="e4220-130">Specifies the ID of resource group to remove.</span></span>
<span data-ttu-id="e4220-131">Znaki wieloznaczne są niedozwolone.</span><span class="sxs-lookup"><span data-stu-id="e4220-131">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4220-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e4220-132">-Name</span></span>
<span data-ttu-id="e4220-133">Określa nazwy grup zasobów do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="e4220-133">Specifies the names of resource groups to remove.</span></span>
<span data-ttu-id="e4220-134">Znaki wieloznaczne są niedozwolone.</span><span class="sxs-lookup"><span data-stu-id="e4220-134">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4220-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="e4220-135">-Pre</span></span>
<span data-ttu-id="e4220-136">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="e4220-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e4220-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e4220-137">-Confirm</span></span>
<span data-ttu-id="e4220-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4220-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4220-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4220-139">-WhatIf</span></span>
<span data-ttu-id="e4220-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4220-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4220-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e4220-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4220-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4220-142">CommonParameters</span></span>
<span data-ttu-id="e4220-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4220-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4220-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4220-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4220-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4220-145">INPUTS</span></span>

## <span data-ttu-id="e4220-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e4220-146">OUTPUTS</span></span>

## <span data-ttu-id="e4220-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e4220-147">NOTES</span></span>

## <span data-ttu-id="e4220-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e4220-148">RELATED LINKS</span></span>

[<span data-ttu-id="e4220-149">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e4220-149">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="e4220-150">Nowe — AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e4220-150">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="e4220-151">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e4220-151">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)


