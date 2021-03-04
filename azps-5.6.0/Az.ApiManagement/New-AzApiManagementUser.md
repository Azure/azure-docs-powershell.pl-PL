---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
ms.openlocfilehash: 7e141cb5c1bde59bec9e981ffd228dba6db33089
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959178"
---
# <span data-ttu-id="b6bd2-101">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="b6bd2-101">New-AzApiManagementUser</span></span>

## <span data-ttu-id="b6bd2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6bd2-102">SYNOPSIS</span></span>
<span data-ttu-id="b6bd2-103">Rejestruje nowego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b6bd2-103">Registers a new user.</span></span>

## <span data-ttu-id="b6bd2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b6bd2-104">SYNTAX</span></span>

```
New-AzApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <SecureString> [-State <PsApiManagementUserState>]
 [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6bd2-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b6bd2-105">DESCRIPTION</span></span>
<span data-ttu-id="b6bd2-106">Polecenie **cmdlet New-AzApiManagementUser** rejestruje nowego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b6bd2-106">The **New-AzApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="b6bd2-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b6bd2-107">EXAMPLES</span></span>

### <span data-ttu-id="b6bd2-108">Przykład 1. Rejestrowanie nowego użytkownika</span><span class="sxs-lookup"><span data-stu-id="b6bd2-108">Example 1: Register a new user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>New-AzApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password $securePassword
```

<span data-ttu-id="b6bd2-109">To polecenie rejestruje nowego użytkownika o nazwie Patti Fuller.</span><span class="sxs-lookup"><span data-stu-id="b6bd2-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="b6bd2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6bd2-110">PARAMETERS</span></span>

### <span data-ttu-id="b6bd2-111">— kontekst</span><span class="sxs-lookup"><span data-stu-id="b6bd2-111">-Context</span></span>
<span data-ttu-id="b6bd2-112">Określa obiekt **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="b6bd2-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b6bd2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6bd2-113">-DefaultProfile</span></span>
<span data-ttu-id="b6bd2-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b6bd2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6bd2-115">— Poczta e-mail</span><span class="sxs-lookup"><span data-stu-id="b6bd2-115">-Email</span></span>
<span data-ttu-id="b6bd2-116">Określa adres e-mail użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b6bd2-116">Specifies the email address of the user.</span></span>

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

### <span data-ttu-id="b6bd2-117">-FirstName</span><span class="sxs-lookup"><span data-stu-id="b6bd2-117">-FirstName</span></span>
<span data-ttu-id="b6bd2-118">Określa imię użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b6bd2-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="b6bd2-119">Ten parametr musi mieć od 1 do 100 znaków.</span><span class="sxs-lookup"><span data-stu-id="b6bd2-119">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="b6bd2-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="b6bd2-120">-LastName</span></span>
<span data-ttu-id="b6bd2-121">Określa nazwisko użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b6bd2-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="b6bd2-122">Ten parametr musi mieć od 1 do 100 znaków.</span><span class="sxs-lookup"><span data-stu-id="b6bd2-122">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="b6bd2-123">— Uwaga</span><span class="sxs-lookup"><span data-stu-id="b6bd2-123">-Note</span></span>
<span data-ttu-id="b6bd2-124">Określa uwagę użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b6bd2-124">Specifies a note about the user.</span></span>
<span data-ttu-id="b6bd2-125">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="b6bd2-125">This parameter is optional.</span></span>
<span data-ttu-id="b6bd2-126">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="b6bd2-126">The default value is $Null.</span></span>

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

### <span data-ttu-id="b6bd2-127">— Hasło</span><span class="sxs-lookup"><span data-stu-id="b6bd2-127">-Password</span></span>
<span data-ttu-id="b6bd2-128">Określa hasło użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b6bd2-128">Specifies the user password.</span></span>
<span data-ttu-id="b6bd2-129">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="b6bd2-129">This parameter is required.</span></span>

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

### <span data-ttu-id="b6bd2-130">— województwo</span><span class="sxs-lookup"><span data-stu-id="b6bd2-130">-State</span></span>
<span data-ttu-id="b6bd2-131">Określa stan użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b6bd2-131">Specifies the user state.</span></span>
<span data-ttu-id="b6bd2-132">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="b6bd2-132">This parameter is optional.</span></span>
<span data-ttu-id="b6bd2-133">Wartość domyślna tego parametru to $Null.</span><span class="sxs-lookup"><span data-stu-id="b6bd2-133">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="b6bd2-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="b6bd2-134">-UserId</span></span>
<span data-ttu-id="b6bd2-135">Określa identyfikator użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b6bd2-135">Specifies the user ID.</span></span>
<span data-ttu-id="b6bd2-136">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="b6bd2-136">This parameter is optional.</span></span>
<span data-ttu-id="b6bd2-137">Jeśli ten parametr nie jest określony, to polecenie cmdlet generuje identyfikator użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b6bd2-137">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

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

### <span data-ttu-id="b6bd2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6bd2-138">CommonParameters</span></span>
<span data-ttu-id="b6bd2-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6bd2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6bd2-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b6bd2-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6bd2-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6bd2-141">INPUTS</span></span>

### <span data-ttu-id="b6bd2-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b6bd2-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b6bd2-143">System.String</span><span class="sxs-lookup"><span data-stu-id="b6bd2-143">System.String</span></span>

### <span data-ttu-id="b6bd2-144">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="b6bd2-144">System.Security.SecureString</span></span>

### <span data-ttu-id="b6bd2-145">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlet.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="b6bd2-145">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b6bd2-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6bd2-146">OUTPUTS</span></span>

### <span data-ttu-id="b6bd2-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="b6bd2-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="b6bd2-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b6bd2-148">NOTES</span></span>

## <span data-ttu-id="b6bd2-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6bd2-149">RELATED LINKS</span></span>

[<span data-ttu-id="b6bd2-150">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="b6bd2-150">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="b6bd2-151">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="b6bd2-151">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


