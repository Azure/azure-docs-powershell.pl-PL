---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
ms.openlocfilehash: 6cc922ceb09509e70a4017241dc6beb6e5443d1a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382328"
---
# <span data-ttu-id="e3036-101">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="e3036-101">New-AzApiManagementUser</span></span>

## <span data-ttu-id="e3036-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e3036-102">SYNOPSIS</span></span>
<span data-ttu-id="e3036-103">Rejestruje nowego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e3036-103">Registers a new user.</span></span>

## <span data-ttu-id="e3036-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e3036-104">SYNTAX</span></span>

```
New-AzApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <SecureString> [-State <PsApiManagementUserState>]
 [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3036-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e3036-105">DESCRIPTION</span></span>
<span data-ttu-id="e3036-106">Polecenie cmdlet **New-AzApiManagementUser** rejestruje nowego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e3036-106">The **New-AzApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="e3036-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e3036-107">EXAMPLES</span></span>

### <span data-ttu-id="e3036-108">Przykład 1: rejestrowanie nowego użytkownika</span><span class="sxs-lookup"><span data-stu-id="e3036-108">Example 1: Register a new user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>New-AzApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password $securePassword
```

<span data-ttu-id="e3036-109">To polecenie rejestruje nowego użytkownika o nazwie Patti.</span><span class="sxs-lookup"><span data-stu-id="e3036-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="e3036-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e3036-110">PARAMETERS</span></span>

### <span data-ttu-id="e3036-111">-Context</span><span class="sxs-lookup"><span data-stu-id="e3036-111">-Context</span></span>
<span data-ttu-id="e3036-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="e3036-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e3036-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3036-113">-DefaultProfile</span></span>
<span data-ttu-id="e3036-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e3036-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3036-115">-Mail</span><span class="sxs-lookup"><span data-stu-id="e3036-115">-Email</span></span>
<span data-ttu-id="e3036-116">Określa adres e-mail użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e3036-116">Specifies the email address of the user.</span></span>

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

### <span data-ttu-id="e3036-117">-FirstName</span><span class="sxs-lookup"><span data-stu-id="e3036-117">-FirstName</span></span>
<span data-ttu-id="e3036-118">Określa Imię użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e3036-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="e3036-119">Ten parametr musi mieć długość od 1 do 100 znaków.</span><span class="sxs-lookup"><span data-stu-id="e3036-119">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="e3036-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="e3036-120">-LastName</span></span>
<span data-ttu-id="e3036-121">Określa nazwisko użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e3036-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="e3036-122">Ten parametr musi mieć długość od 1 do 100 znaków.</span><span class="sxs-lookup"><span data-stu-id="e3036-122">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="e3036-123">-Uwaga</span><span class="sxs-lookup"><span data-stu-id="e3036-123">-Note</span></span>
<span data-ttu-id="e3036-124">Określa notatkę dotyczącą użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e3036-124">Specifies a note about the user.</span></span>
<span data-ttu-id="e3036-125">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="e3036-125">This parameter is optional.</span></span>
<span data-ttu-id="e3036-126">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="e3036-126">The default value is $Null.</span></span>

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

### <span data-ttu-id="e3036-127">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="e3036-127">-Password</span></span>
<span data-ttu-id="e3036-128">Określa hasło użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e3036-128">Specifies the user password.</span></span>
<span data-ttu-id="e3036-129">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="e3036-129">This parameter is required.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3036-130">-State</span><span class="sxs-lookup"><span data-stu-id="e3036-130">-State</span></span>
<span data-ttu-id="e3036-131">Określa stan użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e3036-131">Specifies the user state.</span></span>
<span data-ttu-id="e3036-132">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="e3036-132">This parameter is optional.</span></span>
<span data-ttu-id="e3036-133">Domyślną wartością tego parametru jest $Null.</span><span class="sxs-lookup"><span data-stu-id="e3036-133">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: (All)
Aliases:
Accepted values: Active, Blocked, Deleted, Pending

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3036-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="e3036-134">-UserId</span></span>
<span data-ttu-id="e3036-135">Określa identyfikator użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e3036-135">Specifies the user ID.</span></span>
<span data-ttu-id="e3036-136">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="e3036-136">This parameter is optional.</span></span>
<span data-ttu-id="e3036-137">Jeśli ten parametr nie zostanie określony, polecenie cmdlet generuje identyfikator użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e3036-137">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

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

### <span data-ttu-id="e3036-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3036-138">CommonParameters</span></span>
<span data-ttu-id="e3036-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3036-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3036-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3036-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3036-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e3036-141">INPUTS</span></span>

### <span data-ttu-id="e3036-142">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e3036-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e3036-143">System. String</span><span class="sxs-lookup"><span data-stu-id="e3036-143">System.String</span></span>

### <span data-ttu-id="e3036-144">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="e3036-144">System.Security.SecureString</span></span>

### <span data-ttu-id="e3036-145">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. servicemanagement. modele. PsApiManagementUserState, Microsoft. Azure. PowerShell. cmdlet. ApiManagement. servicemanagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e3036-145">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e3036-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e3036-146">OUTPUTS</span></span>

### <span data-ttu-id="e3036-147">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="e3036-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="e3036-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e3036-148">NOTES</span></span>

## <span data-ttu-id="e3036-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e3036-149">RELATED LINKS</span></span>

[<span data-ttu-id="e3036-150">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="e3036-150">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="e3036-151">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="e3036-151">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


