---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADUser.md
ms.openlocfilehash: 39413c8279b84bb75d3e86bbf41ff40afe05ad06
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223642"
---
# <span data-ttu-id="1413e-101">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="1413e-101">Remove-AzADUser</span></span>

## <span data-ttu-id="1413e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1413e-102">SYNOPSIS</span></span>
<span data-ttu-id="1413e-103">Usuwa użytkownika usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1413e-103">Deletes an active directory user.</span></span>

## <span data-ttu-id="1413e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1413e-104">SYNTAX</span></span>

### <span data-ttu-id="1413e-105">UPNOrObjectIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1413e-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Remove-AzADUser -UPNOrObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1413e-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="1413e-106">UPNParameterSet</span></span>
```
Remove-AzADUser -UserPrincipalName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1413e-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1413e-107">ObjectIdParameterSet</span></span>
```
Remove-AzADUser -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1413e-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1413e-108">DisplayNameParameterSet</span></span>
```
Remove-AzADUser -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1413e-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1413e-109">InputObjectParameterSet</span></span>
```
Remove-AzADUser -InputObject <PSADUser> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1413e-110">Opis</span><span class="sxs-lookup"><span data-stu-id="1413e-110">DESCRIPTION</span></span>
<span data-ttu-id="1413e-111">Usuwa użytkownika usługi Active Directory (konto służbowe jest również popularnym znanym jako identyfikator organizacji).</span><span class="sxs-lookup"><span data-stu-id="1413e-111">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="1413e-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1413e-112">EXAMPLES</span></span>

### <span data-ttu-id="1413e-113">Przykład 1: Usuwanie użytkownika według głównej nazwy użytkownika</span><span class="sxs-lookup"><span data-stu-id="1413e-113">Example 1: Remove a user by user principal name</span></span>

```powershell
PS C:\> Remove-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="1413e-114">Usuwa użytkownika o nazwie głównej użytkownika " foo@domain.com " z dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="1413e-114">Removes the user with user principal name "foo@domain.com" from the tenant.</span></span>

### <span data-ttu-id="1413e-115">Przykład 2: Usuwanie użytkownika według identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="1413e-115">Example 2: Remove a user by object id</span></span>

```powershell
PS C:\> Remove-AzADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69
```

<span data-ttu-id="1413e-116">Usuwa użytkownika o identyfikatorze obiektu "7a9582cf-88c4-4319-842b-7a5d60967a69" z dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="1413e-116">Removes the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' from the tenant.</span></span>

### <span data-ttu-id="1413e-117">Przykład 3: Usuwanie użytkownika przez rurociąg</span><span class="sxs-lookup"><span data-stu-id="1413e-117">Example 3: Remove a user by piping</span></span>

```powershell
PS C:\> Get-AzADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69 | Remove-AzADUser
```

<span data-ttu-id="1413e-118">Pobiera użytkownika o identyfikatorze obiektu "7a9582cf-88c4-4319-842b-7a5d60967a69" oraz potokach, które zostaną usunięte przez polecenie cmdlet Remove-AzADUser, aby usunąć użytkownika z dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="1413e-118">Gets the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' and pipes that to the Remove-AzADUser cmdlet to remove the user from the tenant.</span></span>

## <span data-ttu-id="1413e-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1413e-119">PARAMETERS</span></span>

### <span data-ttu-id="1413e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1413e-120">-DefaultProfile</span></span>
<span data-ttu-id="1413e-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1413e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1413e-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1413e-122">-DisplayName</span></span>
<span data-ttu-id="1413e-123">Nazwa wyświetlana użytkownika, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="1413e-123">The display name of the user to be deleted.</span></span>

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

### <span data-ttu-id="1413e-124">-Force</span><span class="sxs-lookup"><span data-stu-id="1413e-124">-Force</span></span>
<span data-ttu-id="1413e-125">Jeśli ta osoba jest określona, nie prosi o potwierdzenie usunięcia użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1413e-125">If specified, doesn't ask for confirmation for deleting the user.</span></span>

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

### <span data-ttu-id="1413e-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1413e-126">-InputObject</span></span>
<span data-ttu-id="1413e-127">Obiekt użytkownika, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="1413e-127">The user object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADUser
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1413e-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="1413e-128">-ObjectId</span></span>
<span data-ttu-id="1413e-129">Identyfikator obiektu użytkownika, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="1413e-129">The object id of the user to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1413e-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1413e-130">-PassThru</span></span>
<span data-ttu-id="1413e-131">Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="1413e-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="1413e-132">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="1413e-132">-UPNOrObjectId</span></span>
<span data-ttu-id="1413e-133">Główna nazwa użytkownika lub identyfikator obiektu (objectId) użytkownika, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="1413e-133">The user principal name or the objectId of the user to be deleted.</span></span>

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

### <span data-ttu-id="1413e-134">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="1413e-134">-UserPrincipalName</span></span>
<span data-ttu-id="1413e-135">Główna nazwa użytkownika, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="1413e-135">The user principal name of the user to be deleted.</span></span>

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

### <span data-ttu-id="1413e-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1413e-136">-Confirm</span></span>
<span data-ttu-id="1413e-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1413e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1413e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1413e-138">-WhatIf</span></span>
<span data-ttu-id="1413e-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1413e-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1413e-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1413e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1413e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1413e-141">CommonParameters</span></span>
<span data-ttu-id="1413e-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1413e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1413e-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1413e-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1413e-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1413e-144">INPUTS</span></span>

### <span data-ttu-id="1413e-145">System. String</span><span class="sxs-lookup"><span data-stu-id="1413e-145">System.String</span></span>

### <span data-ttu-id="1413e-146">Microsoft. Azure. Commands. pozycji. PSADUser</span><span class="sxs-lookup"><span data-stu-id="1413e-146">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="1413e-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1413e-147">OUTPUTS</span></span>

### <span data-ttu-id="1413e-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1413e-148">System.Boolean</span></span>

## <span data-ttu-id="1413e-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1413e-149">NOTES</span></span>

## <span data-ttu-id="1413e-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1413e-150">RELATED LINKS</span></span>

[<span data-ttu-id="1413e-151">Nowe — AzADUser</span><span class="sxs-lookup"><span data-stu-id="1413e-151">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="1413e-152">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="1413e-152">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="1413e-153">Update-AzADUser</span><span class="sxs-lookup"><span data-stu-id="1413e-153">Update-AzADUser</span></span>](./Update-AzADUser.md)

