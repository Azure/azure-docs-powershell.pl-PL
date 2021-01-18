---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
ms.openlocfilehash: b267fc854127c1cb098481ac483a7572c8b2e12f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502490"
---
# <span data-ttu-id="7299a-101">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="7299a-101">Get-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="7299a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7299a-102">SYNOPSIS</span></span>
<span data-ttu-id="7299a-103">Pobierz szczegóły konfiguracji dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="7299a-103">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="7299a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7299a-104">SYNTAX</span></span>

### <span data-ttu-id="7299a-105">AllIdentityProviders (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7299a-105">AllIdentityProviders (Default)</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7299a-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="7299a-106">IdentityProviderByType</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7299a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7299a-107">DESCRIPTION</span></span>
<span data-ttu-id="7299a-108">Pobierz szczegóły konfiguracji dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="7299a-108">Get the identity provider configuration details.</span></span>
<span data-ttu-id="7299a-109">ClientSecret nie zostaną uwzględnione w szczegółach wyników.</span><span class="sxs-lookup"><span data-stu-id="7299a-109">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="7299a-110">Aby uzyskać klucz tajny klienta, użyj polecenie **Get-AzApiManagementIdentityProviderClientSecret**.</span><span class="sxs-lookup"><span data-stu-id="7299a-110">To get client secret, use **Get-AzApiManagementIdentityProviderClientSecret**.</span></span>

## <span data-ttu-id="7299a-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7299a-111">EXAMPLES</span></span>

### <span data-ttu-id="7299a-112">Przykład 1: Uzyskaj wszystkich dostawców tożsamości</span><span class="sxs-lookup"><span data-stu-id="7299a-112">Example 1: Get all Identity Providers</span></span>

```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementIdentityProvider -Context $apimContext
```

<span data-ttu-id="7299a-113">Pobierz całą konfigurację dostawcy tożsamości w usłudze.</span><span class="sxs-lookup"><span data-stu-id="7299a-113">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="7299a-114">Przykład 2: Uzyskaj dostawcę tożsamości typu AAD</span><span class="sxs-lookup"><span data-stu-id="7299a-114">Example 2: Get the AAD Type Identity Provider</span></span>
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

<span data-ttu-id="7299a-115">Pobiera konfigurację dostawcy tożsamości usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7299a-115">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

### <span data-ttu-id="7299a-116">Przykład 3: uzyskiwanie dostawcy tożsamości typu usługi AAD B2C</span><span class="sxs-lookup"><span data-stu-id="7299a-116">Example 3: Get the AAD B2C Type Identity Provider</span></span>
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

<span data-ttu-id="7299a-117">Pobiera konfigurację dostawcy tożsamości usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7299a-117">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="7299a-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7299a-118">PARAMETERS</span></span>

### <span data-ttu-id="7299a-119">-Context</span><span class="sxs-lookup"><span data-stu-id="7299a-119">-Context</span></span>
<span data-ttu-id="7299a-120">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="7299a-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="7299a-121">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="7299a-121">This parameter is required.</span></span>

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

### <span data-ttu-id="7299a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7299a-122">-DefaultProfile</span></span>
<span data-ttu-id="7299a-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7299a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7299a-124">-Type</span><span class="sxs-lookup"><span data-stu-id="7299a-124">-Type</span></span>
<span data-ttu-id="7299a-125">Identyfikator dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="7299a-125">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="7299a-126">Jeśli zostanie określona, spróbuje znaleźć konfigurację dostawcy tożsamości przez identyfikator.</span><span class="sxs-lookup"><span data-stu-id="7299a-126">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="7299a-127">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="7299a-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="7299a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7299a-128">CommonParameters</span></span>
<span data-ttu-id="7299a-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7299a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7299a-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7299a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7299a-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7299a-131">INPUTS</span></span>

### <span data-ttu-id="7299a-132">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7299a-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7299a-133">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="7299a-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="7299a-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7299a-134">OUTPUTS</span></span>

### <span data-ttu-id="7299a-135">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="7299a-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="7299a-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7299a-136">NOTES</span></span>

## <span data-ttu-id="7299a-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7299a-137">RELATED LINKS</span></span>
