---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: d97090f6374890d9ae7ba24e53d6e1d60430f7b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525802"
---
# <span data-ttu-id="d8e9f-101">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="d8e9f-101">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="d8e9f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d8e9f-102">SYNOPSIS</span></span>
<span data-ttu-id="d8e9f-103">Pobiera dostawców z OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="d8e9f-103">Gets OpenID Connect providers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8e9f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d8e9f-104">SYNTAX</span></span>

### <span data-ttu-id="d8e9f-105">Pobierz wszystkich dostawców połączeń OpenID (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="d8e9f-105">Get all OpenID Connect Providers (Default)</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8e9f-106">Identyfikator dostawcy połączenia Get wg OpenID</span><span class="sxs-lookup"><span data-stu-id="d8e9f-106">Get by OpenID Connect Provider ID</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8e9f-107">Znajdowanie według przyjaznej nazwy dostawcy OpenID Connect</span><span class="sxs-lookup"><span data-stu-id="d8e9f-107">Find by OpenID Connect Provider friendly Name</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8e9f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d8e9f-108">DESCRIPTION</span></span>
<span data-ttu-id="d8e9f-109">Polecenie cmdlet **Get-AzureRmApiManagementOpenIdConnectProvider** Pobiera dostawców usługi OpenID Connect w usłudze Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="d8e9f-109">The **Get-AzureRmApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>

## <span data-ttu-id="d8e9f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d8e9f-110">EXAMPLES</span></span>

### <span data-ttu-id="d8e9f-111">Przykład 1: Pobierz wszystkich dostawców</span><span class="sxs-lookup"><span data-stu-id="d8e9f-111">Example 1: Get all providers</span></span>
```
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext
```

<span data-ttu-id="d8e9f-112">To polecenie pobiera wszystkich dostawców usługi OpenID Connect dla określonego kontekstu.</span><span class="sxs-lookup"><span data-stu-id="d8e9f-112">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="d8e9f-113">Przykład 2: Uzyskaj dostawcę przy użyciu identyfikatora</span><span class="sxs-lookup"><span data-stu-id="d8e9f-113">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -OpenIdConnectProviderId "OICProvicer01"
```

<span data-ttu-id="d8e9f-114">To polecenie uzyskuje dostawcę o IDENTYFIKATORze OICProvicer01.</span><span class="sxs-lookup"><span data-stu-id="d8e9f-114">This command gets the provider that has the ID OICProvicer01.</span></span>

### <span data-ttu-id="d8e9f-115">Przykład 3: Uzyskaj dostawcę przy użyciu nazwy</span><span class="sxs-lookup"><span data-stu-id="d8e9f-115">Example 3: Get a provider by using a name</span></span>
```
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="d8e9f-116">To polecenie uzyskuje dostawcę o nazwie contoso OpenID Connect Provider.</span><span class="sxs-lookup"><span data-stu-id="d8e9f-116">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="d8e9f-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d8e9f-117">PARAMETERS</span></span>

### <span data-ttu-id="d8e9f-118">-Context</span><span class="sxs-lookup"><span data-stu-id="d8e9f-118">-Context</span></span>
<span data-ttu-id="d8e9f-119">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="d8e9f-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d8e9f-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d8e9f-120">-Name</span></span>
<span data-ttu-id="d8e9f-121">Określa przyjazną nazwę dostawcy.</span><span class="sxs-lookup"><span data-stu-id="d8e9f-121">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="d8e9f-122">Jeśli określisz nazwę, to polecenie cmdlet otrzyma tego dostawcę.</span><span class="sxs-lookup"><span data-stu-id="d8e9f-122">If you specify a name, this cmdlet gets that provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Find by OpenID Connect Provider friendly Name
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8e9f-123">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="d8e9f-123">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="d8e9f-124">Określa identyfikator dostawcy, który usunie to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8e9f-124">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="d8e9f-125">Jeśli określisz identyfikator, to polecenie cmdlet otrzyma tego dostawcę.</span><span class="sxs-lookup"><span data-stu-id="d8e9f-125">If you specify an ID, this cmdlet gets that provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by OpenID Connect Provider ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8e9f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8e9f-126">-DefaultProfile</span></span>
<span data-ttu-id="d8e9f-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d8e9f-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8e9f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8e9f-128">CommonParameters</span></span>
<span data-ttu-id="d8e9f-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8e9f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8e9f-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8e9f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8e9f-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8e9f-131">INPUTS</span></span>

## <span data-ttu-id="d8e9f-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d8e9f-132">OUTPUTS</span></span>

### <span data-ttu-id="d8e9f-133">IList<Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementOpenIdConnectProvider></span><span class="sxs-lookup"><span data-stu-id="d8e9f-133">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider></span></span>

## <span data-ttu-id="d8e9f-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d8e9f-134">NOTES</span></span>

## <span data-ttu-id="d8e9f-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d8e9f-135">RELATED LINKS</span></span>

[<span data-ttu-id="d8e9f-136">Nowe — AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="d8e9f-136">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="d8e9f-137">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="d8e9f-137">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="d8e9f-138">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="d8e9f-138">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


