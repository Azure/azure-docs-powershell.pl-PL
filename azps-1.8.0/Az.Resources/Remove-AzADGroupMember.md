---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroupMember.md
ms.openlocfilehash: 1196480735705186ad3493b6c34a473baf35dc0e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708322"
---
# <span data-ttu-id="04e8d-101">Remove-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="04e8d-101">Remove-AzADGroupMember</span></span>

## <span data-ttu-id="04e8d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="04e8d-102">SYNOPSIS</span></span>
<span data-ttu-id="04e8d-103">Usuwa użytkownika z grupy usługi AD.</span><span class="sxs-lookup"><span data-stu-id="04e8d-103">Removes a user from an AD group.</span></span>

## <span data-ttu-id="04e8d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="04e8d-104">SYNTAX</span></span>

### <span data-ttu-id="04e8d-105">ExplicitParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="04e8d-105">ExplicitParameterSet (Default)</span></span>
```
Remove-AzADGroupMember [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="04e8d-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="04e8d-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04e8d-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="04e8d-107">MemberObjectIdWithGroupObject</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04e8d-108">MemberObjectIdWithGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="04e8d-108">MemberObjectIdWithGroupObjectId</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04e8d-109">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="04e8d-109">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04e8d-110">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="04e8d-110">MemberUPNWithGroupObjectParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04e8d-111">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="04e8d-111">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04e8d-112">Opis</span><span class="sxs-lookup"><span data-stu-id="04e8d-112">DESCRIPTION</span></span>
<span data-ttu-id="04e8d-113">Usuwa użytkownika z grupy usługi AD.</span><span class="sxs-lookup"><span data-stu-id="04e8d-113">Removes a user from an AD group.</span></span>

## <span data-ttu-id="04e8d-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="04e8d-114">EXAMPLES</span></span>

### <span data-ttu-id="04e8d-115">Przykład 1 — Usuwanie użytkownika z grupy według identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="04e8d-115">Example 1 - Remove a user from a group by object id</span></span>

```
PS C:\> Remove-AzADGroup -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="04e8d-116">Usuwa użytkownika o identyfikatorze obiektu "D9076BBC-D62C-4105-9C78-A7F5BC4A3405" z grupy o identyfikatorze obiektu "85F89C90-780E-4AA6-9F4F-6F268D322EEE".</span><span class="sxs-lookup"><span data-stu-id="04e8d-116">Removes the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' from the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="04e8d-117">Przykład 2 — Usuwanie użytkownika z grupy według połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="04e8d-117">Example 2 - Remove a user from a group by piping</span></span>

```
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="04e8d-118">Pobiera grupę o identyfikatorze obiektu "85F89C90-780E-4AA6-9F4F-6F268D322EEE" i przekazuje ją do polecenia cmdlet Remove-AzADGroupMember, aby usunąć użytkownika z tej grupy.</span><span class="sxs-lookup"><span data-stu-id="04e8d-118">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Remove-AzADGroupMember cmdlet to remove the user to that group.</span></span>

## <span data-ttu-id="04e8d-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="04e8d-119">PARAMETERS</span></span>

### <span data-ttu-id="04e8d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04e8d-120">-DefaultProfile</span></span>
<span data-ttu-id="04e8d-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="04e8d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04e8d-122">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="04e8d-122">-GroupDisplayName</span></span>
<span data-ttu-id="04e8d-123">Nazwa wyświetlana grupy, z której mają zostać usunięte elementy członkowskie.</span><span class="sxs-lookup"><span data-stu-id="04e8d-123">The display name of the group to remove the member(s) from.</span></span>

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

### <span data-ttu-id="04e8d-124">-Groupobject</span><span class="sxs-lookup"><span data-stu-id="04e8d-124">-GroupObject</span></span>
<span data-ttu-id="04e8d-125">Reprezentacja obiektu grupy, z której ma zostać usunięty członek.</span><span class="sxs-lookup"><span data-stu-id="04e8d-125">The object representation of the group to remove the member from.</span></span>

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

### <span data-ttu-id="04e8d-126">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="04e8d-126">-GroupObjectId</span></span>
<span data-ttu-id="04e8d-127">Identyfikator obiektu grupy, z której ma zostać usunięty członek.</span><span class="sxs-lookup"><span data-stu-id="04e8d-127">The object id of the group to remove the member from.</span></span>

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

### <span data-ttu-id="04e8d-128">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="04e8d-128">-MemberObjectId</span></span>
<span data-ttu-id="04e8d-129">Identyfikator obiektu elementu członkowskiego.</span><span class="sxs-lookup"><span data-stu-id="04e8d-129">The object id of the member.</span></span>

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

### <span data-ttu-id="04e8d-130">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="04e8d-130">-MemberUserPrincipalName</span></span>
<span data-ttu-id="04e8d-131">Główna nazwa użytkownika (-y) członków do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="04e8d-131">The UPN of the member(s) to remove.</span></span>

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

### <span data-ttu-id="04e8d-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04e8d-132">-PassThru</span></span>
<span data-ttu-id="04e8d-133">Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="04e8d-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="04e8d-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="04e8d-134">-Confirm</span></span>
<span data-ttu-id="04e8d-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04e8d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04e8d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04e8d-136">-WhatIf</span></span>
<span data-ttu-id="04e8d-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04e8d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04e8d-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="04e8d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04e8d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04e8d-139">CommonParameters</span></span>
<span data-ttu-id="04e8d-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04e8d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04e8d-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04e8d-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04e8d-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="04e8d-142">INPUTS</span></span>

### <span data-ttu-id="04e8d-143">Microsoft. Azure. Commands. pozycji. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="04e8d-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="04e8d-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="04e8d-144">OUTPUTS</span></span>

### <span data-ttu-id="04e8d-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="04e8d-145">System.Boolean</span></span>

## <span data-ttu-id="04e8d-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="04e8d-146">NOTES</span></span>

## <span data-ttu-id="04e8d-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="04e8d-147">RELATED LINKS</span></span>
