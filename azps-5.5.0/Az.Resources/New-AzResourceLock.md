---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceLock.md
ms.openlocfilehash: 7f21704783a9992cc0d1b0fdf3da50cb21656b0e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198746"
---
# <span data-ttu-id="f98f9-101">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="f98f9-101">New-AzResourceLock</span></span>

## <span data-ttu-id="f98f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f98f9-102">SYNOPSIS</span></span>
<span data-ttu-id="f98f9-103">Tworzy blokadę zasobu.</span><span class="sxs-lookup"><span data-stu-id="f98f9-103">Creates a resource lock.</span></span>

## <span data-ttu-id="f98f9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f98f9-104">SYNTAX</span></span>

### <span data-ttu-id="f98f9-105">BySpecifiedScope (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="f98f9-105">BySpecifiedScope (Default)</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f98f9-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f98f9-106">ByResourceGroup</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f98f9-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="f98f9-107">ByResourceGroupLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f98f9-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="f98f9-108">BySubscription</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f98f9-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="f98f9-109">BySubscriptionLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f98f9-110">ByLockId</span><span class="sxs-lookup"><span data-stu-id="f98f9-110">ByLockId</span></span>
```
New-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f98f9-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="f98f9-111">DESCRIPTION</span></span>
<span data-ttu-id="f98f9-112">Polecenie **cmdlet New-AzResourceLock** tworzy blokadę zasobów.</span><span class="sxs-lookup"><span data-stu-id="f98f9-112">The **New-AzResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="f98f9-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f98f9-113">EXAMPLES</span></span>

### <span data-ttu-id="f98f9-114">Przykład 1. Tworzenie blokady zasobów w witrynie sieci Web</span><span class="sxs-lookup"><span data-stu-id="f98f9-114">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="f98f9-115">To polecenie tworzy blokadę zasobów w witrynie sieci Web.</span><span class="sxs-lookup"><span data-stu-id="f98f9-115">This command creates a resource lock on a website.</span></span>

### <span data-ttu-id="f98f9-116">Przykład 2. Tworzenie blokady zasobów w bazie danych</span><span class="sxs-lookup"><span data-stu-id="f98f9-116">Example 2: Create a resource lock on a database</span></span>
```
PS C:\>New-AzResourceLock -LockLevel CanNotDelete -LockNotes "Lock note" -LockName "db-lock" -ResourceName "server1/ContosoDB"  -ResourceGroupName "RG1" -ResourceType "Microsoft.Sql/servers/databases"
```

<span data-ttu-id="f98f9-117">To polecenie tworzy blokadę zasobów w bazie danych Azure.</span><span class="sxs-lookup"><span data-stu-id="f98f9-117">This command creates a resource lock on a Azure database.</span></span>

## <span data-ttu-id="f98f9-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f98f9-118">PARAMETERS</span></span>

### <span data-ttu-id="f98f9-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f98f9-119">-ApiVersion</span></span>
<span data-ttu-id="f98f9-120">Określa wersję interfejsu API dostawcy zasobów do użycia.</span><span class="sxs-lookup"><span data-stu-id="f98f9-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="f98f9-121">Jeśli nie określisz wersji, to polecenie cmdlet użyje najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="f98f9-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="f98f9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f98f9-122">-DefaultProfile</span></span>
<span data-ttu-id="f98f9-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="f98f9-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f98f9-124">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="f98f9-124">-Force</span></span>
<span data-ttu-id="f98f9-125">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f98f9-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f98f9-126">- LockId</span><span class="sxs-lookup"><span data-stu-id="f98f9-126">-LockId</span></span>
<span data-ttu-id="f98f9-127">Określa identyfikator blokady.</span><span class="sxs-lookup"><span data-stu-id="f98f9-127">Specifies the ID of the lock.</span></span>

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

### <span data-ttu-id="f98f9-128">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="f98f9-128">-LockLevel</span></span>
<span data-ttu-id="f98f9-129">Określa poziom blokady.</span><span class="sxs-lookup"><span data-stu-id="f98f9-129">Specifies the level for the lock.</span></span>
<span data-ttu-id="f98f9-130">Obecnie prawidłowe wartości to CanNotDelete, ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="f98f9-130">Currently, valid values are CanNotDelete, ReadOnly.</span></span>

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

### <span data-ttu-id="f98f9-131">-LockName</span><span class="sxs-lookup"><span data-stu-id="f98f9-131">-LockName</span></span>
<span data-ttu-id="f98f9-132">Określa nazwę kłódki.</span><span class="sxs-lookup"><span data-stu-id="f98f9-132">Specifies the name of the lock.</span></span>

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

### <span data-ttu-id="f98f9-133">- LockNotes</span><span class="sxs-lookup"><span data-stu-id="f98f9-133">-LockNotes</span></span>
<span data-ttu-id="f98f9-134">Określa uwagi dotyczące kłódki.</span><span class="sxs-lookup"><span data-stu-id="f98f9-134">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="f98f9-135">— Przed</span><span class="sxs-lookup"><span data-stu-id="f98f9-135">-Pre</span></span>
<span data-ttu-id="f98f9-136">Wskazuje, że to polecenie cmdlet uwzględnia wersje przedpremierowe interfejsu API, gdy automatycznie określa, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="f98f9-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f98f9-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f98f9-137">-ResourceGroupName</span></span>
<span data-ttu-id="f98f9-138">Określa nazwę grupy zasobów, do której ma zastosowanie blokada, lub zawierającej grupę zasobów, do której ma zastosowanie blokada.</span><span class="sxs-lookup"><span data-stu-id="f98f9-138">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="f98f9-139">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f98f9-139">-ResourceName</span></span>
<span data-ttu-id="f98f9-140">Określa nazwę zasobu, którego dotyczy blokada.</span><span class="sxs-lookup"><span data-stu-id="f98f9-140">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="f98f9-141">Aby na przykład określić bazę danych, użyj następującego formatu: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="f98f9-141">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="f98f9-142">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="f98f9-142">-ResourceType</span></span>
<span data-ttu-id="f98f9-143">Określa typ zasobu, którego kłódka ma zastosowanie.</span><span class="sxs-lookup"><span data-stu-id="f98f9-143">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="f98f9-144">— Zakres</span><span class="sxs-lookup"><span data-stu-id="f98f9-144">-Scope</span></span>
<span data-ttu-id="f98f9-145">Określa zakres, do którego ma zastosowanie blokada.</span><span class="sxs-lookup"><span data-stu-id="f98f9-145">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="f98f9-146">Aby na przykład określić bazę danych, użyj następującego formatu: Nazwa bazy danych Nazwa bazy danych nazwa grupy nazw grupy zasobów w ramach identyfikatora subskrypcji. Aby określić grupę zasobów, użyj następującego formatu: nazwa grupy zasobów identyfikatora `/subscriptions/` `/resourceGroups/` `/providers/Microsoft.Sql/servers/` `/databases/` `/subscriptions/` `/resourceGroups/` subskrypcji</span><span class="sxs-lookup"><span data-stu-id="f98f9-146">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="f98f9-147">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f98f9-147">-Confirm</span></span>
<span data-ttu-id="f98f9-148">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f98f9-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f98f9-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f98f9-149">-WhatIf</span></span>
<span data-ttu-id="f98f9-150">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f98f9-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f98f9-151">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f98f9-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f98f9-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f98f9-152">CommonParameters</span></span>
<span data-ttu-id="f98f9-153">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f98f9-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f98f9-154">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f98f9-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f98f9-155">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f98f9-155">INPUTS</span></span>

### <span data-ttu-id="f98f9-156">System.String</span><span class="sxs-lookup"><span data-stu-id="f98f9-156">System.String</span></span>

### <span data-ttu-id="f98f9-157">Microsoft.Azure.Commands.ResourceManager.Cmdlet.Entities.Locks.LockLevel</span><span class="sxs-lookup"><span data-stu-id="f98f9-157">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="f98f9-158">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f98f9-158">OUTPUTS</span></span>

### <span data-ttu-id="f98f9-159">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="f98f9-159">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f98f9-160">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f98f9-160">NOTES</span></span>

## <span data-ttu-id="f98f9-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f98f9-161">RELATED LINKS</span></span>

[<span data-ttu-id="f98f9-162">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="f98f9-162">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="f98f9-163">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="f98f9-163">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="f98f9-164">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="f98f9-164">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


