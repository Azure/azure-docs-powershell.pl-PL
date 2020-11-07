---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
ms.openlocfilehash: fa7b44710aa51a138729d9a04a41a82ec2769f5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719599"
---
# <span data-ttu-id="00714-101">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="00714-101">New-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="00714-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="00714-102">SYNOPSIS</span></span>
<span data-ttu-id="00714-103">Rejestruje nowego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="00714-103">Registers a new user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00714-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="00714-104">SYNTAX</span></span>

```
New-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <SecureString> [-State <PsApiManagementUserState>]
 [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00714-105">Opis</span><span class="sxs-lookup"><span data-stu-id="00714-105">DESCRIPTION</span></span>
<span data-ttu-id="00714-106">Polecenie cmdlet **New-AzureRmApiManagementUser** rejestruje nowego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="00714-106">The **New-AzureRmApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="00714-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="00714-107">EXAMPLES</span></span>

### <span data-ttu-id="00714-108">Przykład 1: rejestrowanie nowego użytkownika</span><span class="sxs-lookup"><span data-stu-id="00714-108">Example 1: Register a new user</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>New-AzureRmApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password $securePassword
```

<span data-ttu-id="00714-109">To polecenie rejestruje nowego użytkownika o nazwie Patti.</span><span class="sxs-lookup"><span data-stu-id="00714-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="00714-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="00714-110">PARAMETERS</span></span>

### <span data-ttu-id="00714-111">-Context</span><span class="sxs-lookup"><span data-stu-id="00714-111">-Context</span></span>
<span data-ttu-id="00714-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="00714-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="00714-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00714-113">-DefaultProfile</span></span>
<span data-ttu-id="00714-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="00714-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="00714-115">-Mail</span><span class="sxs-lookup"><span data-stu-id="00714-115">-Email</span></span>
<span data-ttu-id="00714-116">Określa adres e-mail użytkownika.</span><span class="sxs-lookup"><span data-stu-id="00714-116">Specifies the email address of the user.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00714-117">-FirstName</span><span class="sxs-lookup"><span data-stu-id="00714-117">-FirstName</span></span>
<span data-ttu-id="00714-118">Określa Imię użytkownika.</span><span class="sxs-lookup"><span data-stu-id="00714-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="00714-119">Ten parametr musi mieć długość od 1 do 100 znaków.</span><span class="sxs-lookup"><span data-stu-id="00714-119">This parameter must be 1 to 100 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00714-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="00714-120">-LastName</span></span>
<span data-ttu-id="00714-121">Określa nazwisko użytkownika.</span><span class="sxs-lookup"><span data-stu-id="00714-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="00714-122">Ten parametr musi mieć długość od 1 do 100 znaków.</span><span class="sxs-lookup"><span data-stu-id="00714-122">This parameter must be 1 to 100 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00714-123">-Uwaga</span><span class="sxs-lookup"><span data-stu-id="00714-123">-Note</span></span>
<span data-ttu-id="00714-124">Określa notatkę dotyczącą użytkownika.</span><span class="sxs-lookup"><span data-stu-id="00714-124">Specifies a note about the user.</span></span>
<span data-ttu-id="00714-125">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="00714-125">This parameter is optional.</span></span>
<span data-ttu-id="00714-126">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="00714-126">The default value is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00714-127">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="00714-127">-Password</span></span>
<span data-ttu-id="00714-128">Określa hasło użytkownika.</span><span class="sxs-lookup"><span data-stu-id="00714-128">Specifies the user password.</span></span>
<span data-ttu-id="00714-129">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="00714-129">This parameter is required.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00714-130">-State</span><span class="sxs-lookup"><span data-stu-id="00714-130">-State</span></span>
<span data-ttu-id="00714-131">Określa stan użytkownika.</span><span class="sxs-lookup"><span data-stu-id="00714-131">Specifies the user state.</span></span>
<span data-ttu-id="00714-132">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="00714-132">This parameter is optional.</span></span>
<span data-ttu-id="00714-133">Domyślną wartością tego parametru jest $Null.</span><span class="sxs-lookup"><span data-stu-id="00714-133">The default value of this parameter is $Null.</span></span>

```yaml
Type: PsApiManagementUserState
Parameter Sets: (All)
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00714-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="00714-134">-UserId</span></span>
<span data-ttu-id="00714-135">Określa identyfikator użytkownika.</span><span class="sxs-lookup"><span data-stu-id="00714-135">Specifies the user ID.</span></span>
<span data-ttu-id="00714-136">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="00714-136">This parameter is optional.</span></span>
<span data-ttu-id="00714-137">Jeśli ten parametr nie zostanie określony, polecenie cmdlet generuje identyfikator użytkownika.</span><span class="sxs-lookup"><span data-stu-id="00714-137">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00714-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00714-138">CommonParameters</span></span>
<span data-ttu-id="00714-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00714-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00714-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00714-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00714-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="00714-141">INPUTS</span></span>

### <span data-ttu-id="00714-142">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="00714-142">None</span></span>
<span data-ttu-id="00714-143">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="00714-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="00714-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="00714-144">OUTPUTS</span></span>

### <span data-ttu-id="00714-145">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="00714-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="00714-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="00714-146">NOTES</span></span>

## <span data-ttu-id="00714-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="00714-147">RELATED LINKS</span></span>

[<span data-ttu-id="00714-148">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="00714-148">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="00714-149">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="00714-149">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


