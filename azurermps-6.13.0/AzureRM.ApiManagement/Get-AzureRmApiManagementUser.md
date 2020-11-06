---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
ms.openlocfilehash: 8f02b88115ec6dc415ecf6cf5464503d61778cca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547699"
---
# <span data-ttu-id="3a788-101">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="3a788-101">Get-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="3a788-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3a788-102">SYNOPSIS</span></span>
<span data-ttu-id="3a788-103">Pobiera użytkownika lub użytkowników.</span><span class="sxs-lookup"><span data-stu-id="3a788-103">Gets a user or users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a788-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3a788-104">SYNTAX</span></span>

### <span data-ttu-id="3a788-105">GeAllUsers (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3a788-105">GeAllUsers (Default)</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3a788-106">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="3a788-106">GetByUserId</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a788-107">GetByUser</span><span class="sxs-lookup"><span data-stu-id="3a788-107">GetByUser</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a788-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3a788-108">DESCRIPTION</span></span>
<span data-ttu-id="3a788-109">Polecenie cmdlet **Get-AzureRmApiManagementUser** pobiera określonego użytkownika lub wszystkich użytkowników, jeśli nie określono żadnego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3a788-109">The **Get-AzureRmApiManagementUser** cmdlet gets a specified user, or all users, if no user is specified.</span></span>

## <span data-ttu-id="3a788-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3a788-110">EXAMPLES</span></span>

### <span data-ttu-id="3a788-111">Przykład 1: Pobierz wszystkich użytkowników</span><span class="sxs-lookup"><span data-stu-id="3a788-111">Example 1: Get all users</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext
```

<span data-ttu-id="3a788-112">To polecenie pobiera wszystkich użytkowników.</span><span class="sxs-lookup"><span data-stu-id="3a788-112">This command gets all users.</span></span>

### <span data-ttu-id="3a788-113">Przykład 2: Uzyskaj użytkownika według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="3a788-113">Example 2: Get a user by ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="3a788-114">To polecenie pobiera użytkownika według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="3a788-114">This command gets a user by ID.</span></span>

### <span data-ttu-id="3a788-115">Przykład: pobieranie użytkowników według nazwisk</span><span class="sxs-lookup"><span data-stu-id="3a788-115">Example: Get users by last name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -LastName "Fuller"
```

<span data-ttu-id="3a788-116">To polecenie umożliwia użytkownikom, których imiona i nazwiska są określone przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3a788-116">This command gets users that have a specified last name, Fuller.</span></span>

### <span data-ttu-id="3a788-117">Przykład 4: Uzyskaj użytkownikowi na podstawie adresu e-mail</span><span class="sxs-lookup"><span data-stu-id="3a788-117">Example 4: Get a user by email address</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -Email "user@contoso.com"
```

<span data-ttu-id="3a788-118">To polecenie uzyskuje użytkownika o określonym adresie e-mail.</span><span class="sxs-lookup"><span data-stu-id="3a788-118">This command gets the user that has the specified email address.</span></span>

### <span data-ttu-id="3a788-119">Przykład 5: uzyskiwanie wszystkich użytkowników w grupie</span><span class="sxs-lookup"><span data-stu-id="3a788-119">Example 5: Get all users within a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -GroupId "0001"
```

<span data-ttu-id="3a788-120">To polecenie pobiera wszystkich użytkowników w określonej grupie.</span><span class="sxs-lookup"><span data-stu-id="3a788-120">This command gets all users within the specified group.</span></span>

## <span data-ttu-id="3a788-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3a788-121">PARAMETERS</span></span>

### <span data-ttu-id="3a788-122">-Context</span><span class="sxs-lookup"><span data-stu-id="3a788-122">-Context</span></span>
<span data-ttu-id="3a788-123">Określa wystąpienie **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="3a788-123">Specifies an instance of **PsApiManagementContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a788-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a788-124">-DefaultProfile</span></span>
<span data-ttu-id="3a788-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3a788-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a788-126">-Mail</span><span class="sxs-lookup"><span data-stu-id="3a788-126">-Email</span></span>
<span data-ttu-id="3a788-127">Określa adres e-mail użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3a788-127">Specifies the email address of the user.</span></span>
<span data-ttu-id="3a788-128">Jeśli ten parametr jest określony, to polecenie cmdlet odnajdzie użytkownika pocztą e-mail.</span><span class="sxs-lookup"><span data-stu-id="3a788-128">If this parameter is specified, this cmdlet finds a user by email.</span></span>
<span data-ttu-id="3a788-129">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="3a788-129">This parameter is optional.</span></span>

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

### <span data-ttu-id="3a788-130">-FirstName</span><span class="sxs-lookup"><span data-stu-id="3a788-130">-FirstName</span></span>
<span data-ttu-id="3a788-131">Określa Imię użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3a788-131">Specifies the first name of the user.</span></span>
<span data-ttu-id="3a788-132">Jeśli ten parametr jest określony, to polecenie cmdlet odnajdzie użytkownika według imienia i nazwiska.</span><span class="sxs-lookup"><span data-stu-id="3a788-132">If this parameter is specified, this cmdlet finds a user by first name.</span></span>
<span data-ttu-id="3a788-133">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="3a788-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="3a788-134">-GroupId</span><span class="sxs-lookup"><span data-stu-id="3a788-134">-GroupId</span></span>
<span data-ttu-id="3a788-135">Określa identyfikator grupy.</span><span class="sxs-lookup"><span data-stu-id="3a788-135">Specifies the group identifier.</span></span>
<span data-ttu-id="3a788-136">Jeśli ta funkcja jest określona, to polecenie cmdlet odnajdzie wszystkich użytkowników w określonej grupie.</span><span class="sxs-lookup"><span data-stu-id="3a788-136">If specified, this cmdlet finds all users within the specified group.</span></span>
<span data-ttu-id="3a788-137">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="3a788-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="3a788-138">-LastName</span><span class="sxs-lookup"><span data-stu-id="3a788-138">-LastName</span></span>
<span data-ttu-id="3a788-139">Określa nazwisko użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3a788-139">Specifies the last name of a user.</span></span>
<span data-ttu-id="3a788-140">Jeśli ta funkcja jest określona, to polecenie cmdlet wyszukuje użytkowników według nazwiska.</span><span class="sxs-lookup"><span data-stu-id="3a788-140">If specified, this cmdlet finds users by last name.</span></span>
<span data-ttu-id="3a788-141">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="3a788-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="3a788-142">-State</span><span class="sxs-lookup"><span data-stu-id="3a788-142">-State</span></span>
<span data-ttu-id="3a788-143">Określa stan użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3a788-143">Specifies the user state.</span></span>
<span data-ttu-id="3a788-144">Jeśli ta funkcja jest określona, to polecenie cmdlet umożliwia znalezienie użytkowników w tym stanie.</span><span class="sxs-lookup"><span data-stu-id="3a788-144">If specified, this cmdlet finds users in this state.</span></span>
<span data-ttu-id="3a788-145">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="3a788-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="3a788-146">-UserId</span><span class="sxs-lookup"><span data-stu-id="3a788-146">-UserId</span></span>
<span data-ttu-id="3a788-147">Określa identyfikator użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3a788-147">Specifies a user ID.</span></span>
<span data-ttu-id="3a788-148">Jeśli ta funkcja jest określona, to polecenie cmdlet odnajdzie użytkownika przy użyciu tego identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="3a788-148">If specified, this cmdlet finds the user by this identifier.</span></span>
<span data-ttu-id="3a788-149">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="3a788-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="3a788-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a788-150">CommonParameters</span></span>
<span data-ttu-id="3a788-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a788-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a788-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a788-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a788-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a788-153">INPUTS</span></span>

### <span data-ttu-id="3a788-154">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3a788-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3a788-155">System. String</span><span class="sxs-lookup"><span data-stu-id="3a788-155">System.String</span></span>

### <span data-ttu-id="3a788-156">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. servicemanagement. modele. PsApiManagementUserState, Microsoft. Azure. Commands. ApiManagement. servicemanagement, Version = 6.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="3a788-156">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.Commands.ApiManagement.ServiceManagement, Version=6.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="3a788-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3a788-157">OUTPUTS</span></span>

### <span data-ttu-id="3a788-158">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="3a788-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="3a788-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3a788-159">NOTES</span></span>

## <span data-ttu-id="3a788-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a788-160">RELATED LINKS</span></span>

[<span data-ttu-id="3a788-161">Nowe — AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="3a788-161">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="3a788-162">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="3a788-162">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)

[<span data-ttu-id="3a788-163">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="3a788-163">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


