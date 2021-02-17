---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/add-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Add-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Add-AzADGroupMember.md
ms.openlocfilehash: bf64c2fd139a4174496ba48cdb94aab89486a62a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192787"
---
# <span data-ttu-id="c471a-101">Add-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="c471a-101">Add-AzADGroupMember</span></span>

## <span data-ttu-id="c471a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c471a-102">SYNOPSIS</span></span>
<span data-ttu-id="c471a-103">Dodaje użytkownika do istniejącej grupy usługi AD.</span><span class="sxs-lookup"><span data-stu-id="c471a-103">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="c471a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c471a-104">SYNTAX</span></span>

### <span data-ttu-id="c471a-105">MemberObjectIdWithGroupObjectId (domyślne)</span><span class="sxs-lookup"><span data-stu-id="c471a-105">MemberObjectIdWithGroupObjectId (Default)</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c471a-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="c471a-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c471a-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="c471a-107">MemberObjectIdWithGroupObject</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c471a-108">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c471a-108">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c471a-109">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c471a-109">MemberUPNWithGroupObjectParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c471a-110">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c471a-110">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c471a-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="c471a-111">DESCRIPTION</span></span>
<span data-ttu-id="c471a-112">Dodaje użytkownika do istniejącej grupy usługi AD.</span><span class="sxs-lookup"><span data-stu-id="c471a-112">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="c471a-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c471a-113">EXAMPLES</span></span>

### <span data-ttu-id="c471a-114">Przykład 1. Dodawanie użytkownika do grupy według identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="c471a-114">Example 1: Add a user to a group by object id</span></span>

```powershell
PS C:\> Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -TargetGroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="c471a-115">Dodaje użytkownika o identyfikatorze obiektu "D9076BBC-D62C-4105-9C78-A7F5BC4A3405" do grupy o identyfikatorze obiektu '85F89C90-780E-4AA6-9F4F-6F268D322EEEE'.</span><span class="sxs-lookup"><span data-stu-id="c471a-115">Adds the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' to the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="c471a-116">Przykład 2. Dodawanie użytkownika do grupy za pomocą funkcji rurowych</span><span class="sxs-lookup"><span data-stu-id="c471a-116">Example 2: Add a user to a group by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="c471a-117">Pobiera grupę o identyfikatorze obiektu "85F89C90-780E-4AA6-9F4F-6F268D322EEE" i potokuje ją do polecenia cmdlet Add-AzADGroupMember, aby dodać użytkownika do tej grupy.</span><span class="sxs-lookup"><span data-stu-id="c471a-117">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Add-AzADGroupMember cmdlet to add the user to that group.</span></span>

### <span data-ttu-id="c471a-118">Przykład 3. Dodawanie użytkownika do grupy według nazwy głównej</span><span class="sxs-lookup"><span data-stu-id="c471a-118">Example 3: Add a user to a group by principal name</span></span>

```powershell
PS C:\> Add-AzADGroupMember -MemberUserPrincipalName "myemail@domain.com" -TargetGroupDisplayName "MyGroupDisplayName" 
PS C:\> Get-AzADGroupMember -GroupDisplayName "MyGroupDisplayName"
```

<span data-ttu-id="c471a-119">Dodaje użytkownika do grupy i zawiera listę członków grupy.</span><span class="sxs-lookup"><span data-stu-id="c471a-119">Adds an user to a group and list the members of the group.</span></span>

## <span data-ttu-id="c471a-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c471a-120">PARAMETERS</span></span>

### <span data-ttu-id="c471a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c471a-121">-DefaultProfile</span></span>
<span data-ttu-id="c471a-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c471a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c471a-123">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="c471a-123">-MemberObjectId</span></span>
<span data-ttu-id="c471a-124">Identyfikator obiektu członka.</span><span class="sxs-lookup"><span data-stu-id="c471a-124">The object id of the member.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MemberObjectIdWithGroupObjectId, MemberObjectIdWithGroupDisplayName, MemberObjectIdWithGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c471a-125">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="c471a-125">-MemberUserPrincipalName</span></span>
<span data-ttu-id="c471a-126">UpN członków, których chcesz dodać do grupy.</span><span class="sxs-lookup"><span data-stu-id="c471a-126">The UPN of the member(s) to add to the group.</span></span>

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

### <span data-ttu-id="c471a-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c471a-127">-PassThru</span></span>
<span data-ttu-id="c471a-128">Określenie tej wartości spowoduje zwrócenie wartości prawda, jeśli polecenie zostało pomyślnie określone.</span><span class="sxs-lookup"><span data-stu-id="c471a-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="c471a-129">-TargetGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="c471a-129">-TargetGroupDisplayName</span></span>
<span data-ttu-id="c471a-130">Nazwa wyświetlana grupy, do których chcesz dodać członków.</span><span class="sxs-lookup"><span data-stu-id="c471a-130">The display name of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="c471a-131">-TargetGroupObject</span><span class="sxs-lookup"><span data-stu-id="c471a-131">-TargetGroupObject</span></span>
<span data-ttu-id="c471a-132">Object representation of the group to add the member(s) to.</span><span class="sxs-lookup"><span data-stu-id="c471a-132">The object representation of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="c471a-133">-TargetGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="c471a-133">-TargetGroupObjectId</span></span>
<span data-ttu-id="c471a-134">Identyfikator obiektu grupy, do których mają być dodawania członków.</span><span class="sxs-lookup"><span data-stu-id="c471a-134">The object id of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="c471a-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c471a-135">-Confirm</span></span>
<span data-ttu-id="c471a-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c471a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c471a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c471a-137">-WhatIf</span></span>
<span data-ttu-id="c471a-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c471a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c471a-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c471a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c471a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c471a-140">CommonParameters</span></span>
<span data-ttu-id="c471a-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c471a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c471a-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c471a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c471a-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c471a-143">INPUTS</span></span>

### <span data-ttu-id="c471a-144">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="c471a-144">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="c471a-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c471a-145">OUTPUTS</span></span>

### <span data-ttu-id="c471a-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c471a-146">System.Boolean</span></span>

## <span data-ttu-id="c471a-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c471a-147">NOTES</span></span>

## <span data-ttu-id="c471a-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c471a-148">RELATED LINKS</span></span>
