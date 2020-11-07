---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresourcelock
schema: 2.0.0
ms.openlocfilehash: 8556f71263aefe721225906aa1480c4f0bc19f7c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899042"
---
# <span data-ttu-id="60a62-101">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="60a62-101">New-AzureRmResourceLock</span></span>

## <span data-ttu-id="60a62-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="60a62-102">SYNOPSIS</span></span>
<span data-ttu-id="60a62-103">Tworzy blokadę zasobu.</span><span class="sxs-lookup"><span data-stu-id="60a62-103">Creates a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60a62-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="60a62-104">SYNTAX</span></span>

### <span data-ttu-id="60a62-105">BySpecifiedScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="60a62-105">BySpecifiedScope (Default)</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="60a62-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="60a62-106">ByResourceGroup</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="60a62-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="60a62-107">ByResourceGroupLevel</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60a62-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="60a62-108">BySubscription</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="60a62-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="60a62-109">BySubscriptionLevel</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60a62-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="60a62-110">ByTenantLevel</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60a62-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="60a62-111">ByLockId</span></span>
```
New-AzureRmResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="60a62-112">Opis</span><span class="sxs-lookup"><span data-stu-id="60a62-112">DESCRIPTION</span></span>
<span data-ttu-id="60a62-113">Polecenie cmdlet **New-AzureRmResourceLock** umożliwia utworzenie blokady zasobów.</span><span class="sxs-lookup"><span data-stu-id="60a62-113">The **New-AzureRmResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="60a62-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="60a62-114">EXAMPLES</span></span>

### <span data-ttu-id="60a62-115">Przykład 1. Tworzenie blokady zasobów w witrynie sieci Web</span><span class="sxs-lookup"><span data-stu-id="60a62-115">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzureRmResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="60a62-116">To polecenie tworzy blokadę zasobu w witrynie sieci Web.</span><span class="sxs-lookup"><span data-stu-id="60a62-116">This command creates a resource lock on a website.</span></span>

## <span data-ttu-id="60a62-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="60a62-117">PARAMETERS</span></span>

### <span data-ttu-id="60a62-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="60a62-118">-ApiVersion</span></span>
<span data-ttu-id="60a62-119">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="60a62-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="60a62-120">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="60a62-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="60a62-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60a62-121">-DefaultProfile</span></span>
<span data-ttu-id="60a62-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="60a62-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60a62-123">-Force</span><span class="sxs-lookup"><span data-stu-id="60a62-123">-Force</span></span>
<span data-ttu-id="60a62-124">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="60a62-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="60a62-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="60a62-125">-InformationAction</span></span>
<span data-ttu-id="60a62-126">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="60a62-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="60a62-127">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="60a62-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="60a62-128">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="60a62-128">Continue</span></span>
- <span data-ttu-id="60a62-129">Ignorować</span><span class="sxs-lookup"><span data-stu-id="60a62-129">Ignore</span></span>
- <span data-ttu-id="60a62-130">Inquire</span><span class="sxs-lookup"><span data-stu-id="60a62-130">Inquire</span></span>
- <span data-ttu-id="60a62-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="60a62-131">SilentlyContinue</span></span>
- <span data-ttu-id="60a62-132">Przestaw</span><span class="sxs-lookup"><span data-stu-id="60a62-132">Stop</span></span>
- <span data-ttu-id="60a62-133">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="60a62-133">Suspend</span></span>

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

### <span data-ttu-id="60a62-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="60a62-134">-InformationVariable</span></span>
<span data-ttu-id="60a62-135">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="60a62-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="60a62-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="60a62-136">-LockId</span></span>
<span data-ttu-id="60a62-137">Określa identyfikator blokady.</span><span class="sxs-lookup"><span data-stu-id="60a62-137">Specifies the ID of the lock.</span></span>

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

### <span data-ttu-id="60a62-138">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="60a62-138">-LockLevel</span></span>
<span data-ttu-id="60a62-139">Określa poziom blokady.</span><span class="sxs-lookup"><span data-stu-id="60a62-139">Specifies the level for the lock.</span></span>
<span data-ttu-id="60a62-140">Obecnie prawidłowe wartości to CanNotDelete, ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="60a62-140">Currently, valid values are CanNotDelete, ReadOnly.</span></span>

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

### <span data-ttu-id="60a62-141">-Kłódkaname</span><span class="sxs-lookup"><span data-stu-id="60a62-141">-LockName</span></span>
<span data-ttu-id="60a62-142">Określa nazwę blokady.</span><span class="sxs-lookup"><span data-stu-id="60a62-142">Specifies the name of the lock.</span></span>

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

### <span data-ttu-id="60a62-143">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="60a62-143">-LockNotes</span></span>
<span data-ttu-id="60a62-144">Określa uwagi dotyczące blokady.</span><span class="sxs-lookup"><span data-stu-id="60a62-144">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="60a62-145">-Pre</span><span class="sxs-lookup"><span data-stu-id="60a62-145">-Pre</span></span>
<span data-ttu-id="60a62-146">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="60a62-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="60a62-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60a62-147">-ResourceGroupName</span></span>
<span data-ttu-id="60a62-148">Określa nazwę grupy zasobów, do której odnosi się blokada, lub zawierającej grupę zasobów, której dotyczy blokada.</span><span class="sxs-lookup"><span data-stu-id="60a62-148">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="60a62-149">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="60a62-149">-ResourceName</span></span>
<span data-ttu-id="60a62-150">Określa nazwę zasobu, którego dotyczy blokada.</span><span class="sxs-lookup"><span data-stu-id="60a62-150">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="60a62-151">Aby na przykład określić bazę danych, użyj następującego formatu: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="60a62-151">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="60a62-152">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="60a62-152">-ResourceType</span></span>
<span data-ttu-id="60a62-153">Określa typ zasobu zasobu, którego dotyczy blokada.</span><span class="sxs-lookup"><span data-stu-id="60a62-153">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="60a62-154">-Zakres</span><span class="sxs-lookup"><span data-stu-id="60a62-154">-Scope</span></span>
<span data-ttu-id="60a62-155">Określa zakres, do którego jest stosowana blokada.</span><span class="sxs-lookup"><span data-stu-id="60a62-155">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="60a62-156">Aby na przykład określić bazę danych, użyj następującego formatu: `/subscriptions/` Identyfikator subskrypcji nazwa `/resourceGroups/` grupy zasobów nazwa `/providers/Microsoft.Sql/servers/` `/databases/` bazy danych aby określić grupę zasobów, użyj następującego formatu: `/subscriptions/` `/resourceGroups/` Nazwa grupy zasobów identyfikator subskrypcji</span><span class="sxs-lookup"><span data-stu-id="60a62-156">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="60a62-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="60a62-157">-TenantLevel</span></span>
<span data-ttu-id="60a62-158">Wskazuje, że ten aplet polecenia działa na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="60a62-158">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="60a62-159">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="60a62-159">-Confirm</span></span>
<span data-ttu-id="60a62-160">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60a62-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60a62-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60a62-161">-WhatIf</span></span>
<span data-ttu-id="60a62-162">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60a62-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60a62-163">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="60a62-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60a62-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60a62-164">CommonParameters</span></span>
<span data-ttu-id="60a62-165">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60a62-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60a62-166">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60a62-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60a62-167">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="60a62-167">INPUTS</span></span>

## <span data-ttu-id="60a62-168">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="60a62-168">OUTPUTS</span></span>

## <span data-ttu-id="60a62-169">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="60a62-169">NOTES</span></span>

## <span data-ttu-id="60a62-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="60a62-170">RELATED LINKS</span></span>

[<span data-ttu-id="60a62-171">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="60a62-171">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="60a62-172">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="60a62-172">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

[<span data-ttu-id="60a62-173">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="60a62-173">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


