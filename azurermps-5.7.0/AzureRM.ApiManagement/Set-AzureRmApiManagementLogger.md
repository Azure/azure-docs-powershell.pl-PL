---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 5B4ADD38-FA22-4C25-9B9C-FD7861883811
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
ms.openlocfilehash: 16a60f5f9951aaa40ac8da8584e1c2690206cdb7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553706"
---
# <span data-ttu-id="6e8af-101">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="6e8af-101">Set-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="6e8af-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6e8af-102">SYNOPSIS</span></span>
<span data-ttu-id="6e8af-103">Modyfikuje rejestratora zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="6e8af-103">Modifies an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e8af-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6e8af-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-Name <String>]
 [-ConnectionString <String>] [-Description <String>] [-IsBuffered] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e8af-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6e8af-105">DESCRIPTION</span></span>
<span data-ttu-id="6e8af-106">Polecenie cmdlet **Set-AzureRmApiManagementLogger** modyfikuje ustawienia **rejestratora** zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="6e8af-106">The **Set-AzureRmApiManagementLogger** cmdlet modifies settings of an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="6e8af-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6e8af-107">EXAMPLES</span></span>

### <span data-ttu-id="6e8af-108">Przykład 1: modyfikowanie rejestratora</span><span class="sxs-lookup"><span data-stu-id="6e8af-108">Example 1: Modify a logger</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "updated SDK event hub logger" -PassThru
```

<span data-ttu-id="6e8af-109">To polecenie modyfikuje rejestratora o IDENTYFIKATORze Logger123.</span><span class="sxs-lookup"><span data-stu-id="6e8af-109">This command modifies a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="6e8af-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6e8af-110">PARAMETERS</span></span>

### <span data-ttu-id="6e8af-111">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="6e8af-111">-ConnectionString</span></span>
<span data-ttu-id="6e8af-112">Określa parametry połączenia z koncentratorem zdarzeń platformy Azure, które zawiera prawa do wysyłania.</span><span class="sxs-lookup"><span data-stu-id="6e8af-112">Specifies an Azure Event Hubs connection string that includes Send policy rights.</span></span>

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

### <span data-ttu-id="6e8af-113">-Context</span><span class="sxs-lookup"><span data-stu-id="6e8af-113">-Context</span></span>
<span data-ttu-id="6e8af-114">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="6e8af-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="6e8af-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e8af-115">-DefaultProfile</span></span>
<span data-ttu-id="6e8af-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6e8af-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="6e8af-117">— Opis</span><span class="sxs-lookup"><span data-stu-id="6e8af-117">-Description</span></span>
<span data-ttu-id="6e8af-118">Określa opis.</span><span class="sxs-lookup"><span data-stu-id="6e8af-118">Specifies a description.</span></span>

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

### <span data-ttu-id="6e8af-119">-IsBuffered</span><span class="sxs-lookup"><span data-stu-id="6e8af-119">-IsBuffered</span></span>
<span data-ttu-id="6e8af-120">Określa, że rekordy w rejestratorze są buforowane przed opublikowaniem.</span><span class="sxs-lookup"><span data-stu-id="6e8af-120">Specifies that the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="6e8af-121">Gdy rekordy są buforowane, są one wysyłane do koncentratorów zdarzeń co 15 sekund lub za każdym razem, gdy bufor otrzymuje 256 KB wiadomości.</span><span class="sxs-lookup"><span data-stu-id="6e8af-121">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e8af-122">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="6e8af-122">-LoggerId</span></span>
<span data-ttu-id="6e8af-123">Określa identyfikator rejestratora do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="6e8af-123">Specifies the ID of the logger to update.</span></span>

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

### <span data-ttu-id="6e8af-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6e8af-124">-Name</span></span>
<span data-ttu-id="6e8af-125">Określa nazwę encji centrum zdarzeń w portalu klasycznym usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="6e8af-125">Specifies the entity name of an event hub from Azure classic portal.</span></span>

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

### <span data-ttu-id="6e8af-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e8af-126">-PassThru</span></span>
<span data-ttu-id="6e8af-127">Wskazuje, że to polecenie cmdlet zwróci  **PsApiManagementLogger** , które modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e8af-127">Indicates that this cmdlet returns the  **PsApiManagementLogger** that this cmdlet modifies.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e8af-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e8af-128">CommonParameters</span></span>
<span data-ttu-id="6e8af-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e8af-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e8af-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e8af-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e8af-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6e8af-131">INPUTS</span></span>

### <span data-ttu-id="6e8af-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6e8af-132">None</span></span>
<span data-ttu-id="6e8af-133">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="6e8af-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6e8af-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6e8af-134">OUTPUTS</span></span>

### <span data-ttu-id="6e8af-135">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="6e8af-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="6e8af-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6e8af-136">NOTES</span></span>

## <span data-ttu-id="6e8af-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6e8af-137">RELATED LINKS</span></span>

[<span data-ttu-id="6e8af-138">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="6e8af-138">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="6e8af-139">Nowe — AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="6e8af-139">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="6e8af-140">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="6e8af-140">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)


