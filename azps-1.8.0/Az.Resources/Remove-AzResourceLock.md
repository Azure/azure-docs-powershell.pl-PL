---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceLock.md
ms.openlocfilehash: 32a3dbb458c4848a5578309593b205b4ced5be03
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708297"
---
# <span data-ttu-id="ae317-101">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="ae317-101">Remove-AzResourceLock</span></span>

## <span data-ttu-id="ae317-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ae317-102">SYNOPSIS</span></span>
<span data-ttu-id="ae317-103">Usuwa blokadę zasobu.</span><span class="sxs-lookup"><span data-stu-id="ae317-103">Removes a resource lock.</span></span>

## <span data-ttu-id="ae317-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ae317-104">SYNTAX</span></span>

### <span data-ttu-id="ae317-105">ByLockId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ae317-105">ByLockId (Default)</span></span>
```
Remove-AzResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae317-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ae317-106">ByResourceGroup</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae317-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="ae317-107">ByResourceGroupLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae317-108">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="ae317-108">BySpecifiedScope</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae317-109">BySubscription</span><span class="sxs-lookup"><span data-stu-id="ae317-109">BySubscription</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae317-110">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="ae317-110">BySubscriptionLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ae317-111">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="ae317-111">ByTenantLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String> [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ae317-112">Opis</span><span class="sxs-lookup"><span data-stu-id="ae317-112">DESCRIPTION</span></span>
<span data-ttu-id="ae317-113">Polecenie cmdlet **Remove-AzResourceLock** usuwa blokadę zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ae317-113">The **Remove-AzResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="ae317-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ae317-114">EXAMPLES</span></span>

### <span data-ttu-id="ae317-115">Przykład 1: Usuwanie blokady</span><span class="sxs-lookup"><span data-stu-id="ae317-115">Example 1: Remove a lock</span></span>
```
PS C:\>Remove-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="ae317-116">To polecenie usuwa blokadę o nazwie ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="ae317-116">This command removes the lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="ae317-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ae317-117">PARAMETERS</span></span>

### <span data-ttu-id="ae317-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ae317-118">-ApiVersion</span></span>
<span data-ttu-id="ae317-119">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="ae317-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="ae317-120">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="ae317-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="ae317-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae317-121">-DefaultProfile</span></span>
<span data-ttu-id="ae317-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ae317-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae317-123">-Force</span><span class="sxs-lookup"><span data-stu-id="ae317-123">-Force</span></span>
<span data-ttu-id="ae317-124">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="ae317-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ae317-125">-LockId</span><span class="sxs-lookup"><span data-stu-id="ae317-125">-LockId</span></span>
<span data-ttu-id="ae317-126">Określa identyfikator blokady, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae317-126">Specifies the ID of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ae317-127">-Kłódkaname</span><span class="sxs-lookup"><span data-stu-id="ae317-127">-LockName</span></span>
<span data-ttu-id="ae317-128">Określa nazwę blokady usuniętej przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae317-128">Specifies the name of the lock that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae317-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="ae317-129">-Pre</span></span>
<span data-ttu-id="ae317-130">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="ae317-130">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ae317-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae317-131">-ResourceGroupName</span></span>
<span data-ttu-id="ae317-132">Określa nazwę grupy zasobów, której dotyczy blokada.</span><span class="sxs-lookup"><span data-stu-id="ae317-132">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="ae317-133">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="ae317-133">-ResourceName</span></span>
<span data-ttu-id="ae317-134">Określa nazwę zasobu, którego dotyczy blokada.</span><span class="sxs-lookup"><span data-stu-id="ae317-134">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="ae317-135">Aby na przykład określić bazę danych, użyj następującego formatu: `/` baza danych serwera</span><span class="sxs-lookup"><span data-stu-id="ae317-135">For instance, to specify a database, use the following format: Server`/`Database</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae317-136">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="ae317-136">-ResourceType</span></span>
<span data-ttu-id="ae317-137">Określa typ zasobu zasobu, którego dotyczy blokada.</span><span class="sxs-lookup"><span data-stu-id="ae317-137">Specifies the resource type of the resource for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae317-138">-Zakres</span><span class="sxs-lookup"><span data-stu-id="ae317-138">-Scope</span></span>
<span data-ttu-id="ae317-139">Określa zakres, do którego jest stosowana blokada.</span><span class="sxs-lookup"><span data-stu-id="ae317-139">Specifies the scope to which the lock applies.</span></span>

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

### <span data-ttu-id="ae317-140">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="ae317-140">-TenantLevel</span></span>
<span data-ttu-id="ae317-141">Wskazuje, że ten aplet polecenia działa na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="ae317-141">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae317-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ae317-142">-Confirm</span></span>
<span data-ttu-id="ae317-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae317-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae317-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae317-144">-WhatIf</span></span>
<span data-ttu-id="ae317-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae317-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae317-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ae317-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae317-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae317-147">CommonParameters</span></span>
<span data-ttu-id="ae317-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae317-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae317-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae317-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae317-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae317-150">INPUTS</span></span>

### <span data-ttu-id="ae317-151">System. String</span><span class="sxs-lookup"><span data-stu-id="ae317-151">System.String</span></span>

## <span data-ttu-id="ae317-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ae317-152">OUTPUTS</span></span>

### <span data-ttu-id="ae317-153">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="ae317-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="ae317-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ae317-154">NOTES</span></span>

## <span data-ttu-id="ae317-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae317-155">RELATED LINKS</span></span>

[<span data-ttu-id="ae317-156">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="ae317-156">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="ae317-157">Nowe — AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="ae317-157">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="ae317-158">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="ae317-158">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


