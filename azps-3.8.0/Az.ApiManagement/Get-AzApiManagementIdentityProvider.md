---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
ms.openlocfilehash: 75525d3c77c3e2113c0e3cff5a7741ab916d7485
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050899"
---
# <span data-ttu-id="903b9-101">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="903b9-101">Get-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="903b9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="903b9-102">SYNOPSIS</span></span>
<span data-ttu-id="903b9-103">Pobierz szczegóły konfiguracji dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="903b9-103">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="903b9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="903b9-104">SYNTAX</span></span>

### <span data-ttu-id="903b9-105">AllIdentityProviders (domyślny)</span><span class="sxs-lookup"><span data-stu-id="903b9-105">AllIdentityProviders (Default)</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="903b9-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="903b9-106">IdentityProviderByType</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="903b9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="903b9-107">DESCRIPTION</span></span>
<span data-ttu-id="903b9-108">Pobierz szczegóły konfiguracji dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="903b9-108">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="903b9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="903b9-109">EXAMPLES</span></span>

### <span data-ttu-id="903b9-110">Przykład 1: Uzyskaj wszystkich dostawców tożsamości</span><span class="sxs-lookup"><span data-stu-id="903b9-110">Example 1: Get all Identity Providers</span></span>

```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementIdentityProvider -Context $apimContext
```

<span data-ttu-id="903b9-111">Pobierz całą konfigurację dostawcy tożsamości w usłudze.</span><span class="sxs-lookup"><span data-stu-id="903b9-111">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="903b9-112">Przykład 2: Uzyskaj dostawcę tożsamości typu AAD</span><span class="sxs-lookup"><span data-stu-id="903b9-112">Example 2: Get the AAD Type Identity Provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Get-AzApiManagementIdentityProvider -Context $apimContext -Type Aad


Type                     : Aad
ClientId                 : aaa
ClientSecret             : xxxxx
AllowedTenants           : {contosotest.onmicrosoft.com}
Authority                : login.microsoftonline.com
SignupPolicyName         :
SigninPolicyName         :
ProfileEditingPolicyName :
PasswordResetPolicyName  :
SigninTenant             :
Id                       : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/identityProviders/Aad
ResourceGroupName        : Api-Default-West-US
ServiceName              : contoso
```

<span data-ttu-id="903b9-113">Pobiera konfigurację dostawcy tożsamości usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="903b9-113">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

### <span data-ttu-id="903b9-114">Przykład 3: uzyskiwanie dostawcy tożsamości typu usługi AAD B2C</span><span class="sxs-lookup"><span data-stu-id="903b9-114">Example 3: Get the AAD B2C Type Identity Provider</span></span>
```powershell
PS C:\>$context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Get-AzApiManagementIdentityProvider -Context $context -Type AadB2C


Type                     : AadB2C
ClientId                 : f02dafe2-b8b8-48ec-a38e-27e5c16c51e5
ClientSecret             : xxxxxx
AllowedTenants           : {contosoaadb2c.onmicrosoft.com}
Authority                : login.microsoftonline.com
SignupPolicyName         : B2C_1_policy-signup
SigninPolicyName         : B2C_1_policy-signin
ProfileEditingPolicyName :
PasswordResetPolicyName  :
SigninTenant             : contosoaadb2c.onmicrosoft.com
Id                       : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/identityProviders/AadB2C
ResourceGroupName        : Api-Default-West-US
ServiceName              : contoso
```

<span data-ttu-id="903b9-115">Pobiera konfigurację dostawcy tożsamości usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="903b9-115">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="903b9-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="903b9-116">PARAMETERS</span></span>

### <span data-ttu-id="903b9-117">-Context</span><span class="sxs-lookup"><span data-stu-id="903b9-117">-Context</span></span>
<span data-ttu-id="903b9-118">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="903b9-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="903b9-119">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="903b9-119">This parameter is required.</span></span>

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

### <span data-ttu-id="903b9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="903b9-120">-DefaultProfile</span></span>
<span data-ttu-id="903b9-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="903b9-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="903b9-122">-Type</span><span class="sxs-lookup"><span data-stu-id="903b9-122">-Type</span></span>
<span data-ttu-id="903b9-123">Identyfikator dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="903b9-123">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="903b9-124">Jeśli zostanie określona, spróbuje znaleźć konfigurację dostawcy tożsamości przez identyfikator.</span><span class="sxs-lookup"><span data-stu-id="903b9-124">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="903b9-125">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="903b9-125">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: IdentityProviderByType
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="903b9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="903b9-126">CommonParameters</span></span>
<span data-ttu-id="903b9-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="903b9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="903b9-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="903b9-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="903b9-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="903b9-129">INPUTS</span></span>

### <span data-ttu-id="903b9-130">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="903b9-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="903b9-131">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="903b9-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="903b9-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="903b9-132">OUTPUTS</span></span>

### <span data-ttu-id="903b9-133">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="903b9-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="903b9-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="903b9-134">NOTES</span></span>

## <span data-ttu-id="903b9-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="903b9-135">RELATED LINKS</span></span>
