---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceLock.md
ms.openlocfilehash: 5047ce0ebeb4f93d1d73473edbec50eaf65c6875
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234298"
---
# <span data-ttu-id="48639-101">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="48639-101">Remove-AzResourceLock</span></span>

## <span data-ttu-id="48639-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="48639-102">SYNOPSIS</span></span>
<span data-ttu-id="48639-103">Usuwa blokadę zasobu.</span><span class="sxs-lookup"><span data-stu-id="48639-103">Removes a resource lock.</span></span>

## <span data-ttu-id="48639-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="48639-104">SYNTAX</span></span>

### <span data-ttu-id="48639-105">ByLockId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="48639-105">ByLockId (Default)</span></span>
```
Remove-AzResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48639-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="48639-106">ByResourceGroup</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48639-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="48639-107">ByResourceGroupLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48639-108">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="48639-108">BySpecifiedScope</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48639-109">BySubscription</span><span class="sxs-lookup"><span data-stu-id="48639-109">BySubscription</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48639-110">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="48639-110">BySubscriptionLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="48639-111">Opis</span><span class="sxs-lookup"><span data-stu-id="48639-111">DESCRIPTION</span></span>
<span data-ttu-id="48639-112">Polecenie cmdlet **Remove-AzResourceLock** usuwa blokadę zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="48639-112">The **Remove-AzResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="48639-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="48639-113">EXAMPLES</span></span>

### <span data-ttu-id="48639-114">Przykład 1: Usuwanie blokady</span><span class="sxs-lookup"><span data-stu-id="48639-114">Example 1: Remove a lock</span></span>
```powershell
PS C:\>Remove-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="48639-115">To polecenie usuwa blokadę o nazwie ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="48639-115">This command removes the lock named ContosoSiteLock.</span></span>

### <span data-ttu-id="48639-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="48639-116">Example 2</span></span>

<span data-ttu-id="48639-117">Usuwa blokadę zasobu.</span><span class="sxs-lookup"><span data-stu-id="48639-117">Removes a resource lock.</span></span> <span data-ttu-id="48639-118">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="48639-118">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->


```powershell
Remove-AzResourceLock -LockName 'ContosoSiteLock' -ResourceGroupName myresourcegroup -ResourceName '/subscriptions/00000000-0000-0000-0000-00000000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test' -ResourceType 'Microsoft.ClassicCompute/storageAccounts'
```

## <span data-ttu-id="48639-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="48639-119">PARAMETERS</span></span>

### <span data-ttu-id="48639-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="48639-120">-ApiVersion</span></span>
<span data-ttu-id="48639-121">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="48639-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="48639-122">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="48639-122">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="48639-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48639-123">-DefaultProfile</span></span>
<span data-ttu-id="48639-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="48639-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48639-125">-Force</span><span class="sxs-lookup"><span data-stu-id="48639-125">-Force</span></span>
<span data-ttu-id="48639-126">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="48639-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="48639-127">-LockId</span><span class="sxs-lookup"><span data-stu-id="48639-127">-LockId</span></span>
<span data-ttu-id="48639-128">Określa identyfikator blokady, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48639-128">Specifies the ID of the lock that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLockId
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48639-129">-Kłódkaname</span><span class="sxs-lookup"><span data-stu-id="48639-129">-LockName</span></span>
<span data-ttu-id="48639-130">Określa nazwę blokady usuniętej przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48639-130">Specifies the name of the lock that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48639-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="48639-131">-Pre</span></span>
<span data-ttu-id="48639-132">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="48639-132">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="48639-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48639-133">-ResourceGroupName</span></span>
<span data-ttu-id="48639-134">Określa nazwę grupy zasobów, której dotyczy blokada.</span><span class="sxs-lookup"><span data-stu-id="48639-134">Specifies the name of the resource group for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48639-135">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="48639-135">-ResourceName</span></span>
<span data-ttu-id="48639-136">Określa nazwę zasobu, którego dotyczy blokada.</span><span class="sxs-lookup"><span data-stu-id="48639-136">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="48639-137">Aby na przykład określić bazę danych, użyj następującego formatu: `/` baza danych serwera</span><span class="sxs-lookup"><span data-stu-id="48639-137">For instance, to specify a database, use the following format: Server`/`Database</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48639-138">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="48639-138">-ResourceType</span></span>
<span data-ttu-id="48639-139">Określa typ zasobu zasobu, którego dotyczy blokada.</span><span class="sxs-lookup"><span data-stu-id="48639-139">Specifies the resource type of the resource for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48639-140">-Zakres</span><span class="sxs-lookup"><span data-stu-id="48639-140">-Scope</span></span>
<span data-ttu-id="48639-141">Określa zakres, do którego jest stosowana blokada.</span><span class="sxs-lookup"><span data-stu-id="48639-141">Specifies the scope to which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48639-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="48639-142">-Confirm</span></span>
<span data-ttu-id="48639-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48639-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48639-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48639-144">-WhatIf</span></span>
<span data-ttu-id="48639-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48639-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48639-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="48639-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48639-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48639-147">CommonParameters</span></span>
<span data-ttu-id="48639-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48639-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48639-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="48639-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48639-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48639-150">INPUTS</span></span>

### <span data-ttu-id="48639-151">System. String</span><span class="sxs-lookup"><span data-stu-id="48639-151">System.String</span></span>

## <span data-ttu-id="48639-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="48639-152">OUTPUTS</span></span>

### <span data-ttu-id="48639-153">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="48639-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="48639-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="48639-154">NOTES</span></span>

## <span data-ttu-id="48639-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="48639-155">RELATED LINKS</span></span>

[<span data-ttu-id="48639-156">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="48639-156">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="48639-157">Nowe — AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="48639-157">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="48639-158">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="48639-158">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


