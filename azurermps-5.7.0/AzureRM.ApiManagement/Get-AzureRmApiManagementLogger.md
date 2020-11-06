---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A935ABAC-6C60-4AE3-9434-B9BCC1182A34
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementLogger.md
ms.openlocfilehash: bcfcd052d2278fa39bc310a5c1927457a1b0fcd3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549783"
---
# <span data-ttu-id="33d15-101">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="33d15-101">Get-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="33d15-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="33d15-102">SYNOPSIS</span></span>
<span data-ttu-id="33d15-103">Pobiera obiekty rejestratora zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="33d15-103">Gets API Management Logger objects.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33d15-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="33d15-104">SYNTAX</span></span>

### <span data-ttu-id="33d15-105">GetAllLoggers (domyślny)</span><span class="sxs-lookup"><span data-stu-id="33d15-105">GetAllLoggers (Default)</span></span>
```
Get-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="33d15-106">GetByLoggerId</span><span class="sxs-lookup"><span data-stu-id="33d15-106">GetByLoggerId</span></span>
```
Get-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33d15-107">Opis</span><span class="sxs-lookup"><span data-stu-id="33d15-107">DESCRIPTION</span></span>
<span data-ttu-id="33d15-108">Polecenie cmdlet **Get-AzureRmApiManagementLogger** pobiera **rejestratora** zarządzania usługą Azure API lub wszystkich rejestratorów.</span><span class="sxs-lookup"><span data-stu-id="33d15-108">The **Get-AzureRmApiManagementLogger** cmdlet gets an Azure API Management **Logger** or all the loggers.</span></span>

## <span data-ttu-id="33d15-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="33d15-109">EXAMPLES</span></span>

### <span data-ttu-id="33d15-110">Przykład 1. Pobierz wszystkie rejestratory</span><span class="sxs-lookup"><span data-stu-id="33d15-110">Example 1: Get all loggers</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementLogger -Context $apimContext
```

<span data-ttu-id="33d15-111">To polecenie pobiera wszystkie rejestratory dla określonego kontekstu.</span><span class="sxs-lookup"><span data-stu-id="33d15-111">This command gets all the loggers for the specified context.</span></span>

### <span data-ttu-id="33d15-112">Przykład 2: uzyskiwanie określonego rejestratora</span><span class="sxs-lookup"><span data-stu-id="33d15-112">Example 2: Get a specific logger</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123"
```

<span data-ttu-id="33d15-113">To polecenie usuwa rejestratora o IDENTYFIKATORze Logger123.</span><span class="sxs-lookup"><span data-stu-id="33d15-113">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="33d15-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="33d15-114">PARAMETERS</span></span>

### <span data-ttu-id="33d15-115">-Context</span><span class="sxs-lookup"><span data-stu-id="33d15-115">-Context</span></span>
<span data-ttu-id="33d15-116">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="33d15-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="33d15-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33d15-117">-DefaultProfile</span></span>
<span data-ttu-id="33d15-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="33d15-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="33d15-119">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="33d15-119">-LoggerId</span></span>
<span data-ttu-id="33d15-120">Określa identyfikator konkretnego rejestratora do pobrania.</span><span class="sxs-lookup"><span data-stu-id="33d15-120">Specifies the ID of the specific logger to get.</span></span>

```yaml
Type: String
Parameter Sets: GetByLoggerId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33d15-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33d15-121">CommonParameters</span></span>
<span data-ttu-id="33d15-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33d15-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33d15-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33d15-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33d15-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="33d15-124">INPUTS</span></span>

### <span data-ttu-id="33d15-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="33d15-125">None</span></span>
<span data-ttu-id="33d15-126">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="33d15-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="33d15-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="33d15-127">OUTPUTS</span></span>

### <span data-ttu-id="33d15-128">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="33d15-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>
<span data-ttu-id="33d15-129">Szczegóły rejestratora skonfigurowanego w usłudze zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="33d15-129">The detail of the Logger configured in API Management service.</span></span>

### <span data-ttu-id="33d15-130">IList<Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementLogger></span><span class="sxs-lookup"><span data-stu-id="33d15-130">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger></span></span>
<span data-ttu-id="33d15-131">Lista rejestratorów skonfigurowanych w usłudze zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="33d15-131">The list of Loggers configured in API Management service.</span></span>

## <span data-ttu-id="33d15-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="33d15-132">NOTES</span></span>

## <span data-ttu-id="33d15-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="33d15-133">RELATED LINKS</span></span>

[<span data-ttu-id="33d15-134">Nowe — AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="33d15-134">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="33d15-135">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="33d15-135">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)

[<span data-ttu-id="33d15-136">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="33d15-136">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


