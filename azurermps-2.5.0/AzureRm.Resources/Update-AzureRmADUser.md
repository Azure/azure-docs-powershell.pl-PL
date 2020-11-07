---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/update-azurermaduser
schema: 2.0.0
ms.openlocfilehash: 504ce8bd2c7ae5dce3fe859d678b27ad829b2932
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898169"
---
# <span data-ttu-id="b3fd8-101">Update-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="b3fd8-101">Update-AzureRmADUser</span></span>

## <span data-ttu-id="b3fd8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b3fd8-102">SYNOPSIS</span></span>
<span data-ttu-id="b3fd8-103">Aktualizuje istniejącego użytkownika usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b3fd8-103">Updates an existing active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3fd8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b3fd8-104">SYNTAX</span></span>

### <span data-ttu-id="b3fd8-105">UPNOrObjectIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b3fd8-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Update-AzureRmADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3fd8-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3fd8-106">UPNParameterSet</span></span>
```
Update-AzureRmADUser -UserPrincipalName <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3fd8-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3fd8-107">ObjectIdParameterSet</span></span>
```
Update-AzureRmADUser -ObjectId <Guid> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3fd8-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3fd8-108">InputObjectParameterSet</span></span>
```
Update-AzureRmADUser -InputObject <PSADUser> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3fd8-109">Opis</span><span class="sxs-lookup"><span data-stu-id="b3fd8-109">DESCRIPTION</span></span>
<span data-ttu-id="b3fd8-110">Aktualizuje istniejącego użytkownika usługi Active Directory (konto służbowe jest znane również pod nazwą org-ID).</span><span class="sxs-lookup"><span data-stu-id="b3fd8-110">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="b3fd8-111">Aby uzyskać więcej informacji: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="b3fd8-111">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="b3fd8-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b3fd8-112">EXAMPLES</span></span>

### <span data-ttu-id="b3fd8-113">Przykład 1 — Aktualizowanie nazwy wyświetlanej użytkownika przy użyciu identyfikatora obiektu</span><span class="sxs-lookup"><span data-stu-id="b3fd8-113">Example 1 - Update the display name of a user using object id</span></span>

```
PS C:\> Update-AzureRmADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 -DisplayName MyNewDisplayName
```

<span data-ttu-id="b3fd8-114">Aktualizuje nazwę wyświetlaną użytkownika o identyfikatorze obiektu "155a5c10-93a9-4941-a0df-96d83ab5ab24" na "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="b3fd8-114">Updates the display name of the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="b3fd8-115">Przykład 2 — aktualizowanie nazwy wyświetlanej użytkownika przy użyciu nazwy głównej użytkownika</span><span class="sxs-lookup"><span data-stu-id="b3fd8-115">Example 2 - Update the display name of a user using user principal name</span></span>

```
PS C:\> Update-AzureRmADUser -UserPrincipalName foo@domain.com -DisplayName MyNewDisplayName
```

<span data-ttu-id="b3fd8-116">Aktualizuje nazwę wyświetlaną użytkownika o nazwie głównej użytkownika ' foo@domain.com "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="b3fd8-116">Updates the display name of the user with user principal name 'foo@domain.com' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="b3fd8-117">Przykład 3 — Aktualizowanie nazwy wyświetlanej użytkownika przy użyciu połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="b3fd8-117">Example 3 - Update the display name of a user using piping</span></span>

```
PS C:\> Get-AzureRmADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 | Update-AzureRmADUser -DisplayName MyNewDisplayName
```

<span data-ttu-id="b3fd8-118">Pobiera użytkownika o identyfikatorze obiektu "155a5c10-93a9-4941-a0df-96d83ab5ab24" oraz potokach, które są wyświetlane za pomocą polecenia cmdlet Update-AzureRmADUser w celu zaktualizowania nazwy wyświetlanej użytkownika na "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="b3fd8-118">Gets the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' and pipes that to the Update-AzureRmADUser cmdlet to update the display name of that user to 'MyNewDisplayName'.</span></span>

## <span data-ttu-id="b3fd8-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b3fd8-119">PARAMETERS</span></span>

### <span data-ttu-id="b3fd8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3fd8-120">-DefaultProfile</span></span>
<span data-ttu-id="b3fd8-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b3fd8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3fd8-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b3fd8-122">-DisplayName</span></span>
<span data-ttu-id="b3fd8-123">Nowa nazwa wyświetlana użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b3fd8-123">New display name for the user.</span></span>

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

### <span data-ttu-id="b3fd8-124">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="b3fd8-124">-EnableAccount</span></span>
<span data-ttu-id="b3fd8-125">prawda, aby włączyć konto; w przeciwnym razie zwraca wartość false.</span><span class="sxs-lookup"><span data-stu-id="b3fd8-125">true for enabling the account; otherwise, false.</span></span>

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

### <span data-ttu-id="b3fd8-126">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="b3fd8-126">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="b3fd8-127">Należy określić, czy użytkownik powinien zmienić hasło przy następnym poprawnym logowaniu.</span><span class="sxs-lookup"><span data-stu-id="b3fd8-127">It must be specified if the user should change the password on the next successful login.</span></span>
<span data-ttu-id="b3fd8-128">Ważne tylko w przypadku, gdy hasło zostanie zaktualizowane w przeciwnym razie zostanie zignorowane.</span><span class="sxs-lookup"><span data-stu-id="b3fd8-128">Only valid if password is updated otherwise it will be ignored.</span></span>

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

### <span data-ttu-id="b3fd8-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b3fd8-129">-InputObject</span></span>
<span data-ttu-id="b3fd8-130">Obiekt reprezentujący użytkownika, który ma zostać zaktualizowany.</span><span class="sxs-lookup"><span data-stu-id="b3fd8-130">The object representing the user to be updated.</span></span>

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

### <span data-ttu-id="b3fd8-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b3fd8-131">-ObjectId</span></span>
<span data-ttu-id="b3fd8-132">Identyfikator obiektu użytkownika, który ma zostać zaktualizowany.</span><span class="sxs-lookup"><span data-stu-id="b3fd8-132">The object id of the user to be updated.</span></span>

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

### <span data-ttu-id="b3fd8-133">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="b3fd8-133">-Password</span></span>
<span data-ttu-id="b3fd8-134">Nowe hasło dla użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b3fd8-134">New password for the user.</span></span>

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

### <span data-ttu-id="b3fd8-135">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="b3fd8-135">-UPNOrObjectId</span></span>
<span data-ttu-id="b3fd8-136">Główna nazwa użytkownika lub identyfikator obiektu użytkownika, który ma zostać zaktualizowany.</span><span class="sxs-lookup"><span data-stu-id="b3fd8-136">The user principal name or object id of the user to be updated.</span></span>

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

### <span data-ttu-id="b3fd8-137">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="b3fd8-137">-UserPrincipalName</span></span>
<span data-ttu-id="b3fd8-138">Główna nazwa użytkownika, który ma zostać zaktualizowany.</span><span class="sxs-lookup"><span data-stu-id="b3fd8-138">The user principal name of the user to be updated.</span></span>

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

### <span data-ttu-id="b3fd8-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b3fd8-139">-Confirm</span></span>
<span data-ttu-id="b3fd8-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3fd8-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3fd8-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3fd8-141">-WhatIf</span></span>
<span data-ttu-id="b3fd8-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3fd8-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3fd8-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b3fd8-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3fd8-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3fd8-144">CommonParameters</span></span>
<span data-ttu-id="b3fd8-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3fd8-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3fd8-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3fd8-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3fd8-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b3fd8-147">INPUTS</span></span>

### <span data-ttu-id="b3fd8-148">System. String</span><span class="sxs-lookup"><span data-stu-id="b3fd8-148">System.String</span></span>

### <span data-ttu-id="b3fd8-149">System. GUID</span><span class="sxs-lookup"><span data-stu-id="b3fd8-149">System.Guid</span></span>

### <span data-ttu-id="b3fd8-150">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADUser</span><span class="sxs-lookup"><span data-stu-id="b3fd8-150">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>
<span data-ttu-id="b3fd8-151">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b3fd8-151">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="b3fd8-152">System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b3fd8-152">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="b3fd8-153">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="b3fd8-153">System.Security.SecureString</span></span>

## <span data-ttu-id="b3fd8-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b3fd8-154">OUTPUTS</span></span>

### <span data-ttu-id="b3fd8-155">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADUser</span><span class="sxs-lookup"><span data-stu-id="b3fd8-155">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="b3fd8-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b3fd8-156">NOTES</span></span>

## <span data-ttu-id="b3fd8-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b3fd8-157">RELATED LINKS</span></span>
