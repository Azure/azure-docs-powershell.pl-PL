---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
ms.openlocfilehash: c532633de593294c6b5dbe0e09b9615a1d5355a3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351697"
---
# <span data-ttu-id="2a2cb-101">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="2a2cb-101">Set-AzResourceLock</span></span>

## <span data-ttu-id="2a2cb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2a2cb-102">SYNOPSIS</span></span>
<span data-ttu-id="2a2cb-103">Modyfikuje blokadę zasobu.</span><span class="sxs-lookup"><span data-stu-id="2a2cb-103">Modifies a resource lock.</span></span>

## <span data-ttu-id="2a2cb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2a2cb-104">SYNTAX</span></span>

### <span data-ttu-id="2a2cb-105">BySpecifiedScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2a2cb-105">BySpecifiedScope (Default)</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2a2cb-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2a2cb-106">ByResourceGroup</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a2cb-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="2a2cb-107">ByResourceGroupLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a2cb-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="2a2cb-108">BySubscription</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2a2cb-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="2a2cb-109">BySubscriptionLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a2cb-110">ByLockId</span><span class="sxs-lookup"><span data-stu-id="2a2cb-110">ByLockId</span></span>
```
Set-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2a2cb-111">Opis</span><span class="sxs-lookup"><span data-stu-id="2a2cb-111">DESCRIPTION</span></span>
<span data-ttu-id="2a2cb-112">Polecenie cmdlet **Set-AzResourceLock** modyfikuje blokadę zasobu.</span><span class="sxs-lookup"><span data-stu-id="2a2cb-112">The **Set-AzResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="2a2cb-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2a2cb-113">EXAMPLES</span></span>

### <span data-ttu-id="2a2cb-114">Przykład 1: aktualizowanie notatek w celu zablokowania</span><span class="sxs-lookup"><span data-stu-id="2a2cb-114">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="2a2cb-115">To polecenie aktualizuje notatkę dla blokady o nazwie ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="2a2cb-115">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="2a2cb-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2a2cb-116">PARAMETERS</span></span>

### <span data-ttu-id="2a2cb-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2a2cb-117">-ApiVersion</span></span>
<span data-ttu-id="2a2cb-118">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="2a2cb-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="2a2cb-119">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="2a2cb-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="2a2cb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a2cb-120">-DefaultProfile</span></span>
<span data-ttu-id="2a2cb-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="2a2cb-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2a2cb-122">-Force</span><span class="sxs-lookup"><span data-stu-id="2a2cb-122">-Force</span></span>
<span data-ttu-id="2a2cb-123">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="2a2cb-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2a2cb-124">-LockId</span><span class="sxs-lookup"><span data-stu-id="2a2cb-124">-LockId</span></span>
<span data-ttu-id="2a2cb-125">Określa identyfikator blokady modyfikowanej przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a2cb-125">Specifies the ID of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="2a2cb-126">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="2a2cb-126">-LockLevel</span></span>
<span data-ttu-id="2a2cb-127">Określa poziom blokady.</span><span class="sxs-lookup"><span data-stu-id="2a2cb-127">Specifies the level for the lock.</span></span>
<span data-ttu-id="2a2cb-128">Obecnie jedyną prawidłową wartością jest CanNotDelete.</span><span class="sxs-lookup"><span data-stu-id="2a2cb-128">Currently, the only valid value is CanNotDelete.</span></span>

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

### <span data-ttu-id="2a2cb-129">-Kłódkaname</span><span class="sxs-lookup"><span data-stu-id="2a2cb-129">-LockName</span></span>
<span data-ttu-id="2a2cb-130">Określa nazwę blokady modyfikowanej przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a2cb-130">Specifies the name of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="2a2cb-131">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="2a2cb-131">-LockNotes</span></span>
<span data-ttu-id="2a2cb-132">Określa uwagi dotyczące blokady.</span><span class="sxs-lookup"><span data-stu-id="2a2cb-132">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="2a2cb-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="2a2cb-133">-Pre</span></span>
<span data-ttu-id="2a2cb-134">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="2a2cb-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="2a2cb-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a2cb-135">-ResourceGroupName</span></span>
<span data-ttu-id="2a2cb-136">Określa nazwę grupy zasobów, której dotyczy blokada.</span><span class="sxs-lookup"><span data-stu-id="2a2cb-136">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="2a2cb-137">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="2a2cb-137">-ResourceName</span></span>
<span data-ttu-id="2a2cb-138">Określa nazwę zasobu, którego dotyczy blokada.</span><span class="sxs-lookup"><span data-stu-id="2a2cb-138">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="2a2cb-139">Aby na przykład określić bazę danych, użyj następującego formatu: `/` baza danych serwera</span><span class="sxs-lookup"><span data-stu-id="2a2cb-139">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="2a2cb-140">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="2a2cb-140">-ResourceType</span></span>
<span data-ttu-id="2a2cb-141">Określa typ zasobu, którego dotyczy blokada.</span><span class="sxs-lookup"><span data-stu-id="2a2cb-141">Specifies the resource type for which the lock applies.</span></span>

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

### <span data-ttu-id="2a2cb-142">-Zakres</span><span class="sxs-lookup"><span data-stu-id="2a2cb-142">-Scope</span></span>
<span data-ttu-id="2a2cb-143">Określa zakres, do którego jest stosowana blokada.</span><span class="sxs-lookup"><span data-stu-id="2a2cb-143">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="2a2cb-144">Aby na przykład określić bazę danych, użyj następującego formatu: `/subscriptions/` Identyfikator subskrypcji nazwa `/resourceGroups/` grupy zasobów nazwa `/providers/Microsoft.Sql/servers/` `/databases/` bazy danych aby określić grupę zasobów, użyj następującego formatu: `/subscriptions/` `/resourceGroups/` Nazwa grupy zasobów identyfikator subskrypcji</span><span class="sxs-lookup"><span data-stu-id="2a2cb-144">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="2a2cb-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2a2cb-145">-Confirm</span></span>
<span data-ttu-id="2a2cb-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a2cb-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a2cb-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a2cb-147">-WhatIf</span></span>
<span data-ttu-id="2a2cb-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a2cb-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a2cb-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2a2cb-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a2cb-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a2cb-150">CommonParameters</span></span>
<span data-ttu-id="2a2cb-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a2cb-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a2cb-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a2cb-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a2cb-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a2cb-153">INPUTS</span></span>

### <span data-ttu-id="2a2cb-154">System. String</span><span class="sxs-lookup"><span data-stu-id="2a2cb-154">System.String</span></span>

### <span data-ttu-id="2a2cb-155">Microsoft. Azure. Commands. resourceName. cmdlets. Entities. blokady. LockLevel</span><span class="sxs-lookup"><span data-stu-id="2a2cb-155">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="2a2cb-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2a2cb-156">OUTPUTS</span></span>

### <span data-ttu-id="2a2cb-157">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="2a2cb-157">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="2a2cb-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2a2cb-158">NOTES</span></span>

## <span data-ttu-id="2a2cb-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2a2cb-159">RELATED LINKS</span></span>

[<span data-ttu-id="2a2cb-160">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="2a2cb-160">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="2a2cb-161">Nowe — AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="2a2cb-161">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="2a2cb-162">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="2a2cb-162">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)


