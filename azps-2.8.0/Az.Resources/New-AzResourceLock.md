---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResourceLock.md
ms.openlocfilehash: a0d796d49114cc11fcc50aef85a3ab502593dc35
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873335"
---
# <span data-ttu-id="fc9ef-101">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="fc9ef-101">New-AzResourceLock</span></span>

## <span data-ttu-id="fc9ef-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fc9ef-102">SYNOPSIS</span></span>
<span data-ttu-id="fc9ef-103">Tworzy blokadę zasobu.</span><span class="sxs-lookup"><span data-stu-id="fc9ef-103">Creates a resource lock.</span></span>

## <span data-ttu-id="fc9ef-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fc9ef-104">SYNTAX</span></span>

### <span data-ttu-id="fc9ef-105">BySpecifiedScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fc9ef-105">BySpecifiedScope (Default)</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -Scope <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fc9ef-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fc9ef-106">ByResourceGroup</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc9ef-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="fc9ef-107">ByResourceGroupLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc9ef-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="fc9ef-108">BySubscription</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fc9ef-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="fc9ef-109">BySubscriptionLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc9ef-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="fc9ef-110">ByTenantLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc9ef-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="fc9ef-111">ByLockId</span></span>
```
New-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fc9ef-112">Opis</span><span class="sxs-lookup"><span data-stu-id="fc9ef-112">DESCRIPTION</span></span>
<span data-ttu-id="fc9ef-113">Polecenie cmdlet **New-AzResourceLock** umożliwia utworzenie blokady zasobów.</span><span class="sxs-lookup"><span data-stu-id="fc9ef-113">The **New-AzResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="fc9ef-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fc9ef-114">EXAMPLES</span></span>

### <span data-ttu-id="fc9ef-115">Przykład 1. Tworzenie blokady zasobów w witrynie sieci Web</span><span class="sxs-lookup"><span data-stu-id="fc9ef-115">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="fc9ef-116">To polecenie tworzy blokadę zasobu w witrynie sieci Web.</span><span class="sxs-lookup"><span data-stu-id="fc9ef-116">This command creates a resource lock on a website.</span></span>

## <span data-ttu-id="fc9ef-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fc9ef-117">PARAMETERS</span></span>

### <span data-ttu-id="fc9ef-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="fc9ef-118">-ApiVersion</span></span>
<span data-ttu-id="fc9ef-119">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="fc9ef-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="fc9ef-120">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="fc9ef-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="fc9ef-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc9ef-121">-DefaultProfile</span></span>
<span data-ttu-id="fc9ef-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="fc9ef-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc9ef-123">-Force</span><span class="sxs-lookup"><span data-stu-id="fc9ef-123">-Force</span></span>
<span data-ttu-id="fc9ef-124">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="fc9ef-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fc9ef-125">-LockId</span><span class="sxs-lookup"><span data-stu-id="fc9ef-125">-LockId</span></span>
<span data-ttu-id="fc9ef-126">Określa identyfikator blokady.</span><span class="sxs-lookup"><span data-stu-id="fc9ef-126">Specifies the ID of the lock.</span></span>

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

### <span data-ttu-id="fc9ef-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="fc9ef-127">-LockLevel</span></span>
<span data-ttu-id="fc9ef-128">Określa poziom blokady.</span><span class="sxs-lookup"><span data-stu-id="fc9ef-128">Specifies the level for the lock.</span></span>
<span data-ttu-id="fc9ef-129">Obecnie prawidłowe wartości to CanNotDelete, ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="fc9ef-129">Currently, valid values are CanNotDelete, ReadOnly.</span></span>

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

### <span data-ttu-id="fc9ef-130">-Kłódkaname</span><span class="sxs-lookup"><span data-stu-id="fc9ef-130">-LockName</span></span>
<span data-ttu-id="fc9ef-131">Określa nazwę blokady.</span><span class="sxs-lookup"><span data-stu-id="fc9ef-131">Specifies the name of the lock.</span></span>

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

### <span data-ttu-id="fc9ef-132">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="fc9ef-132">-LockNotes</span></span>
<span data-ttu-id="fc9ef-133">Określa uwagi dotyczące blokady.</span><span class="sxs-lookup"><span data-stu-id="fc9ef-133">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="fc9ef-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="fc9ef-134">-Pre</span></span>
<span data-ttu-id="fc9ef-135">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="fc9ef-135">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="fc9ef-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc9ef-136">-ResourceGroupName</span></span>
<span data-ttu-id="fc9ef-137">Określa nazwę grupy zasobów, do której odnosi się blokada, lub zawierającej grupę zasobów, której dotyczy blokada.</span><span class="sxs-lookup"><span data-stu-id="fc9ef-137">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="fc9ef-138">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="fc9ef-138">-ResourceName</span></span>
<span data-ttu-id="fc9ef-139">Określa nazwę zasobu, którego dotyczy blokada.</span><span class="sxs-lookup"><span data-stu-id="fc9ef-139">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="fc9ef-140">Aby na przykład określić bazę danych, użyj następującego formatu: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="fc9ef-140">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="fc9ef-141">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="fc9ef-141">-ResourceType</span></span>
<span data-ttu-id="fc9ef-142">Określa typ zasobu zasobu, którego dotyczy blokada.</span><span class="sxs-lookup"><span data-stu-id="fc9ef-142">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="fc9ef-143">-Zakres</span><span class="sxs-lookup"><span data-stu-id="fc9ef-143">-Scope</span></span>
<span data-ttu-id="fc9ef-144">Określa zakres, do którego jest stosowana blokada.</span><span class="sxs-lookup"><span data-stu-id="fc9ef-144">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="fc9ef-145">Aby na przykład określić bazę danych, użyj następującego formatu: `/subscriptions/` Identyfikator subskrypcji nazwa `/resourceGroups/` grupy zasobów nazwa `/providers/Microsoft.Sql/servers/` `/databases/` bazy danych aby określić grupę zasobów, użyj następującego formatu: `/subscriptions/` `/resourceGroups/` Nazwa grupy zasobów identyfikator subskrypcji</span><span class="sxs-lookup"><span data-stu-id="fc9ef-145">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="fc9ef-146">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="fc9ef-146">-TenantLevel</span></span>
<span data-ttu-id="fc9ef-147">Wskazuje, że ten aplet polecenia działa na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="fc9ef-147">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="fc9ef-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fc9ef-148">-Confirm</span></span>
<span data-ttu-id="fc9ef-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc9ef-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc9ef-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc9ef-150">-WhatIf</span></span>
<span data-ttu-id="fc9ef-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc9ef-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc9ef-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fc9ef-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc9ef-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc9ef-153">CommonParameters</span></span>
<span data-ttu-id="fc9ef-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc9ef-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc9ef-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc9ef-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc9ef-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fc9ef-156">INPUTS</span></span>

### <span data-ttu-id="fc9ef-157">System. String</span><span class="sxs-lookup"><span data-stu-id="fc9ef-157">System.String</span></span>

### <span data-ttu-id="fc9ef-158">Microsoft. Azure. Commands. resourceName. cmdlets. Entities. blokady. LockLevel</span><span class="sxs-lookup"><span data-stu-id="fc9ef-158">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel</span></span>

## <span data-ttu-id="fc9ef-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fc9ef-159">OUTPUTS</span></span>

### <span data-ttu-id="fc9ef-160">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="fc9ef-160">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="fc9ef-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fc9ef-161">NOTES</span></span>

## <span data-ttu-id="fc9ef-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fc9ef-162">RELATED LINKS</span></span>

[<span data-ttu-id="fc9ef-163">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="fc9ef-163">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="fc9ef-164">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="fc9ef-164">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="fc9ef-165">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="fc9ef-165">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


