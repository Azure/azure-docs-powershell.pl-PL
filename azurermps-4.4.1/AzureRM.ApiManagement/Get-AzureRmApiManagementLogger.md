---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A935ABAC-6C60-4AE3-9434-B9BCC1182A34
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementLogger.md
ms.openlocfilehash: 48033c250286c59e2cadfadc1a5b5d28f869a66c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550132"
---
# <span data-ttu-id="cdf60-101">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="cdf60-101">Get-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="cdf60-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cdf60-102">SYNOPSIS</span></span>
<span data-ttu-id="cdf60-103">Pobiera obiekty rejestratora zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="cdf60-103">Gets API Management Logger objects.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cdf60-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cdf60-104">SYNTAX</span></span>

### <span data-ttu-id="cdf60-105">Pobierz wszystkie rejestratory (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="cdf60-105">Get all loggers (Default)</span></span>
```
Get-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cdf60-106">Zapoznaj się z IDENTYFIKATORem rejestratora</span><span class="sxs-lookup"><span data-stu-id="cdf60-106">Get by logger ID</span></span>
```
Get-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cdf60-107">Opis</span><span class="sxs-lookup"><span data-stu-id="cdf60-107">DESCRIPTION</span></span>
<span data-ttu-id="cdf60-108">Polecenie cmdlet **Get-AzureRmApiManagementLogger** pobiera **rejestratora** zarządzania usługą Azure API lub wszystkich rejestratorów.</span><span class="sxs-lookup"><span data-stu-id="cdf60-108">The **Get-AzureRmApiManagementLogger** cmdlet gets an Azure API Management **Logger** or all the loggers.</span></span>

## <span data-ttu-id="cdf60-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cdf60-109">EXAMPLES</span></span>

### <span data-ttu-id="cdf60-110">Przykład 1. Pobierz wszystkie rejestratory</span><span class="sxs-lookup"><span data-stu-id="cdf60-110">Example 1: Get all loggers</span></span>
```
PS C:\>Get-AzureRmApiManagementLogger -Context $ApimContext
```

<span data-ttu-id="cdf60-111">To polecenie pobiera wszystkie rejestratory dla określonego kontekstu.</span><span class="sxs-lookup"><span data-stu-id="cdf60-111">This command gets all the loggers for the specified context.</span></span>

### <span data-ttu-id="cdf60-112">Przykład 2: uzyskiwanie określonego rejestratora</span><span class="sxs-lookup"><span data-stu-id="cdf60-112">Example 2: Get a specific logger</span></span>
```
PS C:\>Get-AzureRmApiManagementLogger -Context $ApimContext -LoggerId "Logger123"
```

<span data-ttu-id="cdf60-113">To polecenie usuwa rejestratora o IDENTYFIKATORze Logger123.</span><span class="sxs-lookup"><span data-stu-id="cdf60-113">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="cdf60-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cdf60-114">PARAMETERS</span></span>

### <span data-ttu-id="cdf60-115">-Context</span><span class="sxs-lookup"><span data-stu-id="cdf60-115">-Context</span></span>
<span data-ttu-id="cdf60-116">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="cdf60-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="cdf60-117">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="cdf60-117">-LoggerId</span></span>
<span data-ttu-id="cdf60-118">Określa identyfikator konkretnego rejestratora do pobrania.</span><span class="sxs-lookup"><span data-stu-id="cdf60-118">Specifies the ID of the specific logger to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by logger ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdf60-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdf60-119">-DefaultProfile</span></span>
<span data-ttu-id="cdf60-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cdf60-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cdf60-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdf60-121">CommonParameters</span></span>
<span data-ttu-id="cdf60-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdf60-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdf60-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdf60-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdf60-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cdf60-124">INPUTS</span></span>

## <span data-ttu-id="cdf60-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cdf60-125">OUTPUTS</span></span>

### <span data-ttu-id="cdf60-126">IList<Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementLogger></span><span class="sxs-lookup"><span data-stu-id="cdf60-126">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger></span></span>

## <span data-ttu-id="cdf60-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cdf60-127">NOTES</span></span>

## <span data-ttu-id="cdf60-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cdf60-128">RELATED LINKS</span></span>

[<span data-ttu-id="cdf60-129">Nowe — AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="cdf60-129">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="cdf60-130">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="cdf60-130">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)

[<span data-ttu-id="cdf60-131">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="cdf60-131">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


