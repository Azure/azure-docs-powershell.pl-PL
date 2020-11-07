---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 880D321E-30F2-4CAE-B14A-5F6DD8E1DB99
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroup.md
ms.openlocfilehash: 7878932b0e7a2aad6e171c39e546ad86b2ea0a7c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708301"
---
# <span data-ttu-id="bf78e-101">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bf78e-101">Remove-AzResourceGroup</span></span>

## <span data-ttu-id="bf78e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bf78e-102">SYNOPSIS</span></span>
<span data-ttu-id="bf78e-103">Usuwa grupę zasobów.</span><span class="sxs-lookup"><span data-stu-id="bf78e-103">Removes a resource group.</span></span>

## <span data-ttu-id="bf78e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bf78e-104">SYNTAX</span></span>

### <span data-ttu-id="bf78e-105">RemoveByResourceGroupName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bf78e-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroup [-Name] <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf78e-106">RemoveByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="bf78e-106">RemoveByResourceGroupId</span></span>
```
Remove-AzResourceGroup -Id <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf78e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="bf78e-107">DESCRIPTION</span></span>
<span data-ttu-id="bf78e-108">Polecenie cmdlet **Remove-AzResourceGroup** usuwa grupę zasobów platformy Azure oraz jej zasoby z bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="bf78e-108">The **Remove-AzResourceGroup** cmdlet removes an Azure resource group and its resources from the current subscription.</span></span>
<span data-ttu-id="bf78e-109">Aby usunąć zasób, ale pozostawić grupę zasobów, użyj polecenia cmdlet Remove-AzResource.</span><span class="sxs-lookup"><span data-stu-id="bf78e-109">To delete a resource, but leave the resource group, use the Remove-AzResource cmdlet.</span></span>

## <span data-ttu-id="bf78e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bf78e-110">EXAMPLES</span></span>

### <span data-ttu-id="bf78e-111">Przykład 1. Usuń grupę zasobów</span><span class="sxs-lookup"><span data-stu-id="bf78e-111">Example 1: Remove a resource group</span></span>
```
PS C:\>Remove-AzResourceGroup -Name "ContosoRG01"
```

<span data-ttu-id="bf78e-112">To polecenie usuwa grupę zasobów ContosoRG01 z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="bf78e-112">This command removes the ContosoRG01 resource group from the subscription.</span></span>
<span data-ttu-id="bf78e-113">Polecenie cmdlet monituje o potwierdzenie i nie zwraca wyników.</span><span class="sxs-lookup"><span data-stu-id="bf78e-113">The cmdlet prompts you for confirmation and returns no output.</span></span>

### <span data-ttu-id="bf78e-114">Przykład 2: Usuwanie grupy zasobów bez potwierdzenia</span><span class="sxs-lookup"><span data-stu-id="bf78e-114">Example 2: Remove a resource group without confirmation</span></span>
```
PS C:\>Get-AzResourceGroup -Name "ContosoRG01" | Remove-AzResourceGroup -Verbose -Force
```

<span data-ttu-id="bf78e-115">To polecenie używa polecenia cmdlet Get-AzResourceGroup, aby uzyskać ContosoRG01 grupy zasobów, a następnie przekazuje je do polecenia **Remove-AzResourceGroup** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="bf78e-115">This command uses the Get-AzResourceGroup cmdlet to get the resource group ContosoRG01, and then passes it to **Remove-AzResourceGroup** by using the pipeline operator.</span></span>
<span data-ttu-id="bf78e-116">*Pełny* parametr Common jest pobierany na informacje o stanie operacji, a parametr *Force* pomija monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bf78e-116">The *Verbose* common parameter gets status information about the operation, and the *Force* parameter suppresses the confirmation prompt.</span></span>

### <span data-ttu-id="bf78e-117">Przykład 3: Usuwanie wszystkich grup zasobów</span><span class="sxs-lookup"><span data-stu-id="bf78e-117">Example 3: Remove all resource groups</span></span>
```
PS C:\>Get-AzResourceGroup | Remove-AzResourceGroup
```

<span data-ttu-id="bf78e-118">To polecenie używa polecenia cmdlet **Get-AzResourceGroup** w celu uzyskania wszystkich grup zasobów, a następnie przekazuje je do polecenia **Remove-AzResourceGroup** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="bf78e-118">This command uses the **Get-AzResourceGroup** cmdlet to get all resource groups, and then passes them to **Remove-AzResourceGroup** by using the pipeline operator.</span></span>

## <span data-ttu-id="bf78e-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bf78e-119">PARAMETERS</span></span>

### <span data-ttu-id="bf78e-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="bf78e-120">-ApiVersion</span></span>
<span data-ttu-id="bf78e-121">Określa wersję API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="bf78e-121">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="bf78e-122">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="bf78e-122">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="bf78e-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bf78e-123">-AsJob</span></span>
<span data-ttu-id="bf78e-124">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="bf78e-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bf78e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf78e-125">-DefaultProfile</span></span>
<span data-ttu-id="bf78e-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="bf78e-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bf78e-127">-Force</span><span class="sxs-lookup"><span data-stu-id="bf78e-127">-Force</span></span>
<span data-ttu-id="bf78e-128">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="bf78e-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bf78e-129">-ID</span><span class="sxs-lookup"><span data-stu-id="bf78e-129">-Id</span></span>
<span data-ttu-id="bf78e-130">Określa identyfikator grupy zasobów do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="bf78e-130">Specifies the ID of resource group to remove.</span></span>
<span data-ttu-id="bf78e-131">Znaki wieloznaczne są niedozwolone.</span><span class="sxs-lookup"><span data-stu-id="bf78e-131">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf78e-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bf78e-132">-Name</span></span>
<span data-ttu-id="bf78e-133">Określa nazwy grup zasobów do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="bf78e-133">Specifies the names of resource groups to remove.</span></span>
<span data-ttu-id="bf78e-134">Znaki wieloznaczne są niedozwolone.</span><span class="sxs-lookup"><span data-stu-id="bf78e-134">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="bf78e-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="bf78e-135">-Pre</span></span>
<span data-ttu-id="bf78e-136">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="bf78e-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="bf78e-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bf78e-137">-Confirm</span></span>
<span data-ttu-id="bf78e-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf78e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf78e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf78e-139">-WhatIf</span></span>
<span data-ttu-id="bf78e-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf78e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf78e-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bf78e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf78e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf78e-142">CommonParameters</span></span>
<span data-ttu-id="bf78e-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf78e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf78e-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf78e-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf78e-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bf78e-145">INPUTS</span></span>

### <span data-ttu-id="bf78e-146">System. String</span><span class="sxs-lookup"><span data-stu-id="bf78e-146">System.String</span></span>

## <span data-ttu-id="bf78e-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bf78e-147">OUTPUTS</span></span>

### <span data-ttu-id="bf78e-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bf78e-148">System.Boolean</span></span>

## <span data-ttu-id="bf78e-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bf78e-149">NOTES</span></span>

## <span data-ttu-id="bf78e-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bf78e-150">RELATED LINKS</span></span>

[<span data-ttu-id="bf78e-151">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bf78e-151">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="bf78e-152">Nowe — AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bf78e-152">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="bf78e-153">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bf78e-153">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)

