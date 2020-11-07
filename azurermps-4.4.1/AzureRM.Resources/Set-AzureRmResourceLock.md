---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResourceLock.md
ms.openlocfilehash: 73d82366cc0120e057d0c083e7f6da0b3cdebb76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718093"
---
# <span data-ttu-id="edc7f-101">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="edc7f-101">Set-AzureRmResourceLock</span></span>

## <span data-ttu-id="edc7f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="edc7f-102">SYNOPSIS</span></span>
<span data-ttu-id="edc7f-103">Modyfikuje blokadę zasobu.</span><span class="sxs-lookup"><span data-stu-id="edc7f-103">Modifies a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="edc7f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="edc7f-104">SYNTAX</span></span>

### <span data-ttu-id="edc7f-105">Blokada w określonym zakresie.</span><span class="sxs-lookup"><span data-stu-id="edc7f-105">A lock at the specified scope.</span></span> <span data-ttu-id="edc7f-106">Domyślne</span><span class="sxs-lookup"><span data-stu-id="edc7f-106">(Default)</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="edc7f-107">Blokada zakresu grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="edc7f-107">A lock at the resource group scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="edc7f-108">Blokada zakresu zasobów grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="edc7f-108">A lock at the resource group resource scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edc7f-109">Blokada zakresu subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="edc7f-109">A lock at the subscription scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="edc7f-110">Blokada w zakresie zasobów subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="edc7f-110">A lock at the subscription resource scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edc7f-111">Blokada w zakresie zasobów dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="edc7f-111">A lock at the tenant resource scope.</span></span>
```
Set-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edc7f-112">Blokada za pomocą identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="edc7f-112">A lock, by Id.</span></span>
```
Set-AzureRmResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="edc7f-113">Opis</span><span class="sxs-lookup"><span data-stu-id="edc7f-113">DESCRIPTION</span></span>
<span data-ttu-id="edc7f-114">Polecenie cmdlet **Set-AzureRmResourceLock** modyfikuje blokadę zasobu.</span><span class="sxs-lookup"><span data-stu-id="edc7f-114">The **Set-AzureRmResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="edc7f-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="edc7f-115">EXAMPLES</span></span>

### <span data-ttu-id="edc7f-116">Przykład 1: aktualizowanie notatek w celu zablokowania</span><span class="sxs-lookup"><span data-stu-id="edc7f-116">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzureRmResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="edc7f-117">To polecenie aktualizuje notatkę dla blokady o nazwie ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="edc7f-117">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="edc7f-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="edc7f-118">PARAMETERS</span></span>

### <span data-ttu-id="edc7f-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="edc7f-119">-ApiVersion</span></span>
<span data-ttu-id="edc7f-120">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="edc7f-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="edc7f-121">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="edc7f-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="edc7f-122">-Force</span><span class="sxs-lookup"><span data-stu-id="edc7f-122">-Force</span></span>
<span data-ttu-id="edc7f-123">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="edc7f-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="edc7f-124">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="edc7f-124">-InformationAction</span></span>
<span data-ttu-id="edc7f-125">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="edc7f-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="edc7f-126">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="edc7f-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="edc7f-127">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="edc7f-127">Continue</span></span>
- <span data-ttu-id="edc7f-128">Ignorować</span><span class="sxs-lookup"><span data-stu-id="edc7f-128">Ignore</span></span>
- <span data-ttu-id="edc7f-129">Inquire</span><span class="sxs-lookup"><span data-stu-id="edc7f-129">Inquire</span></span>
- <span data-ttu-id="edc7f-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="edc7f-130">SilentlyContinue</span></span>
- <span data-ttu-id="edc7f-131">Przestaw</span><span class="sxs-lookup"><span data-stu-id="edc7f-131">Stop</span></span>
- <span data-ttu-id="edc7f-132">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="edc7f-132">Suspend</span></span>

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

### <span data-ttu-id="edc7f-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="edc7f-133">-InformationVariable</span></span>
<span data-ttu-id="edc7f-134">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="edc7f-134">Specifies an information variable.</span></span>

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

### <span data-ttu-id="edc7f-135">-LockId</span><span class="sxs-lookup"><span data-stu-id="edc7f-135">-LockId</span></span>
<span data-ttu-id="edc7f-136">Określa identyfikator blokady modyfikowanej przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edc7f-136">Specifies the ID of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="edc7f-137">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="edc7f-137">-LockLevel</span></span>
<span data-ttu-id="edc7f-138">Określa poziom blokady.</span><span class="sxs-lookup"><span data-stu-id="edc7f-138">Specifies the level for the lock.</span></span>
<span data-ttu-id="edc7f-139">Obecnie jedyną prawidłową wartością jest CanNotDelete.</span><span class="sxs-lookup"><span data-stu-id="edc7f-139">Currently, the only valid value is CanNotDelete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel
Parameter Sets: (All)
Aliases: Level

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edc7f-140">-Kłódkaname</span><span class="sxs-lookup"><span data-stu-id="edc7f-140">-LockName</span></span>
<span data-ttu-id="edc7f-141">Określa nazwę blokady modyfikowanej przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edc7f-141">Specifies the name of the lock that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the specified scope., A lock at the resource group scope., A lock at the resource group resource scope., A lock at the subscription scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edc7f-142">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="edc7f-142">-LockNotes</span></span>
<span data-ttu-id="edc7f-143">Określa uwagi dotyczące blokady.</span><span class="sxs-lookup"><span data-stu-id="edc7f-143">Specifies the notes for the lock.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Notes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edc7f-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="edc7f-144">-Pre</span></span>
<span data-ttu-id="edc7f-145">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="edc7f-145">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="edc7f-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edc7f-146">-ResourceGroupName</span></span>
<span data-ttu-id="edc7f-147">Określa nazwę grupy zasobów, której dotyczy blokada.</span><span class="sxs-lookup"><span data-stu-id="edc7f-147">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="edc7f-148">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="edc7f-148">-ResourceName</span></span>
<span data-ttu-id="edc7f-149">Określa nazwę zasobu, którego dotyczy blokada.</span><span class="sxs-lookup"><span data-stu-id="edc7f-149">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="edc7f-150">Aby na przykład określić bazę danych, użyj następującego formatu:</span><span class="sxs-lookup"><span data-stu-id="edc7f-150">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="edc7f-151">`/`Baza danych serwera</span><span class="sxs-lookup"><span data-stu-id="edc7f-151">Server`/`Database</span></span>

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

### <span data-ttu-id="edc7f-152">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="edc7f-152">-ResourceType</span></span>
<span data-ttu-id="edc7f-153">Określa typ zasobu, którego dotyczy blokada.</span><span class="sxs-lookup"><span data-stu-id="edc7f-153">Specifies the resource type for which the lock applies.</span></span>

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

### <span data-ttu-id="edc7f-154">-Zakres</span><span class="sxs-lookup"><span data-stu-id="edc7f-154">-Scope</span></span>
<span data-ttu-id="edc7f-155">Określa zakres, do którego jest stosowana blokada.</span><span class="sxs-lookup"><span data-stu-id="edc7f-155">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="edc7f-156">Aby na przykład określić bazę danych, użyj następującego formatu:</span><span class="sxs-lookup"><span data-stu-id="edc7f-156">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="edc7f-157">`/subscriptions/`Identyfikator subskrypcji nazwa `/resourceGroups/` grupy zasobów nazwa `/providers/Microsoft.Sql/servers/` serwera nazwa `/databases/` bazy danych</span><span class="sxs-lookup"><span data-stu-id="edc7f-157">`/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name</span></span>

<span data-ttu-id="edc7f-158">Aby określić grupę zasobów, użyj następującego formatu:</span><span class="sxs-lookup"><span data-stu-id="edc7f-158">To specify a resource group, use the following format:</span></span> 

<span data-ttu-id="edc7f-159">`/subscriptions/``/resourceGroups/`Nazwa grupy zasobów identyfikatora subskrypcji</span><span class="sxs-lookup"><span data-stu-id="edc7f-159">`/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="edc7f-160">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="edc7f-160">-TenantLevel</span></span>
<span data-ttu-id="edc7f-161">Wskazuje, że ten aplet polecenia działa na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="edc7f-161">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="edc7f-162">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="edc7f-162">-Confirm</span></span>
<span data-ttu-id="edc7f-163">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edc7f-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edc7f-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edc7f-164">-WhatIf</span></span>
<span data-ttu-id="edc7f-165">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edc7f-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edc7f-166">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="edc7f-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edc7f-167">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edc7f-167">-DefaultProfile</span></span>
<span data-ttu-id="edc7f-168">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="edc7f-168">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="edc7f-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edc7f-169">CommonParameters</span></span>
<span data-ttu-id="edc7f-170">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edc7f-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edc7f-171">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edc7f-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edc7f-172">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="edc7f-172">INPUTS</span></span>

## <span data-ttu-id="edc7f-173">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="edc7f-173">OUTPUTS</span></span>

### <span data-ttu-id="edc7f-174">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="edc7f-174">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="edc7f-175">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="edc7f-175">NOTES</span></span>

## <span data-ttu-id="edc7f-176">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="edc7f-176">RELATED LINKS</span></span>

[<span data-ttu-id="edc7f-177">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="edc7f-177">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="edc7f-178">Nowe — AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="edc7f-178">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="edc7f-179">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="edc7f-179">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)


