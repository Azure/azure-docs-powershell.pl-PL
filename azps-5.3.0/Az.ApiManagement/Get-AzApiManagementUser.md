---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUser.md
ms.openlocfilehash: 44f351870e97d227484bd09be1e75b8cb19ac723
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502455"
---
# <span data-ttu-id="1aa3e-101">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="1aa3e-101">Get-AzApiManagementUser</span></span>

## <span data-ttu-id="1aa3e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1aa3e-102">SYNOPSIS</span></span>
<span data-ttu-id="1aa3e-103">Pobiera użytkownika lub użytkowników.</span><span class="sxs-lookup"><span data-stu-id="1aa3e-103">Gets a user or users.</span></span>

## <span data-ttu-id="1aa3e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1aa3e-104">SYNTAX</span></span>

### <span data-ttu-id="1aa3e-105">GeAllUsers (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1aa3e-105">GeAllUsers (Default)</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1aa3e-106">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="1aa3e-106">GetByUserId</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1aa3e-107">GetByUser</span><span class="sxs-lookup"><span data-stu-id="1aa3e-107">GetByUser</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1aa3e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="1aa3e-108">DESCRIPTION</span></span>
<span data-ttu-id="1aa3e-109">Polecenie cmdlet **Get-AzApiManagementUser** pobiera określonego użytkownika lub wszystkich użytkowników, jeśli nie określono żadnego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1aa3e-109">The **Get-AzApiManagementUser** cmdlet gets a specified user, or all users, if no user is specified.</span></span>

## <span data-ttu-id="1aa3e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1aa3e-110">EXAMPLES</span></span>

### <span data-ttu-id="1aa3e-111">Przykład 1: Pobierz wszystkich użytkowników</span><span class="sxs-lookup"><span data-stu-id="1aa3e-111">Example 1: Get all users</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext
```

<span data-ttu-id="1aa3e-112">To polecenie pobiera wszystkich użytkowników.</span><span class="sxs-lookup"><span data-stu-id="1aa3e-112">This command gets all users.</span></span>

### <span data-ttu-id="1aa3e-113">Przykład 2: Uzyskaj użytkownika według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="1aa3e-113">Example 2: Get a user by ID</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="1aa3e-114">To polecenie pobiera użytkownika według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="1aa3e-114">This command gets a user by ID.</span></span>

### <span data-ttu-id="1aa3e-115">Przykład 3: Uzyskaj użytkowników według nazwisk</span><span class="sxs-lookup"><span data-stu-id="1aa3e-115">Example 3: Get users by last name</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -LastName "Fuller"
```

<span data-ttu-id="1aa3e-116">To polecenie umożliwia użytkownikom, których imiona i nazwiska są określone przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1aa3e-116">This command gets users that have a specified last name, Fuller.</span></span>

### <span data-ttu-id="1aa3e-117">Przykład 4: Uzyskaj użytkownikowi na podstawie adresu e-mail</span><span class="sxs-lookup"><span data-stu-id="1aa3e-117">Example 4: Get a user by email address</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -Email "user@contoso.com"
```

<span data-ttu-id="1aa3e-118">To polecenie uzyskuje użytkownika o określonym adresie e-mail.</span><span class="sxs-lookup"><span data-stu-id="1aa3e-118">This command gets the user that has the specified email address.</span></span>

### <span data-ttu-id="1aa3e-119">Przykład 5: uzyskiwanie wszystkich użytkowników w grupie</span><span class="sxs-lookup"><span data-stu-id="1aa3e-119">Example 5: Get all users within a group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -GroupId "0001"
```

<span data-ttu-id="1aa3e-120">To polecenie pobiera wszystkich użytkowników w określonej grupie.</span><span class="sxs-lookup"><span data-stu-id="1aa3e-120">This command gets all users within the specified group.</span></span>

## <span data-ttu-id="1aa3e-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1aa3e-121">PARAMETERS</span></span>

### <span data-ttu-id="1aa3e-122">-Context</span><span class="sxs-lookup"><span data-stu-id="1aa3e-122">-Context</span></span>
<span data-ttu-id="1aa3e-123">Określa wystąpienie **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="1aa3e-123">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="1aa3e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1aa3e-124">-DefaultProfile</span></span>
<span data-ttu-id="1aa3e-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1aa3e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1aa3e-126">-Mail</span><span class="sxs-lookup"><span data-stu-id="1aa3e-126">-Email</span></span>
<span data-ttu-id="1aa3e-127">Określa adres e-mail użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1aa3e-127">Specifies the email address of the user.</span></span>
<span data-ttu-id="1aa3e-128">Jeśli ten parametr jest określony, to polecenie cmdlet odnajdzie użytkownika pocztą e-mail.</span><span class="sxs-lookup"><span data-stu-id="1aa3e-128">If this parameter is specified, this cmdlet finds a user by email.</span></span>
<span data-ttu-id="1aa3e-129">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="1aa3e-129">This parameter is optional.</span></span>

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

### <span data-ttu-id="1aa3e-130">-FirstName</span><span class="sxs-lookup"><span data-stu-id="1aa3e-130">-FirstName</span></span>
<span data-ttu-id="1aa3e-131">Określa Imię użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1aa3e-131">Specifies the first name of the user.</span></span>
<span data-ttu-id="1aa3e-132">Jeśli ten parametr jest określony, to polecenie cmdlet odnajdzie użytkownika według imienia i nazwiska.</span><span class="sxs-lookup"><span data-stu-id="1aa3e-132">If this parameter is specified, this cmdlet finds a user by first name.</span></span>
<span data-ttu-id="1aa3e-133">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="1aa3e-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="1aa3e-134">-GroupId</span><span class="sxs-lookup"><span data-stu-id="1aa3e-134">-GroupId</span></span>
<span data-ttu-id="1aa3e-135">Określa identyfikator grupy.</span><span class="sxs-lookup"><span data-stu-id="1aa3e-135">Specifies the group identifier.</span></span>
<span data-ttu-id="1aa3e-136">Jeśli ta funkcja jest określona, to polecenie cmdlet odnajdzie wszystkich użytkowników w określonej grupie.</span><span class="sxs-lookup"><span data-stu-id="1aa3e-136">If specified, this cmdlet finds all users within the specified group.</span></span>
<span data-ttu-id="1aa3e-137">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="1aa3e-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="1aa3e-138">-LastName</span><span class="sxs-lookup"><span data-stu-id="1aa3e-138">-LastName</span></span>
<span data-ttu-id="1aa3e-139">Określa nazwisko użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1aa3e-139">Specifies the last name of a user.</span></span>
<span data-ttu-id="1aa3e-140">Jeśli ta funkcja jest określona, to polecenie cmdlet wyszukuje użytkowników według nazwiska.</span><span class="sxs-lookup"><span data-stu-id="1aa3e-140">If specified, this cmdlet finds users by last name.</span></span>
<span data-ttu-id="1aa3e-141">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="1aa3e-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="1aa3e-142">-State</span><span class="sxs-lookup"><span data-stu-id="1aa3e-142">-State</span></span>
<span data-ttu-id="1aa3e-143">Określa stan użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1aa3e-143">Specifies the user state.</span></span>
<span data-ttu-id="1aa3e-144">Jeśli ta funkcja jest określona, to polecenie cmdlet umożliwia znalezienie użytkowników w tym stanie.</span><span class="sxs-lookup"><span data-stu-id="1aa3e-144">If specified, this cmdlet finds users in this state.</span></span>
<span data-ttu-id="1aa3e-145">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="1aa3e-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="1aa3e-146">-UserId</span><span class="sxs-lookup"><span data-stu-id="1aa3e-146">-UserId</span></span>
<span data-ttu-id="1aa3e-147">Określa identyfikator użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1aa3e-147">Specifies a user ID.</span></span>
<span data-ttu-id="1aa3e-148">Jeśli ta funkcja jest określona, to polecenie cmdlet odnajdzie użytkownika przy użyciu tego identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="1aa3e-148">If specified, this cmdlet finds the user by this identifier.</span></span>
<span data-ttu-id="1aa3e-149">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="1aa3e-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="1aa3e-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1aa3e-150">CommonParameters</span></span>
<span data-ttu-id="1aa3e-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1aa3e-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1aa3e-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1aa3e-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1aa3e-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1aa3e-153">INPUTS</span></span>

### <span data-ttu-id="1aa3e-154">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1aa3e-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1aa3e-155">System. String</span><span class="sxs-lookup"><span data-stu-id="1aa3e-155">System.String</span></span>

### <span data-ttu-id="1aa3e-156">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. servicemanagement. modele. PsApiManagementUserState, Microsoft. Azure. PowerShell. cmdlet. ApiManagement. servicemanagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="1aa3e-156">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="1aa3e-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1aa3e-157">OUTPUTS</span></span>

### <span data-ttu-id="1aa3e-158">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="1aa3e-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="1aa3e-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1aa3e-159">NOTES</span></span>

## <span data-ttu-id="1aa3e-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1aa3e-160">RELATED LINKS</span></span>

[<span data-ttu-id="1aa3e-161">Nowe — AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="1aa3e-161">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="1aa3e-162">Remove-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="1aa3e-162">Remove-AzApiManagementUser</span></span>](./Remove-AzApiManagementUser.md)

[<span data-ttu-id="1aa3e-163">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="1aa3e-163">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


