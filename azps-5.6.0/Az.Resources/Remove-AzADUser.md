---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADUser.md
ms.openlocfilehash: 98d5433ca2a8d557c7ca1924b9edb6e4fdca2b2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970330"
---
# <span data-ttu-id="2aefc-101">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="2aefc-101">Remove-AzADUser</span></span>

## <span data-ttu-id="2aefc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2aefc-102">SYNOPSIS</span></span>
<span data-ttu-id="2aefc-103">Usuwa użytkownika usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2aefc-103">Deletes an active directory user.</span></span>

## <span data-ttu-id="2aefc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2aefc-104">SYNTAX</span></span>

### <span data-ttu-id="2aefc-105">UPNOrObjectIdParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="2aefc-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Remove-AzADUser -UPNOrObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2aefc-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="2aefc-106">UPNParameterSet</span></span>
```
Remove-AzADUser -UserPrincipalName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2aefc-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2aefc-107">ObjectIdParameterSet</span></span>
```
Remove-AzADUser -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2aefc-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2aefc-108">DisplayNameParameterSet</span></span>
```
Remove-AzADUser -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2aefc-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2aefc-109">InputObjectParameterSet</span></span>
```
Remove-AzADUser -InputObject <PSADUser> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2aefc-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="2aefc-110">DESCRIPTION</span></span>
<span data-ttu-id="2aefc-111">Usuwa użytkownika usługi Active Directory (konto służbowe, które jest również popularne jako identyfikator organizacji).</span><span class="sxs-lookup"><span data-stu-id="2aefc-111">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="2aefc-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2aefc-112">EXAMPLES</span></span>

### <span data-ttu-id="2aefc-113">Przykład 1. Usuwanie użytkownika według głównej nazwy użytkownika</span><span class="sxs-lookup"><span data-stu-id="2aefc-113">Example 1: Remove a user by user principal name</span></span>

```powershell
PS C:\> Remove-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="2aefc-114">Usuwa użytkownika o głównej nazwie użytkownika " foo@domain.com " z dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="2aefc-114">Removes the user with user principal name "foo@domain.com" from the tenant.</span></span>

### <span data-ttu-id="2aefc-115">Przykład 2. Usuwanie użytkownika według identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="2aefc-115">Example 2: Remove a user by object id</span></span>

```powershell
PS C:\> Remove-AzADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69
```

<span data-ttu-id="2aefc-116">Usuwa użytkownika o identyfikatorze obiektu "7a9582cf-88c4-4319-842b-7a5d60967a69" z dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="2aefc-116">Removes the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' from the tenant.</span></span>

### <span data-ttu-id="2aefc-117">Przykład 3. Usuwanie użytkownika za pomocą funkcji pipingu</span><span class="sxs-lookup"><span data-stu-id="2aefc-117">Example 3: Remove a user by piping</span></span>

```powershell
PS C:\> Get-AzADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69 | Remove-AzADUser
```

<span data-ttu-id="2aefc-118">Pobiera użytkownika z identyfikatorem obiektu "7a9582cf-88c4-4319-842b-7a5d60967a69" i potokami, które do polecenia cmdlet Remove-AzADUser należy usunąć z dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="2aefc-118">Gets the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' and pipes that to the Remove-AzADUser cmdlet to remove the user from the tenant.</span></span>

## <span data-ttu-id="2aefc-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2aefc-119">PARAMETERS</span></span>

### <span data-ttu-id="2aefc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aefc-120">-DefaultProfile</span></span>
<span data-ttu-id="2aefc-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="2aefc-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2aefc-122">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="2aefc-122">-DisplayName</span></span>
<span data-ttu-id="2aefc-123">Nazwa wyświetlana użytkownika, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="2aefc-123">The display name of the user to be deleted.</span></span>

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

### <span data-ttu-id="2aefc-124">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="2aefc-124">-Force</span></span>
<span data-ttu-id="2aefc-125">Jeśli jest to określone, nie należy prosić o potwierdzenie usunięcia użytkownika.</span><span class="sxs-lookup"><span data-stu-id="2aefc-125">If specified, doesn't ask for confirmation for deleting the user.</span></span>

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

### <span data-ttu-id="2aefc-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2aefc-126">-InputObject</span></span>
<span data-ttu-id="2aefc-127">Obiekt użytkownika do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="2aefc-127">The user object to be deleted.</span></span>

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

### <span data-ttu-id="2aefc-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="2aefc-128">-ObjectId</span></span>
<span data-ttu-id="2aefc-129">Identyfikator obiektu użytkownika do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="2aefc-129">The object id of the user to be deleted.</span></span>

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

### <span data-ttu-id="2aefc-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2aefc-130">-PassThru</span></span>
<span data-ttu-id="2aefc-131">Określenie tej wartości spowoduje zwrócenie wartości prawda, jeśli polecenie zostało pomyślnie określone.</span><span class="sxs-lookup"><span data-stu-id="2aefc-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="2aefc-132">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="2aefc-132">-UPNOrObjectId</span></span>
<span data-ttu-id="2aefc-133">Główna nazwa użytkownika lub identyfikator obiektu użytkownika do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="2aefc-133">The user principal name or the objectId of the user to be deleted.</span></span>

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

### <span data-ttu-id="2aefc-134">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="2aefc-134">-UserPrincipalName</span></span>
<span data-ttu-id="2aefc-135">Główna nazwa użytkownika do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="2aefc-135">The user principal name of the user to be deleted.</span></span>

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

### <span data-ttu-id="2aefc-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2aefc-136">-Confirm</span></span>
<span data-ttu-id="2aefc-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2aefc-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2aefc-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2aefc-138">-WhatIf</span></span>
<span data-ttu-id="2aefc-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2aefc-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2aefc-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2aefc-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2aefc-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aefc-141">CommonParameters</span></span>
<span data-ttu-id="2aefc-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2aefc-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aefc-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2aefc-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aefc-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2aefc-144">INPUTS</span></span>

### <span data-ttu-id="2aefc-145">System.String</span><span class="sxs-lookup"><span data-stu-id="2aefc-145">System.String</span></span>

### <span data-ttu-id="2aefc-146">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="2aefc-146">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="2aefc-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2aefc-147">OUTPUTS</span></span>

### <span data-ttu-id="2aefc-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2aefc-148">System.Boolean</span></span>

## <span data-ttu-id="2aefc-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2aefc-149">NOTES</span></span>

## <span data-ttu-id="2aefc-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2aefc-150">RELATED LINKS</span></span>

[<span data-ttu-id="2aefc-151">New-AzadUser</span><span class="sxs-lookup"><span data-stu-id="2aefc-151">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="2aefc-152">Get-AzadUser</span><span class="sxs-lookup"><span data-stu-id="2aefc-152">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="2aefc-153">Update-azadUser</span><span class="sxs-lookup"><span data-stu-id="2aefc-153">Update-AzADUser</span></span>](./Update-AzADUser.md)

