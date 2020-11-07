---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 770093CD-CE2A-4076-8A28-F4DCFFB7A075
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceLock.md
ms.openlocfilehash: f1220db034a2cdcc81ffbd7a146fee8e2c7201be
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708273"
---
# <span data-ttu-id="5d4fd-101">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="5d4fd-101">Set-AzResourceLock</span></span>

## <span data-ttu-id="5d4fd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5d4fd-102">SYNOPSIS</span></span>
<span data-ttu-id="5d4fd-103">Modyfikuje blokadę zasobu.</span><span class="sxs-lookup"><span data-stu-id="5d4fd-103">Modifies a resource lock.</span></span>

## <span data-ttu-id="5d4fd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5d4fd-104">SYNTAX</span></span>

### <span data-ttu-id="5d4fd-105">BySpecifiedScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5d4fd-105">BySpecifiedScope (Default)</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5d4fd-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5d4fd-106">ByResourceGroup</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d4fd-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="5d4fd-107">ByResourceGroupLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d4fd-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="5d4fd-108">BySubscription</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5d4fd-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="5d4fd-109">BySubscriptionLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d4fd-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="5d4fd-110">ByTenantLevel</span></span>
```
Set-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d4fd-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="5d4fd-111">ByLockId</span></span>
```
Set-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5d4fd-112">Opis</span><span class="sxs-lookup"><span data-stu-id="5d4fd-112">DESCRIPTION</span></span>
<span data-ttu-id="5d4fd-113">Polecenie cmdlet **Set-AzResourceLock** modyfikuje blokadę zasobu.</span><span class="sxs-lookup"><span data-stu-id="5d4fd-113">The **Set-AzResourceLock** cmdlet modifies a resource lock.</span></span>

## <span data-ttu-id="5d4fd-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5d4fd-114">EXAMPLES</span></span>

### <span data-ttu-id="5d4fd-115">Przykład 1: aktualizowanie notatek w celu zablokowania</span><span class="sxs-lookup"><span data-stu-id="5d4fd-115">Example 1: Update notes for a lock</span></span>
```
PS C:\>Set-AzResourceLock -LockLevel CanNotDelete -LockNotes "Updated note" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="5d4fd-116">To polecenie aktualizuje notatkę dla blokady o nazwie ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="5d4fd-116">This command updates the note for a lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="5d4fd-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5d4fd-117">PARAMETERS</span></span>

### <span data-ttu-id="5d4fd-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5d4fd-118">-ApiVersion</span></span>
<span data-ttu-id="5d4fd-119">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="5d4fd-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="5d4fd-120">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="5d4fd-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="5d4fd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d4fd-121">-DefaultProfile</span></span>
<span data-ttu-id="5d4fd-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5d4fd-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d4fd-123">-Force</span><span class="sxs-lookup"><span data-stu-id="5d4fd-123">-Force</span></span>
<span data-ttu-id="5d4fd-124">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="5d4fd-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5d4fd-125">-LockId</span><span class="sxs-lookup"><span data-stu-id="5d4fd-125">-LockId</span></span>
<span data-ttu-id="5d4fd-126">Określa identyfikator blokady modyfikowanej przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d4fd-126">Specifies the ID of the lock that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="5d4fd-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="5d4fd-127">-LockLevel</span></span>
<span data-ttu-id="5d4fd-128">Określa poziom blokady.</span><span class="sxs-lookup"><span data-stu-id="5d4fd-128">Specifies the level for the lock.</span></span>
<span data-ttu-id="5d4fd-129">Obecnie jedyną prawidłową wartością jest CanNotDelete.</span><span class="sxs-lookup"><span data-stu-id="5d4fd-129">Currently, the only valid value is CanNotDelete.</span></span>

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

### <span data-ttu-id="5d4fd-130">-Kłódkaname</span><span class="sxs-lookup"><span data-stu-id="5d4fd-130">-LockName</span></span>
<span data-ttu-id="5d4fd-131">Określa nazwę blokady modyfikowanej przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d4fd-131">Specifies the name of the lock that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope, ByResourceGroup, ByResourceGroupLevel, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d4fd-132">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="5d4fd-132">-LockNotes</span></span>
<span data-ttu-id="5d4fd-133">Określa uwagi dotyczące blokady.</span><span class="sxs-lookup"><span data-stu-id="5d4fd-133">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="5d4fd-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="5d4fd-134">-Pre</span></span>
<span data-ttu-id="5d4fd-135">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="5d4fd-135">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="5d4fd-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d4fd-136">-ResourceGroupName</span></span>
<span data-ttu-id="5d4fd-137">Określa nazwę grupy zasobów, której dotyczy blokada.</span><span class="sxs-lookup"><span data-stu-id="5d4fd-137">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="5d4fd-138">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="5d4fd-138">-ResourceName</span></span>
<span data-ttu-id="5d4fd-139">Określa nazwę zasobu, którego dotyczy blokada.</span><span class="sxs-lookup"><span data-stu-id="5d4fd-139">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="5d4fd-140">Aby na przykład określić bazę danych, użyj następującego formatu: `/` baza danych serwera</span><span class="sxs-lookup"><span data-stu-id="5d4fd-140">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="5d4fd-141">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="5d4fd-141">-ResourceType</span></span>
<span data-ttu-id="5d4fd-142">Określa typ zasobu, którego dotyczy blokada.</span><span class="sxs-lookup"><span data-stu-id="5d4fd-142">Specifies the resource type for which the lock applies.</span></span>

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

### <span data-ttu-id="5d4fd-143">-Zakres</span><span class="sxs-lookup"><span data-stu-id="5d4fd-143">-Scope</span></span>
<span data-ttu-id="5d4fd-144">Określa zakres, do którego jest stosowana blokada.</span><span class="sxs-lookup"><span data-stu-id="5d4fd-144">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="5d4fd-145">Aby na przykład określić bazę danych, użyj następującego formatu: `/subscriptions/` Identyfikator subskrypcji nazwa `/resourceGroups/` grupy zasobów nazwa `/providers/Microsoft.Sql/servers/` `/databases/` bazy danych aby określić grupę zasobów, użyj następującego formatu: `/subscriptions/` `/resourceGroups/` Nazwa grupy zasobów identyfikator subskrypcji</span><span class="sxs-lookup"><span data-stu-id="5d4fd-145">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="5d4fd-146">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="5d4fd-146">-TenantLevel</span></span>
<span data-ttu-id="5d4fd-147">Wskazuje, że ten aplet polecenia działa na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="5d4fd-147">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="5d4fd-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5d4fd-148">-Confirm</span></span>
<span data-ttu-id="5d4fd-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d4fd-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d4fd-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d4fd-150">-WhatIf</span></span>
<span data-ttu-id="5d4fd-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d4fd-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d4fd-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5d4fd-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d4fd-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d4fd-153">CommonParameters</span></span>
<span data-ttu-id="5d4fd-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d4fd-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d4fd-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d4fd-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d4fd-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5d4fd-156">INPUTS</span></span>

### <span data-ttu-id="5d4fd-157">System. String</span><span class="sxs-lookup"><span data-stu-id="5d4fd-157">System.String</span></span>

### <span data-ttu-id="5d4fd-158">Microsoft. Azure. Commands. resourceName. cmdlets. Entities. blokady. LockLevel</span><span class="sxs-lookup"><span data-stu-id="5d4fd-158">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="5d4fd-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5d4fd-159">OUTPUTS</span></span>

### <span data-ttu-id="5d4fd-160">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="5d4fd-160">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="5d4fd-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5d4fd-161">NOTES</span></span>

## <span data-ttu-id="5d4fd-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5d4fd-162">RELATED LINKS</span></span>

[<span data-ttu-id="5d4fd-163">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="5d4fd-163">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="5d4fd-164">Nowe — AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="5d4fd-164">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="5d4fd-165">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="5d4fd-165">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)


