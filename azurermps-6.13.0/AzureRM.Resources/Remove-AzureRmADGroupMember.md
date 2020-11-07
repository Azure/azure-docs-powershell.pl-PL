---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADGroupMember.md
ms.openlocfilehash: 515591660abf34399caa5643c05478fd4295141a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716922"
---
# <span data-ttu-id="5db10-101">Remove-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="5db10-101">Remove-AzureRmADGroupMember</span></span>

## <span data-ttu-id="5db10-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5db10-102">SYNOPSIS</span></span>
<span data-ttu-id="5db10-103">Usuwa użytkownika z grupy usługi AD.</span><span class="sxs-lookup"><span data-stu-id="5db10-103">Removes a user from an AD group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5db10-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5db10-104">SYNTAX</span></span>

### <span data-ttu-id="5db10-105">ExplicitParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5db10-105">ExplicitParameterSet (Default)</span></span>
```
Remove-AzureRmADGroupMember [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5db10-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="5db10-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Remove-AzureRmADGroupMember -MemberObjectId <Guid[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5db10-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="5db10-107">MemberObjectIdWithGroupObject</span></span>
```
Remove-AzureRmADGroupMember -MemberObjectId <Guid[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5db10-108">MemberObjectIdWithGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="5db10-108">MemberObjectIdWithGroupObjectId</span></span>
```
Remove-AzureRmADGroupMember -MemberObjectId <Guid[]> -GroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5db10-109">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5db10-109">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Remove-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5db10-110">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5db10-110">MemberUPNWithGroupObjectParameterSet</span></span>
```
Remove-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5db10-111">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5db10-111">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Remove-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -GroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5db10-112">Opis</span><span class="sxs-lookup"><span data-stu-id="5db10-112">DESCRIPTION</span></span>
<span data-ttu-id="5db10-113">Usuwa użytkownika z grupy usługi AD.</span><span class="sxs-lookup"><span data-stu-id="5db10-113">Removes a user from an AD group.</span></span>

## <span data-ttu-id="5db10-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5db10-114">EXAMPLES</span></span>

### <span data-ttu-id="5db10-115">Przykład 1 — Usuwanie użytkownika z grupy według identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="5db10-115">Example 1 - Remove a user from a group by object id</span></span>

```
PS C:\> Remove-AzureRmADGroup -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="5db10-116">Usuwa użytkownika o identyfikatorze obiektu "D9076BBC-D62C-4105-9C78-A7F5BC4A3405" z grupy o identyfikatorze obiektu "85F89C90-780E-4AA6-9F4F-6F268D322EEE".</span><span class="sxs-lookup"><span data-stu-id="5db10-116">Removes the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' from the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="5db10-117">Przykład 2 — Usuwanie użytkownika z grupy według połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="5db10-117">Example 2 - Remove a user from a group by piping</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzureRmADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="5db10-118">Pobiera grupę o identyfikatorze obiektu "85F89C90-780E-4AA6-9F4F-6F268D322EEE" i przekazuje ją do polecenia cmdlet Remove-AzureRmADGroupMember, aby usunąć użytkownika z tej grupy.</span><span class="sxs-lookup"><span data-stu-id="5db10-118">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Remove-AzureRmADGroupMember cmdlet to remove the user to that group.</span></span>

## <span data-ttu-id="5db10-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5db10-119">PARAMETERS</span></span>

### <span data-ttu-id="5db10-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5db10-120">-DefaultProfile</span></span>
<span data-ttu-id="5db10-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5db10-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5db10-122">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="5db10-122">-GroupDisplayName</span></span>
<span data-ttu-id="5db10-123">Nazwa wyświetlana grupy, z której mają zostać usunięte elementy członkowskie.</span><span class="sxs-lookup"><span data-stu-id="5db10-123">The display name of the group to remove the member(s) from.</span></span>

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

### <span data-ttu-id="5db10-124">-Groupobject</span><span class="sxs-lookup"><span data-stu-id="5db10-124">-GroupObject</span></span>
<span data-ttu-id="5db10-125">Reprezentacja obiektu grupy, z której ma zostać usunięty członek.</span><span class="sxs-lookup"><span data-stu-id="5db10-125">The object representation of the group to remove the member from.</span></span>

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

### <span data-ttu-id="5db10-126">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="5db10-126">-GroupObjectId</span></span>
<span data-ttu-id="5db10-127">Identyfikator obiektu grupy, z której ma zostać usunięty członek.</span><span class="sxs-lookup"><span data-stu-id="5db10-127">The object id of the group to remove the member from.</span></span>

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

### <span data-ttu-id="5db10-128">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="5db10-128">-MemberObjectId</span></span>
<span data-ttu-id="5db10-129">Identyfikator obiektu elementu członkowskiego.</span><span class="sxs-lookup"><span data-stu-id="5db10-129">The object id of the member.</span></span>

```yaml
Type: System.Guid[]
Parameter Sets: MemberObjectIdWithGroupDisplayName, MemberObjectIdWithGroupObject, MemberObjectIdWithGroupObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5db10-130">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="5db10-130">-MemberUserPrincipalName</span></span>
<span data-ttu-id="5db10-131">Główna nazwa użytkownika (-y) członków do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="5db10-131">The UPN of the member(s) to remove.</span></span>

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

### <span data-ttu-id="5db10-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5db10-132">-PassThru</span></span>
<span data-ttu-id="5db10-133">Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="5db10-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="5db10-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5db10-134">-Confirm</span></span>
<span data-ttu-id="5db10-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5db10-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5db10-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5db10-136">-WhatIf</span></span>
<span data-ttu-id="5db10-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5db10-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5db10-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5db10-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5db10-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5db10-139">CommonParameters</span></span>
<span data-ttu-id="5db10-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5db10-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5db10-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5db10-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5db10-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5db10-142">INPUTS</span></span>

### <span data-ttu-id="5db10-143">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="5db10-143">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="5db10-144">Parametry: Groupobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5db10-144">Parameters: GroupObject (ByValue)</span></span>

## <span data-ttu-id="5db10-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5db10-145">OUTPUTS</span></span>

### <span data-ttu-id="5db10-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5db10-146">System.Boolean</span></span>

## <span data-ttu-id="5db10-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5db10-147">NOTES</span></span>

## <span data-ttu-id="5db10-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5db10-148">RELATED LINKS</span></span>
