---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 562DE7FA-F2A7-49E9-9273-3C4E2BF8D4B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementUser.md
ms.openlocfilehash: 03ea39c24166b6e44c057907fbc7346996d3dfa7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869308"
---
# <span data-ttu-id="f88c6-101">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f88c6-101">Set-AzApiManagementUser</span></span>

## <span data-ttu-id="f88c6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f88c6-102">SYNOPSIS</span></span>
<span data-ttu-id="f88c6-103">Ustawia szczegóły użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f88c6-103">Sets user details.</span></span>

## <span data-ttu-id="f88c6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f88c6-104">SYNTAX</span></span>

```
Set-AzApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-FirstName <String>]
 [-LastName <String>] [-Email <String>] [-Password <SecureString>] [-State <PsApiManagementUserState>]
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f88c6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f88c6-105">DESCRIPTION</span></span>
<span data-ttu-id="f88c6-106">Polecenie cmdlet **Set-AzApiManagementUser** ustawia szczegóły użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f88c6-106">The **Set-AzApiManagementUser** cmdlet sets user details.</span></span>

## <span data-ttu-id="f88c6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f88c6-107">EXAMPLES</span></span>

### <span data-ttu-id="f88c6-108">Przykład 1: Zmienianie hasła użytkownika, adresu e-mail i stanu</span><span class="sxs-lookup"><span data-stu-id="f88c6-108">Example 1: Change a user's password, email address and state</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>Set-AzApiManagementUser -Context $apimContext -UserId "0123456789" -Email "patti.fuller@contoso.com" -Password $securePassword -State "Blocked"
```

<span data-ttu-id="f88c6-109">To polecenie ustawia nowe hasło użytkownika i adres e-mail oraz blokuje użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f88c6-109">This command sets a new user password and email address and blocks the user.</span></span>

## <span data-ttu-id="f88c6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f88c6-110">PARAMETERS</span></span>

### <span data-ttu-id="f88c6-111">-Context</span><span class="sxs-lookup"><span data-stu-id="f88c6-111">-Context</span></span>
<span data-ttu-id="f88c6-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="f88c6-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="f88c6-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="f88c6-113">This parameter is required.</span></span>

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

### <span data-ttu-id="f88c6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f88c6-114">-DefaultProfile</span></span>
<span data-ttu-id="f88c6-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f88c6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f88c6-116">-Mail</span><span class="sxs-lookup"><span data-stu-id="f88c6-116">-Email</span></span>
<span data-ttu-id="f88c6-117">Określa adres e-mail użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f88c6-117">Specifies the email address of the user.</span></span>
<span data-ttu-id="f88c6-118">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="f88c6-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="f88c6-119">-FirstName</span><span class="sxs-lookup"><span data-stu-id="f88c6-119">-FirstName</span></span>
<span data-ttu-id="f88c6-120">Określa Imię użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f88c6-120">Specifies the first name of the user.</span></span>
<span data-ttu-id="f88c6-121">Ten parametr musi mieć długość od 1 do 100 znaków.</span><span class="sxs-lookup"><span data-stu-id="f88c6-121">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="f88c6-122">-LastName</span><span class="sxs-lookup"><span data-stu-id="f88c6-122">-LastName</span></span>
<span data-ttu-id="f88c6-123">Określa nazwisko użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f88c6-123">Specifies the last name of the user.</span></span>
<span data-ttu-id="f88c6-124">Ten parametr musi mieć długość od 1 do 100 znaków.</span><span class="sxs-lookup"><span data-stu-id="f88c6-124">This parameter is must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="f88c6-125">-Uwaga</span><span class="sxs-lookup"><span data-stu-id="f88c6-125">-Note</span></span>
<span data-ttu-id="f88c6-126">Określa notatkę dotyczącą użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f88c6-126">Specifies a note about the user.</span></span>
<span data-ttu-id="f88c6-127">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="f88c6-127">This parameter is optional.</span></span>
<span data-ttu-id="f88c6-128">Domyślną wartością tego parametru jest $null.</span><span class="sxs-lookup"><span data-stu-id="f88c6-128">The default value of this parameter is $null.</span></span>

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

### <span data-ttu-id="f88c6-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f88c6-129">-PassThru</span></span>
<span data-ttu-id="f88c6-130">passthru</span><span class="sxs-lookup"><span data-stu-id="f88c6-130">passthru</span></span>

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

### <span data-ttu-id="f88c6-131">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="f88c6-131">-Password</span></span>
<span data-ttu-id="f88c6-132">Określa hasło użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f88c6-132">Specifies the user password.</span></span>
<span data-ttu-id="f88c6-133">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="f88c6-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="f88c6-134">-State</span><span class="sxs-lookup"><span data-stu-id="f88c6-134">-State</span></span>
<span data-ttu-id="f88c6-135">Określa stan użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f88c6-135">Specifies the user state.</span></span>
<span data-ttu-id="f88c6-136">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="f88c6-136">This parameter is optional.</span></span>
<span data-ttu-id="f88c6-137">Wartość domyślna jest aktywna.</span><span class="sxs-lookup"><span data-stu-id="f88c6-137">The default value is Active.</span></span>

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

### <span data-ttu-id="f88c6-138">-UserId</span><span class="sxs-lookup"><span data-stu-id="f88c6-138">-UserId</span></span>
<span data-ttu-id="f88c6-139">Określa identyfikator użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f88c6-139">Specifies the user ID.</span></span>
<span data-ttu-id="f88c6-140">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="f88c6-140">This parameter is required.</span></span>

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

### <span data-ttu-id="f88c6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f88c6-141">CommonParameters</span></span>
<span data-ttu-id="f88c6-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f88c6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f88c6-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f88c6-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f88c6-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f88c6-144">INPUTS</span></span>

### <span data-ttu-id="f88c6-145">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f88c6-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f88c6-146">System. String</span><span class="sxs-lookup"><span data-stu-id="f88c6-146">System.String</span></span>

### <span data-ttu-id="f88c6-147">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="f88c6-147">System.Security.SecureString</span></span>

### <span data-ttu-id="f88c6-148">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementUserState</span><span class="sxs-lookup"><span data-stu-id="f88c6-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState</span></span>

### <span data-ttu-id="f88c6-149">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f88c6-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f88c6-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f88c6-150">OUTPUTS</span></span>

### <span data-ttu-id="f88c6-151">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f88c6-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="f88c6-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f88c6-152">NOTES</span></span>

## <span data-ttu-id="f88c6-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f88c6-153">RELATED LINKS</span></span>

[<span data-ttu-id="f88c6-154">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f88c6-154">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="f88c6-155">Nowe — AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f88c6-155">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="f88c6-156">Remove-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f88c6-156">Remove-AzApiManagementUser</span></span>](./Remove-AzApiManagementUser.md)


