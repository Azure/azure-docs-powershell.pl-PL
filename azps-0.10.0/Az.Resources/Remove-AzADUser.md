---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADUser.md
ms.openlocfilehash: 091f54b69cd713d93def4c727181f9c8e7d5b0d6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892425"
---
# <span data-ttu-id="92095-101">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="92095-101">Remove-AzADUser</span></span>

## <span data-ttu-id="92095-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="92095-102">SYNOPSIS</span></span>
<span data-ttu-id="92095-103">Usuwa użytkownika usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="92095-103">Deletes an active directory user.</span></span>

## <span data-ttu-id="92095-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="92095-104">SYNTAX</span></span>

### <span data-ttu-id="92095-105">UPNOrObjectIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="92095-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Remove-AzADUser -UPNOrObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92095-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="92095-106">UPNParameterSet</span></span>
```
Remove-AzADUser -UserPrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92095-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="92095-107">ObjectIdParameterSet</span></span>
```
Remove-AzADUser -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92095-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="92095-108">DisplayNameParameterSet</span></span>
```
Remove-AzADUser -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92095-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="92095-109">InputObjectParameterSet</span></span>
```
Remove-AzADUser -InputObject <PSADUser> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92095-110">Opis</span><span class="sxs-lookup"><span data-stu-id="92095-110">DESCRIPTION</span></span>
<span data-ttu-id="92095-111">Usuwa użytkownika usługi Active Directory (konto służbowe jest również popularnym znanym jako identyfikator organizacji).</span><span class="sxs-lookup"><span data-stu-id="92095-111">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="92095-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="92095-112">EXAMPLES</span></span>

### <span data-ttu-id="92095-113">Przykład 1 — Usuwanie użytkownika według głównej nazwy użytkownika</span><span class="sxs-lookup"><span data-stu-id="92095-113">Example 1 - Remove a user by user principal name</span></span>

```
PS C:\> Remove-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="92095-114">Usuwa użytkownika o nazwie głównej użytkownika " foo@domain.com " z dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="92095-114">Removes the user with user principal name "foo@domain.com" from the tenant.</span></span>

### <span data-ttu-id="92095-115">Przykład 2 — Usuwanie użytkownika według identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="92095-115">Example 2 - Remove a user by object id</span></span>

```
PS C:\> Remove-AzADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69
```

<span data-ttu-id="92095-116">Usuwa użytkownika o identyfikatorze obiektu "7a9582cf-88c4-4319-842b-7a5d60967a69" z dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="92095-116">Removes the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' from the tenant.</span></span>

### <span data-ttu-id="92095-117">Przykład 3 — Usuwanie użytkownika przez rurociąg</span><span class="sxs-lookup"><span data-stu-id="92095-117">Example 3 - Remove a user by piping</span></span>

```
PS C:\> Get-AzADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69 | Remove-AzADUser
```

<span data-ttu-id="92095-118">Pobiera użytkownika o identyfikatorze obiektu "7a9582cf-88c4-4319-842b-7a5d60967a69" oraz potokach, które zostaną usunięte przez polecenie cmdlet Remove-AzADUser, aby usunąć użytkownika z dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="92095-118">Gets the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' and pipes that to the Remove-AzADUser cmdlet to remove the user from the tenant.</span></span>

## <span data-ttu-id="92095-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="92095-119">PARAMETERS</span></span>

### <span data-ttu-id="92095-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92095-120">-DefaultProfile</span></span>
<span data-ttu-id="92095-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="92095-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="92095-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="92095-122">-DisplayName</span></span>
<span data-ttu-id="92095-123">Nazwa wyświetlana użytkownika, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="92095-123">The display name of the user to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92095-124">-Force</span><span class="sxs-lookup"><span data-stu-id="92095-124">-Force</span></span>
<span data-ttu-id="92095-125">Jeśli ta osoba jest określona, nie prosi o potwierdzenie usunięcia użytkownika.</span><span class="sxs-lookup"><span data-stu-id="92095-125">If specified, doesn't ask for confirmation for deleting the user.</span></span>

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

### <span data-ttu-id="92095-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="92095-126">-InputObject</span></span>
<span data-ttu-id="92095-127">Obiekt użytkownika, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="92095-127">The user object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92095-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="92095-128">-ObjectId</span></span>
<span data-ttu-id="92095-129">Identyfikator obiektu użytkownika, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="92095-129">The object id of the user to be deleted.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92095-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92095-130">-PassThru</span></span>
<span data-ttu-id="92095-131">Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="92095-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="92095-132">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="92095-132">-UPNOrObjectId</span></span>
<span data-ttu-id="92095-133">Główna nazwa użytkownika lub identyfikator obiektu (objectId) użytkownika, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="92095-133">The user principal name or the objectId of the user to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: UPNOrObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92095-134">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="92095-134">-UserPrincipalName</span></span>
<span data-ttu-id="92095-135">Główna nazwa użytkownika, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="92095-135">The user principal name of the user to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: UPNParameterSet
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92095-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="92095-136">-Confirm</span></span>
<span data-ttu-id="92095-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92095-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92095-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92095-138">-WhatIf</span></span>
<span data-ttu-id="92095-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92095-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92095-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="92095-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92095-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92095-141">CommonParameters</span></span>
<span data-ttu-id="92095-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92095-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92095-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92095-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92095-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="92095-144">INPUTS</span></span>

### <span data-ttu-id="92095-145">System. String</span><span class="sxs-lookup"><span data-stu-id="92095-145">System.String</span></span>

### <span data-ttu-id="92095-146">System. GUID</span><span class="sxs-lookup"><span data-stu-id="92095-146">System.Guid</span></span>

### <span data-ttu-id="92095-147">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADUser</span><span class="sxs-lookup"><span data-stu-id="92095-147">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>
<span data-ttu-id="92095-148">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="92095-148">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="92095-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="92095-149">OUTPUTS</span></span>

### <span data-ttu-id="92095-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="92095-150">System.Boolean</span></span>

## <span data-ttu-id="92095-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="92095-151">NOTES</span></span>

## <span data-ttu-id="92095-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="92095-152">RELATED LINKS</span></span>

[<span data-ttu-id="92095-153">Nowe — AzADUser</span><span class="sxs-lookup"><span data-stu-id="92095-153">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="92095-154">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="92095-154">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="92095-155">Set-AzADUser</span><span class="sxs-lookup"><span data-stu-id="92095-155">Set-AzADUser</span></span>](./Set-AzADUser.md)

