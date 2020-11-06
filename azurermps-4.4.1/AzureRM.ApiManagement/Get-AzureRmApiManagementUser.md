---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
ms.openlocfilehash: be6c9ee6c0db12e324786052348209703b79601e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525797"
---
# <span data-ttu-id="dc47a-101">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="dc47a-101">Get-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="dc47a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dc47a-102">SYNOPSIS</span></span>
<span data-ttu-id="dc47a-103">Pobiera użytkownika lub użytkowników.</span><span class="sxs-lookup"><span data-stu-id="dc47a-103">Gets a user or users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc47a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dc47a-104">SYNTAX</span></span>

### <span data-ttu-id="dc47a-105">Pobierz wszystkich użytkowników (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="dc47a-105">Get all users (Default)</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dc47a-106">Uzyskaj użytkownika według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="dc47a-106">Get user by ID</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc47a-107">Znajdowanie użytkowników</span><span class="sxs-lookup"><span data-stu-id="dc47a-107">Find users</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc47a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="dc47a-108">DESCRIPTION</span></span>
<span data-ttu-id="dc47a-109">Polecenie cmdlet **Get-AzureRmApiManagementUser** pobiera określonego użytkownika lub wszystkich użytkowników, jeśli nie określono żadnego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="dc47a-109">The **Get-AzureRmApiManagementUser** cmdlet gets a specified user, or all users, if no user is specified.</span></span>

## <span data-ttu-id="dc47a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dc47a-110">EXAMPLES</span></span>

### <span data-ttu-id="dc47a-111">Przykład 1: Pobierz wszystkich użytkowników</span><span class="sxs-lookup"><span data-stu-id="dc47a-111">Example 1: Get all users</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext
```

<span data-ttu-id="dc47a-112">To polecenie pobiera wszystkich użytkowników.</span><span class="sxs-lookup"><span data-stu-id="dc47a-112">This command gets all users.</span></span>

### <span data-ttu-id="dc47a-113">Przykład 2: Uzyskaj użytkownika według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="dc47a-113">Example 2: Get a user by ID</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="dc47a-114">To polecenie pobiera użytkownika według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="dc47a-114">This command gets a user by ID.</span></span>

### <span data-ttu-id="dc47a-115">Przykład: pobieranie użytkowników według nazwisk</span><span class="sxs-lookup"><span data-stu-id="dc47a-115">Example: Get users by last name</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -LastName "Fuller"
```

<span data-ttu-id="dc47a-116">To polecenie umożliwia użytkownikom, których imiona i nazwiska są określone przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="dc47a-116">This command gets users that have a specified last name, Fuller.</span></span>

### <span data-ttu-id="dc47a-117">Przykład 4: Uzyskaj użytkownikowi na podstawie adresu e-mail</span><span class="sxs-lookup"><span data-stu-id="dc47a-117">Example 4: Get a user by email address</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -Email 
"user@contoso.com"
```

<span data-ttu-id="dc47a-118">To polecenie uzyskuje użytkownika o określonym adresie e-mail.</span><span class="sxs-lookup"><span data-stu-id="dc47a-118">This command gets the user that has the specified email address.</span></span>

### <span data-ttu-id="dc47a-119">Przykład 5: uzyskiwanie wszystkich użytkowników w grupie</span><span class="sxs-lookup"><span data-stu-id="dc47a-119">Example 5: Get all users within a group</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -GroupId "0001"
```

<span data-ttu-id="dc47a-120">To polecenie pobiera wszystkich użytkowników w określonej grupie.</span><span class="sxs-lookup"><span data-stu-id="dc47a-120">This command gets all users within the specified group.</span></span>

## <span data-ttu-id="dc47a-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dc47a-121">PARAMETERS</span></span>

### <span data-ttu-id="dc47a-122">-Context</span><span class="sxs-lookup"><span data-stu-id="dc47a-122">-Context</span></span>
<span data-ttu-id="dc47a-123">Określa wystąpienie **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="dc47a-123">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="dc47a-124">-Mail</span><span class="sxs-lookup"><span data-stu-id="dc47a-124">-Email</span></span>
<span data-ttu-id="dc47a-125">Określa adres e-mail użytkownika.</span><span class="sxs-lookup"><span data-stu-id="dc47a-125">Specifies the email address of the user.</span></span>
<span data-ttu-id="dc47a-126">Jeśli ten parametr jest określony, to polecenie cmdlet odnajdzie użytkownika pocztą e-mail.</span><span class="sxs-lookup"><span data-stu-id="dc47a-126">If this parameter is specified, this cmdlet finds a user by email.</span></span>
<span data-ttu-id="dc47a-127">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="dc47a-127">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc47a-128">-FirstName</span><span class="sxs-lookup"><span data-stu-id="dc47a-128">-FirstName</span></span>
<span data-ttu-id="dc47a-129">Określa Imię użytkownika.</span><span class="sxs-lookup"><span data-stu-id="dc47a-129">Specifies the first name of the user.</span></span>
<span data-ttu-id="dc47a-130">Jeśli ten parametr jest określony, to polecenie cmdlet odnajdzie użytkownika według imienia i nazwiska.</span><span class="sxs-lookup"><span data-stu-id="dc47a-130">If this parameter is specified, this cmdlet finds a user by first name.</span></span>
<span data-ttu-id="dc47a-131">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="dc47a-131">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc47a-132">-GroupId</span><span class="sxs-lookup"><span data-stu-id="dc47a-132">-GroupId</span></span>
<span data-ttu-id="dc47a-133">Określa identyfikator grupy.</span><span class="sxs-lookup"><span data-stu-id="dc47a-133">Specifies the group identifier.</span></span>
<span data-ttu-id="dc47a-134">Jeśli ta funkcja jest określona, to polecenie cmdlet odnajdzie wszystkich użytkowników w określonej grupie.</span><span class="sxs-lookup"><span data-stu-id="dc47a-134">If specified, this cmdlet finds all users within the specified group.</span></span>
<span data-ttu-id="dc47a-135">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="dc47a-135">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc47a-136">-LastName</span><span class="sxs-lookup"><span data-stu-id="dc47a-136">-LastName</span></span>
<span data-ttu-id="dc47a-137">Określa nazwisko użytkownika.</span><span class="sxs-lookup"><span data-stu-id="dc47a-137">Specifies the last name of a user.</span></span>
<span data-ttu-id="dc47a-138">Jeśli ta funkcja jest określona, to polecenie cmdlet wyszukuje użytkowników według nazwiska.</span><span class="sxs-lookup"><span data-stu-id="dc47a-138">If specified, this cmdlet finds users by last name.</span></span>
<span data-ttu-id="dc47a-139">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="dc47a-139">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc47a-140">-State</span><span class="sxs-lookup"><span data-stu-id="dc47a-140">-State</span></span>
<span data-ttu-id="dc47a-141">Określa stan użytkownika.</span><span class="sxs-lookup"><span data-stu-id="dc47a-141">Specifies the user state.</span></span>
<span data-ttu-id="dc47a-142">Jeśli ta funkcja jest określona, to polecenie cmdlet umożliwia znalezienie użytkowników w tym stanie.</span><span class="sxs-lookup"><span data-stu-id="dc47a-142">If specified, this cmdlet finds users in this state.</span></span>
<span data-ttu-id="dc47a-143">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="dc47a-143">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: Find users
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc47a-144">-UserId</span><span class="sxs-lookup"><span data-stu-id="dc47a-144">-UserId</span></span>
<span data-ttu-id="dc47a-145">Określa identyfikator użytkownika.</span><span class="sxs-lookup"><span data-stu-id="dc47a-145">Specifies a user ID.</span></span>
<span data-ttu-id="dc47a-146">Jeśli ta funkcja jest określona, to polecenie cmdlet odnajdzie użytkownika przy użyciu tego identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="dc47a-146">If specified, this cmdlet finds the user by this identifier.</span></span>
<span data-ttu-id="dc47a-147">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="dc47a-147">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Get user by ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc47a-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc47a-148">-DefaultProfile</span></span>
<span data-ttu-id="dc47a-149">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dc47a-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc47a-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc47a-150">CommonParameters</span></span>
<span data-ttu-id="dc47a-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc47a-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc47a-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc47a-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc47a-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dc47a-153">INPUTS</span></span>

## <span data-ttu-id="dc47a-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dc47a-154">OUTPUTS</span></span>

### <span data-ttu-id="dc47a-155">IList<Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementUser></span><span class="sxs-lookup"><span data-stu-id="dc47a-155">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser></span></span>

## <span data-ttu-id="dc47a-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dc47a-156">NOTES</span></span>

## <span data-ttu-id="dc47a-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dc47a-157">RELATED LINKS</span></span>

[<span data-ttu-id="dc47a-158">Nowe — AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="dc47a-158">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="dc47a-159">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="dc47a-159">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)

[<span data-ttu-id="dc47a-160">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="dc47a-160">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


