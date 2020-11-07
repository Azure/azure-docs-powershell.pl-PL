---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 17D53F56-6E3B-491E-8776-5EBE109FBE3C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementLogger.md
ms.openlocfilehash: 3df5f6974cd955035c16972a5a7358aa44a30390
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710636"
---
# <span data-ttu-id="a1c5e-101">New-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="a1c5e-101">New-AzApiManagementLogger</span></span>

## <span data-ttu-id="a1c5e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a1c5e-102">SYNOPSIS</span></span>
<span data-ttu-id="a1c5e-103">Tworzy rejestratora zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="a1c5e-103">Creates an API Management Logger.</span></span>

## <span data-ttu-id="a1c5e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a1c5e-104">SYNTAX</span></span>

### <span data-ttu-id="a1c5e-105">EventHubLoggerSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a1c5e-105">EventHubLoggerSet (Default)</span></span>
```
New-AzApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>] -Name <String>
 -ConnectionString <String> [-Description <String>] [-IsBuffered <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1c5e-106">ApplicationInsightsLoggerSet</span><span class="sxs-lookup"><span data-stu-id="a1c5e-106">ApplicationInsightsLoggerSet</span></span>
```
New-AzApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>] -InstrumentationKey <String>
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1c5e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a1c5e-107">DESCRIPTION</span></span>
<span data-ttu-id="a1c5e-108">Polecenie cmdlet **New-AzApiManagementLogger** tworzy **Rejestrator** zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="a1c5e-108">The **New-AzApiManagementLogger** cmdlet creates an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="a1c5e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a1c5e-109">EXAMPLES</span></span>

### <span data-ttu-id="a1c5e-110">Przykład 1. tworzenie rejestratora</span><span class="sxs-lookup"><span data-stu-id="a1c5e-110">Example 1: Create a logger</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "SDK event hub logger"
```

<span data-ttu-id="a1c5e-111">To polecenie tworzy Rejestrator o nazwie ContosoSdkEventHub, używając określonych parametrów połączenia.</span><span class="sxs-lookup"><span data-stu-id="a1c5e-111">This command creates a logger named ContosoSdkEventHub by using the specified connection string.</span></span>

## <span data-ttu-id="a1c5e-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a1c5e-112">PARAMETERS</span></span>

### <span data-ttu-id="a1c5e-113">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="a1c5e-113">-ConnectionString</span></span>
<span data-ttu-id="a1c5e-114">Określa parametry połączenia z koncentratorem zdarzeń platformy Azure, które zaczynają się od następującego: `Endpoint=endpoint and key from Azure classic portal`</span><span class="sxs-lookup"><span data-stu-id="a1c5e-114">Specifies an Azure Event Hubs connection string that starts with the following: `Endpoint=endpoint and key from Azure classic portal`</span></span>
<span data-ttu-id="a1c5e-115">Klucz z prawami wysyłania w parametrach połączenia musi być skonfigurowany.</span><span class="sxs-lookup"><span data-stu-id="a1c5e-115">The Key with Send Rights in the connection string must be configured.</span></span>

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

### <span data-ttu-id="a1c5e-116">-Context</span><span class="sxs-lookup"><span data-stu-id="a1c5e-116">-Context</span></span>
<span data-ttu-id="a1c5e-117">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="a1c5e-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a1c5e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1c5e-118">-DefaultProfile</span></span>
<span data-ttu-id="a1c5e-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a1c5e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1c5e-120">— Opis</span><span class="sxs-lookup"><span data-stu-id="a1c5e-120">-Description</span></span>
<span data-ttu-id="a1c5e-121">Określa opis.</span><span class="sxs-lookup"><span data-stu-id="a1c5e-121">Specifies a description.</span></span>

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

### <span data-ttu-id="a1c5e-122">-InstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="a1c5e-122">-InstrumentationKey</span></span>
<span data-ttu-id="a1c5e-123">Klucz Instrumentacja usługi Application Insights.</span><span class="sxs-lookup"><span data-stu-id="a1c5e-123">Instrumentation Key of the application Insights.</span></span> <span data-ttu-id="a1c5e-124">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="a1c5e-124">This parameter is optional.</span></span>

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

### <span data-ttu-id="a1c5e-125">-IsBuffered</span><span class="sxs-lookup"><span data-stu-id="a1c5e-125">-IsBuffered</span></span>
<span data-ttu-id="a1c5e-126">Określa, czy rekordy w rejestratorze są buforowane przed opublikowaniem.</span><span class="sxs-lookup"><span data-stu-id="a1c5e-126">Specifies whether the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="a1c5e-127">Wartość domyślna to $True.</span><span class="sxs-lookup"><span data-stu-id="a1c5e-127">The default value is $True.</span></span>
<span data-ttu-id="a1c5e-128">Gdy rekordy są buforowane, są one wysyłane do koncentratorów zdarzeń co 15 sekund lub za każdym razem, gdy bufor otrzymuje 256 KB wiadomości.</span><span class="sxs-lookup"><span data-stu-id="a1c5e-128">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

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

### <span data-ttu-id="a1c5e-129">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="a1c5e-129">-LoggerId</span></span>
<span data-ttu-id="a1c5e-130">Określa identyfikator rejestratora.</span><span class="sxs-lookup"><span data-stu-id="a1c5e-130">Specifies an ID for the logger.</span></span>
<span data-ttu-id="a1c5e-131">Jeśli nie określisz identyfikatora, to polecenie cmdlet wygeneruje je.</span><span class="sxs-lookup"><span data-stu-id="a1c5e-131">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="a1c5e-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a1c5e-132">-Name</span></span>
<span data-ttu-id="a1c5e-133">Określa nazwę encji centrum zdarzeń w portalu klasycznym usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="a1c5e-133">Specifies the entity name of an event hub from Azure classic portal.</span></span>

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

### <span data-ttu-id="a1c5e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1c5e-134">CommonParameters</span></span>
<span data-ttu-id="a1c5e-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1c5e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1c5e-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1c5e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1c5e-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1c5e-137">INPUTS</span></span>

### <span data-ttu-id="a1c5e-138">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a1c5e-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a1c5e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a1c5e-139">System.String</span></span>

### <span data-ttu-id="a1c5e-140">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a1c5e-140">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a1c5e-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a1c5e-141">OUTPUTS</span></span>

### <span data-ttu-id="a1c5e-142">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="a1c5e-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="a1c5e-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a1c5e-143">NOTES</span></span>

## <span data-ttu-id="a1c5e-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a1c5e-144">RELATED LINKS</span></span>

[<span data-ttu-id="a1c5e-145">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="a1c5e-145">Get-AzApiManagementLogger</span></span>](./Get-AzApiManagementLogger.md)

[<span data-ttu-id="a1c5e-146">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="a1c5e-146">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)

[<span data-ttu-id="a1c5e-147">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="a1c5e-147">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


