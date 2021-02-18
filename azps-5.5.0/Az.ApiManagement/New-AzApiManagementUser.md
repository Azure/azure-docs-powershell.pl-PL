---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
ms.openlocfilehash: 6cc922ceb09509e70a4017241dc6beb6e5443d1a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239714"
---
# <span data-ttu-id="82d33-101">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="82d33-101">New-AzApiManagementUser</span></span>

## <span data-ttu-id="82d33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82d33-102">SYNOPSIS</span></span>
<span data-ttu-id="82d33-103">Rejestruje nowego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="82d33-103">Registers a new user.</span></span>

## <span data-ttu-id="82d33-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="82d33-104">SYNTAX</span></span>

```
New-AzApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <SecureString> [-State <PsApiManagementUserState>]
 [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82d33-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="82d33-105">DESCRIPTION</span></span>
<span data-ttu-id="82d33-106">Polecenie **cmdlet New-AzApiManagementUser** rejestruje nowego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="82d33-106">The **New-AzApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="82d33-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="82d33-107">EXAMPLES</span></span>

### <span data-ttu-id="82d33-108">Przykład 1. Rejestrowanie nowego użytkownika</span><span class="sxs-lookup"><span data-stu-id="82d33-108">Example 1: Register a new user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>New-AzApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password $securePassword
```

<span data-ttu-id="82d33-109">To polecenie rejestruje nowego użytkownika o nazwie Patti Fuller.</span><span class="sxs-lookup"><span data-stu-id="82d33-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="82d33-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82d33-110">PARAMETERS</span></span>

### <span data-ttu-id="82d33-111">— kontekst</span><span class="sxs-lookup"><span data-stu-id="82d33-111">-Context</span></span>
<span data-ttu-id="82d33-112">Określa obiekt **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="82d33-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="82d33-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82d33-113">-DefaultProfile</span></span>
<span data-ttu-id="82d33-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="82d33-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82d33-115">— Poczta e-mail</span><span class="sxs-lookup"><span data-stu-id="82d33-115">-Email</span></span>
<span data-ttu-id="82d33-116">Określa adres e-mail użytkownika.</span><span class="sxs-lookup"><span data-stu-id="82d33-116">Specifies the email address of the user.</span></span>

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

### <span data-ttu-id="82d33-117">-FirstName</span><span class="sxs-lookup"><span data-stu-id="82d33-117">-FirstName</span></span>
<span data-ttu-id="82d33-118">Określa imię użytkownika.</span><span class="sxs-lookup"><span data-stu-id="82d33-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="82d33-119">Ten parametr musi mieć od 1 do 100 znaków.</span><span class="sxs-lookup"><span data-stu-id="82d33-119">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="82d33-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="82d33-120">-LastName</span></span>
<span data-ttu-id="82d33-121">Określa nazwisko użytkownika.</span><span class="sxs-lookup"><span data-stu-id="82d33-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="82d33-122">Ten parametr musi mieć od 1 do 100 znaków.</span><span class="sxs-lookup"><span data-stu-id="82d33-122">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="82d33-123">— Uwaga</span><span class="sxs-lookup"><span data-stu-id="82d33-123">-Note</span></span>
<span data-ttu-id="82d33-124">Określa notatkę na temat użytkownika.</span><span class="sxs-lookup"><span data-stu-id="82d33-124">Specifies a note about the user.</span></span>
<span data-ttu-id="82d33-125">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="82d33-125">This parameter is optional.</span></span>
<span data-ttu-id="82d33-126">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="82d33-126">The default value is $Null.</span></span>

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

### <span data-ttu-id="82d33-127">— Hasło</span><span class="sxs-lookup"><span data-stu-id="82d33-127">-Password</span></span>
<span data-ttu-id="82d33-128">Określa hasło użytkownika.</span><span class="sxs-lookup"><span data-stu-id="82d33-128">Specifies the user password.</span></span>
<span data-ttu-id="82d33-129">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="82d33-129">This parameter is required.</span></span>

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

### <span data-ttu-id="82d33-130">— województwo</span><span class="sxs-lookup"><span data-stu-id="82d33-130">-State</span></span>
<span data-ttu-id="82d33-131">Określa stan użytkownika.</span><span class="sxs-lookup"><span data-stu-id="82d33-131">Specifies the user state.</span></span>
<span data-ttu-id="82d33-132">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="82d33-132">This parameter is optional.</span></span>
<span data-ttu-id="82d33-133">Wartość domyślna tego parametru to $Null.</span><span class="sxs-lookup"><span data-stu-id="82d33-133">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="82d33-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="82d33-134">-UserId</span></span>
<span data-ttu-id="82d33-135">Określa identyfikator użytkownika.</span><span class="sxs-lookup"><span data-stu-id="82d33-135">Specifies the user ID.</span></span>
<span data-ttu-id="82d33-136">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="82d33-136">This parameter is optional.</span></span>
<span data-ttu-id="82d33-137">Jeśli ten parametr nie zostanie określony, to polecenie cmdlet wygeneruje identyfikator użytkownika.</span><span class="sxs-lookup"><span data-stu-id="82d33-137">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

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

### <span data-ttu-id="82d33-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82d33-138">CommonParameters</span></span>
<span data-ttu-id="82d33-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82d33-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82d33-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="82d33-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82d33-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="82d33-141">INPUTS</span></span>

### <span data-ttu-id="82d33-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="82d33-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="82d33-143">System.String</span><span class="sxs-lookup"><span data-stu-id="82d33-143">System.String</span></span>

### <span data-ttu-id="82d33-144">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="82d33-144">System.Security.SecureString</span></span>

### <span data-ttu-id="82d33-145">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlet.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="82d33-145">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="82d33-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="82d33-146">OUTPUTS</span></span>

### <span data-ttu-id="82d33-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="82d33-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="82d33-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="82d33-148">NOTES</span></span>

## <span data-ttu-id="82d33-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="82d33-149">RELATED LINKS</span></span>

[<span data-ttu-id="82d33-150">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="82d33-150">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="82d33-151">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="82d33-151">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


