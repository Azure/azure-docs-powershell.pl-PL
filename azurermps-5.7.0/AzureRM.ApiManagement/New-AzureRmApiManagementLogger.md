---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 17D53F56-6E3B-491E-8776-5EBE109FBE3C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementLogger.md
ms.openlocfilehash: 2929cbd89328d971b47b748d4aa042ade13c1af9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544567"
---
# <span data-ttu-id="1ec11-101">New-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="1ec11-101">New-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="1ec11-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1ec11-102">SYNOPSIS</span></span>
<span data-ttu-id="1ec11-103">Tworzy rejestratora zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="1ec11-103">Creates an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ec11-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1ec11-104">SYNTAX</span></span>

```
New-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>] -Name <String>
 -ConnectionString <String> [-Description <String>] [-IsBuffered <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ec11-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1ec11-105">DESCRIPTION</span></span>
<span data-ttu-id="1ec11-106">Polecenie cmdlet **New-AzureRmApiManagementLogger** tworzy **Rejestrator** zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="1ec11-106">The **New-AzureRmApiManagementLogger** cmdlet creates an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="1ec11-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1ec11-107">EXAMPLES</span></span>

### <span data-ttu-id="1ec11-108">Przykład 1. tworzenie rejestratora</span><span class="sxs-lookup"><span data-stu-id="1ec11-108">Example 1: Create a logger</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "SDK event hub logger"
```

<span data-ttu-id="1ec11-109">To polecenie tworzy Rejestrator o nazwie ContosoSdkEventHub, używając określonych parametrów połączenia.</span><span class="sxs-lookup"><span data-stu-id="1ec11-109">This command creates a logger named ContosoSdkEventHub by using the specified connection string.</span></span>

## <span data-ttu-id="1ec11-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1ec11-110">PARAMETERS</span></span>

### <span data-ttu-id="1ec11-111">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="1ec11-111">-ConnectionString</span></span>
<span data-ttu-id="1ec11-112">Określa parametry połączenia z koncentratorem zdarzeń platformy Azure, które zaczynają się od następującego:</span><span class="sxs-lookup"><span data-stu-id="1ec11-112">Specifies an Azure Event Hubs connection string that starts with the following:</span></span> 

`Endpoint=endpoint and key from Azure classic portal`

<span data-ttu-id="1ec11-113">Klucz z prawami wysyłania w parametrach połączenia musi być skonfigurowany.</span><span class="sxs-lookup"><span data-stu-id="1ec11-113">The Key with Send Rights in the connection string must be configured.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ec11-114">-Context</span><span class="sxs-lookup"><span data-stu-id="1ec11-114">-Context</span></span>
<span data-ttu-id="1ec11-115">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="1ec11-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1ec11-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ec11-116">-DefaultProfile</span></span>
<span data-ttu-id="1ec11-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1ec11-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="1ec11-118">— Opis</span><span class="sxs-lookup"><span data-stu-id="1ec11-118">-Description</span></span>
<span data-ttu-id="1ec11-119">Określa opis.</span><span class="sxs-lookup"><span data-stu-id="1ec11-119">Specifies a description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ec11-120">-IsBuffered</span><span class="sxs-lookup"><span data-stu-id="1ec11-120">-IsBuffered</span></span>
<span data-ttu-id="1ec11-121">Określa, czy rekordy w rejestratorze są buforowane przed opublikowaniem.</span><span class="sxs-lookup"><span data-stu-id="1ec11-121">Specifies whether the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="1ec11-122">Wartość domyślna to $True.</span><span class="sxs-lookup"><span data-stu-id="1ec11-122">The default value is $True.</span></span>
<span data-ttu-id="1ec11-123">Gdy rekordy są buforowane, są one wysyłane do koncentratorów zdarzeń co 15 sekund lub za każdym razem, gdy bufor otrzymuje 256 KB wiadomości.</span><span class="sxs-lookup"><span data-stu-id="1ec11-123">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ec11-124">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="1ec11-124">-LoggerId</span></span>
<span data-ttu-id="1ec11-125">Określa identyfikator rejestratora.</span><span class="sxs-lookup"><span data-stu-id="1ec11-125">Specifies an ID for the logger.</span></span>
<span data-ttu-id="1ec11-126">Jeśli nie określisz identyfikatora, to polecenie cmdlet wygeneruje je.</span><span class="sxs-lookup"><span data-stu-id="1ec11-126">If you do not specify an ID, this cmdlet generates one.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ec11-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1ec11-127">-Name</span></span>
<span data-ttu-id="1ec11-128">Określa nazwę encji centrum zdarzeń w portalu klasycznym usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="1ec11-128">Specifies the entity name of an event hub from Azure classic portal.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ec11-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ec11-129">CommonParameters</span></span>
<span data-ttu-id="1ec11-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ec11-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ec11-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ec11-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ec11-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1ec11-132">INPUTS</span></span>

### <span data-ttu-id="1ec11-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1ec11-133">None</span></span>
<span data-ttu-id="1ec11-134">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="1ec11-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1ec11-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1ec11-135">OUTPUTS</span></span>

### <span data-ttu-id="1ec11-136">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="1ec11-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="1ec11-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1ec11-137">NOTES</span></span>

## <span data-ttu-id="1ec11-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1ec11-138">RELATED LINKS</span></span>

[<span data-ttu-id="1ec11-139">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="1ec11-139">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="1ec11-140">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="1ec11-140">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)

[<span data-ttu-id="1ec11-141">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="1ec11-141">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


