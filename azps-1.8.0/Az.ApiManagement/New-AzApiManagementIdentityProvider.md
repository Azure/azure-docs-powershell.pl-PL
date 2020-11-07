---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
ms.openlocfilehash: c0730053dce60dbf556ef00f522aa463ffb26601
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710637"
---
# <span data-ttu-id="2b2ff-101">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="2b2ff-101">New-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="2b2ff-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2b2ff-102">SYNOPSIS</span></span>
<span data-ttu-id="2b2ff-103">Tworzy nową konfigurację dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="2b2ff-103">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="2b2ff-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2b2ff-104">SYNTAX</span></span>

```
New-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> -ClientId <String> -ClientSecret <String>
 [-AllowedTenants <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2b2ff-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2b2ff-105">DESCRIPTION</span></span>
<span data-ttu-id="2b2ff-106">Tworzy nową konfigurację dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="2b2ff-106">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="2b2ff-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2b2ff-107">EXAMPLES</span></span>

### <span data-ttu-id="2b2ff-108">Przykład 1: Konfigurowanie serwisu Facebook jako dostawcy tożsamości na potrzeby logowania w portalu dewelopera</span><span class="sxs-lookup"><span data-stu-id="2b2ff-108">Example 1: Configures Facebook as an identity Provider for Developer Portal Logins</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -ClientId 'sdfsfwerwerw' -ClientSecret 'sdgsdfgfst43tewfewrf'
```

<span data-ttu-id="2b2ff-109">To polecenie konfiguruje tożsamość w serwisie Facebook jako zaakceptowanego dostawcy tożsamości w portalu dewelopera usługi ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="2b2ff-109">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="2b2ff-110">Zajmie to ClientId i ClientSecret aplikacji Facebook.</span><span class="sxs-lookup"><span data-stu-id="2b2ff-110">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

## <span data-ttu-id="2b2ff-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2b2ff-111">PARAMETERS</span></span>

### <span data-ttu-id="2b2ff-112">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="2b2ff-112">-AllowedTenants</span></span>
<span data-ttu-id="2b2ff-113">Lista dozwolonych dzierżaw usługi Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="2b2ff-113">List of allowed Azure Active Directory Tenants</span></span>

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

### <span data-ttu-id="2b2ff-114">-ClientId</span><span class="sxs-lookup"><span data-stu-id="2b2ff-114">-ClientId</span></span>
<span data-ttu-id="2b2ff-115">Identyfikator klienta aplikacji w zewnętrznym dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="2b2ff-115">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="2b2ff-116">Jest to identyfikator aplikacji dla logowania do serwisu Facebook, identyfikator klienta Google login, identyfikator aplikacji dla firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2b2ff-116">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="2b2ff-117">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="2b2ff-117">-ClientSecret</span></span>
<span data-ttu-id="2b2ff-118">Klucz tajny klienta aplikacji w zewnętrznym dostawcy tożsamości, służący do uwierzytelniania żądania logowania.</span><span class="sxs-lookup"><span data-stu-id="2b2ff-118">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="2b2ff-119">Na przykład jest to klucz tajny aplikacji dla logowania do serwisu Facebook, klucz interfejsu API logowania Google, klucz publiczny dla firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2b2ff-119">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="2b2ff-120">-Context</span><span class="sxs-lookup"><span data-stu-id="2b2ff-120">-Context</span></span>
<span data-ttu-id="2b2ff-121">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="2b2ff-121">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2b2ff-122">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="2b2ff-122">This parameter is required.</span></span>

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

### <span data-ttu-id="2b2ff-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b2ff-123">-DefaultProfile</span></span>
<span data-ttu-id="2b2ff-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2b2ff-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b2ff-125">-Type</span><span class="sxs-lookup"><span data-stu-id="2b2ff-125">-Type</span></span>
<span data-ttu-id="2b2ff-126">Identyfikator dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="2b2ff-126">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="2b2ff-127">Jeśli zostanie określona, spróbuje znaleźć konfigurację dostawcy tożsamości przez identyfikator.</span><span class="sxs-lookup"><span data-stu-id="2b2ff-127">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="2b2ff-128">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="2b2ff-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="2b2ff-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2b2ff-129">-Confirm</span></span>
<span data-ttu-id="2b2ff-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b2ff-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b2ff-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b2ff-131">-WhatIf</span></span>
<span data-ttu-id="2b2ff-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b2ff-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2b2ff-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2b2ff-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b2ff-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b2ff-134">CommonParameters</span></span>
<span data-ttu-id="2b2ff-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b2ff-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b2ff-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b2ff-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b2ff-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2b2ff-137">INPUTS</span></span>

### <span data-ttu-id="2b2ff-138">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2b2ff-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2b2ff-139">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="2b2ff-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="2b2ff-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2b2ff-140">System.String</span></span>

### <span data-ttu-id="2b2ff-141">System. String []</span><span class="sxs-lookup"><span data-stu-id="2b2ff-141">System.String[]</span></span>

## <span data-ttu-id="2b2ff-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2b2ff-142">OUTPUTS</span></span>

### <span data-ttu-id="2b2ff-143">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="2b2ff-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="2b2ff-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2b2ff-144">NOTES</span></span>

## <span data-ttu-id="2b2ff-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2b2ff-145">RELATED LINKS</span></span>

[<span data-ttu-id="2b2ff-146">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="2b2ff-146">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="2b2ff-147">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="2b2ff-147">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="2b2ff-148">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="2b2ff-148">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)
