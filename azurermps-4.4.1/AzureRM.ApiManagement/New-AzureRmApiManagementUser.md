---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
ms.openlocfilehash: 93e6ce5a96afd1c3b297d6296c3491445593d430
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548432"
---
# <span data-ttu-id="9af47-101">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="9af47-101">New-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="9af47-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9af47-102">SYNOPSIS</span></span>
<span data-ttu-id="9af47-103">Rejestruje nowego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9af47-103">Registers a new user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9af47-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9af47-104">SYNTAX</span></span>

```
New-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <String> [-State <PsApiManagementUserState>] [-Note <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9af47-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9af47-105">DESCRIPTION</span></span>
<span data-ttu-id="9af47-106">Polecenie cmdlet **New-AzureRmApiManagementUser** rejestruje nowego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9af47-106">The **New-AzureRmApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="9af47-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9af47-107">EXAMPLES</span></span>

### <span data-ttu-id="9af47-108">Przykład 1: rejestrowanie nowego użytkownika</span><span class="sxs-lookup"><span data-stu-id="9af47-108">Example 1: Register a new user</span></span>
```
PS C:\>New-AzureRmApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password "qwerty"
```

<span data-ttu-id="9af47-109">To polecenie rejestruje nowego użytkownika o nazwie Patti.</span><span class="sxs-lookup"><span data-stu-id="9af47-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="9af47-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9af47-110">PARAMETERS</span></span>

### <span data-ttu-id="9af47-111">-Context</span><span class="sxs-lookup"><span data-stu-id="9af47-111">-Context</span></span>
<span data-ttu-id="9af47-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="9af47-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="9af47-113">-Mail</span><span class="sxs-lookup"><span data-stu-id="9af47-113">-Email</span></span>
<span data-ttu-id="9af47-114">Określa adres e-mail użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9af47-114">Specifies the email address of the user.</span></span>

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

### <span data-ttu-id="9af47-115">-FirstName</span><span class="sxs-lookup"><span data-stu-id="9af47-115">-FirstName</span></span>
<span data-ttu-id="9af47-116">Określa Imię użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9af47-116">Specifies the first name of the user.</span></span>
<span data-ttu-id="9af47-117">Ten parametr musi mieć długość od 1 do 100 znaków.</span><span class="sxs-lookup"><span data-stu-id="9af47-117">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="9af47-118">-LastName</span><span class="sxs-lookup"><span data-stu-id="9af47-118">-LastName</span></span>
<span data-ttu-id="9af47-119">Określa nazwisko użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9af47-119">Specifies the last name of the user.</span></span>
<span data-ttu-id="9af47-120">Ten parametr musi mieć długość od 1 do 100 znaków.</span><span class="sxs-lookup"><span data-stu-id="9af47-120">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="9af47-121">-Uwaga</span><span class="sxs-lookup"><span data-stu-id="9af47-121">-Note</span></span>
<span data-ttu-id="9af47-122">Określa notatkę dotyczącą użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9af47-122">Specifies a note about the user.</span></span>
<span data-ttu-id="9af47-123">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="9af47-123">This parameter is optional.</span></span>
<span data-ttu-id="9af47-124">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="9af47-124">The default value is $Null.</span></span>

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

### <span data-ttu-id="9af47-125">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="9af47-125">-Password</span></span>
<span data-ttu-id="9af47-126">Określa hasło użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9af47-126">Specifies the user password.</span></span>
<span data-ttu-id="9af47-127">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="9af47-127">This parameter is required.</span></span>

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

### <span data-ttu-id="9af47-128">-State</span><span class="sxs-lookup"><span data-stu-id="9af47-128">-State</span></span>
<span data-ttu-id="9af47-129">Określa stan użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9af47-129">Specifies the user state.</span></span>
<span data-ttu-id="9af47-130">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="9af47-130">This parameter is optional.</span></span>
<span data-ttu-id="9af47-131">Domyślną wartością tego parametru jest $Null.</span><span class="sxs-lookup"><span data-stu-id="9af47-131">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: (All)
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9af47-132">-UserId</span><span class="sxs-lookup"><span data-stu-id="9af47-132">-UserId</span></span>
<span data-ttu-id="9af47-133">Określa identyfikator użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9af47-133">Specifies the user ID.</span></span>
<span data-ttu-id="9af47-134">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="9af47-134">This parameter is optional.</span></span>
<span data-ttu-id="9af47-135">Jeśli ten parametr nie zostanie określony, polecenie cmdlet generuje identyfikator użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9af47-135">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

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

### <span data-ttu-id="9af47-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9af47-136">-DefaultProfile</span></span>
<span data-ttu-id="9af47-137">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9af47-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9af47-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9af47-138">CommonParameters</span></span>
<span data-ttu-id="9af47-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9af47-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9af47-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9af47-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9af47-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9af47-141">INPUTS</span></span>

## <span data-ttu-id="9af47-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9af47-142">OUTPUTS</span></span>

### <span data-ttu-id="9af47-143">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="9af47-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="9af47-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9af47-144">NOTES</span></span>

## <span data-ttu-id="9af47-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9af47-145">RELATED LINKS</span></span>

[<span data-ttu-id="9af47-146">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="9af47-146">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="9af47-147">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="9af47-147">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


