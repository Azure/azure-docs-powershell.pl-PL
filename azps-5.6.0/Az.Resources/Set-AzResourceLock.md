---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: https://docs.microsoft.com/powershell/module/az.resources/set-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
ms.openlocfilehash: a633718402f7c06e583030c379544ff45a216fb1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967649"
---
# <span data-ttu-id="766f1-101">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="766f1-101">Set-AzResourceLock</span></span>

## <span data-ttu-id="766f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="766f1-102">SYNOPSIS</span></span>
<span data-ttu-id="766f1-103">Modyfikuje blokadę zasobów.</span><span class="sxs-lookup"><span data-stu-id="766f1-103">Modifies a resource lock.</span></span>

## <span data-ttu-id="766f1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="766f1-104">SYNTAX</span></span>

### <span data-ttu-id="766f1-105">BySpecifiedScope (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="766f1-105">BySpecifiedScope (Default)</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="766f1-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="766f1-106">ByResourceGroup</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="766f1-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="766f1-107">ByResourceGroupLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="766f1-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="766f1-108">BySubscription</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="766f1-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="766f1-109">BySubscriptionLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="766f1-110">ByLockId</span><span class="sxs-lookup"><span data-stu-id="766f1-110">ByLockId</span></span>
```
Set-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="766f1-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="766f1-111">DESCRIPTION</span></span>
<span data-ttu-id="766f1-112">Polecenie cmdlet **Set-AzResourceLock** modyfikuje blokadę zasobów.</span><span class="sxs-lookup"><span data-stu-id="766f1-112">The **Set-AzResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="766f1-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="766f1-113">EXAMPLES</span></span>

### <span data-ttu-id="766f1-114">Przykład 1. Aktualizowanie notatek dla blokady</span><span class="sxs-lookup"><span data-stu-id="766f1-114">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="766f1-115">To polecenie aktualizuje notatkę dla blokady o nazwie ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="766f1-115">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="766f1-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="766f1-116">PARAMETERS</span></span>

### <span data-ttu-id="766f1-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="766f1-117">-ApiVersion</span></span>
<span data-ttu-id="766f1-118">Określa wersję interfejsu API dostawcy zasobów do użycia.</span><span class="sxs-lookup"><span data-stu-id="766f1-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="766f1-119">Jeśli nie określisz wersji, to polecenie cmdlet użyje najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="766f1-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="766f1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="766f1-120">-DefaultProfile</span></span>
<span data-ttu-id="766f1-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="766f1-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="766f1-122">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="766f1-122">-Force</span></span>
<span data-ttu-id="766f1-123">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="766f1-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="766f1-124">- LockId</span><span class="sxs-lookup"><span data-stu-id="766f1-124">-LockId</span></span>
<span data-ttu-id="766f1-125">Określa identyfikator blokady, która ma być zmieniana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="766f1-125">Specifies the ID of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="766f1-126">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="766f1-126">-LockLevel</span></span>
<span data-ttu-id="766f1-127">Określa poziom blokady.</span><span class="sxs-lookup"><span data-stu-id="766f1-127">Specifies the level for the lock.</span></span>
<span data-ttu-id="766f1-128">Obecnie jedyną prawidłową wartością jest CanNotDelete.</span><span class="sxs-lookup"><span data-stu-id="766f1-128">Currently, the only valid value is CanNotDelete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: CanNotDelete, ReadOnly

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="766f1-129">-LockName</span><span class="sxs-lookup"><span data-stu-id="766f1-129">-LockName</span></span>
<span data-ttu-id="766f1-130">Określa nazwę blokady, która ma być zmieniana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="766f1-130">Specifies the name of the lock that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope, ByResourceGroup, ByResourceGroupLevel, BySubscription, BySubscriptionLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="766f1-131">- LockNotes</span><span class="sxs-lookup"><span data-stu-id="766f1-131">-LockNotes</span></span>
<span data-ttu-id="766f1-132">Określa notatki blokady.</span><span class="sxs-lookup"><span data-stu-id="766f1-132">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="766f1-133">— Przed</span><span class="sxs-lookup"><span data-stu-id="766f1-133">-Pre</span></span>
<span data-ttu-id="766f1-134">Wskazuje, że to polecenie cmdlet uwzględnia wersje przedpremierowe interfejsu API, gdy automatycznie określa, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="766f1-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="766f1-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="766f1-135">-ResourceGroupName</span></span>
<span data-ttu-id="766f1-136">Określa nazwę grupy zasobów, której dotyczy blokada.</span><span class="sxs-lookup"><span data-stu-id="766f1-136">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="766f1-137">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="766f1-137">-ResourceName</span></span>
<span data-ttu-id="766f1-138">Określa nazwę zasobu, którego dotyczy blokada.</span><span class="sxs-lookup"><span data-stu-id="766f1-138">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="766f1-139">Aby na przykład określić bazę danych, użyj następującego formatu: Server `/` Database</span><span class="sxs-lookup"><span data-stu-id="766f1-139">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="766f1-140">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="766f1-140">-ResourceType</span></span>
<span data-ttu-id="766f1-141">Określa typ zasobu, którego dotyczy blokada.</span><span class="sxs-lookup"><span data-stu-id="766f1-141">Specifies the resource type for which the lock applies.</span></span>

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

### <span data-ttu-id="766f1-142">— Zakres</span><span class="sxs-lookup"><span data-stu-id="766f1-142">-Scope</span></span>
<span data-ttu-id="766f1-143">Określa zakres, do którego ma zastosowanie blokada.</span><span class="sxs-lookup"><span data-stu-id="766f1-143">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="766f1-144">Aby na przykład określić bazę danych, użyj następującego formatu: Nazwa bazy danych Nazwa bazy danych nazwa grupy nazw grupy zasobów w ramach identyfikatora subskrypcji. Aby określić grupę zasobów, użyj następującego formatu: nazwa grupy zasobów identyfikatora `/subscriptions/` `/resourceGroups/` `/providers/Microsoft.Sql/servers/` `/databases/` `/subscriptions/` `/resourceGroups/` subskrypcji</span><span class="sxs-lookup"><span data-stu-id="766f1-144">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="766f1-145">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="766f1-145">-Confirm</span></span>
<span data-ttu-id="766f1-146">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="766f1-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="766f1-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="766f1-147">-WhatIf</span></span>
<span data-ttu-id="766f1-148">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="766f1-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="766f1-149">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="766f1-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="766f1-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="766f1-150">CommonParameters</span></span>
<span data-ttu-id="766f1-151">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="766f1-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="766f1-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="766f1-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="766f1-153">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="766f1-153">INPUTS</span></span>

### <span data-ttu-id="766f1-154">System.String</span><span class="sxs-lookup"><span data-stu-id="766f1-154">System.String</span></span>

### <span data-ttu-id="766f1-155">Microsoft.Azure.Commands.ResourceManager.Cmdlet.Entities.Locks.LockLevel</span><span class="sxs-lookup"><span data-stu-id="766f1-155">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="766f1-156">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="766f1-156">OUTPUTS</span></span>

### <span data-ttu-id="766f1-157">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="766f1-157">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="766f1-158">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="766f1-158">NOTES</span></span>

## <span data-ttu-id="766f1-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="766f1-159">RELATED LINKS</span></span>

[<span data-ttu-id="766f1-160">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="766f1-160">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="766f1-161">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="766f1-161">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="766f1-162">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="766f1-162">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)


