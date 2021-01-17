---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityproviderclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProviderClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProviderClientSecret.md
ms.openlocfilehash: d75d385bc158e0855601d3432dff79b2e4339f2f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365855"
---
# <span data-ttu-id="81b25-101">Get-AzApiManagementIdentityProviderClientSecret</span><span class="sxs-lookup"><span data-stu-id="81b25-101">Get-AzApiManagementIdentityProviderClientSecret</span></span>

## <span data-ttu-id="81b25-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="81b25-102">SYNOPSIS</span></span>
<span data-ttu-id="81b25-103">Uzyskaj klucz tajny klienta dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="81b25-103">Get the identity provider client secret.</span></span>

## <span data-ttu-id="81b25-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="81b25-104">SYNTAX</span></span>

```
Get-AzApiManagementIdentityProviderClientSecret -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81b25-105">Opis</span><span class="sxs-lookup"><span data-stu-id="81b25-105">DESCRIPTION</span></span>
<span data-ttu-id="81b25-106">Uzyskaj klucz tajny klienta dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="81b25-106">Get the identity provider client secret.</span></span>

## <span data-ttu-id="81b25-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="81b25-107">EXAMPLES</span></span>

### <span data-ttu-id="81b25-108">Przykład 1: Uzyskiwanie klucza tajnego klienta dla dostawcy tożsamości typu AAD</span><span class="sxs-lookup"><span data-stu-id="81b25-108">Example 1: Get the client secret of AAD Type Identity Provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Get-AzApiManagementIdentityProviderClientSecret -Context $apimContext -Type Aad
```

<span data-ttu-id="81b25-109">Pobiera klucz tajny klienta konfiguracji dostawcy tożsamości usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="81b25-109">Gets the client secret of the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="81b25-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="81b25-110">PARAMETERS</span></span>

### <span data-ttu-id="81b25-111">-Context</span><span class="sxs-lookup"><span data-stu-id="81b25-111">-Context</span></span>
<span data-ttu-id="81b25-112">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="81b25-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="81b25-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="81b25-113">This parameter is required.</span></span>

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

### <span data-ttu-id="81b25-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81b25-114">-DefaultProfile</span></span>
<span data-ttu-id="81b25-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="81b25-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81b25-116">-Type</span><span class="sxs-lookup"><span data-stu-id="81b25-116">-Type</span></span>
<span data-ttu-id="81b25-117">Identyfikator dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="81b25-117">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="81b25-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="81b25-118">This parameter is required.</span></span>

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

### <span data-ttu-id="81b25-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81b25-119">CommonParameters</span></span>
<span data-ttu-id="81b25-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81b25-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81b25-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81b25-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81b25-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="81b25-122">INPUTS</span></span>

### <span data-ttu-id="81b25-123">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="81b25-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="81b25-124">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="81b25-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="81b25-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="81b25-125">OUTPUTS</span></span>

### <span data-ttu-id="81b25-126">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="81b25-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="81b25-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="81b25-127">NOTES</span></span>

## <span data-ttu-id="81b25-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="81b25-128">RELATED LINKS</span></span>
