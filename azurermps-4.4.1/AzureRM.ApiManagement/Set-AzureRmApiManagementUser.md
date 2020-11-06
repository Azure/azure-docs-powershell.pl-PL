---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 562DE7FA-F2A7-49E9-9273-3C4E2BF8D4B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementUser.md
ms.openlocfilehash: a9d36dca9894a10c76f2ca5a96880f4aafecb5e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525742"
---
# <span data-ttu-id="f9fac-101">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f9fac-101">Set-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="f9fac-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f9fac-102">SYNOPSIS</span></span>
<span data-ttu-id="f9fac-103">Ustawia szczegóły użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f9fac-103">Sets user details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9fac-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f9fac-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-FirstName <String>]
 [-LastName <String>] [-Email <String>] [-Password <String>] [-State <PsApiManagementUserState>]
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9fac-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f9fac-105">DESCRIPTION</span></span>
<span data-ttu-id="f9fac-106">Polecenie cmdlet **Set-AzureRmApiManagementUser** ustawia szczegóły użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f9fac-106">The **Set-AzureRmApiManagementUser** cmdlet sets user details.</span></span>

## <span data-ttu-id="f9fac-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f9fac-107">EXAMPLES</span></span>

### <span data-ttu-id="f9fac-108">Przykład 1: Zmienianie hasła użytkownika, adresu e-mail i stanu</span><span class="sxs-lookup"><span data-stu-id="f9fac-108">Example 1: Change a user's password, email address and state</span></span>
```
PS C:\>Set-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Email "patti.fuller@contoso.com" -Password "asdfgh" -State "Blocked"
```

<span data-ttu-id="f9fac-109">To polecenie ustawia nowe hasło użytkownika i adres e-mail oraz blokuje użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f9fac-109">This command sets a new user password and email address and blocks the user.</span></span>

## <span data-ttu-id="f9fac-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f9fac-110">PARAMETERS</span></span>

### <span data-ttu-id="f9fac-111">-Context</span><span class="sxs-lookup"><span data-stu-id="f9fac-111">-Context</span></span>
<span data-ttu-id="f9fac-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="f9fac-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="f9fac-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="f9fac-113">This parameter is required.</span></span>

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

### <span data-ttu-id="f9fac-114">-Mail</span><span class="sxs-lookup"><span data-stu-id="f9fac-114">-Email</span></span>
<span data-ttu-id="f9fac-115">Określa adres e-mail użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f9fac-115">Specifies the email address of the user.</span></span>
<span data-ttu-id="f9fac-116">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="f9fac-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="f9fac-117">-FirstName</span><span class="sxs-lookup"><span data-stu-id="f9fac-117">-FirstName</span></span>
<span data-ttu-id="f9fac-118">Określa Imię użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f9fac-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="f9fac-119">Ten parametr musi mieć długość od 1 do 100 znaków.</span><span class="sxs-lookup"><span data-stu-id="f9fac-119">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="f9fac-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="f9fac-120">-LastName</span></span>
<span data-ttu-id="f9fac-121">Określa nazwisko użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f9fac-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="f9fac-122">Ten parametr musi mieć długość od 1 do 100 znaków.</span><span class="sxs-lookup"><span data-stu-id="f9fac-122">This parameter is must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="f9fac-123">-Uwaga</span><span class="sxs-lookup"><span data-stu-id="f9fac-123">-Note</span></span>
<span data-ttu-id="f9fac-124">Określa notatkę dotyczącą użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f9fac-124">Specifies a note about the user.</span></span>
<span data-ttu-id="f9fac-125">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="f9fac-125">This parameter is optional.</span></span>
<span data-ttu-id="f9fac-126">Domyślną wartością tego parametru jest $null.</span><span class="sxs-lookup"><span data-stu-id="f9fac-126">The default value of this parameter is $null.</span></span>

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

### <span data-ttu-id="f9fac-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f9fac-127">-PassThru</span></span>
<span data-ttu-id="f9fac-128">passthru</span><span class="sxs-lookup"><span data-stu-id="f9fac-128">passthru</span></span>

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

### <span data-ttu-id="f9fac-129">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="f9fac-129">-Password</span></span>
<span data-ttu-id="f9fac-130">Określa hasło użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f9fac-130">Specifies the user password.</span></span>
<span data-ttu-id="f9fac-131">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="f9fac-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="f9fac-132">-State</span><span class="sxs-lookup"><span data-stu-id="f9fac-132">-State</span></span>
<span data-ttu-id="f9fac-133">Określa stan użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f9fac-133">Specifies the user state.</span></span>
<span data-ttu-id="f9fac-134">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="f9fac-134">This parameter is optional.</span></span>
<span data-ttu-id="f9fac-135">Wartość domyślna jest aktywna.</span><span class="sxs-lookup"><span data-stu-id="f9fac-135">The default value is Active.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState
Parameter Sets: (All)
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9fac-136">-UserId</span><span class="sxs-lookup"><span data-stu-id="f9fac-136">-UserId</span></span>
<span data-ttu-id="f9fac-137">Określa identyfikator użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f9fac-137">Specifies the user ID.</span></span>
<span data-ttu-id="f9fac-138">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="f9fac-138">This parameter is required.</span></span>

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

### <span data-ttu-id="f9fac-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9fac-139">-DefaultProfile</span></span>
<span data-ttu-id="f9fac-140">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f9fac-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9fac-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9fac-141">CommonParameters</span></span>
<span data-ttu-id="f9fac-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9fac-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9fac-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9fac-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9fac-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f9fac-144">INPUTS</span></span>

## <span data-ttu-id="f9fac-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f9fac-145">OUTPUTS</span></span>

### <span data-ttu-id="f9fac-146">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f9fac-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="f9fac-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f9fac-147">NOTES</span></span>

## <span data-ttu-id="f9fac-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f9fac-148">RELATED LINKS</span></span>

[<span data-ttu-id="f9fac-149">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f9fac-149">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="f9fac-150">Nowe — AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f9fac-150">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="f9fac-151">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f9fac-151">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)


