---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceLock.md
ms.openlocfilehash: c45d78b815586e54c9f39cfd536fed5a26c2eb19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549864"
---
# <span data-ttu-id="d58c9-101">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="d58c9-101">Remove-AzureRmResourceLock</span></span>

## <span data-ttu-id="d58c9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d58c9-102">SYNOPSIS</span></span>
<span data-ttu-id="d58c9-103">Usuwa blokadę zasobu.</span><span class="sxs-lookup"><span data-stu-id="d58c9-103">Removes a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d58c9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d58c9-104">SYNTAX</span></span>

### <span data-ttu-id="d58c9-105">Blokada z identyfikatorem (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="d58c9-105">A lock, by Id. (Default)</span></span>
```
Remove-AzureRmResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d58c9-106">Blokada zakresu grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d58c9-106">A lock at the resource group scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d58c9-107">Blokada zakresu zasobów grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d58c9-107">A lock at the resource group resource scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d58c9-108">Blokada w określonym zakresie.</span><span class="sxs-lookup"><span data-stu-id="d58c9-108">A lock at the specified scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d58c9-109">Blokada zakresu subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d58c9-109">A lock at the subscription scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d58c9-110">Blokada w zakresie zasobów subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d58c9-110">A lock at the subscription resource scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d58c9-111">Blokada w zakresie zasobów dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="d58c9-111">A lock at the tenant resource scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d58c9-112">Opis</span><span class="sxs-lookup"><span data-stu-id="d58c9-112">DESCRIPTION</span></span>
<span data-ttu-id="d58c9-113">Polecenie cmdlet **Remove-AzureRmResourceLock** usuwa blokadę zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d58c9-113">The **Remove-AzureRmResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="d58c9-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d58c9-114">EXAMPLES</span></span>

### <span data-ttu-id="d58c9-115">Przykład 1: Usuwanie blokady</span><span class="sxs-lookup"><span data-stu-id="d58c9-115">Example 1: Remove a lock</span></span>
```
PS C:\>Remove-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="d58c9-116">To polecenie usuwa blokadę o nazwie ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="d58c9-116">This command removes the lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="d58c9-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d58c9-117">PARAMETERS</span></span>

### <span data-ttu-id="d58c9-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d58c9-118">-ApiVersion</span></span>
<span data-ttu-id="d58c9-119">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="d58c9-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="d58c9-120">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="d58c9-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="d58c9-121">-Force</span><span class="sxs-lookup"><span data-stu-id="d58c9-121">-Force</span></span>
<span data-ttu-id="d58c9-122">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d58c9-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d58c9-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d58c9-123">-InformationAction</span></span>
<span data-ttu-id="d58c9-124">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="d58c9-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d58c9-125">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d58c9-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d58c9-126">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="d58c9-126">Continue</span></span>
- <span data-ttu-id="d58c9-127">Ignorować</span><span class="sxs-lookup"><span data-stu-id="d58c9-127">Ignore</span></span>
- <span data-ttu-id="d58c9-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="d58c9-128">Inquire</span></span>
- <span data-ttu-id="d58c9-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d58c9-129">SilentlyContinue</span></span>
- <span data-ttu-id="d58c9-130">Przestaw</span><span class="sxs-lookup"><span data-stu-id="d58c9-130">Stop</span></span>
- <span data-ttu-id="d58c9-131">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="d58c9-131">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d58c9-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d58c9-132">-InformationVariable</span></span>
<span data-ttu-id="d58c9-133">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="d58c9-133">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d58c9-134">-LockId</span><span class="sxs-lookup"><span data-stu-id="d58c9-134">-LockId</span></span>
<span data-ttu-id="d58c9-135">Określa identyfikator blokady, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d58c9-135">Specifies the ID of the lock that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock, by Id.
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d58c9-136">-Kłódkaname</span><span class="sxs-lookup"><span data-stu-id="d58c9-136">-LockName</span></span>
<span data-ttu-id="d58c9-137">Określa nazwę blokady usuniętej przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d58c9-137">Specifies the name of the lock that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group scope., A lock at the resource group resource scope., A lock at the specified scope., A lock at the subscription scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d58c9-138">-Pre</span><span class="sxs-lookup"><span data-stu-id="d58c9-138">-Pre</span></span>
<span data-ttu-id="d58c9-139">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="d58c9-139">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="d58c9-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d58c9-140">-ResourceGroupName</span></span>
<span data-ttu-id="d58c9-141">Określa nazwę grupy zasobów, której dotyczy blokada.</span><span class="sxs-lookup"><span data-stu-id="d58c9-141">Specifies the name of the resource group for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group scope., A lock at the resource group resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d58c9-142">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="d58c9-142">-ResourceName</span></span>
<span data-ttu-id="d58c9-143">Określa nazwę zasobu, którego dotyczy blokada.</span><span class="sxs-lookup"><span data-stu-id="d58c9-143">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="d58c9-144">Aby na przykład określić bazę danych, użyj następującego formatu:</span><span class="sxs-lookup"><span data-stu-id="d58c9-144">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="d58c9-145">`/`Baza danych serwera</span><span class="sxs-lookup"><span data-stu-id="d58c9-145">Server`/`Database</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group resource scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d58c9-146">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="d58c9-146">-ResourceType</span></span>
<span data-ttu-id="d58c9-147">Określa typ zasobu zasobu, którego dotyczy blokada.</span><span class="sxs-lookup"><span data-stu-id="d58c9-147">Specifies the resource type of the resource for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group resource scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d58c9-148">-Zakres</span><span class="sxs-lookup"><span data-stu-id="d58c9-148">-Scope</span></span>
<span data-ttu-id="d58c9-149">Określa zakres, do którego jest stosowana blokada.</span><span class="sxs-lookup"><span data-stu-id="d58c9-149">Specifies the scope to which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the specified scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d58c9-150">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="d58c9-150">-TenantLevel</span></span>
<span data-ttu-id="d58c9-151">Wskazuje, że ten aplet polecenia działa na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="d58c9-151">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d58c9-152">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d58c9-152">-Confirm</span></span>
<span data-ttu-id="d58c9-153">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d58c9-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d58c9-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d58c9-154">-WhatIf</span></span>
<span data-ttu-id="d58c9-155">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d58c9-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d58c9-156">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d58c9-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d58c9-157">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d58c9-157">-DefaultProfile</span></span>
<span data-ttu-id="d58c9-158">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d58c9-158">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d58c9-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d58c9-159">CommonParameters</span></span>
<span data-ttu-id="d58c9-160">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d58c9-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d58c9-161">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d58c9-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d58c9-162">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d58c9-162">INPUTS</span></span>

## <span data-ttu-id="d58c9-163">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d58c9-163">OUTPUTS</span></span>

### <span data-ttu-id="d58c9-164">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="d58c9-164">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="d58c9-165">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d58c9-165">NOTES</span></span>

## <span data-ttu-id="d58c9-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d58c9-166">RELATED LINKS</span></span>

[<span data-ttu-id="d58c9-167">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="d58c9-167">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="d58c9-168">Nowe — AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="d58c9-168">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="d58c9-169">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="d58c9-169">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


