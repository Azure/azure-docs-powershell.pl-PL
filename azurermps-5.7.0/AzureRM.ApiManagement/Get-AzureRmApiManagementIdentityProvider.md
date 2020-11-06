---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: e25e3bfad6c40b136c3cbaa65999b8118e0abd11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549784"
---
# <span data-ttu-id="e29ad-101">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="e29ad-101">Get-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="e29ad-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e29ad-102">SYNOPSIS</span></span>
<span data-ttu-id="e29ad-103">Pobierz szczegóły konfiguracji dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="e29ad-103">Get the identity provider configuration details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e29ad-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e29ad-104">SYNTAX</span></span>

### <span data-ttu-id="e29ad-105">AllIdentityProviders (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e29ad-105">AllIdentityProviders (Default)</span></span>
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e29ad-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="e29ad-106">IdentityProviderByType</span></span>
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e29ad-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e29ad-107">DESCRIPTION</span></span>
<span data-ttu-id="e29ad-108">Pobierz szczegóły konfiguracji dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="e29ad-108">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="e29ad-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e29ad-109">EXAMPLES</span></span>

### <span data-ttu-id="e29ad-110">Przykład 1: Uzyskaj wszystkich dostawców tożsamości</span><span class="sxs-lookup"><span data-stu-id="e29ad-110">Example 1: Get all Identity Providers</span></span>

```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementIdentityProvider -Context $apimContext
```

<span data-ttu-id="e29ad-111">Pobierz całą konfigurację dostawcy tożsamości w usłudze.</span><span class="sxs-lookup"><span data-stu-id="e29ad-111">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="e29ad-112">Pobierz dostawcę tożsamości typu AAD</span><span class="sxs-lookup"><span data-stu-id="e29ad-112">Get the AAD Type Identity Provider</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementIdentityProvider -Context $apimContext -Type Aad
```

<span data-ttu-id="e29ad-113">Pobiera konfigurację dostawcy tożsamości usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e29ad-113">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="e29ad-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e29ad-114">PARAMETERS</span></span>

### <span data-ttu-id="e29ad-115">-Context</span><span class="sxs-lookup"><span data-stu-id="e29ad-115">-Context</span></span>
<span data-ttu-id="e29ad-116">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="e29ad-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e29ad-117">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="e29ad-117">This parameter is required.</span></span>

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

### <span data-ttu-id="e29ad-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e29ad-118">-DefaultProfile</span></span>
<span data-ttu-id="e29ad-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e29ad-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="e29ad-120">-Type</span><span class="sxs-lookup"><span data-stu-id="e29ad-120">-Type</span></span>
<span data-ttu-id="e29ad-121">Identyfikator dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="e29ad-121">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="e29ad-122">Jeśli zostanie określona, spróbuje znaleźć konfigurację dostawcy tożsamości przez identyfikator.</span><span class="sxs-lookup"><span data-stu-id="e29ad-122">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="e29ad-123">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="e29ad-123">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementIdentityProviderType
Parameter Sets: IdentityProviderByType
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e29ad-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e29ad-124">CommonParameters</span></span>
<span data-ttu-id="e29ad-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e29ad-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e29ad-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e29ad-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e29ad-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e29ad-127">INPUTS</span></span>

### <span data-ttu-id="e29ad-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e29ad-128">None</span></span>
<span data-ttu-id="e29ad-129">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="e29ad-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e29ad-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e29ad-130">OUTPUTS</span></span>

### <span data-ttu-id="e29ad-131">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="e29ad-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>
<span data-ttu-id="e29ad-132">Szczegóły dostawcy tożsamości skonfigurowanego w usłudze zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="e29ad-132">The details of the Identity Provider configured in API Management service.</span></span>

### <span data-ttu-id="e29ad-133">IList<Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementIdentityProvider></span><span class="sxs-lookup"><span data-stu-id="e29ad-133">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider></span></span>
<span data-ttu-id="e29ad-134">Lista dostawców tożsamości skonfigurowanych w usłudze zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="e29ad-134">The list of Identity Providers configured in API Management service.</span></span>

## <span data-ttu-id="e29ad-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e29ad-135">NOTES</span></span>

## <span data-ttu-id="e29ad-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e29ad-136">RELATED LINKS</span></span>

