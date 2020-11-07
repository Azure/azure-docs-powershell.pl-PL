---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADUser.md
ms.openlocfilehash: 991b81e9314c5f9c1959e8f352f8c2e218a1b701
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894982"
---
# <span data-ttu-id="ea734-101">Update-AzADUser</span><span class="sxs-lookup"><span data-stu-id="ea734-101">Update-AzADUser</span></span>

## <span data-ttu-id="ea734-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ea734-102">SYNOPSIS</span></span>
<span data-ttu-id="ea734-103">Aktualizuje istniejącego użytkownika usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ea734-103">Updates an existing active directory user.</span></span>

## <span data-ttu-id="ea734-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ea734-104">SYNTAX</span></span>

### <span data-ttu-id="ea734-105">UPNOrObjectIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ea734-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Update-AzADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea734-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea734-106">UPNParameterSet</span></span>
```
Update-AzADUser -UserPrincipalName <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea734-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea734-107">ObjectIdParameterSet</span></span>
```
Update-AzADUser -ObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea734-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea734-108">InputObjectParameterSet</span></span>
```
Update-AzADUser -InputObject <PSADUser> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea734-109">Opis</span><span class="sxs-lookup"><span data-stu-id="ea734-109">DESCRIPTION</span></span>
<span data-ttu-id="ea734-110">Aktualizuje istniejącego użytkownika usługi Active Directory (konto służbowe jest znane również pod nazwą org-ID).</span><span class="sxs-lookup"><span data-stu-id="ea734-110">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="ea734-111">Aby uzyskać więcej informacji: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="ea734-111">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="ea734-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ea734-112">EXAMPLES</span></span>

### <span data-ttu-id="ea734-113">Przykład 1 — Aktualizowanie nazwy wyświetlanej użytkownika przy użyciu identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="ea734-113">Example 1 - Update the display name of a user using object id</span></span>

```
PS C:\> Update-AzADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 -DisplayName MyNewDisplayName
```

<span data-ttu-id="ea734-114">Aktualizuje nazwę wyświetlaną użytkownika o identyfikatorze obiektu "155a5c10-93a9-4941-a0df-96d83ab5ab24" na "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="ea734-114">Updates the display name of the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="ea734-115">Przykład 2 — aktualizowanie nazwy wyświetlanej użytkownika przy użyciu nazwy głównej użytkownika</span><span class="sxs-lookup"><span data-stu-id="ea734-115">Example 2 - Update the display name of a user using user principal name</span></span>

```
PS C:\> Update-AzADUser -UserPrincipalName foo@domain.com -DisplayName MyNewDisplayName
```

<span data-ttu-id="ea734-116">Aktualizuje nazwę wyświetlaną użytkownika o nazwie głównej użytkownika ' foo@domain.com "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="ea734-116">Updates the display name of the user with user principal name 'foo@domain.com' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="ea734-117">Przykład 3 — Aktualizowanie nazwy wyświetlanej użytkownika przy użyciu połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="ea734-117">Example 3 - Update the display name of a user using piping</span></span>

```
PS C:\> Get-AzADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 | Update-AzADUser -DisplayName MyNewDisplayName
```

<span data-ttu-id="ea734-118">Pobiera użytkownika o identyfikatorze obiektu "155a5c10-93a9-4941-a0df-96d83ab5ab24" oraz potokach, które są wyświetlane za pomocą polecenia cmdlet Update-AzADUser w celu zaktualizowania nazwy wyświetlanej użytkownika na "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="ea734-118">Gets the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' and pipes that to the Update-AzADUser cmdlet to update the display name of that user to 'MyNewDisplayName'.</span></span>

## <span data-ttu-id="ea734-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ea734-119">PARAMETERS</span></span>

### <span data-ttu-id="ea734-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea734-120">-DefaultProfile</span></span>
<span data-ttu-id="ea734-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ea734-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea734-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ea734-122">-DisplayName</span></span>
<span data-ttu-id="ea734-123">Nowa nazwa wyświetlana użytkownika.</span><span class="sxs-lookup"><span data-stu-id="ea734-123">New display name for the user.</span></span>

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

### <span data-ttu-id="ea734-124">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="ea734-124">-EnableAccount</span></span>
<span data-ttu-id="ea734-125">prawda, aby włączyć konto; w przeciwnym razie zwraca wartość false.</span><span class="sxs-lookup"><span data-stu-id="ea734-125">true for enabling the account; otherwise, false.</span></span>

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

### <span data-ttu-id="ea734-126">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="ea734-126">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="ea734-127">Należy określić, czy użytkownik powinien zmienić hasło przy następnym poprawnym logowaniu.</span><span class="sxs-lookup"><span data-stu-id="ea734-127">It must be specified if the user should change the password on the next successful login.</span></span>
<span data-ttu-id="ea734-128">Ważne tylko w przypadku, gdy hasło zostanie zaktualizowane w przeciwnym razie zostanie zignorowane.</span><span class="sxs-lookup"><span data-stu-id="ea734-128">Only valid if password is updated otherwise it will be ignored.</span></span>

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

### <span data-ttu-id="ea734-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ea734-129">-InputObject</span></span>
<span data-ttu-id="ea734-130">Obiekt reprezentujący użytkownika, który ma zostać zaktualizowany.</span><span class="sxs-lookup"><span data-stu-id="ea734-130">The object representing the user to be updated.</span></span>

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

### <span data-ttu-id="ea734-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ea734-131">-ObjectId</span></span>
<span data-ttu-id="ea734-132">Identyfikator obiektu użytkownika, który ma zostać zaktualizowany.</span><span class="sxs-lookup"><span data-stu-id="ea734-132">The object id of the user to be updated.</span></span>

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

### <span data-ttu-id="ea734-133">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="ea734-133">-Password</span></span>
<span data-ttu-id="ea734-134">Nowe hasło dla użytkownika.</span><span class="sxs-lookup"><span data-stu-id="ea734-134">New password for the user.</span></span>

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

### <span data-ttu-id="ea734-135">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="ea734-135">-UPNOrObjectId</span></span>
<span data-ttu-id="ea734-136">Główna nazwa użytkownika lub identyfikator obiektu użytkownika, który ma zostać zaktualizowany.</span><span class="sxs-lookup"><span data-stu-id="ea734-136">The user principal name or object id of the user to be updated.</span></span>

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

### <span data-ttu-id="ea734-137">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="ea734-137">-UserPrincipalName</span></span>
<span data-ttu-id="ea734-138">Główna nazwa użytkownika, który ma zostać zaktualizowany.</span><span class="sxs-lookup"><span data-stu-id="ea734-138">The user principal name of the user to be updated.</span></span>

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

### <span data-ttu-id="ea734-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ea734-139">-Confirm</span></span>
<span data-ttu-id="ea734-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea734-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea734-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea734-141">-WhatIf</span></span>
<span data-ttu-id="ea734-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea734-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea734-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ea734-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea734-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea734-144">CommonParameters</span></span>
<span data-ttu-id="ea734-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea734-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea734-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea734-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea734-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea734-147">INPUTS</span></span>

### <span data-ttu-id="ea734-148">System. String</span><span class="sxs-lookup"><span data-stu-id="ea734-148">System.String</span></span>

### <span data-ttu-id="ea734-149">Microsoft. Azure. Commands. pozycji. PSADUser</span><span class="sxs-lookup"><span data-stu-id="ea734-149">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

### <span data-ttu-id="ea734-150">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ea734-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ea734-151">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="ea734-151">System.Security.SecureString</span></span>

## <span data-ttu-id="ea734-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ea734-152">OUTPUTS</span></span>

### <span data-ttu-id="ea734-153">Microsoft. Azure. Commands. pozycji. PSADUser</span><span class="sxs-lookup"><span data-stu-id="ea734-153">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="ea734-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ea734-154">NOTES</span></span>

## <span data-ttu-id="ea734-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ea734-155">RELATED LINKS</span></span>
