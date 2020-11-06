---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceLock.md
ms.openlocfilehash: c363279c0cbb6dc20b0ddcc7bae32266a848fb3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553769"
---
# <span data-ttu-id="d96f2-101">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="d96f2-101">New-AzureRmResourceLock</span></span>

## <span data-ttu-id="d96f2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d96f2-102">SYNOPSIS</span></span>
<span data-ttu-id="d96f2-103">Tworzy blokadę zasobu.</span><span class="sxs-lookup"><span data-stu-id="d96f2-103">Creates a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d96f2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d96f2-104">SYNTAX</span></span>

### <span data-ttu-id="d96f2-105">Blokada w określonym zakresie.</span><span class="sxs-lookup"><span data-stu-id="d96f2-105">A lock at the specified scope.</span></span> <span data-ttu-id="d96f2-106">Domyślne</span><span class="sxs-lookup"><span data-stu-id="d96f2-106">(Default)</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d96f2-107">Blokada zakresu grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d96f2-107">A lock at the resource group scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d96f2-108">Blokada zakresu zasobów grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d96f2-108">A lock at the resource group resource scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d96f2-109">Blokada zakresu subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d96f2-109">A lock at the subscription scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d96f2-110">Blokada w zakresie zasobów subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d96f2-110">A lock at the subscription resource scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d96f2-111">Blokada w zakresie zasobów dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="d96f2-111">A lock at the tenant resource scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d96f2-112">Blokada za pomocą identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="d96f2-112">A lock, by Id.</span></span>
```
New-AzureRmResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d96f2-113">Opis</span><span class="sxs-lookup"><span data-stu-id="d96f2-113">DESCRIPTION</span></span>
<span data-ttu-id="d96f2-114">Polecenie cmdlet **New-AzureRmResourceLock** umożliwia utworzenie blokady zasobów.</span><span class="sxs-lookup"><span data-stu-id="d96f2-114">The **New-AzureRmResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="d96f2-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d96f2-115">EXAMPLES</span></span>

### <span data-ttu-id="d96f2-116">Przykład 1. Tworzenie blokady zasobów w witrynie sieci Web</span><span class="sxs-lookup"><span data-stu-id="d96f2-116">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzureRmResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="d96f2-117">To polecenie tworzy blokadę zasobu w witrynie sieci Web.</span><span class="sxs-lookup"><span data-stu-id="d96f2-117">This command creates a resource lock on a website.</span></span>

## <span data-ttu-id="d96f2-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d96f2-118">PARAMETERS</span></span>

### <span data-ttu-id="d96f2-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d96f2-119">-ApiVersion</span></span>
<span data-ttu-id="d96f2-120">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="d96f2-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="d96f2-121">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="d96f2-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="d96f2-122">-Force</span><span class="sxs-lookup"><span data-stu-id="d96f2-122">-Force</span></span>
<span data-ttu-id="d96f2-123">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d96f2-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d96f2-124">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d96f2-124">-InformationAction</span></span>
<span data-ttu-id="d96f2-125">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="d96f2-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d96f2-126">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d96f2-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d96f2-127">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="d96f2-127">Continue</span></span>
- <span data-ttu-id="d96f2-128">Ignorować</span><span class="sxs-lookup"><span data-stu-id="d96f2-128">Ignore</span></span>
- <span data-ttu-id="d96f2-129">Inquire</span><span class="sxs-lookup"><span data-stu-id="d96f2-129">Inquire</span></span>
- <span data-ttu-id="d96f2-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d96f2-130">SilentlyContinue</span></span>
- <span data-ttu-id="d96f2-131">Przestaw</span><span class="sxs-lookup"><span data-stu-id="d96f2-131">Stop</span></span>
- <span data-ttu-id="d96f2-132">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="d96f2-132">Suspend</span></span>

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

### <span data-ttu-id="d96f2-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d96f2-133">-InformationVariable</span></span>
<span data-ttu-id="d96f2-134">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="d96f2-134">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d96f2-135">-LockId</span><span class="sxs-lookup"><span data-stu-id="d96f2-135">-LockId</span></span>
<span data-ttu-id="d96f2-136">Określa identyfikator blokady.</span><span class="sxs-lookup"><span data-stu-id="d96f2-136">Specifies the ID of the lock.</span></span>

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

### <span data-ttu-id="d96f2-137">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="d96f2-137">-LockLevel</span></span>
<span data-ttu-id="d96f2-138">Określa poziom blokady.</span><span class="sxs-lookup"><span data-stu-id="d96f2-138">Specifies the level for the lock.</span></span>
<span data-ttu-id="d96f2-139">Obecnie jedyną prawidłową wartością jest CanNotDelete.</span><span class="sxs-lookup"><span data-stu-id="d96f2-139">Currently, the only valid value is CanNotDelete.</span></span>

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

### <span data-ttu-id="d96f2-140">-Kłódkaname</span><span class="sxs-lookup"><span data-stu-id="d96f2-140">-LockName</span></span>
<span data-ttu-id="d96f2-141">Określa nazwę blokady.</span><span class="sxs-lookup"><span data-stu-id="d96f2-141">Specifies the name of the lock.</span></span>

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

### <span data-ttu-id="d96f2-142">-LockNotes</span><span class="sxs-lookup"><span data-stu-id="d96f2-142">-LockNotes</span></span>
<span data-ttu-id="d96f2-143">Określa uwagi dotyczące blokady.</span><span class="sxs-lookup"><span data-stu-id="d96f2-143">Specifies the notes for the lock.</span></span>

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

### <span data-ttu-id="d96f2-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="d96f2-144">-Pre</span></span>
<span data-ttu-id="d96f2-145">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="d96f2-145">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="d96f2-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d96f2-146">-ResourceGroupName</span></span>
<span data-ttu-id="d96f2-147">Określa nazwę grupy zasobów, do której odnosi się blokada, lub zawierającej grupę zasobów, której dotyczy blokada.</span><span class="sxs-lookup"><span data-stu-id="d96f2-147">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="d96f2-148">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="d96f2-148">-ResourceName</span></span>
<span data-ttu-id="d96f2-149">Określa nazwę zasobu, którego dotyczy blokada.</span><span class="sxs-lookup"><span data-stu-id="d96f2-149">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="d96f2-150">Aby na przykład określić bazę danych, użyj następującego formatu:</span><span class="sxs-lookup"><span data-stu-id="d96f2-150">For instance, to specify a database, use the following format:</span></span> 

`ContosoServer/ContosoDatabase`

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

### <span data-ttu-id="d96f2-151">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="d96f2-151">-ResourceType</span></span>
<span data-ttu-id="d96f2-152">Określa typ zasobu zasobu, którego dotyczy blokada.</span><span class="sxs-lookup"><span data-stu-id="d96f2-152">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="d96f2-153">-Zakres</span><span class="sxs-lookup"><span data-stu-id="d96f2-153">-Scope</span></span>
<span data-ttu-id="d96f2-154">Określa zakres, do którego jest stosowana blokada.</span><span class="sxs-lookup"><span data-stu-id="d96f2-154">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="d96f2-155">Aby na przykład określić bazę danych, użyj następującego formatu:</span><span class="sxs-lookup"><span data-stu-id="d96f2-155">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="d96f2-156">`/subscriptions/`Identyfikator subskrypcji nazwa `/resourceGroups/` grupy zasobów nazwa `/providers/Microsoft.Sql/servers/` serwera nazwa `/databases/` bazy danych</span><span class="sxs-lookup"><span data-stu-id="d96f2-156">`/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name</span></span>

<span data-ttu-id="d96f2-157">Aby określić grupę zasobów, użyj następującego formatu:</span><span class="sxs-lookup"><span data-stu-id="d96f2-157">To specify a resource group, use the following format:</span></span> 

<span data-ttu-id="d96f2-158">`/subscriptions/``/resourceGroups/`Nazwa grupy zasobów identyfikatora subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d96f2-158">`/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

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

### <span data-ttu-id="d96f2-159">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="d96f2-159">-TenantLevel</span></span>
<span data-ttu-id="d96f2-160">Wskazuje, że ten aplet polecenia działa na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="d96f2-160">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="d96f2-161">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d96f2-161">-Confirm</span></span>
<span data-ttu-id="d96f2-162">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d96f2-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d96f2-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d96f2-163">-WhatIf</span></span>
<span data-ttu-id="d96f2-164">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d96f2-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d96f2-165">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d96f2-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d96f2-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d96f2-166">-DefaultProfile</span></span>
<span data-ttu-id="d96f2-167">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d96f2-167">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d96f2-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d96f2-168">CommonParameters</span></span>
<span data-ttu-id="d96f2-169">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d96f2-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d96f2-170">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d96f2-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d96f2-171">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d96f2-171">INPUTS</span></span>

## <span data-ttu-id="d96f2-172">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d96f2-172">OUTPUTS</span></span>

### <span data-ttu-id="d96f2-173">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="d96f2-173">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="d96f2-174">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d96f2-174">NOTES</span></span>

## <span data-ttu-id="d96f2-175">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d96f2-175">RELATED LINKS</span></span>

[<span data-ttu-id="d96f2-176">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="d96f2-176">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="d96f2-177">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="d96f2-177">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

[<span data-ttu-id="d96f2-178">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="d96f2-178">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


