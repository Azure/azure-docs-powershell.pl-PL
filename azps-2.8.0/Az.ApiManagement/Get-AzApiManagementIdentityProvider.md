---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
ms.openlocfilehash: f3692383f5fc93c0d76951f6dcaeb409ae3ee0f7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707074"
---
# <span data-ttu-id="2d6d7-101">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="2d6d7-101">Get-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="2d6d7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2d6d7-102">SYNOPSIS</span></span>
<span data-ttu-id="2d6d7-103">Pobierz szczegóły konfiguracji dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="2d6d7-103">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="2d6d7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2d6d7-104">SYNTAX</span></span>

### <span data-ttu-id="2d6d7-105">AllIdentityProviders (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2d6d7-105">AllIdentityProviders (Default)</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d6d7-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="2d6d7-106">IdentityProviderByType</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d6d7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2d6d7-107">DESCRIPTION</span></span>
<span data-ttu-id="2d6d7-108">Pobierz szczegóły konfiguracji dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="2d6d7-108">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="2d6d7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2d6d7-109">EXAMPLES</span></span>

### <span data-ttu-id="2d6d7-110">Przykład 1: Uzyskaj wszystkich dostawców tożsamości</span><span class="sxs-lookup"><span data-stu-id="2d6d7-110">Example 1: Get all Identity Providers</span></span>

```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementIdentityProvider -Context $apimContext
```

<span data-ttu-id="2d6d7-111">Pobierz całą konfigurację dostawcy tożsamości w usłudze.</span><span class="sxs-lookup"><span data-stu-id="2d6d7-111">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="2d6d7-112">Pobierz dostawcę tożsamości typu AAD</span><span class="sxs-lookup"><span data-stu-id="2d6d7-112">Get the AAD Type Identity Provider</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementIdentityProvider -Context $apimContext -Type Aad
```

<span data-ttu-id="2d6d7-113">Pobiera konfigurację dostawcy tożsamości usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2d6d7-113">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="2d6d7-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2d6d7-114">PARAMETERS</span></span>

### <span data-ttu-id="2d6d7-115">-Context</span><span class="sxs-lookup"><span data-stu-id="2d6d7-115">-Context</span></span>
<span data-ttu-id="2d6d7-116">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="2d6d7-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2d6d7-117">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="2d6d7-117">This parameter is required.</span></span>

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

### <span data-ttu-id="2d6d7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d6d7-118">-DefaultProfile</span></span>
<span data-ttu-id="2d6d7-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2d6d7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d6d7-120">-Type</span><span class="sxs-lookup"><span data-stu-id="2d6d7-120">-Type</span></span>
<span data-ttu-id="2d6d7-121">Identyfikator dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="2d6d7-121">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="2d6d7-122">Jeśli zostanie określona, spróbuje znaleźć konfigurację dostawcy tożsamości przez identyfikator.</span><span class="sxs-lookup"><span data-stu-id="2d6d7-122">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="2d6d7-123">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="2d6d7-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="2d6d7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d6d7-124">CommonParameters</span></span>
<span data-ttu-id="2d6d7-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d6d7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d6d7-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2d6d7-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d6d7-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2d6d7-127">INPUTS</span></span>

### <span data-ttu-id="2d6d7-128">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2d6d7-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2d6d7-129">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="2d6d7-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="2d6d7-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2d6d7-130">OUTPUTS</span></span>

### <span data-ttu-id="2d6d7-131">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="2d6d7-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="2d6d7-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2d6d7-132">NOTES</span></span>

## <span data-ttu-id="2d6d7-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2d6d7-133">RELATED LINKS</span></span>
