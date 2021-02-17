---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroupMember.md
ms.openlocfilehash: 7450588905deeb900efbffffa253f5c06ae63272
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178770"
---
# <span data-ttu-id="62b9e-101">Remove-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="62b9e-101">Remove-AzADGroupMember</span></span>

## <span data-ttu-id="62b9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62b9e-102">SYNOPSIS</span></span>
<span data-ttu-id="62b9e-103">Usuwa użytkownika z grupy usługi AD.</span><span class="sxs-lookup"><span data-stu-id="62b9e-103">Removes a user from an AD group.</span></span>

## <span data-ttu-id="62b9e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="62b9e-104">SYNTAX</span></span>

### <span data-ttu-id="62b9e-105">ExplicitParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="62b9e-105">ExplicitParameterSet (Default)</span></span>
```
Remove-AzADGroupMember [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="62b9e-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="62b9e-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62b9e-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="62b9e-107">MemberObjectIdWithGroupObject</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62b9e-108">MemberObjectIdWithGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="62b9e-108">MemberObjectIdWithGroupObjectId</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62b9e-109">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="62b9e-109">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62b9e-110">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="62b9e-110">MemberUPNWithGroupObjectParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62b9e-111">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="62b9e-111">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62b9e-112">OPIS</span><span class="sxs-lookup"><span data-stu-id="62b9e-112">DESCRIPTION</span></span>
<span data-ttu-id="62b9e-113">Usuwa użytkownika z grupy usługi AD.</span><span class="sxs-lookup"><span data-stu-id="62b9e-113">Removes a user from an AD group.</span></span>

## <span data-ttu-id="62b9e-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="62b9e-114">EXAMPLES</span></span>

### <span data-ttu-id="62b9e-115">Przykład 1. Usuwanie użytkownika z grupy według identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="62b9e-115">Example 1: Remove a user from a group by object id</span></span>

```powershell
PS C:\> Remove-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="62b9e-116">Usuwa użytkownika o identyfikatorze obiektu "D9076BBC-D62C-4105-9C78-A7F5BC4A3405" z grupy o identyfikatorze obiektu '85F89C90-780E-4AA6-9F4F-6F268D322EEEE'.</span><span class="sxs-lookup"><span data-stu-id="62b9e-116">Removes the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' from the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="62b9e-117">Przykład 2. Usuwanie użytkownika z grupy za pomocą funkcji pipingu</span><span class="sxs-lookup"><span data-stu-id="62b9e-117">Example 2: Remove a user from a group by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="62b9e-118">Pobiera grupę o identyfikatorze obiektu "85F89C90-780E-4AA6-9F4F-6F268D322EEE" i potokuje ją do polecenia cmdlet Remove-AzADGroupMember w celu usunięcia użytkownika do tej grupy.</span><span class="sxs-lookup"><span data-stu-id="62b9e-118">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Remove-AzADGroupMember cmdlet to remove the user to that group.</span></span>

## <span data-ttu-id="62b9e-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62b9e-119">PARAMETERS</span></span>

### <span data-ttu-id="62b9e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62b9e-120">-DefaultProfile</span></span>
<span data-ttu-id="62b9e-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="62b9e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62b9e-122">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="62b9e-122">-GroupDisplayName</span></span>
<span data-ttu-id="62b9e-123">Nazwa wyświetlana grupy, z których mają być usunięci jej grupę.</span><span class="sxs-lookup"><span data-stu-id="62b9e-123">The display name of the group to remove the member(s) from.</span></span>

```yaml
Type: System.String
Parameter Sets: MemberObjectIdWithGroupDisplayName, MemberUPNWithGroupDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62b9e-124">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="62b9e-124">-GroupObject</span></span>
<span data-ttu-id="62b9e-125">Object representation of the group to remove the member from.</span><span class="sxs-lookup"><span data-stu-id="62b9e-125">The object representation of the group to remove the member from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADGroup
Parameter Sets: MemberObjectIdWithGroupObject, MemberUPNWithGroupObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62b9e-126">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="62b9e-126">-GroupObjectId</span></span>
<span data-ttu-id="62b9e-127">Identyfikator obiektu grupy, z których ma być usuwany członek.</span><span class="sxs-lookup"><span data-stu-id="62b9e-127">The object id of the group to remove the member from.</span></span>

```yaml
Type: System.String
Parameter Sets: MemberObjectIdWithGroupObjectId, MemberUPNWithGroupObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62b9e-128">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="62b9e-128">-MemberObjectId</span></span>
<span data-ttu-id="62b9e-129">Identyfikator obiektu członka.</span><span class="sxs-lookup"><span data-stu-id="62b9e-129">The object id of the member.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MemberObjectIdWithGroupDisplayName, MemberObjectIdWithGroupObject, MemberObjectIdWithGroupObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62b9e-130">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="62b9e-130">-MemberUserPrincipalName</span></span>
<span data-ttu-id="62b9e-131">UpN (UpN) członków, których chcesz usunąć.</span><span class="sxs-lookup"><span data-stu-id="62b9e-131">The UPN of the member(s) to remove.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MemberUPNWithGroupDisplayNameParameterSet, MemberUPNWithGroupObjectParameterSet, MemberUPNWithGroupObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62b9e-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62b9e-132">-PassThru</span></span>
<span data-ttu-id="62b9e-133">Określenie tej wartości spowoduje zwrócenie wartości prawda, jeśli polecenie zostało pomyślnie określone.</span><span class="sxs-lookup"><span data-stu-id="62b9e-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="62b9e-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="62b9e-134">-Confirm</span></span>
<span data-ttu-id="62b9e-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="62b9e-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62b9e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62b9e-136">-WhatIf</span></span>
<span data-ttu-id="62b9e-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62b9e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62b9e-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="62b9e-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62b9e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62b9e-139">CommonParameters</span></span>
<span data-ttu-id="62b9e-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62b9e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62b9e-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62b9e-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62b9e-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62b9e-142">INPUTS</span></span>

### <span data-ttu-id="62b9e-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="62b9e-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="62b9e-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="62b9e-144">OUTPUTS</span></span>

### <span data-ttu-id="62b9e-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="62b9e-145">System.Boolean</span></span>

## <span data-ttu-id="62b9e-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="62b9e-146">NOTES</span></span>

## <span data-ttu-id="62b9e-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="62b9e-147">RELATED LINKS</span></span>
