---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceLock.md
ms.openlocfilehash: f3034d7197a26e8dd2ba803f478b6a71c8d50e8c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717312"
---
# <span data-ttu-id="9d0cd-101">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="9d0cd-101">Remove-AzureRmResourceLock</span></span>

## <span data-ttu-id="9d0cd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9d0cd-102">SYNOPSIS</span></span>
<span data-ttu-id="9d0cd-103">Usuwa blokadę zasobu.</span><span class="sxs-lookup"><span data-stu-id="9d0cd-103">Removes a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d0cd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9d0cd-104">SYNTAX</span></span>

### <span data-ttu-id="9d0cd-105">ByLockId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9d0cd-105">ByLockId (Default)</span></span>
```
Remove-AzureRmResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d0cd-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9d0cd-106">ByResourceGroup</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d0cd-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="9d0cd-107">ByResourceGroupLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9d0cd-108">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="9d0cd-108">BySpecifiedScope</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d0cd-109">BySubscription</span><span class="sxs-lookup"><span data-stu-id="9d0cd-109">BySubscription</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d0cd-110">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="9d0cd-110">BySubscriptionLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9d0cd-111">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="9d0cd-111">ByTenantLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9d0cd-112">Opis</span><span class="sxs-lookup"><span data-stu-id="9d0cd-112">DESCRIPTION</span></span>
<span data-ttu-id="9d0cd-113">Polecenie cmdlet **Remove-AzureRmResourceLock** usuwa blokadę zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9d0cd-113">The **Remove-AzureRmResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="9d0cd-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9d0cd-114">EXAMPLES</span></span>

### <span data-ttu-id="9d0cd-115">Przykład 1: Usuwanie blokady</span><span class="sxs-lookup"><span data-stu-id="9d0cd-115">Example 1: Remove a lock</span></span>
```
PS C:\>Remove-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="9d0cd-116">To polecenie usuwa blokadę o nazwie ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="9d0cd-116">This command removes the lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="9d0cd-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9d0cd-117">PARAMETERS</span></span>

### <span data-ttu-id="9d0cd-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9d0cd-118">-ApiVersion</span></span>
<span data-ttu-id="9d0cd-119">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="9d0cd-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="9d0cd-120">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="9d0cd-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="9d0cd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d0cd-121">-DefaultProfile</span></span>
<span data-ttu-id="9d0cd-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="9d0cd-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9d0cd-123">-Force</span><span class="sxs-lookup"><span data-stu-id="9d0cd-123">-Force</span></span>
<span data-ttu-id="9d0cd-124">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9d0cd-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9d0cd-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="9d0cd-125">-InformationAction</span></span>
<span data-ttu-id="9d0cd-126">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="9d0cd-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9d0cd-127">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="9d0cd-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9d0cd-128">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="9d0cd-128">Continue</span></span>
- <span data-ttu-id="9d0cd-129">Ignorować</span><span class="sxs-lookup"><span data-stu-id="9d0cd-129">Ignore</span></span>
- <span data-ttu-id="9d0cd-130">Inquire</span><span class="sxs-lookup"><span data-stu-id="9d0cd-130">Inquire</span></span>
- <span data-ttu-id="9d0cd-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9d0cd-131">SilentlyContinue</span></span>
- <span data-ttu-id="9d0cd-132">Przestaw</span><span class="sxs-lookup"><span data-stu-id="9d0cd-132">Stop</span></span>
- <span data-ttu-id="9d0cd-133">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="9d0cd-133">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d0cd-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9d0cd-134">-InformationVariable</span></span>
<span data-ttu-id="9d0cd-135">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="9d0cd-135">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d0cd-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="9d0cd-136">-LockId</span></span>
<span data-ttu-id="9d0cd-137">Określa identyfikator blokady, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d0cd-137">Specifies the ID of the lock that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByLockId
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d0cd-138">-Kłódkaname</span><span class="sxs-lookup"><span data-stu-id="9d0cd-138">-LockName</span></span>
<span data-ttu-id="9d0cd-139">Określa nazwę blokady usuniętej przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d0cd-139">Specifies the name of the lock that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d0cd-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="9d0cd-140">-Pre</span></span>
<span data-ttu-id="9d0cd-141">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="9d0cd-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="9d0cd-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d0cd-142">-ResourceGroupName</span></span>
<span data-ttu-id="9d0cd-143">Określa nazwę grupy zasobów, której dotyczy blokada.</span><span class="sxs-lookup"><span data-stu-id="9d0cd-143">Specifies the name of the resource group for which the lock applies.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d0cd-144">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="9d0cd-144">-ResourceName</span></span>
<span data-ttu-id="9d0cd-145">Określa nazwę zasobu, którego dotyczy blokada.</span><span class="sxs-lookup"><span data-stu-id="9d0cd-145">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="9d0cd-146">Aby na przykład określić bazę danych, użyj następującego formatu:</span><span class="sxs-lookup"><span data-stu-id="9d0cd-146">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="9d0cd-147">`/`Baza danych serwera</span><span class="sxs-lookup"><span data-stu-id="9d0cd-147">Server`/`Database</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d0cd-148">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="9d0cd-148">-ResourceType</span></span>
<span data-ttu-id="9d0cd-149">Określa typ zasobu zasobu, którego dotyczy blokada.</span><span class="sxs-lookup"><span data-stu-id="9d0cd-149">Specifies the resource type of the resource for which the lock applies.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d0cd-150">-Zakres</span><span class="sxs-lookup"><span data-stu-id="9d0cd-150">-Scope</span></span>
<span data-ttu-id="9d0cd-151">Określa zakres, do którego jest stosowana blokada.</span><span class="sxs-lookup"><span data-stu-id="9d0cd-151">Specifies the scope to which the lock applies.</span></span>

```yaml
Type: String
Parameter Sets: BySpecifiedScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d0cd-152">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="9d0cd-152">-TenantLevel</span></span>
<span data-ttu-id="9d0cd-153">Wskazuje, że ten aplet polecenia działa na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="9d0cd-153">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d0cd-154">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9d0cd-154">-Confirm</span></span>
<span data-ttu-id="9d0cd-155">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d0cd-155">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d0cd-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d0cd-156">-WhatIf</span></span>
<span data-ttu-id="9d0cd-157">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d0cd-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d0cd-158">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9d0cd-158">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d0cd-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d0cd-159">CommonParameters</span></span>
<span data-ttu-id="9d0cd-160">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d0cd-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d0cd-161">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d0cd-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d0cd-162">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d0cd-162">INPUTS</span></span>

### <span data-ttu-id="9d0cd-163">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9d0cd-163">None</span></span>
<span data-ttu-id="9d0cd-164">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="9d0cd-164">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9d0cd-165">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9d0cd-165">OUTPUTS</span></span>

### <span data-ttu-id="9d0cd-166">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="9d0cd-166">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="9d0cd-167">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9d0cd-167">NOTES</span></span>

## <span data-ttu-id="9d0cd-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9d0cd-168">RELATED LINKS</span></span>

[<span data-ttu-id="9d0cd-169">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="9d0cd-169">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="9d0cd-170">Nowe — AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="9d0cd-170">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="9d0cd-171">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="9d0cd-171">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


