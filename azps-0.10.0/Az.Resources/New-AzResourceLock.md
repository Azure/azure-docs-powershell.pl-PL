---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzResourceLock.md
ms.openlocfilehash: 8d4f4180cc827c879dde0252044d30d5242d2300
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892477"
---
# <span data-ttu-id="93090-101">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="93090-101">New-AzResourceLock</span></span>

## <span data-ttu-id="93090-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="93090-102">SYNOPSIS</span></span>
<span data-ttu-id="93090-103">Tworzy blokadę zasobu.</span><span class="sxs-lookup"><span data-stu-id="93090-103">Creates a resource lock.</span></span>

## <span data-ttu-id="93090-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="93090-104">SYNTAX</span></span>

### <span data-ttu-id="93090-105">BySpecifiedScope (domyślny)</span><span class="sxs-lookup"><span data-stu-id="93090-105">BySpecifiedScope (Default)</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="93090-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="93090-106">ByResourceGroup</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="93090-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="93090-107">ByResourceGroupLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93090-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="93090-108">BySubscription</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="93090-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="93090-109">BySubscriptionLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93090-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="93090-110">ByTenantLevel</span></span>
```
New-AzResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93090-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="93090-111">ByLockId</span></span>
```
New-AzResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="93090-112">Opis</span><span class="sxs-lookup"><span data-stu-id="93090-112">DESCRIPTION</span></span>
<span data-ttu-id="93090-113">Polecenie cmdlet **New-AzResourceLock** umożliwia utworzenie blokady zasobów.</span><span class="sxs-lookup"><span data-stu-id="93090-113">The **New-AzResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="93090-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="93090-114">EXAMPLES</span></span>

### <span data-ttu-id="93090-115">Przykład 1. Tworzenie blokady zasobów w witrynie sieci Web</span><span class="sxs-lookup"><span data-stu-id="93090-115">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="93090-116">To polecenie tworzy blokadę zasobu w witrynie sieci Web.</span><span class="sxs-lookup"><span data-stu-id="93090-116">This command creates a resource lock on a website.</span></span>

## <span data-ttu-id="93090-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="93090-117">PARAMETERS</span></span>

### <span data-ttu-id="93090-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="93090-118">-ApiVersion</span></span>
<span data-ttu-id="93090-119">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="93090-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="93090-120">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="93090-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="93090-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93090-121">-DefaultProfile</span></span>
<span data-ttu-id="93090-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="93090-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93090-123">-Force</span><span class="sxs-lookup"><span data-stu-id="93090-123">-Force</span></span>
<span data-ttu-id="93090-124">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="93090-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="93090-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="93090-125">-InformationAction</span></span>
<span data-ttu-id="93090-126">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="93090-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="93090-127">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="93090-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="93090-128">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="93090-128">Continue</span></span>
- <span data-ttu-id="93090-129">Ignorować</span><span class="sxs-lookup"><span data-stu-id="93090-129">Ignore</span></span>
- <span data-ttu-id="93090-130">Inquire</span><span class="sxs-lookup"><span data-stu-id="93090-130">Inquire</span></span>
- <span data-ttu-id="93090-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="93090-131">SilentlyContinue</span></span>
- <span data-ttu-id="93090-132">Przestaw</span><span class="sxs-lookup"><span data-stu-id="93090-132">Stop</span></span>
- <span data-ttu-id="93090-133">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="93090-133">Suspend</span></span>

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

### <span data-ttu-id="93090-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="93090-134">-InformationVariable</span></span>
<span data-ttu-id="93090-135">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="93090-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="93090-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="93090-136">-LockId</span></span>
<span data-ttu-id="93090-137">Określa identyfikator blokady.</span><span class="sxs-lookup"><span data-stu-id="93090-137">Specifies the ID of the lock.</span></span>

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

### <span data-ttu-id="93090-138">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="93090-138">-LockLevel</span></span>
<span data-ttu-id="93090-139">Określa poziom blokady.</span><span class="sxs-lookup"><span data-stu-id="93090-139">Specifies the level for the lock.</span></span>
<span data-ttu-id="93090-140">Obecnie prawidłowe wartości to CanNotDelete, ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="93090-140">Currently, valid values are CanNotDelete, ReadOnly.</span></span>

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

### <span data-ttu-id="93090-141">-Kłódkaname</span><span class="sxs-lookup"><span data-stu-id="93090-141">-LockName</span></span>
<span data-ttu-id="93090-142">Określa nazwę blokady.</span><span class="sxs-lookup"><span data-stu-id="93090-142">Specifies the name of the lock.</span></span>

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

### <span data-ttu-id="93090-143">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="93090-143">-LockNotes</span></span>
<span data-ttu-id="93090-144">Określa uwagi dotyczące blokady.</span><span class="sxs-lookup"><span data-stu-id="93090-144">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="93090-145">-Pre</span><span class="sxs-lookup"><span data-stu-id="93090-145">-Pre</span></span>
<span data-ttu-id="93090-146">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="93090-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="93090-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93090-147">-ResourceGroupName</span></span>
<span data-ttu-id="93090-148">Określa nazwę grupy zasobów, do której odnosi się blokada, lub zawierającej grupę zasobów, której dotyczy blokada.</span><span class="sxs-lookup"><span data-stu-id="93090-148">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="93090-149">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="93090-149">-ResourceName</span></span>
<span data-ttu-id="93090-150">Określa nazwę zasobu, którego dotyczy blokada.</span><span class="sxs-lookup"><span data-stu-id="93090-150">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="93090-151">Aby na przykład określić bazę danych, użyj następującego formatu: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="93090-151">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="93090-152">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="93090-152">-ResourceType</span></span>
<span data-ttu-id="93090-153">Określa typ zasobu zasobu, którego dotyczy blokada.</span><span class="sxs-lookup"><span data-stu-id="93090-153">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="93090-154">-Zakres</span><span class="sxs-lookup"><span data-stu-id="93090-154">-Scope</span></span>
<span data-ttu-id="93090-155">Określa zakres, do którego jest stosowana blokada.</span><span class="sxs-lookup"><span data-stu-id="93090-155">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="93090-156">Aby na przykład określić bazę danych, użyj następującego formatu: `/subscriptions/` Identyfikator subskrypcji nazwa `/resourceGroups/` grupy zasobów nazwa `/providers/Microsoft.Sql/servers/` `/databases/` bazy danych aby określić grupę zasobów, użyj następującego formatu: `/subscriptions/` `/resourceGroups/` Nazwa grupy zasobów identyfikator subskrypcji</span><span class="sxs-lookup"><span data-stu-id="93090-156">For instance, to specify a database, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name To specify a resource group, use the following format: `/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="93090-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="93090-157">-TenantLevel</span></span>
<span data-ttu-id="93090-158">Wskazuje, że ten aplet polecenia działa na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="93090-158">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="93090-159">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="93090-159">-Confirm</span></span>
<span data-ttu-id="93090-160">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93090-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93090-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93090-161">-WhatIf</span></span>
<span data-ttu-id="93090-162">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93090-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93090-163">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="93090-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93090-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93090-164">CommonParameters</span></span>
<span data-ttu-id="93090-165">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93090-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93090-166">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93090-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93090-167">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="93090-167">INPUTS</span></span>

## <span data-ttu-id="93090-168">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="93090-168">OUTPUTS</span></span>

## <span data-ttu-id="93090-169">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="93090-169">NOTES</span></span>

## <span data-ttu-id="93090-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="93090-170">RELATED LINKS</span></span>

[<span data-ttu-id="93090-171">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="93090-171">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="93090-172">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="93090-172">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="93090-173">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="93090-173">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


