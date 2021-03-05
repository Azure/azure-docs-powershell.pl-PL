---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/update-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADUser.md
ms.openlocfilehash: 3875b697b801760b2db78ecfa55f3cbfc734b250
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970314"
---
# <span data-ttu-id="b560f-101">Update-AzADUser</span><span class="sxs-lookup"><span data-stu-id="b560f-101">Update-AzADUser</span></span>

## <span data-ttu-id="b560f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b560f-102">SYNOPSIS</span></span>
<span data-ttu-id="b560f-103">Aktualizuje istniejącego użytkownika usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b560f-103">Updates an existing active directory user.</span></span>

## <span data-ttu-id="b560f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b560f-104">SYNTAX</span></span>

### <span data-ttu-id="b560f-105">UPNOrObjectIdParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="b560f-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Update-AzADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b560f-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="b560f-106">UPNParameterSet</span></span>
```
Update-AzADUser -UserPrincipalName <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b560f-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b560f-107">ObjectIdParameterSet</span></span>
```
Update-AzADUser -ObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b560f-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b560f-108">InputObjectParameterSet</span></span>
```
Update-AzADUser -InputObject <PSADUser> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b560f-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="b560f-109">DESCRIPTION</span></span>
<span data-ttu-id="b560f-110">Aktualizuje istniejącego użytkownika usługi Active Directory (konto służbowe lub szkolne, nazywane również identyfikatorem organizacji).</span><span class="sxs-lookup"><span data-stu-id="b560f-110">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="b560f-111">Aby uzyskać więcej informacji: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="b560f-111">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="b560f-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b560f-112">EXAMPLES</span></span>

### <span data-ttu-id="b560f-113">Przykład 1. Aktualizowanie nazwy wyświetlanej użytkownika przy użyciu identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="b560f-113">Example 1: Update the display name of a user using object id</span></span>

```powershell
PS C:\> Update-AzADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 -DisplayName MyNewDisplayName
```

<span data-ttu-id="b560f-114">Aktualizuje nazwę wyświetlaną użytkownika o identyfikatorze obiektu "155a5c10-93a9-4941-a0df-96d83ab5ab24" na "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="b560f-114">Updates the display name of the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="b560f-115">Przykład 2. Aktualizowanie nazwy wyświetlanej użytkownika przy użyciu głównej nazwy użytkownika</span><span class="sxs-lookup"><span data-stu-id="b560f-115">Example 2: Update the display name of a user using user principal name</span></span>

```powershell
PS C:\> Update-AzADUser -UserPrincipalName foo@domain.com -DisplayName MyNewDisplayName
```

<span data-ttu-id="b560f-116">Aktualizuje nazwę wyświetlaną użytkownika za pomocą głównej nazwy użytkownika ' na foo@domain.com 'MyNewDisplayName'.</span><span class="sxs-lookup"><span data-stu-id="b560f-116">Updates the display name of the user with user principal name 'foo@domain.com' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="b560f-117">Przykład 3. Aktualizowanie nazwy wyświetlanej użytkownika za pomocą funkcji rurowania</span><span class="sxs-lookup"><span data-stu-id="b560f-117">Example 3: Update the display name of a user using piping</span></span>

```powershell
PS C:\> Get-AzADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 | Update-AzADUser -DisplayName MyNewDisplayName
```

<span data-ttu-id="b560f-118">Pobiera użytkownika o identyfikatorze obiektu "155a5c10-93a9-4941-a0df-96d83ab5ab24" i potoków, które są do polecenia cmdlet programu Update-AzADUser, aby zaktualizować nazwę wyświetlaną tego użytkownika na "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="b560f-118">Gets the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' and pipes that to the Update-AzADUser cmdlet to update the display name of that user to 'MyNewDisplayName'.</span></span>

## <span data-ttu-id="b560f-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b560f-119">PARAMETERS</span></span>

### <span data-ttu-id="b560f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b560f-120">-DefaultProfile</span></span>
<span data-ttu-id="b560f-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b560f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b560f-122">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="b560f-122">-DisplayName</span></span>
<span data-ttu-id="b560f-123">Nowa nazwa wyświetlana użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b560f-123">New display name for the user.</span></span>

```yaml
Type: System.String
Parameter Sets: UPNOrObjectIdParameterSet, UPNParameterSet, ObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b560f-124">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="b560f-124">-EnableAccount</span></span>
<span data-ttu-id="b560f-125">ma wartość true dla włączenia konta; w przeciwnym razie fałsz.</span><span class="sxs-lookup"><span data-stu-id="b560f-125">true for enabling the account; otherwise, false.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: UPNOrObjectIdParameterSet, UPNParameterSet, ObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b560f-126">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="b560f-126">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="b560f-127">Należy określić, czy użytkownik powinien zmienić hasło podczas następnego pomyślnego logowania.</span><span class="sxs-lookup"><span data-stu-id="b560f-127">It must be specified if the user should change the password on the next successful login.</span></span>
<span data-ttu-id="b560f-128">Prawidłowe hasło jest ważne tylko w przypadku zaktualizowania w przeciwnym razie zostanie zignorowane.</span><span class="sxs-lookup"><span data-stu-id="b560f-128">Only valid if password is updated otherwise it will be ignored.</span></span>

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

### <span data-ttu-id="b560f-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b560f-129">-InputObject</span></span>
<span data-ttu-id="b560f-130">Obiekt reprezentujący użytkownika do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="b560f-130">The object representing the user to be updated.</span></span>

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

### <span data-ttu-id="b560f-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b560f-131">-ObjectId</span></span>
<span data-ttu-id="b560f-132">Identyfikator obiektu użytkownika do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="b560f-132">The object id of the user to be updated.</span></span>

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

### <span data-ttu-id="b560f-133">— Hasło</span><span class="sxs-lookup"><span data-stu-id="b560f-133">-Password</span></span>
<span data-ttu-id="b560f-134">Nowe hasło użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b560f-134">New password for the user.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: UPNOrObjectIdParameterSet, UPNParameterSet, ObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b560f-135">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="b560f-135">-UPNOrObjectId</span></span>
<span data-ttu-id="b560f-136">Główna nazwa użytkownika lub identyfikator obiektu użytkownika do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="b560f-136">The user principal name or object id of the user to be updated.</span></span>

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

### <span data-ttu-id="b560f-137">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="b560f-137">-UserPrincipalName</span></span>
<span data-ttu-id="b560f-138">Główna nazwa użytkownika do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="b560f-138">The user principal name of the user to be updated.</span></span>

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

### <span data-ttu-id="b560f-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b560f-139">-Confirm</span></span>
<span data-ttu-id="b560f-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b560f-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b560f-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b560f-141">-WhatIf</span></span>
<span data-ttu-id="b560f-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b560f-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b560f-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b560f-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b560f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b560f-144">CommonParameters</span></span>
<span data-ttu-id="b560f-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b560f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b560f-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b560f-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b560f-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b560f-147">INPUTS</span></span>

### <span data-ttu-id="b560f-148">System.String</span><span class="sxs-lookup"><span data-stu-id="b560f-148">System.String</span></span>

### <span data-ttu-id="b560f-149">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="b560f-149">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

### <span data-ttu-id="b560f-150">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b560f-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b560f-151">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="b560f-151">System.Security.SecureString</span></span>

## <span data-ttu-id="b560f-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b560f-152">OUTPUTS</span></span>

### <span data-ttu-id="b560f-153">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="b560f-153">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="b560f-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b560f-154">NOTES</span></span>

## <span data-ttu-id="b560f-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b560f-155">RELATED LINKS</span></span>
