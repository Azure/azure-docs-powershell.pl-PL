---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 17D53F56-6E3B-491E-8776-5EBE109FBE3C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementLogger.md
ms.openlocfilehash: 04119d70f1cf3ae01b1d74e24cb2e030eecaa46b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716465"
---
# <span data-ttu-id="22b7a-101">New-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="22b7a-101">New-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="22b7a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="22b7a-102">SYNOPSIS</span></span>
<span data-ttu-id="22b7a-103">Tworzy rejestratora zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="22b7a-103">Creates an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22b7a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="22b7a-104">SYNTAX</span></span>

### <span data-ttu-id="22b7a-105">EventHubLoggerSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="22b7a-105">EventHubLoggerSet (Default)</span></span>
```
New-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>] -Name <String>
 -ConnectionString <String> [-Description <String>] [-IsBuffered <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22b7a-106">ApplicationInsightsLoggerSet</span><span class="sxs-lookup"><span data-stu-id="22b7a-106">ApplicationInsightsLoggerSet</span></span>
```
New-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>]
 -InstrumentationKey <String> [-Description <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="22b7a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="22b7a-107">DESCRIPTION</span></span>
<span data-ttu-id="22b7a-108">Polecenie cmdlet **New-AzureRmApiManagementLogger** tworzy **Rejestrator** zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="22b7a-108">The **New-AzureRmApiManagementLogger** cmdlet creates an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="22b7a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="22b7a-109">EXAMPLES</span></span>

### <span data-ttu-id="22b7a-110">Przykład 1. tworzenie rejestratora</span><span class="sxs-lookup"><span data-stu-id="22b7a-110">Example 1: Create a logger</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "SDK event hub logger"
```

<span data-ttu-id="22b7a-111">To polecenie tworzy Rejestrator o nazwie ContosoSdkEventHub, używając określonych parametrów połączenia.</span><span class="sxs-lookup"><span data-stu-id="22b7a-111">This command creates a logger named ContosoSdkEventHub by using the specified connection string.</span></span>

## <span data-ttu-id="22b7a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="22b7a-112">PARAMETERS</span></span>

### <span data-ttu-id="22b7a-113">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="22b7a-113">-ConnectionString</span></span>
<span data-ttu-id="22b7a-114">Określa parametry połączenia z koncentratorem zdarzeń platformy Azure, które zaczynają się od następującego: `Endpoint=endpoint and key from Azure classic portal`</span><span class="sxs-lookup"><span data-stu-id="22b7a-114">Specifies an Azure Event Hubs connection string that starts with the following: `Endpoint=endpoint and key from Azure classic portal`</span></span>
<span data-ttu-id="22b7a-115">Klucz z prawami wysyłania w parametrach połączenia musi być skonfigurowany.</span><span class="sxs-lookup"><span data-stu-id="22b7a-115">The Key with Send Rights in the connection string must be configured.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22b7a-116">-Context</span><span class="sxs-lookup"><span data-stu-id="22b7a-116">-Context</span></span>
<span data-ttu-id="22b7a-117">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="22b7a-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="22b7a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22b7a-118">-DefaultProfile</span></span>
<span data-ttu-id="22b7a-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="22b7a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22b7a-120">— Opis</span><span class="sxs-lookup"><span data-stu-id="22b7a-120">-Description</span></span>
<span data-ttu-id="22b7a-121">Określa opis.</span><span class="sxs-lookup"><span data-stu-id="22b7a-121">Specifies a description.</span></span>

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

### <span data-ttu-id="22b7a-122">-InstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="22b7a-122">-InstrumentationKey</span></span>
<span data-ttu-id="22b7a-123">Klucz Instrumentacja usługi Application Insights.</span><span class="sxs-lookup"><span data-stu-id="22b7a-123">Instrumentation Key of the application Insights.</span></span> <span data-ttu-id="22b7a-124">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="22b7a-124">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationInsightsLoggerSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22b7a-125">-IsBuffered</span><span class="sxs-lookup"><span data-stu-id="22b7a-125">-IsBuffered</span></span>
<span data-ttu-id="22b7a-126">Określa, czy rekordy w rejestratorze są buforowane przed opublikowaniem.</span><span class="sxs-lookup"><span data-stu-id="22b7a-126">Specifies whether the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="22b7a-127">Wartość domyślna to $True.</span><span class="sxs-lookup"><span data-stu-id="22b7a-127">The default value is $True.</span></span>
<span data-ttu-id="22b7a-128">Gdy rekordy są buforowane, są one wysyłane do koncentratorów zdarzeń co 15 sekund lub za każdym razem, gdy bufor otrzymuje 256 KB wiadomości.</span><span class="sxs-lookup"><span data-stu-id="22b7a-128">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22b7a-129">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="22b7a-129">-LoggerId</span></span>
<span data-ttu-id="22b7a-130">Określa identyfikator rejestratora.</span><span class="sxs-lookup"><span data-stu-id="22b7a-130">Specifies an ID for the logger.</span></span>
<span data-ttu-id="22b7a-131">Jeśli nie określisz identyfikatora, to polecenie cmdlet wygeneruje je.</span><span class="sxs-lookup"><span data-stu-id="22b7a-131">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="22b7a-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="22b7a-132">-Name</span></span>
<span data-ttu-id="22b7a-133">Określa nazwę encji centrum zdarzeń w portalu klasycznym usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="22b7a-133">Specifies the entity name of an event hub from Azure classic portal.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22b7a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22b7a-134">CommonParameters</span></span>
<span data-ttu-id="22b7a-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22b7a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22b7a-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22b7a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22b7a-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="22b7a-137">INPUTS</span></span>

### <span data-ttu-id="22b7a-138">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="22b7a-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="22b7a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="22b7a-139">System.String</span></span>

### <span data-ttu-id="22b7a-140">System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="22b7a-140">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="22b7a-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="22b7a-141">OUTPUTS</span></span>

### <span data-ttu-id="22b7a-142">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="22b7a-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="22b7a-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="22b7a-143">NOTES</span></span>

## <span data-ttu-id="22b7a-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="22b7a-144">RELATED LINKS</span></span>

[<span data-ttu-id="22b7a-145">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="22b7a-145">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="22b7a-146">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="22b7a-146">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)

[<span data-ttu-id="22b7a-147">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="22b7a-147">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


