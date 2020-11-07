---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: 470692c946175c75bf21bd613e6bbf3590854768
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717021"
---
# <span data-ttu-id="9e90f-101">New-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="9e90f-101">New-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="9e90f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9e90f-102">SYNOPSIS</span></span>
<span data-ttu-id="9e90f-103">Tworzy nową konfigurację dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="9e90f-103">Creates a new Identity Provider configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e90f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9e90f-104">SYNTAX</span></span>

```
New-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> -ClientId <String> -ClientSecret <String>
 [-AllowedTenants <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9e90f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9e90f-105">DESCRIPTION</span></span>
<span data-ttu-id="9e90f-106">Tworzy nową konfigurację dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="9e90f-106">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="9e90f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9e90f-107">EXAMPLES</span></span>

### <span data-ttu-id="9e90f-108">Przykład 1: Konfigurowanie serwisu Facebook jako dostawcy tożsamości na potrzeby logowania w portalu dewelopera</span><span class="sxs-lookup"><span data-stu-id="9e90f-108">Example 1: Configures Facebook as an identity Provider for Developer Portal Logins</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -ClientId 'sdfsfwerwerw' -ClientSecret 'sdgsdfgfst43tewfewrf'
```

<span data-ttu-id="9e90f-109">To polecenie konfiguruje tożsamość w serwisie Facebook jako zaakceptowanego dostawcy tożsamości w portalu dewelopera usługi ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="9e90f-109">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="9e90f-110">Zajmie to ClientId i ClientSecret aplikacji Facebook.</span><span class="sxs-lookup"><span data-stu-id="9e90f-110">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

## <span data-ttu-id="9e90f-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9e90f-111">PARAMETERS</span></span>

### <span data-ttu-id="9e90f-112">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="9e90f-112">-AllowedTenants</span></span>
<span data-ttu-id="9e90f-113">Lista dozwolonych dzierżaw usługi Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="9e90f-113">List of allowed Azure Active Directory Tenants</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e90f-114">-ClientId</span><span class="sxs-lookup"><span data-stu-id="9e90f-114">-ClientId</span></span>
<span data-ttu-id="9e90f-115">Identyfikator klienta aplikacji w zewnętrznym dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="9e90f-115">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="9e90f-116">Jest to identyfikator aplikacji dla logowania do serwisu Facebook, identyfikator klienta Google login, identyfikator aplikacji dla firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9e90f-116">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="9e90f-117">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="9e90f-117">-ClientSecret</span></span>
<span data-ttu-id="9e90f-118">Klucz tajny klienta aplikacji w zewnętrznym dostawcy tożsamości, służący do uwierzytelniania żądania logowania.</span><span class="sxs-lookup"><span data-stu-id="9e90f-118">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="9e90f-119">Na przykład jest to klucz tajny aplikacji dla logowania do serwisu Facebook, klucz interfejsu API logowania Google, klucz publiczny dla firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9e90f-119">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="9e90f-120">-Context</span><span class="sxs-lookup"><span data-stu-id="9e90f-120">-Context</span></span>
<span data-ttu-id="9e90f-121">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="9e90f-121">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9e90f-122">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="9e90f-122">This parameter is required.</span></span>

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

### <span data-ttu-id="9e90f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e90f-123">-DefaultProfile</span></span>
<span data-ttu-id="9e90f-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9e90f-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="9e90f-125">-Type</span><span class="sxs-lookup"><span data-stu-id="9e90f-125">-Type</span></span>
<span data-ttu-id="9e90f-126">Identyfikator dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="9e90f-126">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="9e90f-127">Jeśli zostanie określona, spróbuje znaleźć konfigurację dostawcy tożsamości przez identyfikator.</span><span class="sxs-lookup"><span data-stu-id="9e90f-127">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="9e90f-128">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="9e90f-128">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e90f-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9e90f-129">-Confirm</span></span>
<span data-ttu-id="9e90f-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e90f-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e90f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e90f-131">-WhatIf</span></span>
<span data-ttu-id="9e90f-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e90f-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9e90f-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9e90f-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e90f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e90f-134">CommonParameters</span></span>
<span data-ttu-id="9e90f-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e90f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e90f-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e90f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e90f-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e90f-137">INPUTS</span></span>

### <span data-ttu-id="9e90f-138">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9e90f-138">None</span></span>
<span data-ttu-id="9e90f-139">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="9e90f-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9e90f-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9e90f-140">OUTPUTS</span></span>

### <span data-ttu-id="9e90f-141">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="9e90f-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="9e90f-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9e90f-142">NOTES</span></span>

## <span data-ttu-id="9e90f-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9e90f-143">RELATED LINKS</span></span>

[<span data-ttu-id="9e90f-144">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="9e90f-144">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="9e90f-145">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="9e90f-145">Remove-AzureRmApiManagementIdentityProvider</span></span>](./Remove-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="9e90f-146">Set-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="9e90f-146">Set-AzureRmApiManagementIdentityProvider</span></span>](./Set-AzureRmApiManagementIdentityProvider.md)
