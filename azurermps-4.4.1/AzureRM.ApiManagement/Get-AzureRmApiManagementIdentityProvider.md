---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: 2b38728f90de4639bf3e125f226ae2b40527ca45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547267"
---
# <span data-ttu-id="d6d96-101">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="d6d96-101">Get-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="d6d96-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d6d96-102">SYNOPSIS</span></span>
<span data-ttu-id="d6d96-103">Pobierz szczegóły konfiguracji dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="d6d96-103">Get the identity provider configuration details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6d96-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d6d96-104">SYNTAX</span></span>

### <span data-ttu-id="d6d96-105">AllIdentityProviders (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d6d96-105">AllIdentityProviders (Default)</span></span>
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6d96-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="d6d96-106">IdentityProviderByType</span></span>
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6d96-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d6d96-107">DESCRIPTION</span></span>
<span data-ttu-id="d6d96-108">Pobierz szczegóły konfiguracji dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="d6d96-108">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="d6d96-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d6d96-109">EXAMPLES</span></span>

### <span data-ttu-id="d6d96-110">--------------------------Przykład 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d6d96-110">--------------------------  Example 1  --------------------------</span></span>
<span data-ttu-id="d6d96-111">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="d6d96-111">@{paragraph=PS C:\\\>}</span></span>







```
Get-AzureRmApiManagementIdentityProvider -Context $context
```

<span data-ttu-id="d6d96-112">Pobierz całą konfigurację dostawcy tożsamości w usłudze.</span><span class="sxs-lookup"><span data-stu-id="d6d96-112">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="d6d96-113">--------------------------Przykład 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="d6d96-113">--------------------------  Example 2  --------------------------</span></span>
<span data-ttu-id="d6d96-114">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="d6d96-114">@{paragraph=PS C:\\\>}</span></span>







```
Get-AzureRmApiManagementIdentityProvider -Context $context -Type Aad
```

<span data-ttu-id="d6d96-115">Pobiera konfigurację dostawcy tożsamości usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d6d96-115">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="d6d96-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d6d96-116">PARAMETERS</span></span>

### <span data-ttu-id="d6d96-117">-Context</span><span class="sxs-lookup"><span data-stu-id="d6d96-117">-Context</span></span>
<span data-ttu-id="d6d96-118">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d6d96-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d6d96-119">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="d6d96-119">This parameter is required.</span></span>

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

### <span data-ttu-id="d6d96-120">-Type</span><span class="sxs-lookup"><span data-stu-id="d6d96-120">-Type</span></span>
<span data-ttu-id="d6d96-121">Identyfikator dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="d6d96-121">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="d6d96-122">Jeśli zostanie określona, spróbuje znaleźć konfigurację dostawcy tożsamości przez identyfikator.</span><span class="sxs-lookup"><span data-stu-id="d6d96-122">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="d6d96-123">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="d6d96-123">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: IdentityProviderByType
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6d96-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6d96-124">-DefaultProfile</span></span>
<span data-ttu-id="d6d96-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d6d96-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6d96-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6d96-126">CommonParameters</span></span>
<span data-ttu-id="d6d96-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6d96-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6d96-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6d96-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6d96-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6d96-129">INPUTS</span></span>

## <span data-ttu-id="d6d96-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d6d96-130">OUTPUTS</span></span>

### <span data-ttu-id="d6d96-131">IList<Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementIdentityProvider></span><span class="sxs-lookup"><span data-stu-id="d6d96-131">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider></span></span>

### <span data-ttu-id="d6d96-132">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="d6d96-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="d6d96-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d6d96-133">NOTES</span></span>

## <span data-ttu-id="d6d96-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d6d96-134">RELATED LINKS</span></span>

