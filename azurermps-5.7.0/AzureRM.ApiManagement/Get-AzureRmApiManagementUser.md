---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
ms.openlocfilehash: 07f387239bdaad526c36c3928e7d2c5f490b0c7b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544584"
---
# <span data-ttu-id="f06e1-101">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f06e1-101">Get-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="f06e1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f06e1-102">SYNOPSIS</span></span>
<span data-ttu-id="f06e1-103">Pobiera użytkownika lub użytkowników.</span><span class="sxs-lookup"><span data-stu-id="f06e1-103">Gets a user or users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f06e1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f06e1-104">SYNTAX</span></span>

### <span data-ttu-id="f06e1-105">GeAllUsers (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f06e1-105">GeAllUsers (Default)</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f06e1-106">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="f06e1-106">GetByUserId</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f06e1-107">GetByUser</span><span class="sxs-lookup"><span data-stu-id="f06e1-107">GetByUser</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f06e1-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f06e1-108">DESCRIPTION</span></span>
<span data-ttu-id="f06e1-109">Polecenie cmdlet **Get-AzureRmApiManagementUser** pobiera określonego użytkownika lub wszystkich użytkowników, jeśli nie określono żadnego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f06e1-109">The **Get-AzureRmApiManagementUser** cmdlet gets a specified user, or all users, if no user is specified.</span></span>

## <span data-ttu-id="f06e1-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f06e1-110">EXAMPLES</span></span>

### <span data-ttu-id="f06e1-111">Przykład 1: Pobierz wszystkich użytkowników</span><span class="sxs-lookup"><span data-stu-id="f06e1-111">Example 1: Get all users</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext
```

<span data-ttu-id="f06e1-112">To polecenie pobiera wszystkich użytkowników.</span><span class="sxs-lookup"><span data-stu-id="f06e1-112">This command gets all users.</span></span>

### <span data-ttu-id="f06e1-113">Przykład 2: Uzyskaj użytkownika według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="f06e1-113">Example 2: Get a user by ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="f06e1-114">To polecenie pobiera użytkownika według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="f06e1-114">This command gets a user by ID.</span></span>

### <span data-ttu-id="f06e1-115">Przykład: pobieranie użytkowników według nazwisk</span><span class="sxs-lookup"><span data-stu-id="f06e1-115">Example: Get users by last name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -LastName "Fuller"
```

<span data-ttu-id="f06e1-116">To polecenie umożliwia użytkownikom, których imiona i nazwiska są określone przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f06e1-116">This command gets users that have a specified last name, Fuller.</span></span>

### <span data-ttu-id="f06e1-117">Przykład 4: Uzyskaj użytkownikowi na podstawie adresu e-mail</span><span class="sxs-lookup"><span data-stu-id="f06e1-117">Example 4: Get a user by email address</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -Email "user@contoso.com"
```

<span data-ttu-id="f06e1-118">To polecenie uzyskuje użytkownika o określonym adresie e-mail.</span><span class="sxs-lookup"><span data-stu-id="f06e1-118">This command gets the user that has the specified email address.</span></span>

### <span data-ttu-id="f06e1-119">Przykład 5: uzyskiwanie wszystkich użytkowników w grupie</span><span class="sxs-lookup"><span data-stu-id="f06e1-119">Example 5: Get all users within a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -GroupId "0001"
```

<span data-ttu-id="f06e1-120">To polecenie pobiera wszystkich użytkowników w określonej grupie.</span><span class="sxs-lookup"><span data-stu-id="f06e1-120">This command gets all users within the specified group.</span></span>

## <span data-ttu-id="f06e1-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f06e1-121">PARAMETERS</span></span>

### <span data-ttu-id="f06e1-122">-Context</span><span class="sxs-lookup"><span data-stu-id="f06e1-122">-Context</span></span>
<span data-ttu-id="f06e1-123">Określa wystąpienie **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="f06e1-123">Specifies an instance of **PsApiManagementContext**.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f06e1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f06e1-124">-DefaultProfile</span></span>
<span data-ttu-id="f06e1-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f06e1-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f06e1-126">-Mail</span><span class="sxs-lookup"><span data-stu-id="f06e1-126">-Email</span></span>
<span data-ttu-id="f06e1-127">Określa adres e-mail użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f06e1-127">Specifies the email address of the user.</span></span>
<span data-ttu-id="f06e1-128">Jeśli ten parametr jest określony, to polecenie cmdlet odnajdzie użytkownika pocztą e-mail.</span><span class="sxs-lookup"><span data-stu-id="f06e1-128">If this parameter is specified, this cmdlet finds a user by email.</span></span>
<span data-ttu-id="f06e1-129">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="f06e1-129">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByUser
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f06e1-130">-FirstName</span><span class="sxs-lookup"><span data-stu-id="f06e1-130">-FirstName</span></span>
<span data-ttu-id="f06e1-131">Określa Imię użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f06e1-131">Specifies the first name of the user.</span></span>
<span data-ttu-id="f06e1-132">Jeśli ten parametr jest określony, to polecenie cmdlet odnajdzie użytkownika według imienia i nazwiska.</span><span class="sxs-lookup"><span data-stu-id="f06e1-132">If this parameter is specified, this cmdlet finds a user by first name.</span></span>
<span data-ttu-id="f06e1-133">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="f06e1-133">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByUser
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f06e1-134">-GroupId</span><span class="sxs-lookup"><span data-stu-id="f06e1-134">-GroupId</span></span>
<span data-ttu-id="f06e1-135">Określa identyfikator grupy.</span><span class="sxs-lookup"><span data-stu-id="f06e1-135">Specifies the group identifier.</span></span>
<span data-ttu-id="f06e1-136">Jeśli ta funkcja jest określona, to polecenie cmdlet odnajdzie wszystkich użytkowników w określonej grupie.</span><span class="sxs-lookup"><span data-stu-id="f06e1-136">If specified, this cmdlet finds all users within the specified group.</span></span>
<span data-ttu-id="f06e1-137">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="f06e1-137">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByUser
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f06e1-138">-LastName</span><span class="sxs-lookup"><span data-stu-id="f06e1-138">-LastName</span></span>
<span data-ttu-id="f06e1-139">Określa nazwisko użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f06e1-139">Specifies the last name of a user.</span></span>
<span data-ttu-id="f06e1-140">Jeśli ta funkcja jest określona, to polecenie cmdlet wyszukuje użytkowników według nazwiska.</span><span class="sxs-lookup"><span data-stu-id="f06e1-140">If specified, this cmdlet finds users by last name.</span></span>
<span data-ttu-id="f06e1-141">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="f06e1-141">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByUser
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f06e1-142">-State</span><span class="sxs-lookup"><span data-stu-id="f06e1-142">-State</span></span>
<span data-ttu-id="f06e1-143">Określa stan użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f06e1-143">Specifies the user state.</span></span>
<span data-ttu-id="f06e1-144">Jeśli ta funkcja jest określona, to polecenie cmdlet umożliwia znalezienie użytkowników w tym stanie.</span><span class="sxs-lookup"><span data-stu-id="f06e1-144">If specified, this cmdlet finds users in this state.</span></span>
<span data-ttu-id="f06e1-145">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="f06e1-145">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementUserState
Parameter Sets: GetByUser
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f06e1-146">-UserId</span><span class="sxs-lookup"><span data-stu-id="f06e1-146">-UserId</span></span>
<span data-ttu-id="f06e1-147">Określa identyfikator użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f06e1-147">Specifies a user ID.</span></span>
<span data-ttu-id="f06e1-148">Jeśli ta funkcja jest określona, to polecenie cmdlet odnajdzie użytkownika przy użyciu tego identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="f06e1-148">If specified, this cmdlet finds the user by this identifier.</span></span>
<span data-ttu-id="f06e1-149">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="f06e1-149">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByUserId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f06e1-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f06e1-150">CommonParameters</span></span>
<span data-ttu-id="f06e1-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f06e1-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f06e1-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f06e1-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f06e1-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f06e1-153">INPUTS</span></span>

### <span data-ttu-id="f06e1-154">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f06e1-154">None</span></span>
<span data-ttu-id="f06e1-155">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="f06e1-155">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f06e1-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f06e1-156">OUTPUTS</span></span>

### <span data-ttu-id="f06e1-157">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f06e1-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>
<span data-ttu-id="f06e1-158">Szczegóły dotyczące użytkownika w usłudze zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="f06e1-158">The details of User in API Management service.</span></span>

### <span data-ttu-id="f06e1-159">IList<Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementUser></span><span class="sxs-lookup"><span data-stu-id="f06e1-159">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser></span></span>
<span data-ttu-id="f06e1-160">Lista użytkowników w usłudze zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="f06e1-160">The list of User in the API Management  service.</span></span>

## <span data-ttu-id="f06e1-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f06e1-161">NOTES</span></span>

## <span data-ttu-id="f06e1-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f06e1-162">RELATED LINKS</span></span>

[<span data-ttu-id="f06e1-163">Nowe — AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f06e1-163">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="f06e1-164">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f06e1-164">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)

[<span data-ttu-id="f06e1-165">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f06e1-165">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


