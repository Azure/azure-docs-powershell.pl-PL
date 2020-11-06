---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 17D53F56-6E3B-491E-8776-5EBE109FBE3C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementLogger.md
ms.openlocfilehash: c7827f0df8b1baf4bb2fead9df091619751c969c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547199"
---
# <span data-ttu-id="0d689-101">New-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="0d689-101">New-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="0d689-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0d689-102">SYNOPSIS</span></span>
<span data-ttu-id="0d689-103">Tworzy rejestratora zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="0d689-103">Creates an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d689-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0d689-104">SYNTAX</span></span>

```
New-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>] -Name <String>
 -ConnectionString <String> [-Description <String>] [-IsBuffered <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d689-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0d689-105">DESCRIPTION</span></span>
<span data-ttu-id="0d689-106">Polecenie cmdlet **New-AzureRmApiManagementLogger** tworzy **Rejestrator** zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="0d689-106">The **New-AzureRmApiManagementLogger** cmdlet creates an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="0d689-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0d689-107">EXAMPLES</span></span>

### <span data-ttu-id="0d689-108">Przykład 1. tworzenie rejestratora</span><span class="sxs-lookup"><span data-stu-id="0d689-108">Example 1: Create a logger</span></span>
```
PS C:\>New-AzureRmApiManagementLogger -Context $ApimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "SDK event hub logger"
```

<span data-ttu-id="0d689-109">To polecenie tworzy Rejestrator o nazwie ContosoSdkEventHub, używając określonych parametrów połączenia.</span><span class="sxs-lookup"><span data-stu-id="0d689-109">This command creates a logger named ContosoSdkEventHub by using the specified connection string.</span></span>

## <span data-ttu-id="0d689-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0d689-110">PARAMETERS</span></span>

### <span data-ttu-id="0d689-111">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="0d689-111">-ConnectionString</span></span>
<span data-ttu-id="0d689-112">Określa parametry połączenia z koncentratorem zdarzeń platformy Azure, które zaczynają się od następującego:</span><span class="sxs-lookup"><span data-stu-id="0d689-112">Specifies an Azure Event Hubs connection string that starts with the following:</span></span> 

`Endpoint=endpoint and key from Azure classic portal`

<span data-ttu-id="0d689-113">Klucz z prawami wysyłania w parametrach połączenia musi być skonfigurowany.</span><span class="sxs-lookup"><span data-stu-id="0d689-113">The Key with Send Rights in the connection string must be configured.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d689-114">-Context</span><span class="sxs-lookup"><span data-stu-id="0d689-114">-Context</span></span>
<span data-ttu-id="0d689-115">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="0d689-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="0d689-116">— Opis</span><span class="sxs-lookup"><span data-stu-id="0d689-116">-Description</span></span>
<span data-ttu-id="0d689-117">Określa opis.</span><span class="sxs-lookup"><span data-stu-id="0d689-117">Specifies a description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d689-118">-IsBuffered</span><span class="sxs-lookup"><span data-stu-id="0d689-118">-IsBuffered</span></span>
<span data-ttu-id="0d689-119">Określa, czy rekordy w rejestratorze są buforowane przed opublikowaniem.</span><span class="sxs-lookup"><span data-stu-id="0d689-119">Specifies whether the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="0d689-120">Wartość domyślna to $True.</span><span class="sxs-lookup"><span data-stu-id="0d689-120">The default value is $True.</span></span>
<span data-ttu-id="0d689-121">Gdy rekordy są buforowane, są one wysyłane do koncentratorów zdarzeń co 15 sekund lub za każdym razem, gdy bufor otrzymuje 256 KB wiadomości.</span><span class="sxs-lookup"><span data-stu-id="0d689-121">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d689-122">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="0d689-122">-LoggerId</span></span>
<span data-ttu-id="0d689-123">Określa identyfikator rejestratora.</span><span class="sxs-lookup"><span data-stu-id="0d689-123">Specifies an ID for the logger.</span></span>
<span data-ttu-id="0d689-124">Jeśli nie określisz identyfikatora, to polecenie cmdlet wygeneruje je.</span><span class="sxs-lookup"><span data-stu-id="0d689-124">If you do not specify an ID, this cmdlet generates one.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d689-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0d689-125">-Name</span></span>
<span data-ttu-id="0d689-126">Określa nazwę encji centrum zdarzeń w portalu klasycznym usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="0d689-126">Specifies the entity name of an event hub from Azure classic portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d689-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d689-127">-DefaultProfile</span></span>
<span data-ttu-id="0d689-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0d689-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d689-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d689-129">CommonParameters</span></span>
<span data-ttu-id="0d689-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d689-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d689-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d689-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d689-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0d689-132">INPUTS</span></span>

## <span data-ttu-id="0d689-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0d689-133">OUTPUTS</span></span>

### <span data-ttu-id="0d689-134">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="0d689-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="0d689-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0d689-135">NOTES</span></span>

## <span data-ttu-id="0d689-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0d689-136">RELATED LINKS</span></span>

[<span data-ttu-id="0d689-137">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="0d689-137">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="0d689-138">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="0d689-138">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)

[<span data-ttu-id="0d689-139">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="0d689-139">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


