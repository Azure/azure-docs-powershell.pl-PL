---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/add-Azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Add-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Add-AzADGroupMember.md
ms.openlocfilehash: 069705ffc119fae964e931164f97bfbae72eca35
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892650"
---
# <span data-ttu-id="eb1dc-101">Add-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="eb1dc-101">Add-AzADGroupMember</span></span>

## <span data-ttu-id="eb1dc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eb1dc-102">SYNOPSIS</span></span>
<span data-ttu-id="eb1dc-103">Dodaje użytkownika do istniejącej grupy usługi AD.</span><span class="sxs-lookup"><span data-stu-id="eb1dc-103">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="eb1dc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eb1dc-104">SYNTAX</span></span>

### <span data-ttu-id="eb1dc-105">MemberObjectIdWithGroupObjectId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="eb1dc-105">MemberObjectIdWithGroupObjectId (Default)</span></span>
```
Add-AzADGroupMember -MemberObjectId <Guid[]> -TargetGroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb1dc-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="eb1dc-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Add-AzADGroupMember -MemberObjectId <Guid[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb1dc-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="eb1dc-107">MemberObjectIdWithGroupObject</span></span>
```
Add-AzADGroupMember -MemberObjectId <Guid[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb1dc-108">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb1dc-108">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb1dc-109">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb1dc-109">MemberUPNWithGroupObjectParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb1dc-110">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb1dc-110">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb1dc-111">Opis</span><span class="sxs-lookup"><span data-stu-id="eb1dc-111">DESCRIPTION</span></span>
<span data-ttu-id="eb1dc-112">Dodaje użytkownika do istniejącej grupy usługi AD.</span><span class="sxs-lookup"><span data-stu-id="eb1dc-112">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="eb1dc-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eb1dc-113">EXAMPLES</span></span>

### <span data-ttu-id="eb1dc-114">Przykład 1-Dodawanie użytkownika do grupy według identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="eb1dc-114">Example 1 - Add a user to a group by object id</span></span>

```
PS C:\> Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -TargetGroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="eb1dc-115">Dodaje użytkownika o identyfikatorze obiektu "D9076BBC-D62C-4105-9C78-A7F5BC4A3405" do grupy o identyfikatorze obiektu "85F89C90-780E-4AA6-9F4F-6F268D322EEE".</span><span class="sxs-lookup"><span data-stu-id="eb1dc-115">Adds the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' to the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="eb1dc-116">Przykład 2 — Dodawanie użytkownika do grupy według połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="eb1dc-116">Example 2 - Add a user to a group by piping</span></span>

```
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="eb1dc-117">Pobiera grupę o identyfikatorze obiektu "85F89C90-780E-4AA6-9F4F-6F268D322EEE" i przekazuje ją do polecenia cmdlet Add-AzADGroupMember, aby dodać użytkownika do tej grupy.</span><span class="sxs-lookup"><span data-stu-id="eb1dc-117">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Add-AzADGroupMember cmdlet to add the user to that group.</span></span>

## <span data-ttu-id="eb1dc-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eb1dc-118">PARAMETERS</span></span>

### <span data-ttu-id="eb1dc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb1dc-119">-DefaultProfile</span></span>
<span data-ttu-id="eb1dc-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="eb1dc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb1dc-121">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="eb1dc-121">-MemberObjectId</span></span>
<span data-ttu-id="eb1dc-122">Identyfikator obiektu elementu członkowskiego.</span><span class="sxs-lookup"><span data-stu-id="eb1dc-122">The object id of the member.</span></span>

```yaml
Type: System.Guid[]
Parameter Sets: MemberObjectIdWithGroupObjectId, MemberObjectIdWithGroupDisplayName, MemberObjectIdWithGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb1dc-123">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="eb1dc-123">-MemberUserPrincipalName</span></span>
<span data-ttu-id="eb1dc-124">Główna nazwa użytkownika (ów) członków, którą należy dodać do grupy.</span><span class="sxs-lookup"><span data-stu-id="eb1dc-124">The UPN of the member(s) to add to the group.</span></span>

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

### <span data-ttu-id="eb1dc-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eb1dc-125">-PassThru</span></span>
<span data-ttu-id="eb1dc-126">Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="eb1dc-126">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="eb1dc-127">-TargetGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="eb1dc-127">-TargetGroupDisplayName</span></span>
<span data-ttu-id="eb1dc-128">Nazwa wyświetlana grupy, do której mają zostać dodane elementy członkowskie.</span><span class="sxs-lookup"><span data-stu-id="eb1dc-128">The display name of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="eb1dc-129">-TargetGroupObject</span><span class="sxs-lookup"><span data-stu-id="eb1dc-129">-TargetGroupObject</span></span>
<span data-ttu-id="eb1dc-130">Reprezentacja obiektu grupy, do której mają zostać dodane elementy członkowskie.</span><span class="sxs-lookup"><span data-stu-id="eb1dc-130">The object representation of the group to add the member(s) to.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup
Parameter Sets: MemberObjectIdWithGroupObject, MemberUPNWithGroupObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb1dc-131">-TargetGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="eb1dc-131">-TargetGroupObjectId</span></span>
<span data-ttu-id="eb1dc-132">Identyfikator obiektu grupy, do którego mają zostać dodane elementy członkowskie.</span><span class="sxs-lookup"><span data-stu-id="eb1dc-132">The object id of the group to add the member(s) to.</span></span>

```yaml
Type: System.Guid
Parameter Sets: MemberObjectIdWithGroupObjectId, MemberUPNWithGroupObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb1dc-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="eb1dc-133">-Confirm</span></span>
<span data-ttu-id="eb1dc-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb1dc-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb1dc-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb1dc-135">-WhatIf</span></span>
<span data-ttu-id="eb1dc-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb1dc-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb1dc-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="eb1dc-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb1dc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb1dc-138">CommonParameters</span></span>
<span data-ttu-id="eb1dc-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb1dc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb1dc-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb1dc-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb1dc-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eb1dc-141">INPUTS</span></span>

### <span data-ttu-id="eb1dc-142">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="eb1dc-142">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="eb1dc-143">Parametry: TargetGroupObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="eb1dc-143">Parameters: TargetGroupObject (ByValue)</span></span>

## <span data-ttu-id="eb1dc-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eb1dc-144">OUTPUTS</span></span>

### <span data-ttu-id="eb1dc-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="eb1dc-145">System.Boolean</span></span>

## <span data-ttu-id="eb1dc-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eb1dc-146">NOTES</span></span>

## <span data-ttu-id="eb1dc-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eb1dc-147">RELATED LINKS</span></span>
