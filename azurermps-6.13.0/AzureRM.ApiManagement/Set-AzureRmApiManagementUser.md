---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 562DE7FA-F2A7-49E9-9273-3C4E2BF8D4B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
ms.openlocfilehash: 705deeb8e9b248b480bd2a28662cc7e968f8c228
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526365"
---
# <span data-ttu-id="e6844-101">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="e6844-101">Set-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="e6844-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e6844-102">SYNOPSIS</span></span>
<span data-ttu-id="e6844-103">Ustawia szczegóły użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e6844-103">Sets user details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6844-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e6844-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-FirstName <String>]
 [-LastName <String>] [-Email <String>] [-Password <SecureString>] [-State <PsApiManagementUserState>]
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6844-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e6844-105">DESCRIPTION</span></span>
<span data-ttu-id="e6844-106">Polecenie cmdlet **Set-AzureRmApiManagementUser** ustawia szczegóły użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e6844-106">The **Set-AzureRmApiManagementUser** cmdlet sets user details.</span></span>

## <span data-ttu-id="e6844-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e6844-107">EXAMPLES</span></span>

### <span data-ttu-id="e6844-108">Przykład 1: Zmienianie hasła użytkownika, adresu e-mail i stanu</span><span class="sxs-lookup"><span data-stu-id="e6844-108">Example 1: Change a user's password, email address and state</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>Set-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Email "patti.fuller@contoso.com" -Password $securePassword -State "Blocked"
```

<span data-ttu-id="e6844-109">To polecenie ustawia nowe hasło użytkownika i adres e-mail oraz blokuje użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e6844-109">This command sets a new user password and email address and blocks the user.</span></span>

## <span data-ttu-id="e6844-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e6844-110">PARAMETERS</span></span>

### <span data-ttu-id="e6844-111">-Context</span><span class="sxs-lookup"><span data-stu-id="e6844-111">-Context</span></span>
<span data-ttu-id="e6844-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="e6844-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="e6844-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="e6844-113">This parameter is required.</span></span>

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

### <span data-ttu-id="e6844-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6844-114">-DefaultProfile</span></span>
<span data-ttu-id="e6844-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e6844-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6844-116">-Mail</span><span class="sxs-lookup"><span data-stu-id="e6844-116">-Email</span></span>
<span data-ttu-id="e6844-117">Określa adres e-mail użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e6844-117">Specifies the email address of the user.</span></span>
<span data-ttu-id="e6844-118">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="e6844-118">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6844-119">-FirstName</span><span class="sxs-lookup"><span data-stu-id="e6844-119">-FirstName</span></span>
<span data-ttu-id="e6844-120">Określa Imię użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e6844-120">Specifies the first name of the user.</span></span>
<span data-ttu-id="e6844-121">Ten parametr musi mieć długość od 1 do 100 znaków.</span><span class="sxs-lookup"><span data-stu-id="e6844-121">This parameter must be 1 to 100 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6844-122">-LastName</span><span class="sxs-lookup"><span data-stu-id="e6844-122">-LastName</span></span>
<span data-ttu-id="e6844-123">Określa nazwisko użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e6844-123">Specifies the last name of the user.</span></span>
<span data-ttu-id="e6844-124">Ten parametr musi mieć długość od 1 do 100 znaków.</span><span class="sxs-lookup"><span data-stu-id="e6844-124">This parameter is must be 1 to 100 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6844-125">-Uwaga</span><span class="sxs-lookup"><span data-stu-id="e6844-125">-Note</span></span>
<span data-ttu-id="e6844-126">Określa notatkę dotyczącą użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e6844-126">Specifies a note about the user.</span></span>
<span data-ttu-id="e6844-127">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="e6844-127">This parameter is optional.</span></span>
<span data-ttu-id="e6844-128">Domyślną wartością tego parametru jest $null.</span><span class="sxs-lookup"><span data-stu-id="e6844-128">The default value of this parameter is $null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6844-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e6844-129">-PassThru</span></span>
<span data-ttu-id="e6844-130">passthru</span><span class="sxs-lookup"><span data-stu-id="e6844-130">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6844-131">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="e6844-131">-Password</span></span>
<span data-ttu-id="e6844-132">Określa hasło użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e6844-132">Specifies the user password.</span></span>
<span data-ttu-id="e6844-133">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="e6844-133">This parameter is optional.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6844-134">-State</span><span class="sxs-lookup"><span data-stu-id="e6844-134">-State</span></span>
<span data-ttu-id="e6844-135">Określa stan użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e6844-135">Specifies the user state.</span></span>
<span data-ttu-id="e6844-136">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="e6844-136">This parameter is optional.</span></span>
<span data-ttu-id="e6844-137">Wartość domyślna jest aktywna.</span><span class="sxs-lookup"><span data-stu-id="e6844-137">The default value is Active.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState
Parameter Sets: (All)
Aliases:
Accepted values: Active, Blocked, Deleted, Pending

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6844-138">-UserId</span><span class="sxs-lookup"><span data-stu-id="e6844-138">-UserId</span></span>
<span data-ttu-id="e6844-139">Określa identyfikator użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e6844-139">Specifies the user ID.</span></span>
<span data-ttu-id="e6844-140">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="e6844-140">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6844-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6844-141">CommonParameters</span></span>
<span data-ttu-id="e6844-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6844-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6844-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6844-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6844-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e6844-144">INPUTS</span></span>

### <span data-ttu-id="e6844-145">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e6844-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e6844-146">System. String</span><span class="sxs-lookup"><span data-stu-id="e6844-146">System.String</span></span>

### <span data-ttu-id="e6844-147">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="e6844-147">System.Security.SecureString</span></span>

### <span data-ttu-id="e6844-148">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementUserState</span><span class="sxs-lookup"><span data-stu-id="e6844-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState</span></span>

### <span data-ttu-id="e6844-149">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e6844-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e6844-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e6844-150">OUTPUTS</span></span>

### <span data-ttu-id="e6844-151">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="e6844-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="e6844-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e6844-152">NOTES</span></span>

## <span data-ttu-id="e6844-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e6844-153">RELATED LINKS</span></span>

[<span data-ttu-id="e6844-154">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="e6844-154">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="e6844-155">Nowe — AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="e6844-155">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="e6844-156">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="e6844-156">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)

