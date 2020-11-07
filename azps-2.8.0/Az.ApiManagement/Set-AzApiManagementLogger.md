---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B4ADD38-FA22-4C25-9B9C-FD7861883811
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementLogger.md
ms.openlocfilehash: 8f1931cb5e73e3850cd011c16d327f8e8abc3a47
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706900"
---
# <span data-ttu-id="f46aa-101">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="f46aa-101">Set-AzApiManagementLogger</span></span>

## <span data-ttu-id="f46aa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f46aa-102">SYNOPSIS</span></span>
<span data-ttu-id="f46aa-103">Modyfikuje rejestratora zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="f46aa-103">Modifies an API Management Logger.</span></span>

## <span data-ttu-id="f46aa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f46aa-104">SYNTAX</span></span>

### <span data-ttu-id="f46aa-105">EventHubLoggerSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f46aa-105">EventHubLoggerSet (Default)</span></span>
```
Set-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-Name <String>]
 [-ConnectionString <String>] [-Description <String>] [-IsBuffered] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f46aa-106">ApplicationInsightsLoggerSet</span><span class="sxs-lookup"><span data-stu-id="f46aa-106">ApplicationInsightsLoggerSet</span></span>
```
Set-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-InstrumentationKey <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f46aa-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f46aa-107">DESCRIPTION</span></span>
<span data-ttu-id="f46aa-108">Polecenie cmdlet **Set-AzApiManagementLogger** modyfikuje ustawienia **rejestratora** zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="f46aa-108">The **Set-AzApiManagementLogger** cmdlet modifies settings of an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="f46aa-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f46aa-109">EXAMPLES</span></span>

### <span data-ttu-id="f46aa-110">Przykład 1: modyfikowanie rejestratora EventHub</span><span class="sxs-lookup"><span data-stu-id="f46aa-110">Example 1: Modify EventHub logger</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "updated SDK event hub logger" -PassThru
```

<span data-ttu-id="f46aa-111">To polecenie modyfikuje rejestratora o IDENTYFIKATORze Logger123.</span><span class="sxs-lookup"><span data-stu-id="f46aa-111">This command modifies a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="f46aa-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f46aa-112">PARAMETERS</span></span>

### <span data-ttu-id="f46aa-113">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="f46aa-113">-ConnectionString</span></span>
<span data-ttu-id="f46aa-114">Określa parametry połączenia z koncentratorem zdarzeń platformy Azure, które zawiera prawa do wysyłania.</span><span class="sxs-lookup"><span data-stu-id="f46aa-114">Specifies an Azure Event Hubs connection string that includes Send policy rights.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f46aa-115">-Context</span><span class="sxs-lookup"><span data-stu-id="f46aa-115">-Context</span></span>
<span data-ttu-id="f46aa-116">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="f46aa-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f46aa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f46aa-117">-DefaultProfile</span></span>
<span data-ttu-id="f46aa-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f46aa-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f46aa-119">— Opis</span><span class="sxs-lookup"><span data-stu-id="f46aa-119">-Description</span></span>
<span data-ttu-id="f46aa-120">Określa opis.</span><span class="sxs-lookup"><span data-stu-id="f46aa-120">Specifies a description.</span></span>

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

### <span data-ttu-id="f46aa-121">-InstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="f46aa-121">-InstrumentationKey</span></span>
<span data-ttu-id="f46aa-122">Klucz Instrumentacja usługi Application Insights.</span><span class="sxs-lookup"><span data-stu-id="f46aa-122">Instrumentation Key of the application Insights.</span></span> <span data-ttu-id="f46aa-123">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="f46aa-123">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationInsightsLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f46aa-124">-IsBuffered</span><span class="sxs-lookup"><span data-stu-id="f46aa-124">-IsBuffered</span></span>
<span data-ttu-id="f46aa-125">Określa, że rekordy w rejestratorze są buforowane przed opublikowaniem.</span><span class="sxs-lookup"><span data-stu-id="f46aa-125">Specifies that the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="f46aa-126">Gdy rekordy są buforowane, są one wysyłane do koncentratorów zdarzeń co 15 sekund lub za każdym razem, gdy bufor otrzymuje 256 KB wiadomości.</span><span class="sxs-lookup"><span data-stu-id="f46aa-126">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f46aa-127">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="f46aa-127">-LoggerId</span></span>
<span data-ttu-id="f46aa-128">Określa identyfikator rejestratora do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="f46aa-128">Specifies the ID of the logger to update.</span></span>

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

### <span data-ttu-id="f46aa-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f46aa-129">-Name</span></span>
<span data-ttu-id="f46aa-130">Określa nazwę encji centrum zdarzeń w portalu klasycznym usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="f46aa-130">Specifies the entity name of an event hub from Azure classic portal.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f46aa-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f46aa-131">-PassThru</span></span>
<span data-ttu-id="f46aa-132">Wskazuje, że to polecenie cmdlet zwróci  **PsApiManagementLogger** , które modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f46aa-132">Indicates that this cmdlet returns the  **PsApiManagementLogger** that this cmdlet modifies.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f46aa-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f46aa-133">-Confirm</span></span>
<span data-ttu-id="f46aa-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f46aa-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f46aa-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f46aa-135">-WhatIf</span></span>
<span data-ttu-id="f46aa-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f46aa-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f46aa-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f46aa-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f46aa-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f46aa-138">CommonParameters</span></span>
<span data-ttu-id="f46aa-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f46aa-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f46aa-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f46aa-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f46aa-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f46aa-141">INPUTS</span></span>

### <span data-ttu-id="f46aa-142">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f46aa-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f46aa-143">System. String</span><span class="sxs-lookup"><span data-stu-id="f46aa-143">System.String</span></span>

### <span data-ttu-id="f46aa-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f46aa-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f46aa-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f46aa-145">OUTPUTS</span></span>

### <span data-ttu-id="f46aa-146">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="f46aa-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="f46aa-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f46aa-147">NOTES</span></span>

## <span data-ttu-id="f46aa-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f46aa-148">RELATED LINKS</span></span>

[<span data-ttu-id="f46aa-149">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="f46aa-149">Get-AzApiManagementLogger</span></span>](./Get-AzApiManagementLogger.md)

[<span data-ttu-id="f46aa-150">Nowe — AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="f46aa-150">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="f46aa-151">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="f46aa-151">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)


