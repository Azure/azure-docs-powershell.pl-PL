---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: d0883edb698000ae0aaff957899a03e9936e4d93
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547691"
---
# <span data-ttu-id="191c7-101">New-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="191c7-101">New-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="191c7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="191c7-102">SYNOPSIS</span></span>
<span data-ttu-id="191c7-103">Tworzy nową konfigurację dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="191c7-103">Creates a new Identity Provider configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="191c7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="191c7-104">SYNTAX</span></span>

```
New-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> -ClientId <String> -ClientSecret <String>
 [-AllowedTenants <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="191c7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="191c7-105">DESCRIPTION</span></span>
<span data-ttu-id="191c7-106">Tworzy nową konfigurację dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="191c7-106">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="191c7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="191c7-107">EXAMPLES</span></span>

### <span data-ttu-id="191c7-108">Przykład 1: Konfigurowanie serwisu Facebook jako dostawcy tożsamości na potrzeby logowania w portalu dewelopera</span><span class="sxs-lookup"><span data-stu-id="191c7-108">Example 1: Configures Facebook as an identity Provider for Developer Portal Logins</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -ClientId 'sdfsfwerwerw' -ClientSecret 'sdgsdfgfst43tewfewrf'
```

<span data-ttu-id="191c7-109">To polecenie konfiguruje tożsamość w serwisie Facebook jako zaakceptowanego dostawcy tożsamości w portalu dewelopera usługi ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="191c7-109">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="191c7-110">Zajmie to ClientId i ClientSecret aplikacji Facebook.</span><span class="sxs-lookup"><span data-stu-id="191c7-110">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

## <span data-ttu-id="191c7-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="191c7-111">PARAMETERS</span></span>

### <span data-ttu-id="191c7-112">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="191c7-112">-AllowedTenants</span></span>
<span data-ttu-id="191c7-113">Lista dozwolonych dzierżaw usługi Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="191c7-113">List of allowed Azure Active Directory Tenants</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="191c7-114">-ClientId</span><span class="sxs-lookup"><span data-stu-id="191c7-114">-ClientId</span></span>
<span data-ttu-id="191c7-115">Identyfikator klienta aplikacji w zewnętrznym dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="191c7-115">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="191c7-116">Jest to identyfikator aplikacji dla logowania do serwisu Facebook, identyfikator klienta Google login, identyfikator aplikacji dla firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="191c7-116">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="191c7-117">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="191c7-117">-ClientSecret</span></span>
<span data-ttu-id="191c7-118">Klucz tajny klienta aplikacji w zewnętrznym dostawcy tożsamości, służący do uwierzytelniania żądania logowania.</span><span class="sxs-lookup"><span data-stu-id="191c7-118">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="191c7-119">Na przykład jest to klucz tajny aplikacji dla logowania do serwisu Facebook, klucz interfejsu API logowania Google, klucz publiczny dla firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="191c7-119">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="191c7-120">-Context</span><span class="sxs-lookup"><span data-stu-id="191c7-120">-Context</span></span>
<span data-ttu-id="191c7-121">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="191c7-121">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="191c7-122">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="191c7-122">This parameter is required.</span></span>

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

### <span data-ttu-id="191c7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="191c7-123">-DefaultProfile</span></span>
<span data-ttu-id="191c7-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="191c7-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="191c7-125">-Type</span><span class="sxs-lookup"><span data-stu-id="191c7-125">-Type</span></span>
<span data-ttu-id="191c7-126">Identyfikator dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="191c7-126">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="191c7-127">Jeśli zostanie określona, spróbuje znaleźć konfigurację dostawcy tożsamości przez identyfikator.</span><span class="sxs-lookup"><span data-stu-id="191c7-127">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="191c7-128">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="191c7-128">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="191c7-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="191c7-129">-Confirm</span></span>
<span data-ttu-id="191c7-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="191c7-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="191c7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="191c7-131">-WhatIf</span></span>
<span data-ttu-id="191c7-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="191c7-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="191c7-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="191c7-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="191c7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="191c7-134">CommonParameters</span></span>
<span data-ttu-id="191c7-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="191c7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="191c7-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="191c7-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="191c7-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="191c7-137">INPUTS</span></span>

### <span data-ttu-id="191c7-138">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="191c7-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="191c7-139">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="191c7-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="191c7-140">System. String</span><span class="sxs-lookup"><span data-stu-id="191c7-140">System.String</span></span>

### <span data-ttu-id="191c7-141">System. String []</span><span class="sxs-lookup"><span data-stu-id="191c7-141">System.String[]</span></span>

## <span data-ttu-id="191c7-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="191c7-142">OUTPUTS</span></span>

### <span data-ttu-id="191c7-143">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="191c7-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="191c7-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="191c7-144">NOTES</span></span>

## <span data-ttu-id="191c7-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="191c7-145">RELATED LINKS</span></span>

[<span data-ttu-id="191c7-146">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="191c7-146">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="191c7-147">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="191c7-147">Remove-AzureRmApiManagementIdentityProvider</span></span>](./Remove-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="191c7-148">Set-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="191c7-148">Set-AzureRmApiManagementIdentityProvider</span></span>](./Set-AzureRmApiManagementIdentityProvider.md)
