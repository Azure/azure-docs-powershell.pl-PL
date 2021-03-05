---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementidentityproviderclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProviderClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProviderClientSecret.md
ms.openlocfilehash: 94480eb224d9ef6cb4e4244fc863e79c39a8d23e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997004"
---
# <span data-ttu-id="9e1b8-101">Get-AzApiManagementIdentityProviderClientSecret</span><span class="sxs-lookup"><span data-stu-id="9e1b8-101">Get-AzApiManagementIdentityProviderClientSecret</span></span>

## <span data-ttu-id="9e1b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e1b8-102">SYNOPSIS</span></span>
<span data-ttu-id="9e1b8-103">Klucz tajny klienta dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-103">Get the identity provider client secret.</span></span>

## <span data-ttu-id="9e1b8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9e1b8-104">SYNTAX</span></span>

```
Get-AzApiManagementIdentityProviderClientSecret -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e1b8-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9e1b8-105">DESCRIPTION</span></span>
<span data-ttu-id="9e1b8-106">Klucz tajny klienta dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-106">Get the identity provider client secret.</span></span>

## <span data-ttu-id="9e1b8-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9e1b8-107">EXAMPLES</span></span>

### <span data-ttu-id="9e1b8-108">Przykład 1. Uzyskiwanie tajemnicy klienta dostawcy tożsamości typu AAD</span><span class="sxs-lookup"><span data-stu-id="9e1b8-108">Example 1: Get the client secret of AAD Type Identity Provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Get-AzApiManagementIdentityProviderClientSecret -Context $apimContext -Type Aad
```

<span data-ttu-id="9e1b8-109">Kluczem tajnym klienta jest konfiguracja dostawcy tożsamości usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-109">Gets the client secret of the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="9e1b8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e1b8-110">PARAMETERS</span></span>

### <span data-ttu-id="9e1b8-111">— kontekst</span><span class="sxs-lookup"><span data-stu-id="9e1b8-111">-Context</span></span>
<span data-ttu-id="9e1b8-112">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9e1b8-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-113">This parameter is required.</span></span>

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

### <span data-ttu-id="9e1b8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e1b8-114">-DefaultProfile</span></span>
<span data-ttu-id="9e1b8-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e1b8-116">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="9e1b8-116">-Type</span></span>
<span data-ttu-id="9e1b8-117">Identyfikator dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-117">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="9e1b8-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-118">This parameter is required.</span></span>

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

### <span data-ttu-id="9e1b8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e1b8-119">CommonParameters</span></span>
<span data-ttu-id="9e1b8-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e1b8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e1b8-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9e1b8-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e1b8-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e1b8-122">INPUTS</span></span>

### <span data-ttu-id="9e1b8-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9e1b8-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9e1b8-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="9e1b8-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="9e1b8-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e1b8-125">OUTPUTS</span></span>

### <span data-ttu-id="9e1b8-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="9e1b8-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="9e1b8-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9e1b8-127">NOTES</span></span>

## <span data-ttu-id="9e1b8-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9e1b8-128">RELATED LINKS</span></span>
