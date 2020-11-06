---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementBackend.md
ms.openlocfilehash: 4f54b361482bad24826d7120e53f96ce8d3b9eef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548443"
---
# <span data-ttu-id="3c419-101">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="3c419-101">Get-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="3c419-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3c419-102">SYNOPSIS</span></span>
<span data-ttu-id="3c419-103">Zapoznaj się z informacjami o wewnętrznej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="3c419-103">Get the details of the Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c419-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3c419-104">SYNTAX</span></span>

### <span data-ttu-id="3c419-105">Pobieranie wszystkich zakończeń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="3c419-105">Get all backends (Default)</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3c419-106">Uzyskaj według identyfikatora zaplecza</span><span class="sxs-lookup"><span data-stu-id="3c419-106">Get by backend ID</span></span>
```
Get-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c419-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3c419-107">DESCRIPTION</span></span>
<span data-ttu-id="3c419-108">Zapoznaj się z informacjami o wewnętrznej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="3c419-108">Get the details of the Backend.</span></span>

## <span data-ttu-id="3c419-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3c419-109">EXAMPLES</span></span>

### <span data-ttu-id="3c419-110">--------------------------Przykład 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3c419-110">--------------------------  Example 1  --------------------------</span></span>
<span data-ttu-id="3c419-111">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="3c419-111">@{paragraph=PS C:\\\>}</span></span>







```
Get-AzureRmApiManagementBackend -Context $apimContext
```

<span data-ttu-id="3c419-112">Pobiera listę wszystkich punktów końcowych skonfigurowanych w usłudze zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="3c419-112">Gets a list of all the Backends configured in the Api Management service.</span></span>

### <span data-ttu-id="3c419-113">--------------------------Przykład 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="3c419-113">--------------------------  Example 2  --------------------------</span></span>
<span data-ttu-id="3c419-114">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="3c419-114">@{paragraph=PS C:\\\>}</span></span>







```
Get-AzureRmApiManagementBackend -Context $apimContext -backendId 123
```

<span data-ttu-id="3c419-115">Uzyskiwanie szczegółów dotyczących określonej zaplecza wewnętrznego określonego identyfikatorem ' 123 '</span><span class="sxs-lookup"><span data-stu-id="3c419-115">Get the details of the specified Backend identified by the Identifier '123'</span></span>

## <span data-ttu-id="3c419-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3c419-116">PARAMETERS</span></span>

### <span data-ttu-id="3c419-117">-BackendId</span><span class="sxs-lookup"><span data-stu-id="3c419-117">-BackendId</span></span>
<span data-ttu-id="3c419-118">Identyfikator wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="3c419-118">Identifier of a backend.</span></span>
<span data-ttu-id="3c419-119">Jeśli zostanie określona, spróbuje znaleźć zaplecze o identyfikatorze.</span><span class="sxs-lookup"><span data-stu-id="3c419-119">If specified will try to find backend by the identifier.</span></span>
<span data-ttu-id="3c419-120">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="3c419-120">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by backend ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c419-121">-Context</span><span class="sxs-lookup"><span data-stu-id="3c419-121">-Context</span></span>
<span data-ttu-id="3c419-122">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="3c419-122">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="3c419-123">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="3c419-123">This parameter is required.</span></span>

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

### <span data-ttu-id="3c419-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c419-124">-DefaultProfile</span></span>
<span data-ttu-id="3c419-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3c419-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c419-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c419-126">CommonParameters</span></span>
<span data-ttu-id="3c419-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c419-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c419-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c419-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c419-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3c419-129">INPUTS</span></span>

## <span data-ttu-id="3c419-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3c419-130">OUTPUTS</span></span>

### <span data-ttu-id="3c419-131">IList<Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementBackend></span><span class="sxs-lookup"><span data-stu-id="3c419-131">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend></span></span>

### <span data-ttu-id="3c419-132">Microsoft. Azure. Commands. ApiManagement. servicemanagement. modele. PsApiManagementLogger. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="3c419-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger.PsApiManagementBackend</span></span>

## <span data-ttu-id="3c419-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3c419-133">NOTES</span></span>

## <span data-ttu-id="3c419-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3c419-134">RELATED LINKS</span></span>

[<span data-ttu-id="3c419-135">Nowe — AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="3c419-135">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="3c419-136">Nowe — AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="3c419-136">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="3c419-137">Nowe — AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="3c419-137">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="3c419-138">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="3c419-138">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="3c419-139">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="3c419-139">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
