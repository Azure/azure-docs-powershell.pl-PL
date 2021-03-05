---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUser.md
ms.openlocfilehash: bd5a83513c23bd4fae8c033e690cb6875c2e98c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995751"
---
# <span data-ttu-id="7860f-101">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="7860f-101">Get-AzApiManagementUser</span></span>

## <span data-ttu-id="7860f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7860f-102">SYNOPSIS</span></span>
<span data-ttu-id="7860f-103">Pobiera użytkownika lub użytkowników.</span><span class="sxs-lookup"><span data-stu-id="7860f-103">Gets a user or users.</span></span>

## <span data-ttu-id="7860f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7860f-104">SYNTAX</span></span>

### <span data-ttu-id="7860f-105">GeAllUsers (Default)</span><span class="sxs-lookup"><span data-stu-id="7860f-105">GeAllUsers (Default)</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7860f-106">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="7860f-106">GetByUserId</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7860f-107">GetByUser</span><span class="sxs-lookup"><span data-stu-id="7860f-107">GetByUser</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7860f-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="7860f-108">DESCRIPTION</span></span>
<span data-ttu-id="7860f-109">Polecenie **cmdlet Get-AzApiManagementUser** pobiera określonego użytkownika lub wszystkich użytkowników, jeśli nie określono żadnego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7860f-109">The **Get-AzApiManagementUser** cmdlet gets a specified user, or all users, if no user is specified.</span></span>

## <span data-ttu-id="7860f-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7860f-110">EXAMPLES</span></span>

### <span data-ttu-id="7860f-111">Przykład 1. Pobierz wszystkich użytkowników</span><span class="sxs-lookup"><span data-stu-id="7860f-111">Example 1: Get all users</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext
```

<span data-ttu-id="7860f-112">To polecenie pobiera wszystkich użytkowników.</span><span class="sxs-lookup"><span data-stu-id="7860f-112">This command gets all users.</span></span>

### <span data-ttu-id="7860f-113">Przykład 2. Uzyskiwanie użytkownika według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="7860f-113">Example 2: Get a user by ID</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="7860f-114">To polecenie pobiera użytkownika według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="7860f-114">This command gets a user by ID.</span></span>

### <span data-ttu-id="7860f-115">Przykład 3. Uzyskiwanie użytkowników według nazwisk</span><span class="sxs-lookup"><span data-stu-id="7860f-115">Example 3: Get users by last name</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -LastName "Fuller"
```

<span data-ttu-id="7860f-116">To polecenie pobiera użytkowników o określonym nazwisku o nazwie Fuller.</span><span class="sxs-lookup"><span data-stu-id="7860f-116">This command gets users that have a specified last name, Fuller.</span></span>

### <span data-ttu-id="7860f-117">Przykład 4. Uzyskiwanie użytkownika za pomocą adresu e-mail</span><span class="sxs-lookup"><span data-stu-id="7860f-117">Example 4: Get a user by email address</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -Email "user@contoso.com"
```

<span data-ttu-id="7860f-118">To polecenie pobiera użytkownika, który ma określony adres e-mail.</span><span class="sxs-lookup"><span data-stu-id="7860f-118">This command gets the user that has the specified email address.</span></span>

### <span data-ttu-id="7860f-119">Przykład 5. Uzyskiwanie wszystkich użytkowników w grupie</span><span class="sxs-lookup"><span data-stu-id="7860f-119">Example 5: Get all users within a group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -GroupId "0001"
```

<span data-ttu-id="7860f-120">To polecenie pobiera wszystkich użytkowników w obrębie określonej grupy.</span><span class="sxs-lookup"><span data-stu-id="7860f-120">This command gets all users within the specified group.</span></span>

## <span data-ttu-id="7860f-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7860f-121">PARAMETERS</span></span>

### <span data-ttu-id="7860f-122">— kontekst</span><span class="sxs-lookup"><span data-stu-id="7860f-122">-Context</span></span>
<span data-ttu-id="7860f-123">Określa wystąpienie obiektu **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="7860f-123">Specifies an instance of **PsApiManagementContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7860f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7860f-124">-DefaultProfile</span></span>
<span data-ttu-id="7860f-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7860f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7860f-126">— Poczta e-mail</span><span class="sxs-lookup"><span data-stu-id="7860f-126">-Email</span></span>
<span data-ttu-id="7860f-127">Określa adres e-mail użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7860f-127">Specifies the email address of the user.</span></span>
<span data-ttu-id="7860f-128">Jeśli ten parametr zostanie określony, to polecenie cmdlet znajdzie użytkownika za pomocą poczty e-mail.</span><span class="sxs-lookup"><span data-stu-id="7860f-128">If this parameter is specified, this cmdlet finds a user by email.</span></span>
<span data-ttu-id="7860f-129">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="7860f-129">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7860f-130">-FirstName</span><span class="sxs-lookup"><span data-stu-id="7860f-130">-FirstName</span></span>
<span data-ttu-id="7860f-131">Określa imię użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7860f-131">Specifies the first name of the user.</span></span>
<span data-ttu-id="7860f-132">Jeśli ten parametr jest określony, to polecenie cmdlet umożliwia znalezienie użytkownika według imienia.</span><span class="sxs-lookup"><span data-stu-id="7860f-132">If this parameter is specified, this cmdlet finds a user by first name.</span></span>
<span data-ttu-id="7860f-133">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="7860f-133">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7860f-134">- GroupId</span><span class="sxs-lookup"><span data-stu-id="7860f-134">-GroupId</span></span>
<span data-ttu-id="7860f-135">Określa identyfikator grupy.</span><span class="sxs-lookup"><span data-stu-id="7860f-135">Specifies the group identifier.</span></span>
<span data-ttu-id="7860f-136">Jeśli zostanie określone, to polecenie cmdlet znajdzie wszystkich użytkowników w określonej grupie.</span><span class="sxs-lookup"><span data-stu-id="7860f-136">If specified, this cmdlet finds all users within the specified group.</span></span>
<span data-ttu-id="7860f-137">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="7860f-137">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7860f-138">-LastName</span><span class="sxs-lookup"><span data-stu-id="7860f-138">-LastName</span></span>
<span data-ttu-id="7860f-139">Określa nazwisko użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7860f-139">Specifies the last name of a user.</span></span>
<span data-ttu-id="7860f-140">Jeśli to określono, to polecenie cmdlet umożliwia znalezienie użytkowników według nazwisk.</span><span class="sxs-lookup"><span data-stu-id="7860f-140">If specified, this cmdlet finds users by last name.</span></span>
<span data-ttu-id="7860f-141">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="7860f-141">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7860f-142">— województwo</span><span class="sxs-lookup"><span data-stu-id="7860f-142">-State</span></span>
<span data-ttu-id="7860f-143">Określa stan użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7860f-143">Specifies the user state.</span></span>
<span data-ttu-id="7860f-144">Jeśli zostanie określone, to polecenie cmdlet znajdzie użytkowników w tym stanie.</span><span class="sxs-lookup"><span data-stu-id="7860f-144">If specified, this cmdlet finds users in this state.</span></span>
<span data-ttu-id="7860f-145">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="7860f-145">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: GetByUser
Aliases:
Accepted values: Active, Blocked, Deleted, Pending

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7860f-146">-UserId</span><span class="sxs-lookup"><span data-stu-id="7860f-146">-UserId</span></span>
<span data-ttu-id="7860f-147">Określa identyfikator użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7860f-147">Specifies a user ID.</span></span>
<span data-ttu-id="7860f-148">Jeśli zostanie określone, to polecenie cmdlet znajdzie użytkownika za pomocą tego identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="7860f-148">If specified, this cmdlet finds the user by this identifier.</span></span>
<span data-ttu-id="7860f-149">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="7860f-149">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUserId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7860f-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7860f-150">CommonParameters</span></span>
<span data-ttu-id="7860f-151">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7860f-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7860f-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7860f-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7860f-153">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7860f-153">INPUTS</span></span>

### <span data-ttu-id="7860f-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7860f-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7860f-155">System.String</span><span class="sxs-lookup"><span data-stu-id="7860f-155">System.String</span></span>

### <span data-ttu-id="7860f-156">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlet.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="7860f-156">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="7860f-157">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7860f-157">OUTPUTS</span></span>

### <span data-ttu-id="7860f-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="7860f-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="7860f-159">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7860f-159">NOTES</span></span>

## <span data-ttu-id="7860f-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7860f-160">RELATED LINKS</span></span>

[<span data-ttu-id="7860f-161">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="7860f-161">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="7860f-162">Remove-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="7860f-162">Remove-AzApiManagementUser</span></span>](./Remove-AzApiManagementUser.md)

[<span data-ttu-id="7860f-163">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="7860f-163">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


