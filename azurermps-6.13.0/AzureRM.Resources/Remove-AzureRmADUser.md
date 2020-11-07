---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADUser.md
ms.openlocfilehash: 1b863b0bc9cb90caca4d7431ec6835cb75836609
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718279"
---
# <span data-ttu-id="fc4bb-101">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="fc4bb-101">Remove-AzureRmADUser</span></span>

## <span data-ttu-id="fc4bb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fc4bb-102">SYNOPSIS</span></span>
<span data-ttu-id="fc4bb-103">Usuwa użytkownika usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="fc4bb-103">Deletes an active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc4bb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fc4bb-104">SYNTAX</span></span>

### <span data-ttu-id="fc4bb-105">UPNOrObjectIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fc4bb-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Remove-AzureRmADUser -UPNOrObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc4bb-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc4bb-106">UPNParameterSet</span></span>
```
Remove-AzureRmADUser -UserPrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc4bb-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc4bb-107">ObjectIdParameterSet</span></span>
```
Remove-AzureRmADUser -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc4bb-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc4bb-108">DisplayNameParameterSet</span></span>
```
Remove-AzureRmADUser -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc4bb-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc4bb-109">InputObjectParameterSet</span></span>
```
Remove-AzureRmADUser -InputObject <PSADUser> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc4bb-110">Opis</span><span class="sxs-lookup"><span data-stu-id="fc4bb-110">DESCRIPTION</span></span>
<span data-ttu-id="fc4bb-111">Usuwa użytkownika usługi Active Directory (konto służbowe jest również popularnym znanym jako identyfikator organizacji).</span><span class="sxs-lookup"><span data-stu-id="fc4bb-111">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="fc4bb-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fc4bb-112">EXAMPLES</span></span>

### <span data-ttu-id="fc4bb-113">Przykład 1 — Usuwanie użytkownika według głównej nazwy użytkownika</span><span class="sxs-lookup"><span data-stu-id="fc4bb-113">Example 1 - Remove a user by user principal name</span></span>

```
PS C:\> Remove-AzureRmADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="fc4bb-114">Usuwa użytkownika o nazwie głównej użytkownika " foo@domain.com " z dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="fc4bb-114">Removes the user with user principal name "foo@domain.com" from the tenant.</span></span>

### <span data-ttu-id="fc4bb-115">Przykład 2 — Usuwanie użytkownika według identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="fc4bb-115">Example 2 - Remove a user by object id</span></span>

```
PS C:\> Remove-AzureRmADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69
```

<span data-ttu-id="fc4bb-116">Usuwa użytkownika o identyfikatorze obiektu "7a9582cf-88c4-4319-842b-7a5d60967a69" z dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="fc4bb-116">Removes the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' from the tenant.</span></span>

### <span data-ttu-id="fc4bb-117">Przykład 3 — Usuwanie użytkownika przez rurociąg</span><span class="sxs-lookup"><span data-stu-id="fc4bb-117">Example 3 - Remove a user by piping</span></span>

```
PS C:\> Get-AzureRmADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69 | Remove-AzureRmADUser
```

<span data-ttu-id="fc4bb-118">Pobiera użytkownika o identyfikatorze obiektu "7a9582cf-88c4-4319-842b-7a5d60967a69" oraz potokach, które zostaną usunięte przez polecenie cmdlet Remove-AzureRmADUser, aby usunąć użytkownika z dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="fc4bb-118">Gets the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' and pipes that to the Remove-AzureRmADUser cmdlet to remove the user from the tenant.</span></span>

## <span data-ttu-id="fc4bb-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fc4bb-119">PARAMETERS</span></span>

### <span data-ttu-id="fc4bb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc4bb-120">-DefaultProfile</span></span>
<span data-ttu-id="fc4bb-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="fc4bb-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc4bb-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="fc4bb-122">-DisplayName</span></span>
<span data-ttu-id="fc4bb-123">Nazwa wyświetlana użytkownika, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="fc4bb-123">The display name of the user to be deleted.</span></span>

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

### <span data-ttu-id="fc4bb-124">-Force</span><span class="sxs-lookup"><span data-stu-id="fc4bb-124">-Force</span></span>
<span data-ttu-id="fc4bb-125">Jeśli ta osoba jest określona, nie prosi o potwierdzenie usunięcia użytkownika.</span><span class="sxs-lookup"><span data-stu-id="fc4bb-125">If specified, doesn't ask for confirmation for deleting the user.</span></span>

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

### <span data-ttu-id="fc4bb-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fc4bb-126">-InputObject</span></span>
<span data-ttu-id="fc4bb-127">Obiekt użytkownika, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="fc4bb-127">The user object to be deleted.</span></span>

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

### <span data-ttu-id="fc4bb-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="fc4bb-128">-ObjectId</span></span>
<span data-ttu-id="fc4bb-129">Identyfikator obiektu użytkownika, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="fc4bb-129">The object id of the user to be deleted.</span></span>

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

### <span data-ttu-id="fc4bb-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc4bb-130">-PassThru</span></span>
<span data-ttu-id="fc4bb-131">Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="fc4bb-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="fc4bb-132">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="fc4bb-132">-UPNOrObjectId</span></span>
<span data-ttu-id="fc4bb-133">Główna nazwa użytkownika lub identyfikator obiektu (objectId) użytkownika, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="fc4bb-133">The user principal name or the objectId of the user to be deleted.</span></span>

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

### <span data-ttu-id="fc4bb-134">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="fc4bb-134">-UserPrincipalName</span></span>
<span data-ttu-id="fc4bb-135">Główna nazwa użytkownika, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="fc4bb-135">The user principal name of the user to be deleted.</span></span>

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

### <span data-ttu-id="fc4bb-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fc4bb-136">-Confirm</span></span>
<span data-ttu-id="fc4bb-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc4bb-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc4bb-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc4bb-138">-WhatIf</span></span>
<span data-ttu-id="fc4bb-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc4bb-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc4bb-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fc4bb-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc4bb-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc4bb-141">CommonParameters</span></span>
<span data-ttu-id="fc4bb-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc4bb-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc4bb-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc4bb-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc4bb-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fc4bb-144">INPUTS</span></span>

### <span data-ttu-id="fc4bb-145">System. String</span><span class="sxs-lookup"><span data-stu-id="fc4bb-145">System.String</span></span>

### <span data-ttu-id="fc4bb-146">System. GUID</span><span class="sxs-lookup"><span data-stu-id="fc4bb-146">System.Guid</span></span>

### <span data-ttu-id="fc4bb-147">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADUser</span><span class="sxs-lookup"><span data-stu-id="fc4bb-147">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>
<span data-ttu-id="fc4bb-148">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fc4bb-148">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="fc4bb-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fc4bb-149">OUTPUTS</span></span>

### <span data-ttu-id="fc4bb-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fc4bb-150">System.Boolean</span></span>

## <span data-ttu-id="fc4bb-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fc4bb-151">NOTES</span></span>

## <span data-ttu-id="fc4bb-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fc4bb-152">RELATED LINKS</span></span>

[<span data-ttu-id="fc4bb-153">Nowe — AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="fc4bb-153">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="fc4bb-154">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="fc4bb-154">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="fc4bb-155">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="fc4bb-155">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

