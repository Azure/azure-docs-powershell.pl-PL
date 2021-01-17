---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/add-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Add-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Add-AzADGroupMember.md
ms.openlocfilehash: bf64c2fd139a4174496ba48cdb94aab89486a62a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490630"
---
# <span data-ttu-id="3a448-101">Add-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="3a448-101">Add-AzADGroupMember</span></span>

## <span data-ttu-id="3a448-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3a448-102">SYNOPSIS</span></span>
<span data-ttu-id="3a448-103">Dodaje użytkownika do istniejącej grupy usługi AD.</span><span class="sxs-lookup"><span data-stu-id="3a448-103">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="3a448-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3a448-104">SYNTAX</span></span>

### <span data-ttu-id="3a448-105">MemberObjectIdWithGroupObjectId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3a448-105">MemberObjectIdWithGroupObjectId (Default)</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a448-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="3a448-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a448-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="3a448-107">MemberObjectIdWithGroupObject</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a448-108">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a448-108">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a448-109">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a448-109">MemberUPNWithGroupObjectParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a448-110">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a448-110">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a448-111">Opis</span><span class="sxs-lookup"><span data-stu-id="3a448-111">DESCRIPTION</span></span>
<span data-ttu-id="3a448-112">Dodaje użytkownika do istniejącej grupy usługi AD.</span><span class="sxs-lookup"><span data-stu-id="3a448-112">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="3a448-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3a448-113">EXAMPLES</span></span>

### <span data-ttu-id="3a448-114">Przykład 1: Dodawanie użytkownika do grupy według identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="3a448-114">Example 1: Add a user to a group by object id</span></span>

```powershell
PS C:\> Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -TargetGroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="3a448-115">Dodaje użytkownika o identyfikatorze obiektu "D9076BBC-D62C-4105-9C78-A7F5BC4A3405" do grupy o identyfikatorze obiektu "85F89C90-780E-4AA6-9F4F-6F268D322EEE".</span><span class="sxs-lookup"><span data-stu-id="3a448-115">Adds the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' to the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="3a448-116">Przykład 2: Dodawanie użytkownika do grupy według połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="3a448-116">Example 2: Add a user to a group by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="3a448-117">Pobiera grupę o identyfikatorze obiektu "85F89C90-780E-4AA6-9F4F-6F268D322EEE" i przekazuje ją do polecenia cmdlet Add-AzADGroupMember, aby dodać użytkownika do tej grupy.</span><span class="sxs-lookup"><span data-stu-id="3a448-117">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Add-AzADGroupMember cmdlet to add the user to that group.</span></span>

### <span data-ttu-id="3a448-118">Przykład 3: Dodawanie użytkownika do grupy według nazwy głównej</span><span class="sxs-lookup"><span data-stu-id="3a448-118">Example 3: Add a user to a group by principal name</span></span>

```powershell
PS C:\> Add-AzADGroupMember -MemberUserPrincipalName "myemail@domain.com" -TargetGroupDisplayName "MyGroupDisplayName" 
PS C:\> Get-AzADGroupMember -GroupDisplayName "MyGroupDisplayName"
```

<span data-ttu-id="3a448-119">Dodaje użytkownika do grupy i wyświetla listę członków grupy.</span><span class="sxs-lookup"><span data-stu-id="3a448-119">Adds an user to a group and list the members of the group.</span></span>

## <span data-ttu-id="3a448-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3a448-120">PARAMETERS</span></span>

### <span data-ttu-id="3a448-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a448-121">-DefaultProfile</span></span>
<span data-ttu-id="3a448-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3a448-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a448-123">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="3a448-123">-MemberObjectId</span></span>
<span data-ttu-id="3a448-124">Identyfikator obiektu elementu członkowskiego.</span><span class="sxs-lookup"><span data-stu-id="3a448-124">The object id of the member.</span></span>

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

### <span data-ttu-id="3a448-125">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="3a448-125">-MemberUserPrincipalName</span></span>
<span data-ttu-id="3a448-126">Główna nazwa użytkownika (ów) członków, którą należy dodać do grupy.</span><span class="sxs-lookup"><span data-stu-id="3a448-126">The UPN of the member(s) to add to the group.</span></span>

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

### <span data-ttu-id="3a448-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a448-127">-PassThru</span></span>
<span data-ttu-id="3a448-128">Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="3a448-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="3a448-129">-TargetGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="3a448-129">-TargetGroupDisplayName</span></span>
<span data-ttu-id="3a448-130">Nazwa wyświetlana grupy, do której mają zostać dodane elementy członkowskie.</span><span class="sxs-lookup"><span data-stu-id="3a448-130">The display name of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="3a448-131">-TargetGroupObject</span><span class="sxs-lookup"><span data-stu-id="3a448-131">-TargetGroupObject</span></span>
<span data-ttu-id="3a448-132">Reprezentacja obiektu grupy, do której mają zostać dodane elementy członkowskie.</span><span class="sxs-lookup"><span data-stu-id="3a448-132">The object representation of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="3a448-133">-TargetGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="3a448-133">-TargetGroupObjectId</span></span>
<span data-ttu-id="3a448-134">Identyfikator obiektu grupy, do którego mają zostać dodane elementy członkowskie.</span><span class="sxs-lookup"><span data-stu-id="3a448-134">The object id of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="3a448-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3a448-135">-Confirm</span></span>
<span data-ttu-id="3a448-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a448-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a448-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a448-137">-WhatIf</span></span>
<span data-ttu-id="3a448-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a448-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a448-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3a448-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a448-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a448-140">CommonParameters</span></span>
<span data-ttu-id="3a448-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a448-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a448-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a448-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a448-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a448-143">INPUTS</span></span>

### <span data-ttu-id="3a448-144">Microsoft. Azure. Commands. pozycji. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="3a448-144">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="3a448-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3a448-145">OUTPUTS</span></span>

### <span data-ttu-id="3a448-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3a448-146">System.Boolean</span></span>

## <span data-ttu-id="3a448-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3a448-147">NOTES</span></span>

## <span data-ttu-id="3a448-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a448-148">RELATED LINKS</span></span>
